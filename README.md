Pets App
===================================

This app displays a list of pets and their related data that the user inputs.
Used in a Udacity course in the Android Basics Nanodegree by Google.

Pre-requisites
--------------

- Android SDK v24
- Android Build Tools v23.0.3
- Android Support Repository v24.1.1

Getting Started
---------------

This sample uses the Gradle build system. To build this project, use the
"gradlew build" command or use "Import Project" in Android Studio.

# STEPS:

1)Database Basics
  >learn how to use sqlite,the database system that runs on andriod.
   
2)Here we use contract class
 >define schemaand have a convention for where to find database constants. 
 >when generating sql commands,remove possibility of introducing spelling errors.
 >ease of updating database system.
  
3)Here we create sqliteopenhelper
 >creates a sqlite database when it is first accessed.
 >gives you a connection to that database.
 >manages updating the database schema if version changes.
  
4)Here we create contentprovider
 >manages access to a structured set of data.
 >good abstract layer between database and UI code.
  
5)Here we create contenturi
 >a contenturi is a uri that defines data in a provider.
 >can point to a part of a database.
 >can point to a file.

6)Use urimatcher in contentprovider
 >setup the urimatcher with the uri pattern.your content provider will accept and assign each pattern an integercode.
 >call urimatcher.match(uri) and pass in a uri,which will return the corresponding integercode
  
7)Add cursoradapter to pets-app.
 
8)We use cursorloader
  >loader that queries the content resolver with a specific URI and returns a cursor.
  >loads data on a backgroundthread because reading and writting to a database can be an expensive operation.
  >works well with contentprovider because a loader is tied to a uri.
  >when the underlying data changes we can automatically refresh the loader to query the datasource again with the same URI.
   
 
