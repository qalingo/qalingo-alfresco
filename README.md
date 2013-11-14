qalingo-alfresco
================

Alfresco Community is use for :
* CMS sync with Qalingo over CMIS and manage your home page, product page, product line, etc
* Use as a collaborative tools. Forum, Wiki, documents repository for your team (developers and business peoples)

The project use Java7 and was created with:

mvn archetype:generate -DarchetypeCatalog=https://artifacts.alfresco.com/nexus/content/groups/public/archetype-catalog.xml 
-DarchetypeGroupId=org.alfresco.maven.archetype -DarchetypeArtifactId=alfresco-allinone-archetype -DarchetypeVersion=1.0.2

cd alfresco-allinone

mvn clean install

Create a database alfresco:

CREATE DATABASE alfresco CHARACTER SET utf8 COLLATE utf8_general_ci;

CREATE USER 'alfresco'@'localhost' IDENTIFIED BY 'alfresco';

GRANT ALL PRIVILEGES ON alfresco.* TO 'alfresco'@'localhost' IDENTIFIED BY 'alfresco' WITH GRANT OPTION;

GRANT ALL PRIVILEGES ON alfresco.* TO 'alfresco'@'%' IDENTIFIED BY 'alfresco' WITH GRANT OPTION;

FLUSH PRIVILEGES;


