Sonar Connector
=====================

The main goal of this plugin is to show sonar violations directly in the IntelliJ IDE. 
This plugin should work in any IDE of the IntelliJ family and for any programming language.
Each sonar violation and rule is converted to an IntelliJ inspection 
and makes it possible to use inspection features like for any other IntelliJ inspection.

Usage
--------------------

First you need to configure your connection to a sonar server. You can connect use a remote server or a local one on your machine.
To configure a project:

Go to File -> Settings (Ctrl+Alt+S)-> Sonar Connector
and test your configuration. 
![alt text][projectConfiguration]

[projectConfiguration]: http://plugins.jetbrains.com/files/7238/screenshot_14229.png "Example project configuration"

If your project has multiple modules, then you can configure each module as well:
Go to File -> Project Structure (Ctrl+Alt+Shift+S)
-> Modules -> Sonar Connector Tab
![alt text][moduleConfiguration]

[moduleConfiguration]: http://plugins.jetbrains.com/files/7238/screenshot_14228.png "Example module configuration"

After the configuration of your project, go to any source file in your project, right click over the source code and press *Sync with sonar*
![alt text][syncWithSonar]
[syncWithSonar]: https://github.com/omayevskiy/sonar-intellij-plugin/blob/master/sonar%20connector%20screenshots/sync_with_sonar.jpg?raw=true

If sync is complete (this should take some while depends on your project size and connection), then you can start inspect your code.
Before inspecting I suggest you to create an inspection profile for all those sonar inspections to separate them from live IntelliJ inspections.
Go to Analyze -> In the window at bottom right to Inspection Profile select box click onto "..." button.
![alt text][specifyInspectionScope]
[specifyInspectionScope]: https://github.com/omayevskiy/sonar-intellij-plugin/blob/master/sonar%20connector%20screenshots/specify_inspection_scope.jpg?raw=true

In the Inspections window click at the top onto the "Add" button and create a new profile, e.g.: Sonar.
Now deselect everything but not the sonar rules for this profile and click "OK"
![alt text][specifyInspectionScope]
[specifyInspectionScope]: https://github.com/omayevskiy/sonar-intellij-plugin/blob/master/sonar%20connector%20screenshots/sonar_profile.jpg?raw=true

To inspect your code you can now
Go to Analyze -> Inspect Code ... -> Choose Sonar Inspection Profile and Inspection Scope -> OK
You should now see something like:
![alt text][sonarInspectionResult]
[sonarInspectionResult]: https://github.com/omayevskiy/sonar-intellij-plugin/blob/master/sonar%20connector%20screenshots/sonar_inspection_result.jpg?raw=true

Please note: you must NOT create a separate inspection profile, you can mix sonar inspection like you want.
One more tip: to run quick only one inspection, press Ctrl+Alt+Shift+I. Type "Sonar" to show all available sonar rules or the name of a rule.

Have fun!
