CHANGES IN VERSION 5.8.1
=================================

* [FIX] Null pointer exception when trying to create reports from missing report data.
* [MAINTENANCE] Upgrade to Cucumber version 6.9.1

CHANGES IN VERSION 5.8.0
=================================

* [ENHANCEMENT] Improve performance and optimize memory when generating Cucumber and Courgette reports.
* [ENHANCEMENT] Use mustache templates when generating the Courgette html report.
* [ENHANCEMENT] Use a new dark theme for the Courgette html report.
* [ENHANCEMENT] Use CDN to deliver Courgette html report files.
* [UPGRADE] Courgette html report assets (js and css)
* [FIX] All security vulnerabilities identified by Nexus Vulnerability Scanner.
* [FIX] Out of memory exception when generating large Cucumber and Courgette reports.
* [BREAKING CHANGE] Previously cached Courgette html report assets (js and css) are no longer available due to security vulnerabilites that exists in those files.


CHANGES IN VERSION 5.7.0
=================================

* [FIX] Incorrect duration value when generating the Cucumber report.
* [MAINTENANCE] Upgrade to Cucumber version 6.9.0

CHANGES IN VERSION 5.6.0
=================================

* [FIX] Known Courgette limitation which resulted in report data from being overridden when using `CourgetteRunLevel.FEATURE` and `rerunFailedScenarios = true`
* [ENHANCEMENT] Use cucumber messages (ndjson) to generate Cucumber reports to improve reporting accuracy.
* [MAINTENANCE] Upgrade to Cucumber version 6.8.2


CHANGES IN VERSION 5.5.1
=================================

* [NEW] Courgette will publish the Cucumber report using the provided token from the `CUCUMBER_PUBLISH_TOKEN` system property or environment variable.


CHANGES IN VERSION 5.5.0
=================================

* [NEW] Add environment information to Courgette html report.
* [NEW] Add new Courgette option `environmentInfo` to allow additional environment information to be provided and displayed in the Courgette html report.
* [NEW] Add a link to the published Cucumber report from the Courgette html report.
* [MAINTENANCE] Upgrade to Cucumber version 6.8.1


CHANGES IN VERSION 5.4.0
=================================

* [NEW] Add scenario grouping to Courgette html report when using CourgetteRunLevel.SCENARIO.
* [MAINTENANCE] Upgrade to Cucumber version 6.7.0


CHANGES IN VERSION 5.3.0
=================================

* [UPGRADE] Extent Reports version to 5.0.3
* [FIX] Handle NumberFormatException in Courgette Reporter.


CHANGES IN VERSION 5.2.1
=================================

* [ENHANCEMENT] Remove CDN and embed CSS and JS in Courgette html report. This enables viewing the Courgette html report when offline.


CHANGES IN VERSION 5.2.0
=================================

* Update Courgette Report Portal plugin.
    * [NEW] Add support to send `rp.tags` to the latest launch.


CHANGES IN VERSION 5.1.0
=================================

* [NEW] Add Cucumber option 'publish' which publishes a single Cucumber Report to https://reports.cucumber.io/ after parallel execution.
* [MAINTENANCE] Upgrade to Cucumber version 6.6.0

CHANGES IN VERSION 5.0.0
=================================

* Upgrade to Cucumber version 6.4.0 [see release notes](https://github.com/cucumber/cucumber-jvm/blob/master/release-notes/v6.0.0.md)
* Remove 'strict' cucumber option as this value is now defaulted to true in Cucumber. (_This is a breaking change so you would need to update your Courgette runner class if you use this option_)
* Code refactoring and improvements.


CHANGES IN VERSION 4.6.2
=================================
* Add new Courgette option 'reportTitle' to support overriding the default Courgette html report title.


CHANGES IN VERSION 4.6.1
=================================
* Add Extent Reports bdd type on feature creation which enables Extent Reports to create a BDD report.


CHANGES IN VERSION 4.6.0
=================================

* Courgette now creates a single Courgette Html Report.
* Changed Courgette Html Report to embed all images as a base64 image source.
* Changed Courgette Html Report to use a CDN to load JS and CSS files.
* Upgrade to Cucumber version 5.6.0
* Updated Extent Reports plugin to mark skipped steps.


CHANGES IN VERSION 4.5.0
=================================

* Courgette runner no longer requires the classpath to be built before execution. This also fixes the CreateProcess error=206 limitation on Windows OS.
* Removed 'shortenJavaClassPath' Courgette option.
* Upgrade to Extent Reports version 4.1.4 


CHANGES IN VERSION 4.4.1
=================================

* Fixed issue which caused a java.nio.file.InvalidPathException in Windows OS.

CHANGES IN VERSION 4.4.0
=================================

* Upgrade to Cucumber version 5.5.0
* Code improvements / refactoring.

CHANGES IN VERSION 4.3.4
=================================

* Add new Courgette option 'shortenJavaClassPath' to provide a workaround to the "CreateProcess error=206, The filename or extension is too long" issue on Windows OS when using Java 8.

CHANGES IN VERSION 4.3.3
=================================

* Fixed bug which caused background steps to be incorrectly reported in the Courgette Html report.

CHANGES IN VERSION 4.3.2
=================================

* Upgrade to Extent Reports version 4.1.3
* Removed Extent Reports Cucumber adaptor
* Extent Reports now uses timestamps from the Cucumber report


CHANGES IN VERSION 4.3.1
=================================

* Upgrade Extent Reports adaptor to version 1.0.10

CHANGES IN VERSION 4.3.0
=================================

* Replace ExtentHtmlReporter with ExtentSparkReporter
* Embed base64 images to Extent Report

CHANGES IN VERSION 4.2.0
=================================

* Fix Extent Reports report issue which duplicated the name of all scenarios when CourgetteRunLevel.FEATURE was used.

CHANGES IN VERSION 4.1.0
=================================

* Add Extent Reports integration.
* Code base improvements.

CHANGES IN VERSION 4.0.3-SNAPSHOT
=================================

* Report Portal launch name and test suite are now customizable.
* Report Portal properties can be overridden at runtime using system properties.
* Removed the file path from before & after hooks in the Courgette html report.
* Add apache httpclient dependency to Courgette.


CHANGES IN VERSION 4.0.2-SNAPSHOT
=================================

* Add support for text/html mime types in the Courgette html report.

CHANGES IN VERSION 4.0.1-SNAPSHOT
=================================

* Replaced REST Assured client with Apache HttpComponents HttpClient - MIME coded entities.
* Removed testng version 6 dependency.


CHANGES IN VERSION 4.0.0-SNAPSHOT
=================================

* Upgrade to Cucumber-JVM 5.0.0-RC1
* Add new Courgette Option "plugin" to support additional Courgette integrations.
    * Add "reportportal" plugin which integrates with https://reportportal.io/ to publish the report after the test run.
* Changed CourgetteOptions to use the courgette.api.CucumberOptions class instead of Cucumber provided classes.
* When the JUnit Courgette runner is invoked from the IDE, the run notifier is now updated with the result (_pass or fail_) after the test run.
    

CHANGES IN VERSION 3.3.0
========================

* Upgrade to Cucumber-JVM 4.3.0


CHANGES IN VERSION 3.2.0
========================

* Add new Courgette Option "rerunAttempts" to enable Courgette to rerun failed scenarios 'X' number of times before failing the test if does not succeed (_default is 1_).


CHANGES IN VERSION 3.1.0
========================

* Add new status labels for _Passed after Rerun_ and _Failed after Rerun_ statuses in the Courgette html report.
* Add functionality to filter reruns in the Courgette html report.
* Fixed issued where the number "2" is appended to the scenario name in the Cucumber xml report.


CHANGES IN VERSION 3.0.1
========================

* Fixed bug in JUnit xml parser which caused a MissingFormatArgumentException.


CHANGES IN VERSION 3.0.0
========================

* Upgrade to Cucumber-JVM 4.2.0
* Add support for JDK 11.
* Fixed jrt module path which raised an error on Windows OS.


CHANGES IN VERSION 2.4.4
========================

* Add setup and teardown hooks to Courgette (PR from jamsesso)


CHANGES IN VERSION 2.4.3
========================

* Add support for multithreaded JUnit reports.
    * A single xml report will be generated if the Cucumber junit plugin is specified: _plugin = { junit:output-dir-path/cucumber.xml }_


CHANGES IN VERSION 2.4.2
========================

* Removed System.exit() from the JUnit runner as this was causing a Gradle MessageIOException on Windows operating systems.
* Updated runtime options to use the default runner options when empty system properties are provided. (_such as -Dcucumber.tag=' '_)


CHANGES IN VERSION 2.4.1
========================

* Add support to specify the feature path(s) at runtime using a system property (_multiple feature paths can be specified using a comma_)
    * Single feature file
      * -Dcucumber.features="src/test/folder/Test.feature"
    * Multiple feature file directorys
      * -Dcucumber.features="src/test/folder1, src/test/folder2"


CHANGES IN VERSION 2.4.0
========================

* Upgrade to Cucumber-JVM 3.0.1
* Remove --format Cucumber option when creating Courgette runtime options as this option is no longer supported.
* Update Courgette-JVM html report to include Before and After step hooks (_new hooks introduced in Cucumber-JVM 3.0.1_)
* Change the way data table values are displayed in the Courgette-JVM html report.
* Fixed bug in JsonReportParser which throws an exception when parsing data table rows.

CHANGES IN VERSION 2.3.2
========================

* Add support to use TestNG to run Cucumber features and scenarios in parallel. You can now extend your runner class with TestNGCourgette. [Enhancement Request](https://github.com/prashant-ramcharan/courgette-jvm/issues/50)


CHANGES IN VERSION 2.3.1
========================

* Add support for JDK 10.
* Update Courgette report to include data table row info.
* Update Courgette report to include feature and line info on the modal title.


CHANGES IN VERSION 2.2.1
========================

* Bug Fixes

    * Fixed issue which caused Cucumber reports to be incorrectly created due to missing plugins.
    * Added missing background steps to Courgette-JVM html report.


CHANGES IN VERSION 2.2.0
========================

* Add ability to override default courgette report target directory (PR from Andrejs)


CHANGES IN VERSION 2.1.0
========================

 * Bug Fix
    * Non reporting plugins are not added to runtime options.


CHANGES IN VERSION 2.0.0
========================

* Upgrade to Cucumber-JVM 2.4.0
* Change Courgette-JVM html report to support additional Cucumber-JVM 2+ statuses.


CHANGES IN VERSION 1.6.1
========================

* Add all custom step outputs (scenario.write) to Courgette html report.
* Fixed modal overflow in Courgette html report where text overflows the bounds of the modal.


CHANGES IN VERSION 1.6.0
========================

* Update Courgette-JVM html report. Report now includes all step definitions, embedded screenshots, thrown exceptions, pie chart and Courgette run information.
* Remove "cucumber.options" system property (if set by the client) before calling the CLI because cucumber options are already parsed by Courgette beforehand.


CHANGES IN VERSION 1.5.1
========================

* Add feature to provide non standard VM options for each VM thread.


CHANGES IN VERSION 1.5.0
========================

* Courgette options (threads, runLevel, rerunFailedScenarios, showTestOutput) can now be overridden at runtime.
* Remove unnecessary href from Courgette Html report.


CHANGES IN VERSION 1.4.3
========================

* Add default Cucumber runtime options (dryRun, strict, monochrome) to Courgette.


CHANGES IN VERSION 1.4.2
========================

* Propagate Cucumber exception to Courgette when Cucumber features fail to load.
* Fixed bug which causes the Gradle build to fail when there are no matching features using the provided tags.


CHANGES IN VERSION 1.4.1
========================

* Add functionality to override the cucumber options set the in Courgette runner.


CHANGES IN VERSION 1.4.0
========================

* Add new Courgette-JVM html report. (Reports are fully searchable and pagniated)


CHANGES IN VERSION 1.3.2
========================

* Fixed temp directory path for Unix (Ubuntu) systems.


CHANGES IN VERSION 1.3.1
========================

* Fixed JSON output bug.


CHANGES IN VERSION 1.3.0
========================

* Add support to run scenarios (in addition to running features) in parallel.
* Add new Courgettte option - runLevel


CHANGES IN VERSION 1.2.0
========================

* Add Courgette Feature runner.
* Removed Courgette CLI runner.
* Add showTestOuput runtime option.
* Add all system properties to Courgette Feature runner.


CHANGES IN VERSION 1.1.1
========================

* Update feature parser.


CHANGES IN VERSION 1.1.1
========================

* Add Cucumber-Java8 dependancy
* Courgette no longer extends from Cucumber - it now extends from ParentRunner.


CHANGES IN VERSION 1.0.0
========================

* Initial version release
