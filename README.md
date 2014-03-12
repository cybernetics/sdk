The Codenvy SDK is a free and open Java framework for building Web client applications that are beautiful, fast, and modular. The SDK contains:
* Codenvy IDE
* Codenvy WCP
* Platform APIs
* Commons Utility Libraries
* 15+ Plug-Ins
* Developer tooling for building and packaging plug-ins

The Codenvy IDE is a Web client application that contains a variety of plug-ins, makes use of the platform APIs, and runs on the Codenvy Web Client Platform (WCP).  The WCP is a thin servlet-based framework that loads and manages plug-ins.  The WCP can be run in any servlet container.  The build process for the SDK combines all of these components into an assembly readied for Tomcat.  Tomcat is also included in the distribution to make startup configuration simpler. 

The Codenvy SDK can be installed on any operating system that supports Java 1.7 - desktop, server or cloud. It has been extensively tested on Ubuntu, Linux, MacOS and Windows.  Java, GWT, GIN and Javascript are the core technologies used to build the SDK.

The Codenvy SDK is licensed on a proprietary Codenvy license. We will provide an open license for the SDK once it has hit a stabilization point.

![image] (http://docs.codenvy.com/wp-content/uploads/editor1.png)

### Clone the Repository

```sh
git clone https://github.com/codenvy/sdk.git
```

The Codenvy SDK is an assembly point for other projects that combine together to construct the system. These projects include:
* **IDE**:                     [IDE and Default Plug-Ins] (http://github.com/codenvy/ide)
* **Platform API**:            [REST APIs and Platform Services] (http://github.com/codenvy/platform-api)
* **Platform API GWT Client**: [Client Library for Platform API] (http://github.com/codenvy/platform-api-client-gwt)
* **Commons**:                 [Shared Utility Libraries] (http://github.com/codenvy/commons)
* **Everrest**:                [Command Palette Abstraction on Web Services] (http://github.com/codenvy/everrest)
* **Plugin Datasource**:       [Community Developed Database Plugin] (http://github.com/codenvy/plugin-datasource)


### Build the Project
```sh
cd /sdk
mvn clean install
```

### Run the Codenvy SDK
```sh
cd assembly-sdk/target/tomcat-ide/bin
./codenvy
```

The hosted IDE will be available at ```localhost:8080```

### Add Your Extensions (Plug-Ins) to the SDK

1. Package your extension as a JAR either offline or in the IDE.  If in the IDE, go to **Project** menu and build your extension. After the build is finished you will see a link in the Output console that points to a location to download your artifacts.  

2. Copy the JAR artifact from the previous step to ```/ext``` directory of the SDK.  

3. Execute ```extInstall``` script in the root of the SDK to load this plug-in. The project will be re-compiled.

4. Restart the SDK to have the changes take affect permanently.

You may need to empty browser’s cache (if you haven’t set appropriate HTTP headers) to see the extension.

### Helping Codenvy

**Contribute**: Codenvy accepts pull requests, so if you feel like contributing to the project, you are definitely welcome to do so.

**Report Bugs**: Our JIRA is private at the moment but we are working to open it up. In the mean time we accept bug and enhancement requests by posting on our Google Group. 

### Documentation & Tutorials
* **SDK Binaries** [docs.codenvy.com/sdk/download] (http://docs.codenvy.com/sdk/download/)
* **SDK Getting Started** [http://docs.codenvy.com/sdk/introduction/] (http://docs.codenvy.com/sdk/introduction/)
* **SDK JavaDoc** [docs.codenvy.com/ide/apidocs/] (http://docs.codenvy.com/ide/apidocs/)
* **SDK Extension Tutorials** [http://docs.codenvy.com/sdk/writing-your-first-codenvy-extension/] (http://docs.codenvy.com/sdk/writing-your-first-codenvy-extension/)


### Contact Information
* **Website:** [www.codenvy.com](https://www.codenvy.com)
* **Twitter:** [@CodenvyHQ](https://twitter.com/CoenvyHQ)
* **Blog:** [blog.codenvy.com](http://blog.codenvy.com)
* **Google Group:** [helpdesk.codenvy.com] (https://groups.google.com/a/codenvy.com/forum/#!forum/codenvy)
