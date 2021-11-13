1. mvn clean  -> This command cleans the maven project by deleting the target directory.
2. mvn compiler:compile  -> This command compiles the java source classes of the maven project.
3. mvn compiler:testCompile  -> This command compiles the test classes of the maven project.
4. mvn package  -> This command builds the maven project and packages them into a JAR, WAR, etc.
5. mvn install  -> This command builds the maven project and installs the project files (JAR, WAR, pom.xml, etc) to the local repository.
6. mvn deploy  -> This command is used to deploy the artifact to the remote repository. The remote repository should be configured properly in the project pom.xml file distributionManagement tag. The server entries in the maven settings.xml file is used to provide authentication details.
7. mvn validate  -> This command validates the maven project that everything is correct and all the necessary information is available.
8. mvn dependency:tree  -> This command generates the dependency tree of the maven project.
9. mvn dependency:analyze  -> This command analyzes the maven project to identify the unused declared and used undeclared dependencies. It’s useful in reducing the build size by identifying the unused dependencies and then remove it from the pom.xml file.
10. mvn archetype:generate  -> Maven archetypes is a maven project templating toolkit. We can use this command to generate a skeleton maven project of different types, such as JAR, web application, maven site, etc.
11. mvn site:site  -> This command generates a site for the project. You will notice a “site” directory in the target after executing this command. There will be multiple HTML files inside the site directory that provides information related to the project.
12. mvn test  -> This command is used to run the test cases of the project using the maven-surefire-plugin.
13. mvn compile  -> It’s used to compile the source Java classes of the project.
14. mvn verify  -> This command build the project, runs all the test cases and run any checks on the results of the integration tests to ensure quality criteria are met.
15. mvn -help  -> This command prints the maven usage and all the available options for us to use.
16. mvn -f maven-example-jar/pom.xml package  -> This command is used to build a project from a different location. We are providing the pom.xml file location to build the project. It’s useful when you have to run a maven build from a script.
17. mvn -o package  -> This command is used to run the maven build in the offline mode. It’s useful when we have all the required JARs download in the local repository and we don’t want Maven to look for any JARs in the remote repository.
18. mvn -q package  -> Runs the maven build in the quiet mode, only the test cases results and errors are displayed.
19. mvn -X package  -> Prints the maven version and runs the build in the debug mode. It’s opposite of the quiet mode and you will see a lot of debug messages in the console.
20. mvn -v  -> Used to display the maven version information.
21. mvn -V package  -> This command prints the maven version and then continue with the build. It’s equivalent to the commands mvn -v;mvn package.
22. mvn -DskipTests package  -> The skipTests system property is used to skip the unit test cases from the build cycle. We can also use -Dmaven.test.skip=true to skip the test cases execution.
23. mvn -T 4 package  -> This command tells maven to run parallel builds using the specified thread count. It’s useful in multiple module projects where modules can be built in parallel. It can reduce the build time of the project.
24. mvn clean install -Dmaven.test.skip=true -> first it will delete the target folder and install the dependencies but ignore the all test cases
 