---
layout: docs
title: Reporters
permalink: /documentation/using-testcafe/common-concepts/reporters.html
checked: true
---
# Reporters

Reporters are plugins used to output test run reports in a certain format.

TestCafe ships with the following reporters:

* [spec](https://github.com/DevExpress/testcafe-reporter-spec) - used by default
* [list](https://github.com/DevExpress/testcafe-reporter-list)
* [minimal](https://github.com/DevExpress/testcafe-reporter-minimal)
* [xUnit](https://github.com/DevExpress/testcafe-reporter-xunit)
* [JSON](https://github.com/DevExpress/testcafe-reporter-json)

You can also create a [custom reporter](/testcafe/documentation/extending-testcafe/custom-reporter-plugin/) that will fulfill your needs.

For more information about the reporters, see the following sections.

* [Searching for Reporter Plugins](#searching-for-reporter-plugins)
* [Installing the Reporters](#installing-the-reporters)
* [Using the Reporters](#using-the-reporters)

## Searching for Reporter Plugins

Reporter plugins are npm packages. The reporter package name consists of two parts - the `{testcafe-reporter-}` prefix and the name of a reporter itself; for example, `{testcafe-reporter-list}`.

You can search for available reporter packages on npm: [https://www.npmjs.com/search?q=testcafe-reporter](https://www.npmjs.com/search?q=testcafe-reporter).

## Installing the Reporters

You can install reporter packages from npm in two ways:

* **locally** - if you are going to use reporters within TestCafe installed locally.

    Navigate to your project directory and run `npm install --save-dev testcafe-reporter-{reporterName}`.
    Note that the reporter package name must follow the `testcafe-reporter-{reporterName}` pattern.

    The following example demonstrates how you can install the list reporter package.

    ```bash
    npm install --save-dev testcafe-reporter-list
    ```

* **globally** - if the TestCafe module is installed globally or you are going to use reporters within other projects as well.

    Run the `npm install` command with the `-g` flag.

    ```bash
    npm install -g testcafe-reporter-list
    ```

## Using the Reporters

When running tests, you can select a reporter to generate test reports.
You can do this when working both through the
[command line](../command-line-interface.md#-r-name---reporter-name)
and [programmatically](../programming-interface/runner.md#reporter).