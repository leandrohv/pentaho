# pentaho
pentaho

Configuração Pentaho

* Primeira configuração 

Verificar o quanto de memória o pentaho poderá utilizar do ambiente.
Verificar no arquivo start-pentaho, o parâmetro "set CATALINA_OPTS=-Xms512m -Xmx2048m "
Parâmetros
-Xms -> mínimo de memória
-Xmx -> máximo de memória

* Segunda configuração 
Apagar o arquivo "mysql-connector-java-5.1.17.jar" que é o driver padrão que vem para conexão com o MySQL constante na pasta "pentaho-server/tomcat/lib/"
Obs.: Não esquecer de incluir todos os drivers nessa pasta, seja para o MySQL, Oracle, PostgreSQL, etc.

* Terceira configuração 
Extrair o driver do mysql na pasta "pentaho-server/tomcat/lib/".

* Quarta configuração 
Verificar o quanto de memória o pentaho data integration(PDI) poderá utilizar do ambiente.
Verificar no arquivo spoon, no parâmetro "if "%PENTAHO_DI_JAVA_OPTIONS%"=="" set PENTAHO_DI_JAVA_OPTIONS="-Xms512m" "-Xmx2048m" "-XX:MaxPermSize=256m" "
Parâmetros
-Xms -> mínimo de memória
-Xmx -> máximo de memória

* Quinta configuração 
Extrair o driver do mysql na pasta "designer-tools/data-integration/lib/".
Obs.: Não esquecer de incluir todos os drivers nessa pasta, seja para o MySQL, Oracle, PostgreSQL, etc.

* Sexta configuração 
Verificar o quanto de memória o pentaho report designer poderá utilizar do ambiente.
Verificar no arquivo report-designer, no parâmetro "start "Pentaho Report Designer" "%_PENTAHO_JAVA%" -Dswing.useSystemFontSettings=false -Xms1024m -Xmx2048m -XX:MaxPermSize=256m -jar "%~dp0launcher.jar" %* "
Parâmetros
-Xms -> mínimo de memória
-Xmx -> máximo de memória

* Sétima configuração 
Extrair o driver do mysql na pasta "designer-tools/report-designer/lib/".
Obs.: Não esquecer de incluir todos os drivers nessa pasta, seja para o MySQL, Oracle, PostgreSQL, etc.

* Oitava configuração 
Verificar o quanto de memória o pentaho schema workbench poderá utilizar do ambiente.
Verificar no arquivo workbench, no parâmetro "%_PENTAHO_JAVA%" -Xms1024m -Xmx2048m -cp "%CP%" -Dlog4j.configuration=file:///%ROOT%\.schemaWorkbench\log4j.xml mondrian.gui.Workbench"
Parâmetros
-Xms -> mínimo de memória
-Xmx -> máximo de memória

* Nona configuração 
Extrair o driver do mysql na pasta "designer-tools/schema-workbench/lib/".
Obs.: Não esquecer de incluir todos os drivers nessa pasta, seja para o MySQL, Oracle, PostgreSQL, etc.


