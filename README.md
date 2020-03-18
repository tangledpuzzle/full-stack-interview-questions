# 3700 Tech Interview Questions and Answers from [FullStack.Cafe](https://www.fullstack.cafe)

> All ~3700 Answers available on [FullStack.Cafe - Never Fail Your Tech Interview Again](https://www.fullstack.cafe).

<p align="center">
  <a href="https://www.fullstack.cafe/?promocode=GITHUB">
  <img src="https://user-images.githubusercontent.com/13550565/76865667-04a0f400-689e-11ea-8500-1bd60f5014ce.png">
  </a>
</p>

## <a name='toc'>Table of Contents</a>
 * [.NET Core](#.NETCore)
 * [ADO.NET](#ADO.NET)
 * [ASP.NET](#ASP.NET)
 * [ASP.NET MVC](#ASP.NETMVC)
 * [ASP.NET Web API](#ASP.NETWebAPI)
 * [AWS](#AWS)
 * [Agile & Scrum](#Agile&Scrum)
 * [Android](#Android)
 * [Angular](#Angular)
 * [AngularJS](#AngularJS)
 * [Azure](#Azure)
 * [Behavioral](#Behavioral)
 * [Big Data](#BigData)
 * [Blockchain](#Blockchain)
 * [Bootstrap](#Bootstrap)
 * [C#](#C#)
 * [CSS](#CSS)
 * [Career](#Career)
 * [Clojure](#Clojure)
 * [Code Problems](#CodeProblems)
 * [Data Science](#DataScience)
 * [Data Structures](#DataStructures)
 * [Design Patterns](#DesignPatterns)
 * [DevOps](#DevOps)
 * [Docker](#Docker)
 * [Entity Framework](#EntityFramework)
 * [Flutter](#Flutter)
 * [Git](#Git)
 * [Golang](#Golang)
 * [GraphQL](#GraphQL)
 * [HTML5](#HTML5)
 * [Ionic](#Ionic)
 * [JSON](#JSON)
 * [Java](#Java)
 * [JavaScript](#JavaScript)
 * [Kotlin](#Kotlin)
 * [LINQ](#LINQ)
 * [Laravel](#Laravel)
 * [MSMQ](#MSMQ)
 * [Machine Learning](#MachineLearning)
 * [Microservices](#Microservices)
 * [MongoDB](#MongoDB)
 * [Node.js](#Node.js)
 * [OOP](#OOP)
 * [PHP](#PHP)
 * [PWA](#PWA)
 * [PowerShell](#PowerShell)
 * [Python](#Python)
 * [Questions to Ask](#QuestionstoAsk)
 * [React](#React)
 * [React Native](#ReactNative)
 * [Reactive Programming](#ReactiveProgramming)
 * [Redux](#Redux)
 * [Ruby](#Ruby)
 * [Ruby on Rails](#RubyonRails)
 * [SOA & REST API](#SOA&RESTAPI)
 * [SQL](#SQL)
 * [Software Architecture](#SoftwareArchitecture)
 * [Software Testing](#SoftwareTesting)
 * [Spring](#Spring)
 * [Statistics](#Statistics)
 * [T-SQL](#T-SQL)
 * [TypeScript](#TypeScript)
 * [UX Design](#UXDesign)
 * [Vue.js](#Vue.js)
 * [WCF](#WCF)
 * [WPF](#WPF)
 * [Web Security](#WebSecurity)
 * [Webpack](#Webpack)
 * [XML & XSLT](#XML&XSLT)
 * [Xamarin](#Xamarin)
 * [iOS & Swift](#iOS&Swift)
 * [jQuery](#jQuery)
## [[⬆]](#toc) <a name=.NETCore>.NET Core</a> Interview Questions
#### Q1: What is the difference between String and string in C#? ⭐
**Answer:**
`string` is an alias in C# for `System.String`. So technically, there is no difference. It's like `int` vs. `System.Int32`.

As far as guidelines, it's generally recommended to use `string` any time you're referring to an object.
```csharp
string place = "world";
```

Likewise, it's generally recommended to use `String` if you need to refer specifically to the class.
```csharp
string greet = String.Format("Hello {0}!", place);
```

**Source:** _blogs.msdn.microsoft.com_

#### Q2: What is .NET Standard? ⭐
**Answer:**
The **.NET Standard** is a formal specification of .NET APIs that are intended to be available on all .NET implementations.

**Source:** _docs.microsoft.com_

#### Q3: What is .NET Core? ⭐
**Answer:**
The .NET Core platform is a new .NET stack that is optimized for open source development and agile delivery on NuGet. 

.NET Core has two major components. It includes a small runtime that is built from the same codebase as the .NET Framework CLR. The .NET Core runtime includes the same GC and JIT (RyuJIT), but doesn’t include features like Application Domains or Code Access Security. The runtime is delivered via NuGet, as part of the ASP.NET Core package.

.NET Core also includes the base class libraries. These libraries are largely the same code as the .NET Framework class libraries, but have been factored (removal of dependencies) to enable to ship a smaller set of libraries. These libraries are shipped as `System.*` NuGet packages on NuGet.org.

**Source:** _stackoverflow.com_

#### Q4: What is the .NET Framework? ⭐
**Answer:**
The .NET is a Framework, which is a collection of classes of reusable libraries given by Microsoft to be used in other .NET applications and to develop, build and deploy many types of applications on the Windows platform including the following:

*   Console Applications
*   Windows Forms Applications
*   Windows Presentation Foundation (WPF) Applications
*   Web Applications
*   Web Services
*   Windows Services
*   Services-oriented applications using Windows Communications Foundation (WCF)
*   Workflow-enabled applications using Windows Workflow Foundation(WF)

**Source:** _c-sharpcorner.com_

#### Q5: What's the difference between SDK and Runtime in .NET Core? ⭐⭐
**Answer:**
* The SDK is all of the stuff that is needed/makes developing a .NET Core application easier, such as the CLI and a compiler.

* The runtime is the "virtual machine" that hosts/runs the application and abstracts all the interaction with the base operating system.

**Source:** _stackoverflow.com_

#### Q6: What is .NET Standard and why we need to consider it? ⭐⭐
**Answer:**
 1. **.NET Standard** solves the code sharing problem for .NET developers across all platforms by bringing all the APIs that you expect and love across the environments that you need: desktop applications, mobile apps & games, and cloud services:
 2. **.NET Standard** is a **set of APIs** that **all** .NET platforms **have to implement**. This **unifies the .NET platforms** and **prevents future fragmentation**.
 3. **.NET Standard 2.0** will be implemented by **.NET Framework**, .**NET Core**,
    and **Xamarin**. For **.NET Core**, this will add many of the existing APIs
    that have been requested.
 3. **.NET Standard 2.0** includes a compatibility shim for **.NET Framework** binaries, significantly increasing the set of libraries that you can reference from your .NET Standard libraries.
 4. **.NET Standard** **will replace Portable Class Libraries (PCLs)** as the
    tooling story for building multi-platform .NET libraries.

<div class="text-center">
<img src="https://i.stack.imgur.com/tE1ny.png" class="img-fluid" style="max-width: 500px;"/>
</div>

**Source:** _stackoverflow.com_

#### Q7: What is the difference between decimal, float and double in .NET?  ⭐⭐
**Details:**
When would someone use one of these?

**Answer:**
Precision is the main difference.

* Float - 7 digits (32 bit)
* Double-15-16 digits (64 bit)
* Decimal -28-29 significant digits (128 bit)

As for what to use when:

* For values which are "naturally exact decimals" it's good to use decimal. This is usually suitable for any concepts invented by humans: financial values are the most obvious example, but there are others too. Consider the score given to divers or ice skaters, for example.

* For values which are more artefacts of nature which can't really be measured exactly anyway, float/double are more appropriate. For example, scientific data would usually be represented in this form. Here, the original values won't be "decimally accurate" to start with, so it's not important for the expected results to maintain the "decimal accuracy". Floating binary point types are much faster to work with than decimals.

**Source:** _blogs.msdn.microsoft.com_

#### Q8: What are some characteristics of .NET Core? ⭐⭐
**Answer:**
* **Flexible deployment**: Can be included in your app or installed side-by-side user- or machine-wide.

* **Cross-platform**: Runs on Windows, macOS and Linux; can be ported to other OSes. The supported Operating Systems (OS), CPUs and application scenarios will grow over time, provided by Microsoft, other companies, and individuals.

* **Command-line tools**: All product scenarios can be exercised at the command-line.

* **Compatible**: .NET Core is compatible with .NET Framework, Xamarin and Mono, via the .NET Standard Library.

* **Open source**: The .NET Core platform is open source, using MIT and Apache 2 licenses. Documentation is licensed under CC-BY. .NET Core is a .NET Foundation project.

* **Supported by Microsoft**: .NET Core is supported by Microsoft, per .NET Core Support

**Source:** _stackoverflow.com_

#### Q9: What is an unmanaged resource?  ⭐⭐
**Answer:**
Use that rule of thumb: 
* If you found it in the Microsoft .NET Framework: _it's managed_. 
* If you went poking around MSDN yourself, _it's unmanaged_. 

Anything you've used P/Invoke calls to get outside of the nice comfy world of everything available to you in the .NET Framwork is unmanaged – and you're now _responsible_ for cleaning it up.

**Source:** _stackoverflow.com_

#### Q10: What is CTS? ⭐⭐
**Answer:**
The **Common Type System (CTS)** standardizes the data types of all programming languages using .NET under the umbrella of .NET to a common data type for easy and smooth communication among these .NET languages. 

CTS is designed as a singly rooted object hierarchy with `System.Object` as the base type from which all other types are derived. CTS supports two different kinds of types: 

1. **Value Types**: Contain the values that need to be stored directly on the stack or allocated inline in a structure. They can be built-in (standard primitive types), user-defined (defined in source code) or enumerations (sets of enumerated values that are represented by labels but stored as a numeric type).
2. **Reference Types**: Store a reference to the value‘s memory address and are allocated on the heap. Reference types can be any of the pointer types, interface types or self-describing types (arrays and class types such as user-defined classes, boxed value types and delegates).

**Source:** _c-sharpcorner.com_

#### Q11: What is the difference between .NET Core and Mono? ⭐⭐
**Answer:**
To be simple:
* Mono is third party implementation of .Net Framework for Linux/Android/iOs
* .Net Core is Microsoft's own implementation for same.

**Source:** _stackoverflow.com_

#### Q12: What is MSIL? ⭐⭐
**Answer:**
When we compile our .NET code then it is not directly converted to native/binary code; it is first converted into intermediate code known as MSIL code which is then interpreted by the CLR. MSIL is independent of hardware and the operating system. Cross language relationships are possible since MSIL is the same for all .NET languages. MSIL is further converted into native code.  

**Source:** _c-sharpcorner.com_

#### Q13: What is a .NET application domain? ⭐⭐
**Answer:**
It is an isolation layer provided by the .NET runtime. As such, App domains live with in a process (1 process can have many app domains) and have their own virtual address space.

App domains are useful because:

* They are less expensive than full processes
* They are multithreaded
* You can stop one without killing everything in the process
* Segregation of resources/config/etc
* Each app domain runs on its own security level

**Source:** _stackoverflow.com_

#### Q14: What is CLR? ⭐⭐
**Answer:**
The **CLR** stands for Common Language Runtime and it is an Execution Environment. It works as a layer between Operating Systems and the applications written in .NET languages that conforms to the Common Language Specification (CLS). The main function of Common Language Runtime (CLR) is to convert the Managed Code into native code and then execute the program.

**Source:** _c-sharpcorner.com_

#### Q15: Name some CLR services? ⭐⭐
**Answer:**
**CLR services**

*   Assembly Resolver
*   Assembly Loader
*   Type Checker
*   COM marshalled
*   Debug Manager
*   Thread Support
*   IL to Native compiler
*   Exception Manager
*   Garbage Collector

**Source:** _c-sharpcorner.com_

#### Q16: Talk about new .csproj file? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q17: Explain what is included in .NET Core? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q18: Is there a way to catch multiple exceptions at once and without code duplication? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q19: What about NuGet packages and packages.config? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q20: Why to use of the IDisposable interface? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q21: When should we use .NET Core and .NET Standard Class Library project types? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q22: What is the difference between Class Library (.NET Standard) and Class Library (.NET Core)? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q23: What is the difference between .NET Standard and PCL (Portable Class Libraries)? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q24: Explain the difference between Task and Thread in .NET ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q25: What is FCL? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q26: What is Kestrel? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q27: What is implicit compilation? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q28: What is JIT compiler? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q29: What is .NET Standard? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q30: What is Explicit Compilation? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q31: What are the benefits of explicit compilation? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q32: Explain the difference between “managed” and “unmanaged” code? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q33: What's the difference between .NET Core, .NET Framework, and Xamarin? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q34: What is difference between .NET Core and .NET Framework? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q35: Explain two types of deployment for .NET Core applications ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q36: What does Common Language Specification (CLS) mean? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q37: What is CoreCLR? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q38: What's is BCL? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q39: What is the difference between CIL and MSIL (IL)? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q40: How to choose the target version of .NET Standard library? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q41: Why does .NET use a JIT compiler instead of just compiling the code once on the target machine? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q42: What is the difference between AppDomain, Assembly, Process, and a Thread? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q43: What are benefits of using JIT? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q44: What is the difference between .NET Framework/Core and .NET Standard Class Library project types? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q45: What's the difference between RyuJIT and Roslyn? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q46: Why does .NET Standard library exist? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q47: Explain how does Asynchronous tasks (Async/Await) work in .NET? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q48: Explain Finalize vs Dispose usage? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q49: How many types of JIT Compilations do you know? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q50: What is the difference between Node.js async model and async/await in .NET? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q51: Could you name the difference between .Net Core, Portable, Standard, Compact, UWP, and PCL? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

## [[⬆]](#toc) <a name=ADO.NET>ADO.NET</a> Interview Questions
#### Q1: What is ADO.NET? ⭐
**Answer:**
**ADO** stands for Active Data Object and ADO.NET is a set of .NET libraries for ADO.
NET is a collection of managed libraries used by .NET applications for data source communication using a driver or provider:

*   Enterprise applications handle a large amount of data. This data is primarily stored in relational databases, such as Oracle, SQL Server, and Access and so on. These databases use Structured Query Language (SQL) for retrieval of data.  
*   To access enterprise data from a .NET application, an interface was needed. This interface acts as a bridge between an RDBMS system and a .NET application. ADO.NET is such an interface that is created to connect .NET applications to RDBMS systems.  
*   In the .NET framework, Microsoft introduced a new version of Active X Data Objects (ADO) called ADO.NET. Any .NET application, either Windows based or web based, can interact with the database using a rich set of classes of the ADO.NET library. Data can be accessed from any database using connected or disconnected architecture.

**Source:** _c-sharpcorner.com_

#### Q2: What is exactly meaning of disconnected and connected approach in ADO.NET? ⭐⭐
**Answer:**
In short:
* **Disconnected** = Make Connection , Fetch Data , Close Connection
* **Connected** = Make Connection , Keep Connection alive , Close Connection when close is called.

The ADO.net architecture, in which connection must be kept open till the end to retrieve and access data from database is called as _connected architecture_. Connected architecture is built on the these types - `connection`, `command`, `datareader`

The ADO.net architecture, in which connection will be kept open only till the data retrieved from database, and later can be accessed even when connection to database is closed is called as _disconnected architecture_. Disconnected architecture of ADO.net is built on these types - `connection`, `dataadapter`, `commandbuilder` and `dataset` and `dataview`. 

**Source:** _stackoverflow.com_

#### Q3: Describe when you would use the DataView in ADO.NET? ⭐⭐
**Answer:**
A **DataView** enables you to create different views of the data stored in a DataTable, a capability that is often used in data binding applications. Using a DataView, you can expose the data in a table with different sort orders, and you can filter the data by row state or based on a filter expression. A DataView provides a dynamic view of data whose content, ordering, and membership reflect changes to the underlying DataTable as they occur. This is different from the Select method of the DataTable, which returns a DataRow array from a table per particular filter and/or sort order and whose content reflects changes to the underlying table, but whose membership and ordering remain static. The dynamic capabilities of the DataView make it ideal for data-binding applications.

**Source:** _stackoverflow.com_

#### Q4: What is the SqlCommandBuilder? ⭐⭐
**Answer:**
**CommandBuilder** helps you to generate update, delete, and insert commands on a single database table for a data adapter. Similar to other objects, each data provider has a command builder class. The OleDbCommandBuilder, SqlCommonBuilder, and OdbcCommandBuilder classes represent the CommonBuilder object in the OleDb, Sql, and ODBC data providers.

**Source:** _c-sharpcorner.com_

#### Q5: What is the DataAdapter Object in ADO.NET? ⭐⭐
**Answer:**
A **DataAdapter** is used to retrieve data from a data source and populate tables within a `DataSet`. Data Adapters form the bridge between a data source and a dataset. The `DataAdapter` also resolves changes made to the `DataSet` back to the data source. The `DataAdapter` uses the `Connection` object of the .NET Framework data provider to connect to a data source, and it uses `Command` objects to retrieve data from and resolve changes to the data source.

A `DataAdapter` supports mainly the following two methods:

*   **Fill():** The Fill method populates a dataset or a data table object with data from the database. It retrieves rows from the data source using the SELECT statement specified by an associated select command property. The Fill method leaves the connection in the same state as it encountered before populating the data.     
*   **Update():** The Update method commits the changes back to the database. It also analyzes the RowState of each record in the DataSet and calls the appropriate INSERT, UPDATE, and DELETE statements.

**Source:** _c-sharpcorner.com_

#### Q6: What is the basic difference between ADO.NET and Entity Framework? ⭐⭐
**Answer:**
ADO.NET Entity Framework is an ORM (object-relational mapping) which creates a higher abstract object model over ADO.NET components. ADO.NET is a layer closer to the database (datatables, datasets and etc...). The main and the only benefit of EF is it auto-generates code for the Model (middle layer), Data Access Layer, and mapping code, thus reducing a lot of development time. Consider the following example:

**ADO.NET**:
```csharp
DataTable table = adoDs.Tables[0];
for (int j = 0; j < table.Rows.Count; j++)
{
    DataRow row = table.Rows[j];

    // Get the values of the fields
    string CustomerName =
        (string)row["Customername"];
    string CustomerCode =
        (string)row["CustomerCode"];
}
```

**EF**:
```csharp
foreach (Customer objCust in obj.Customers)
{}
```

**Source:** _stackoverflow.com_

#### Q7: What is Connection Pooling in ADO.NET? ⭐⭐
**Answer:**
ADO.NET uses a technique called **connection pooling**, which minimizes the cost of repeatedly opening and closing connections. Connection pooling reuses existing active connections with the same connection string instead of creating new connections when a request is made to the database. It involves the use of a connection manager that is responsible for maintaining a list, or pool, of available connections for a given connection string. Several pools exist if different connection strings ask for connection pooling.

**Source:** _c-sharpcorner.com_

#### Q8: What is SqlCommand Object? ⭐⭐
**Answer:**
The **SqlCommand** carries the SQL statement that needs to be executed on the database. SqlCommand carries the command in the CommandText property and this property will be used when the SqlCommand calls any of its execute methods.

*   The Command Object uses the connection object to execute SQL queries.
*   The queries can be in the form of Inline text, Stored Procedures or direct Table access.
*   An important feature of Command object is that it can be used to execute queries and Stored Procedures with Parameters.
*   If a select query is issued, the result set it returns is usually stored in either a DataSet or a DataReader object.

The three important methods exposed by the SqlCommand object is shown below:

*   ExecuteScalar
*   ExecuteNonQuery
*   ExecuteReader

**Source:** _c-sharpcorner.com_

#### Q9: What are the ADO.NET components? ⭐⭐
**Answer:**
ADO.NET components categorized in three modes: 
* disconnected, 
* common or shared and 
* the .NET data providers.

The disconnected components build the basic ADO.NET architecture. You can use these components (or classes) with or without data providers. For example, you can use a `DataTable` object with or without providers and shared or common components are the base classes for data providers. Shared or common components are the base classes for data providers and shared by all data providers. The data provider components are specifically designed to work with different kinds of data sources. For example, ODBC data providers work with ODBC data sources and OleDb data providers work with OLE-DB data sources.

**Source:** _c-sharpcorner.com_

#### Q10: How can you define the DataSet structure? ⭐⭐
**Answer:**
A **DataSet** object falls in disconnected components series. The `DataSet` consists of a collection of tables, rows, columns and relationships.

`DataSet` contains a collection of `DataTables` and the `DataTable` contains a collection of `DataRows`, `DataRelations`, and `DataColumns`. A `DataTable` maps to a table in the database.

**Source:** _c-sharpcorner.com_

#### Q11: What do you understand by DataRelation class? ⭐⭐
**Answer:**
The **DataRelation** is a class of disconnected architecture in the .NET framework. It is found in the System.Data namespace. It represents a relationship between database tables and correlates tables on the basis of matching column.

**Source:** _c-sharpcorner.com_

#### Q12: How could you control connection pooling behavior?  ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q13: What is the difference between ExecuteScalar, ExecuteReader and ExecuteNonQuery? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q14: What is the difference between DataView, DataTable and DataSet? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q15: Could you explain me some of the main differences between Connection-oriented access and connectionless access in ADO.NET? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q16: What is the difference between Integrated Security = True and Integrated Security = SSPI? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q17: What is Unit Of Work? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q18: What are the differences between using SqlDataAdapter vs SqlDataReader for getting data from a DB? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q19: Mention what is the difference between ADO.NET and classic ADO? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q20: Can you explain the difference between a DataReader, a DataAdapter, a Dataset, and a DataView? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q21: Name types of transactions in ADO.NET ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q22: Where should I use disconnected architecture approach? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q23: Where should I use connected architecture approach? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q24: Is there anything faster than SqlDataReader in .NET? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q25: Could you explain some benefits of Repository Pattern? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q26: What is the difference between OLE DB and ODBC data sources? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q27: How could you monitor connection pooling behavior? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q28: Is it necessary to manually close and dispose of SqlDataReader? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q29: What's better: DataSet or DataReader? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q30: What is the difference between ADODB, OLEDB and ADO.NET? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q31: What is the best and fast way to insert 2 million rows of data into SQL Server? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q32: Under what scenarios would setting pooling=false in an ADO.NET connection string be of value when connecting to SQL Server?  ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q33: Name some problems that could occur with connection pooling ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

## [[⬆]](#toc) <a name=ASP.NET>ASP.NET</a> Interview Questions
#### Q1: What is ViewData? ⭐
**Answer:**
Viewdata contains the key, value pairs as dictionary and this is derived from class — “ViewDataDictionary“. In action method we are setting the value for viewdata and in view the value will be fetched by typecasting.

**Source:** _medium.com_

#### Q2: What is ASP.Net? ⭐
**Answer:**
It is a framework developed by Microsoft on which we can develop new generation web sites using web forms(aspx), MVC, HTML, Javascript, CSS etc. Its successor of Microsoft Active Server Pages(ASP). Currently there is ASP.NET 4.0, which is used to develop web sites. There are various page extensions provided by Microsoft that are being used for web site development. Eg: aspx, asmx, ascx, ashx, cs, vb, html, XML etc. 


**Source:** _guru99.com_

#### Q3: Talk about Logging in ASP.NET Core? ⭐⭐
**Answer:**
**Logging** is built-in and you get access to structured logs from the ASP.NET Core host itself to your application. With tools like [Serilog,](https://github.com/serilog/serilog-aspnetcore) you can extend your logging [easily](https://github.com/serilog/serilog-sinks-rollingfile) and save your logs to file, Azure, Amazon or any other output provider. You can configure verbosity and log levels via configuration (appsettings.json by default), and you can configure log levels by different categories.

**Source:** _talkingdotnet.com_

#### Q4: Explain startup process in ASP.NET Core? ⭐⭐
**Answer:**
Everything starts from Program.cs
```csharp
public static void Main(string[] args)
{
    BuildWebHost(args).Run();
}
 
public static IWebHost BuildWebHost(string[] args) =>
    WebHost.CreateDefaultBuilder(args)
        .UseStartup<Startup>()
        .Build();
```

CreateDefaultBuilder extension method will create a default configuration which will look first into `appsettings.json` files then will look for Environment variables and at the end, it will use command line arguments.

This part will also set up default logger sources (debug and console) and load the settings for logging from appsettings.json.

After the `CreateDefaultBuilder` finishes, then `Startup` class is executed. First, the constructor code is executed. After that, services are added to DI container via `AddServices` method that lives in Startup class. After that, an order of middleware that will handle every incoming request is set up.

**Source:** _codingblast.com_

#### Q5: What exactly is an application pool? What is its purpose? ⭐⭐
**Answer:**
**Application pools** allow you to isolate your applications from one another, even if they are running on the same server. This way, if there is an error in one app, it won't take down other applications.

Additionally, applications pools allow you to separate different apps which require different levels of security.

**Source:** _stackoverflow.com_

#### Q6: How you can add an event handler? ⭐⭐
**Answer:**
** **Using the Attributes property of server side control. 

e.g. 
```csharp
btnSubmit.Attributes.Add("onMouseOver","JavascriptCode();")
```

**Source:** _guru99.com_

#### Q7: What's the use of Response.Output.Write()? ⭐⭐
**Answer:**
We can write formatted output using Response.Output.Write(). 

**Source:** _guru99.com_

#### Q8: How to configure your ASP.NET Core app? ⭐⭐
**Answer:**
Another crucial part of ASP.NET Core Framework is Configuration. Also, it is part of Dependency Injection. Use it anywhere in your code with an option to [reload on changes](https://codingblast.com/asp-net-core-configuration-reloading-binding-injecting/) of configuration values from sources (appsettings.json, environment variables, command line arguments, etc.). It is also easy to override, extend and customize the Configuration. No more extensive configurations in web.config, the preferred way now is _**appsettings.json**_ in combination with a mix of Environment variables and cmd-line args.

**Source:** _talkingdotnet.com_

#### Q9: What is ASP.NET Core? ⭐⭐
**Answer:**
ASP.NET Core is a brand new cross-platform web framework built with .NET Core framework. It is not an update to existing ASP.NET framework. It is a complete rewrite of the ASP.NET framework. It works with both .NET Core and .NET Framework.

Main characterestics of ASP.NET Core:

*   DI Container which is quite simple and built-in. You can extend it with other popular DI containers
*   Built-in and extensible structured logging. You can redirect output to as many sources as you want (file, Azure, AWS, console)
*   Extensible strongly typed configuration, which can also be used to reload at run-time
*   Kestrel – new, cross-platform and super fast web server which can stand alone without IIS, Nginx or Apache
*   New, fully async pipeline. It is easily configured via middleware
*   ASP.NET All meta package which improves development speed, and enables you to reference all Microsoft packages for ASP.NET Core and it will deploy only those that are being used by your code
*   There is no _web.config_. We now use _appsettings.json_ file in combination with other sources of configuration (command line args, environment variables, etc.)
*   There is no _Global._asax – We have _Startup.cs_ which is used to set up Middleware and services for DI Container.

**Source:** _talkingdotnet.com_

#### Q10: What is the difference between ASP.NET and ASP.NET MVC? ⭐⭐
**Answer:**
ASP.NET, at its most basic level, provides a means for you to provide general HTML markup combined with server side "controls" within the event-driven programming model that can be leveraged with VB, C#, and so on. You define the page(s) of a site, drop in the controls, and provide the programmatic plumbing to make it all work.

ASP.NET MVC is an application framework based on the Model-View-Controller architectural pattern. This is what might be considered a "canned" framework for a specific way of implementing a web site, with a page acting as the "controller" and dispatching requests to the appropriate pages in the application. The idea is to "partition" the various elements of the application, eg business rules, presentation rules, and so on.

Think of the former as the "blank slate" for implementing a site architecture you've designed more or less from the ground up. MVC provides a mechanism for designing a site around a pre-determined "pattern" of application access, if that makes sense. There's more technical detail to it than that, to be sure, but that's the nickel tour for the purposes of the question.

**Source:** _stackoverflow.com_

#### Q11: What is ViewState? ⭐⭐
**Answer:**
**View State** is the method to preserve the Value of the Page and Controls between round trips. It is a Page-Level State Management technique. View State is turned on by default and normally serializes the data in every control on the page regardless of whether it is actually used during a post-back.  
  
A web application is stateless. That means that a new instance of a page is created every time when we make a request to the server to get the page and after the round trip our page has been lost immediately  

**Source:** _c-sharpcorner.com_

#### Q12: Can ASP.NET Core work with the .NET framework? ⭐⭐
**Answer:**
Yes. This might surprise many, but ASP.NET Core works with .NET framework and this is officially supported by Microsoft.

ASP.NET Core works with:

*   .NET Core framework
*   .NET framework

**Source:** _talkingdotnet.com_

#### Q13: What is the good practice to implement validations in aspx page? ⭐⭐
**Answer:**
Client-side validation is the best way to validate data of a web page. It reduces the network traffic and saves server resources. 

**Source:** _guru99.com_

#### Q14: What is a postback? ⭐⭐
**Answer:**
A **postback** originates from the client browser. Usually one of the controls on the page will be manipulated by the user (a button clicked or dropdown changed, etc), and this control will initiate a postback. The state of this control, plus all other controls on the page (known as the View State) is Posted Back to the web server.

**Source:** _stackoverflow.com_

#### Q15: What is the file extension of ASP.NET web service? ⭐⭐
**Answer:**
Web services have file extension `.asmx`.

**Source:** _guru99.com_

#### Q16: How can we prevent browser from caching an ASPX page? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q17: In which event of page cycle is the ViewState available? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q18: From which base class all Web Forms are inherited? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q19: What is the meaning of Unobtrusive JavaScript? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q20: Explain JSON Binding? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q21: What is new in ASP.NET Core 2, compared to ASP.NET Core 1? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q22: What are the sub types of ActionResult? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q23: What exactly is the difference between .NET Core and ASP.NET Core? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q24: What is the difference between Server.Transfer and Response.Redirect? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q25: Where the viewstate is stored after the page postback? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q26:  How do you register JavaScript for webcontrols? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q27: Explain usage of Dependency Injection in ASP.NET Core ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q28: What are the different validators in ASP.NET?  ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q29: List the events in ASP.NET page life cycle ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q30: What is ViewState? How is it encoded? Is it encrypted? Who uses ViewState? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q31: Can we add code files of different languages in App_Code folder? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q32: What are the different types of caching? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q33: What are the event handlers that we can have in Global.asax file? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q34: Explain Middleware in ASP.NET Core? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q35: How long the items in ViewState exists? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q36: What is the difference between an HtmlInputCheckBox control and an HtmlInputRadioButton control? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q37: In which event are the controls fully loaded? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q38: Which type if caching will be used if we want to cache the portion of a page instead of whole page? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q39: How we can force all the validation controls to run? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q40: List the major built-in objects in ASP.NET? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q41: What is HttpModule in ASP.Net? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q42: What is RedirectPermanent in ASP.Net? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q43: What are the different types of cookies in ASP.NET? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q44: What is the difference between <system.web> and <system.webServer>? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q45: What is an HttpHandler in ASP.NET? Why and how is it used? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q46: What is the difference between Web Service and WCF Service? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q47: What is the difference between web config and machine config? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q48: Is it possible to create web application with both webforms and mvc? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q49: What is the difference between ASP.NET Core Web (.NET Core) vs ASP.NET Core Web (.NET Framework)? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q50: What are the different Session state management options available in ASP.NET? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q51: What is the difference between 'classic' and 'integrated' pipeline mode in IIS7? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q52: How can we apply Themes to an asp.net application? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q53: How to choose between ASP.NET 4.x and ASP.NET Core? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q54: What is Katana? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q55: What exactly is OWIN and what problems does it solve? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q56: Name some ASP.NET WebForms disadvantages over MVC? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q57: What is the difference between a web API and a web service? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q58: What is Cross Page Posting? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q59: What is the equivalent of WebForms in ASP.NET Core? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q60: Are static class instances unique to a request or a server in ASP.NET? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

## [[⬆]](#toc) <a name=ASP.NETMVC>ASP.NET MVC</a> Interview Questions
#### Q1: What is Layout in MVC? ⭐
**Answer:**
Layout pages are similar to master pages in traditional web forms. This is used to set the common look across multiple pages. In each child page we can find —

```html
@{
Layout = “~/Views/Shared/TestLayout1.cshtml”;
}
```

This indicates child page uses TestLayout page as it’s master page.

**Source:** _medium.com_

#### Q2: Explain Bundle.Config in MVC4? ⭐⭐
**Answer:**
**“BundleConfig.cs”** in MVC4 is used to register the bundles by the bundling and minification system. Many bundles are added by default including jQuery libraries like — jquery.validate, Modernizr, and default CSS references.

**Source:** _medium.com_

#### Q3: What is Razor View Engine? ⭐⭐
**Answer:**
**Razor** is the first major update to render HTML in MVC 3. Razor was designed specifically for view engine syntax. Main focus of this would be to simplify and code-focused templating for HTML generation. Below is the sample of using Razor:

```html
@model MvcMusicStore.Models.Customer
@{ViewBag.Title = “Get Customers”;}
<div class=”cust”> <h3><em>@Model.CustomerName</em> </h3>
```


**Source:** _medium.com_

#### Q4: What is the use of ViewModel in MVC? ⭐⭐
**Answer:**
ViewModel is a plain class with properties, which is used to bind it to strongly typed view. ViewModel can have the validation rules defined for its properties using data annotations.

**Source:** _medium.com_

#### Q5: What you mean by Routing in MVC? ⭐⭐
**Answer:**
**Routing** is a pattern matching mechanism of incoming requests to the URL patterns which are registered in route table. Class — “UrlRoutingModule” is used for the same process.

**Source:** _medium.com_

#### Q6: What are Actions in MVC? ⭐⭐
**Answer:**
**Actions** are the methods in Controller class which is responsible for returning the view or json data. Action will mainly have return type — “ActionResult” and it will be invoked from method — “InvokeAction()” called by controller.

**Source:** _medium.com_

#### Q7: What are the advantages of MVC over ASP.NET? ⭐⭐
**Answer:**
* Provides a clean separation of concerns among UI (Presentation layer), model (Transfer objects/Domain Objects/Entities) and Business Logic (Controller).
* Easy to UNIT Test
* Improved reusability of model and views. We can have multiple views which can point to the same model and vice versa.
* Improved structuring of the code

**Source:** _medium.com_

#### Q8: What are Scaffold templates in MVC? ⭐⭐
**Answer:**
Scaffolding in ASP.NET MVC is used to generate the Controllers, Model and Views for create, read, update, and delete (CRUD) functionality in an application. The scaffolding will be knowing the naming conventions used for models and controllers and views.

**Source:** _medium.com_

#### Q9: Can you explain Model, Controller and View in MVC? ⭐⭐
**Answer:**
* **Model** — It’s a business entity and it is used to represent the application data.
* **Controller** — Request sent by the user always scatters through controller and it’s responsibility is to redirect to the specific view using View() method.
* **View** — It’s the presentation layer of MVC.

**Source:** _medium.com_

#### Q10: What is Razor Pages? ⭐⭐
**Answer:**
[Razor Pages](https://codingblast.com/asp-net-core-razor-pages/) is a new feature of ASP.NET Core that makes coding page-focused scenarios easier and more productive.

With Razor Pages, you have this one Razor file (_.cshtml_), and the code for a single page lives inside of that file, and that file also represents the URL structure of the app. Therefore, you got everything inside of one file, and it just works.

However, you can separate your code to the _code behind_ file with _.cshtml.cs_ extension. You would usually have your view model and handlers (like action methods in MVC) in that file and handle the logic there. Of course, you could also have your view model moved to separate place.

Since Razor Pages is part of the MVC stack, you can use anything that comes with MVC inside of our Razor Pages.

**Source:** _codingblast.com_

#### Q11: Explain Sections is MVC? ⭐⭐
**Answer:**
Section are the part of HTML which is to be rendered in layout page. In Layout page we will use the below syntax for rendering the HTML –

```html
@RenderSection(“TestSection”)
```

And in child pages we are defining these sections as shown below –

```html
@section TestSection{
     <h1>Test Content</h1>
}
```

**Source:** _medium.com_

#### Q12: What are Non Action methods in MVC? ⭐⭐
**Answer:**
In MVC all public methods have been treated as Actions. So if you are creating a method and if you do not want to use it as an action method then the method has to be decorated with "NonAction" attribute as shown below:

```csharp
[NonAction]
public void TestMethod()
{
   // Method logic
}
```

**Source:** _stackoverflow.com_

#### Q13: Can a view be shared across multiple controllers? If Yes, How we can do that? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q14: What is the difference between ViewBag and ViewData in MVC? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q15: What is the difference between ViewResult() and ActionResult() in ASP.NET MVC? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q16: What are HTML Helpers in MVC? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q17: Can you explain the page life cycle of MVC? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q18: What is Attribute Routing in MVC? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q19: What is PartialView in MVC? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q20: Can you explain RenderBody and RenderPage in MVC? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q21: Explain the methods used to render the views in MVC? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q22: Explain ASP.NET WebApi vs MVC? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q23: What are some of the advantages of using ASP.Net MVC vs Web Forms? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q24: What is the "HelperPage.IsAjax" Property? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q25: What is RouteConfig.cs in MVC 4? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q26: Why to use Html.Partial in MVC? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q27: What are Validation Annotations? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q28: Explain TempData in MVC? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q29: How route table has been created in ASP.NET MVC? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q30: Explain Dependency Resolution? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q31: What is Separation of Concerns in ASP.NET MVC? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q32: What are AJAX Helpers in MVC? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q33: What is Html.RenderPartial? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

## [[⬆]](#toc) <a name=ASP.NETWebAPI>ASP.NET Web API</a> Interview Questions
#### Q1: What is ASP.NET Web API? ⭐
**Answer:**
ASP.NET Web API is a framework that simplifies building HTTP services for broader range of clients (including browsers as well as mobile devices) on top of .NET Framework.

Using ASP.NET Web API, we can create non-SOAP based services like plain XML or JSON strings, etc. with many other advantages including:

*   Create resource-oriented services using the full features of HTTP
*   Exposing services to a variety of clients easily like browsers or mobile devices, etc.

**Source:** _codeproject.com_

#### Q2: Which status code used for all uncaught exceptions by default? ⭐⭐
**Answer:**
**500** – Internal Server Error

Consider:
```csharp
[Route("CheckId/{id}")]
[HttpGet]
public IHttpActionResult CheckId(int id)
{
    if(id > 100)
    {
        throw new ArgumentOutOfRangeException();
    }
    return Ok(id);
}
```
And the result:
<div class="text-center">
<img src="https://www.exceptionnotfound.net/content/images/2015/09/checkid_invalid.png" class="img-fluid" style="max-width: 500px"/>
</div>

**Source:** _docs.microsoft.com_

#### Q3: What are the Advantages of Using ASP.NET Web API? ⭐⭐
**Answer:**
Using ASP.NET Web API has a number of advantages, but core of the advantages are:

*   It works the HTTP way using standard HTTP verbs like `GET`, `POST`, `PUT`, `DELETE`, etc. for all CRUD operations
*   Complete support for routing
*   Response generated in JSON or XML format using `MediaTypeFormatter`
*   It has the ability to be hosted in IIS as well as self-host outside of IIS
*   Supports Model binding and Validation
*   Support for OData

**Source:** _codeproject.com_

#### Q4: What New Features are Introduced in ASP.NET Web API 2.0? ⭐⭐
**Answer:**
More new features introduced in ASP.NET Web API framework v2.0 are as follows:

*   Attribute Routing
*   External Authentication
*   CORS (Cross-Origin Resource Sharing)
*   OWIN (Open Web Interface for .NET) Self Hosting
*   `IHttpActionResult`
*   Web API OData

**Source:** _codeproject.com_

#### Q5: What exactly is OAuth (Open Authorization)? ⭐⭐
**Answer:**
**OAuth** (Open Authorization) is an open standard for access granting/deligation protocol. It used as a way for Internet users to grant websites or applications access to their information on other websites but without giving them the passwords. It does not deal with authentication.

Basically there are three parties involved: oAuth Provider, oAuth Client and Owner.

* oAuth Client (Application Which wants to access your credential)
* oAuth Provider (eg. facebook, twitter...)
* Owner (the person with facebook,twitter.. account )

**Source:** _stackoverflow.com_

#### Q6: Explain the usage of HttpResponseMessage? ⭐⭐
**Answer:**
`HttpResponseMessage` works with HTTP protocol to return the data with status/error. 

**Source:** _c-sharpcorner.com_

#### Q7: What is the difference between ApiController and Controller? ⭐⭐
**Answer:**
* Use **Controller** to render your normal views. 
* **ApiController** action only return data that is serialized and sent to the client.

Consider:
```csharp
public class TweetsController : Controller {
  // GET: /Tweets/
  [HttpGet]
  public ActionResult Index() {
    return Json(Twitter.GetTweets(), JsonRequestBehavior.AllowGet);
  }
}
```
or
```csharp
public class TweetsController : ApiController {
  // GET: /Api/Tweets/
  public List<Tweet> Get() {
    return Twitter.GetTweets();
  }
}
```

**Source:** _stackoverflow.com_

#### Q8: What are main return types supported in Web API? ⭐⭐
**Answer:**
A Web API controller action can return following values:

*   Void – It will return empty content
*   HttpResponseMessage – It will convert the response to an HTTP message.
*   IHttpActionResult – internally calls ExecuteAsync to create an HttpResponseMessage
*   Other types – You can write the serialized return value into the response body

**Source:** _career.guru99.com_

#### Q9: What are the differences between WebAPI and WebAPI 2? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q10: How to Restrict Access to Web API Method to Specific HTTP Verb? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q11: What is Attribute Routing in ASP.NET Web API 2.0? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q12: Name types of Action Results in Web API 2 ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q13: Compare WCF vs ASP.NET Web API? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q14: Explain the difference between WCF RESTful Service vs ASP.NET Web API? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q15: Is it True that ASP.NET Web API has Replaced WCF? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q16: What's the difference between REST & RESTful? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q17: Explain the difference between MVC vs ASP.NET Web API ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q18: Why are the "FromBody" and "FromUri" attributes needed in ASP.NET Web API`? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q19: What is ASP.NET Web API OData? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q20: Explain briefly CORS(Cross-Origin Resource Sharing)? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q21: Can we use Web API with ASP.NET Web Form? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q22: How Can We Provide an Alias Name for ASP.NET Web API Action? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q23: What is Delegating Handler? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q24: How to register exception filter globally? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q25: What's the difference between OpenID and OAuth? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q26: How to Return View from ASP.NET Web API Method? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q27: Explain advantages/disadvantages of using HttpModule vs DelegatingHandler? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q28: Could you clarify what is the best practice with Web API error management? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q29: What is difference between OData and REST web services? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q30: Explain briefly OWIN (Open Web Interface for .NET) Self Hosting? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q31: Explain the difference between WCF, Web API, WCF REST and Web Service? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q32: Why should I use IHttpActionResult instead of HttpResponseMessage? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q33: What is difference between WCF and Web API and WCF REST and Web Service? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

## [[⬆]](#toc) <a name=AWS>AWS</a> Interview Questions
#### Q1: What is AWS? ⭐
**Answer:**
**AWS** stands for Amazon Web Services and is a platform that provides database storage, secure cloud services, offering to compute power, content delivery, and many other services to develop business levels.

**Source:** _onlineinterviewquestions.com_

#### Q2: Explain the key components of AWS? ⭐
**Answer:**
* **Simple Storage Service (S3)**: S3 is most widely used AWS storage web service.
* **Simple E-mail Service (SES)**: SES is a hosted transactional email service and allows one to fluently send deliverable emails using a RESTFUL API call or through a regular SMTP.
* **Identity and Access Management (IAM)**: IAM provides improved identity and security management for AWS account.
* **Elastic Compute Cloud (EC2)**: EC2 is an AWS ecosystem central piece. It is responsible for providing on-demand and flexible computing resources with a “pay as you go” pricing model.
* **Elastic Block Store (EBS)**: EBS offers continuous storage solution that can be seen in instances as a regular hard drive.
* **CloudWatch**: CloudWatch allows the controller to outlook and gather key metrics and also set a series of alarms to be notified if there is any trouble.

**Source:** _whizlabs.com_

#### Q3: What is buckets in AWS? ⭐
**Answer:**
An Amazon S3 bucket is a public cloud storage resource available in Amazon Web Services' (AWS) Simple Storage Service (S3), an object storage offering. Amazon S3 buckets, which are similar to file folders, store objects, which consist of data and its descriptive metadata.

By default, you can create up to 100 buckets in each of your AWS accounts. If you need more buckets, you can increase your bucket limit by submitting a service limit increase.

**Source:** _whizlabs.com_

#### Q4: What is AWS Cloudfront? ⭐⭐
**Answer:**
Amazon **CloudFront** is a content delivery network (CDN) offered by Amazon Web Services. Content delivery networks provide a globally-distributed network of proxy servers which cache content, such as web videos or other bulky media, more locally to consumers, thus improving access speed for downloading the content.

**Source:** _en.wikipedia.org_

#### Q5: What do you mean by AMI? What does it include? ⭐⭐
**Answer:**
**AMI** stands for the term **Amazon Machine Image**.  It’s an AWS template which provides the information (an application server, and operating system, and applications) required to perform the launch of an instance. This AMI is the copy of the AMI that is running in the cloud as a virtual server.  You can launch instances from as many different AMIs as you need. AMI consists of the followings:

* A root volume template for an existing instance
* Launch permissions to determine which AWS accounts will get the AMI in order to launch the instances
* Mapping for block device to calculate the total volume that will be attached to the instance at the time of launch

**Source:** _whizlabs.com_

#### Q6: How can I download a file from EC2? ⭐⭐
**Answer:**
Use scp:

```sh
scp -i ec2key.pem username@ec2ip:/path/to/file .
```

**Source:** _stackoverflow.com_

#### Q7: Is it possible to clone a EC2 instance data? ⭐⭐
**Answer:**
You can make an AMI of an existing instance, and then launch other instances using that AMI.

**Source:** _stackoverflow.com_

#### Q8: What is AWS Data Pipeline? ⭐⭐
**Answer:**
**AWS Data Pipeline** is a web service that you can use to automate the movement and transformation of data. With AWS Data Pipeline, you can define data-driven workflows, so that tasks can be dependent on the successful completion of previous tasks.

**Source:** _docs.aws.amazon.com_

#### Q9: Explain the features of Amazon EC2 services ⭐⭐
**Answer:**
Amazon EC2 services have following features:

* Virtual Computing Environments
* Proffers Persistent storage volumes
* Firewall validating you to specify the protocol
* Pre-configured templates
* Static IP address for dynamic Cloud Computing

**Source:** _whizlabs.com_

#### Q10: What is the connection between AMI and Instance? ⭐⭐
**Answer:**
Many different types of *instances* can be launched from one *AMI*. The type of an instance generally regulates the hardware components of the host computer that is used for the instance. Each type of instance has distinct computing and memory efficacy.

Once an instance is launched, it casts as host and the user interaction with it is same as with any other computer but we have a completely controlled access to our instances. AWS developer interview questions may contain one or more AMI based questions, so prepare yourself for the AMI topic very well.

**Source:** _whizlabs.com_

#### Q11: Are S3 buckets region specific? ⭐⭐
**Answer:**
Yes, buckets exist in a specific region and you need to specify that region when you create a bucket. Amazon S3 creates bucket in a region you specify. You can choose any AWS region that is geographically close to you to optimize latency, minimize costs, or address regulatory requirements.

**Source:** _stackoverflow.com_

#### Q12: What is AWS Direct Connect? ⭐⭐
**Answer:**
**AWS Direct Connect** bypasses the public Internet and establishes a secure, dedicated connection from your infrastructure into AWS. With established connectivity via AWS Direct Connect, you can access your Amazon VPC and all AWS services.

**Source:** _coresite.com_

#### Q13: What is AWS EBS? ⭐⭐
**Answer:**
**Amazon Elastic Block Store** (Amazon EBS) provides persistent block storage volumes for use with Amazon EC2 instances in the AWS Cloud. Each Amazon EBS volume is automatically replicated within its Availability Zone to protect you from component failure, offering high availability and durability.

**Source:** _aws.amazon.com_

#### Q14: What is AWS Lambda? ⭐⭐
**Answer:**
**AWS Lambda** is a serverless compute service that runs your code in response to events and automatically manages the underlying compute resources for you. You can use AWS Lambda to extend other AWS services with custom logic, or create your own back-end services that operate at AWS scale, performance, and security.

**Source:** _aws.amazon.com_

#### Q15: What is AWS DynamoDB? ⭐⭐
**Answer:**
**Amazon DynamoDB** is a fully managed NoSQL database service that provides fast and predictable performance with seamless scalability. With DynamoDB, you can create database tables that can store and retrieve any amount of data, and serve any level of request traffic.

**Source:** _docs.aws.amazon.com_

#### Q16: What is AWS EMR? ⭐⭐
**Answer:**
**Amazon Elastic MapReduce (EMR)** is an Amazon Web Services (AWS) tool for big data processing and analysis. Amazon EMR offers the expandable low-configuration service as an easier alternative to running in-house cluster computing.

Amazon EMR is based on Apache Hadoop, a Java-based programming framework that supports the processing of large data sets in a distributed computing environment. MapReduce is a software framework that allows developers to write programs that process massive amounts of unstructured data in parallel across a distributed cluster of processors or stand-alone computers.

**Source:** _searchaws.techtarget.com_

#### Q17: Is data stored in S3 is always encrypted? ⭐⭐
**Answer:**
By default data on S3 is not encrypted, but all you could enable server-side encryption in your object metadata when you upload your data to Amazon S3. As soon as your data reaches S3, it is encrypted and stored.

**Source:** _aws.amazon.com_

#### Q18: Can we attach single EBS to multiple EC2s same time? ⭐⭐
**Answer:**
No. After you create a volume, you can attach it to any EC2 instance in the same Availability Zone. An EBS volume can be attached to **only one EC2 instance at a time**, but multiple volumes can be attached to a single instance.

**Source:** _docs.aws.amazon.com_

#### Q19: What is AWS API gateway? ⭐⭐
**Answer:**
Amazon **API Gateway** is an AWS service that enables developers to create, publish, maintain, monitor, and secure APIs at any scale. You can create APIs that access AWS or other web services, as well as data stored in the AWS Cloud.

**Source:** _aws.amazon.com_

#### Q20: What is AWS Direct Connect? ⭐⭐
**Answer:**
Using **AWS Direct Connect**, you can establish private connectivity between AWS and your datacenter, office, or colocation environment, which in many cases can reduce your network costs, increase bandwidth throughput, and provide a more consistent network experience than Internet-based connections.

**Source:** _aws.amazon.com_

#### Q21: What are the security best practices for Amazon EC2 instances? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q22: Can I automatically start and terminate my Amazon instance using Amazon API?  ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q23: Can we still continue working on EBS while creating snapshot of it? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q24: What is AWS Auto Scaling? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q25: What is AWS Auto Scaling group? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q26: What is the maximum size of a single S3 object? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q27: What is AWS bucket policy? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q28: Does AWS has the option for vertical "auto" scaling of EC2 instance? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q29: What is AWS WAF? What are the potential benefits of using WAF? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q30: How to get the instance id from within an EC2 instance? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q31: What is AWS Cloudwatch? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q32: What is the difference between Amazon EC2 and AWS Elastic Beanstalk? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q33: How many storage options are there for EC2 Instance? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q34: What is AWS Route 53? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q35: How would you implement vertical auto scaling of EC2 instance? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q36: What is Amazon Kinesis? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q37: How to find a region from within an EC2 instance? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q38: Where are EC2 snapshots stored? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q39: When should one use the following: Amazon EC2, Google App Engine, Microsoft Azure and Salesforce.com? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q40: When to use Amazon CloudFront and when S3? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q41: Our EC2 micro instance occasionally runs out of memory. Other than using a larger instance size, what else can be done? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q42: What is difference between Lightsail and EC2? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q43: What is the underlying hypervisor for EC2? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q44: How to safely upgrade an Amazon EC2 instance from t1.micro to large? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

## [[⬆]](#toc) <a name=Agile&Scrum>Agile & Scrum</a> Interview Questions
#### Q1: What is ASP.NET MVC? ⭐
**Answer:**
ASP.NET MVC is a web application Framework. It is light weight and highly testable Framework. MVC separates application into three components — Model, View and Controller.

**Source:** _medium.com_

#### Q2: What is Scrum? ⭐
**Answer:**
**Scrum** is one of the most popular frameworks for implementing *Agile*. Many people think scrum and agile are the same thing but they're not.

With scrum, the product is built in a series of fixed-length iterations called sprints that give teams a framework for shipping software on a regular cadence.

**Source:** _atlassian.com_

#### Q3: What is sprint in Scrum? ⭐
**Answer:**
In the Scrum methodology a **sprint** is the basic unit of development. Scrum sprints correspond to Agile iterations. 

Each sprint starts with 
* a **planning meeting**, where the tasks for the sprint are identified and an estimated commitment for the **sprint goal** is made. 

A Sprint ends with 
* a **review or retrospective meeting** where the progress is reviewed and lessons for the next sprint are identified. During each sprint, the team creates finished portions of a product.

**Source:** _stackoverflow.com_

#### Q4: Name roles in Scrum ⭐
**Answer:**
Three essential roles for scrum success are:
* **The Product Owner** are the champions for their product. They are focused on understanding business and market requirements, then prioritizing the work to be done by the engineering team accordingly.
* ** The Scrum Master** are the champion for scrum within their team. They coach the team, the product owner, and the business on the scrum process and look for ways to fine-tune their practice of it.
* **The Scrum Team** are the champions for sustainable development practices. Scrum teams are cross-functional, "the development team" includes testers, designers, and ops engineers in addition to developers. 

**Source:** _atlassian.com_

#### Q5: What is User Stories? ⭐
**Answer:**
**User stories** are features customers might want to see in their software. They are written on index cards to encourage face-to-face communication. Typically no more than a couple days work, they form the basis of our Agile plans.

#### Q6: What is an epic, user stories and task? ⭐
**Answer:**
**Epic:** A customer described software feature that is itemized in the product backlog is known as epic. Epics are sub-divided into stories.

**User Stories:** From the client perspective user stories are prepared which defines project or business functions, and it is delivered in a particular sprint as expected.

**Task:** Further down user stories are broken down into different task

**Source:** _career.guru99.com_

#### Q7: Explain what is Refactoring? ⭐
**Answer:**
To improve the performance, the existing code is modified; this is re-factoring. During re-factoring the code functionality remains same.

**Source:** _career.guru99.com_

#### Q8: What is an Agile iteration? ⭐
**Answer:**
An Agile **iteration** is a short one to two week period where a team takes most important user stories,  builds them completely and deliver as running-tested-software to the customer. Analysis, design, coding, testing happen during an iteration.

#### Q9: Name some types of meetings or ceremonies in Scrum ⭐⭐
**Answer:**
Scrum calls for four ceremonies that bring structure to each sprint:

* **Sprint planning**: A team planning meeting that determines what to complete in the coming sprint.
* **Daily stand-up**: Also known as a daily scrum, a 15-minute mini-meeting for the software team to sync.
* **Sprint demo**: A sharing meeting where the team shows what they've shipped in that sprint.
* **Sprint retrospective**: A review of what did and didn't go well with actions to make the next sprint better.


**Source:** _atlassian.com_

#### Q10: If a timebox plan needs to be reprioritized who should re-prioritise it? ⭐⭐
**Answer:**
If a timebox plan needs to be reprioritized it should include whole team, product owner, and developers.

**Source:** _career.guru99.com_

#### Q11: Mention the key difference between sprint backlog and product backlog? ⭐⭐
**Answer:**
* **Product backlog**: It contains a list of all desired features and is owned by the product owner

* **Sprint backlog**: It is a subset of the product backlog owned by development team and commits to deliver it in a sprint. It is created in Sprint Planning Meeting

**Source:** _career.guru99.com_

#### Q12: What is Agile? ⭐⭐
**Answer:**
**Agile** is a time boxed, **iterative approach (framework) to software delivery** that builds software incrementally from the start of the project, instead of trying to deliver it all at once near the end.

It works by breaking projects down into little bits of user functionality called **user stories**, prioritizing them, and then continuously delivering them in short two week cycles called **iterations**.

Agile refers to any process that aligns with the concepts of the [Agile Manifesto](http://agilemanifesto.org/). 

**Source:** _agilemanifesto.org_

#### Q13: Explain in Agile, burn-up and burn-down chart? ⭐⭐
**Answer:**
To track the project progress burnup and burn down, charts are used

* Burnup Chart: It shows the progress of stories done over time
* Burndown Chart: It shows how much work was left to do overtime

**Source:** _career.guru99.com_

#### Q14: What is Sprint Planning? ⭐⭐
**Answer:**
The work to be performed in the Sprint is planned at the **Sprint Planning**. This plan is created by the collaborative work of the entire Scrum Team.

Sprint Planning answers the following:

* What can be delivered in the Increment resulting from the upcoming Sprint?
* How will the work needed to deliver the Increment be achieved?

The Sprint Goal is an objective set for the Sprint that can be met through the implementation of Product Backlog. 

**Source:** _scrum.org_

#### Q15: Explain difference between a Product and a Sprint Backlog ⭐⭐
**Answer:**
* The **Product Backlog** is an ordered list of everything that is known to be needed in the product. It is the single source of requirements for any changes to be made to the product.

* The **Sprint Backlog** is the set of Product Backlog items selected for the Sprint during the Sprint Planning, plus a plan for delivering the product Increment and realizing the Sprint Goal. 

**Source:** _scrum.org_

#### Q16: What is story points/efforts/ scales? ⭐⭐
**Answer:**
It is used to discuss the difficulty of the story without assigning actual hours. The most common scale used is a Fibonacci sequence (1, 2, 3, 5, 8,1 3,….100) although some teams use linear scale (1, 2, 3, 4….), Powers of 2 (1, 2, 4, 8……) and cloth size (XS, S ,M, L, XL)

**Source:** _career.guru99.com_

#### Q17: How is Agile different from other software delivery aproaches? ⭐⭐
**Answer:**
* Analysis, design, coding, and testing are continuous activities
* Development is iterative
* Planning is adaptive
* Roles blur
* Scope can vary
* Requirements can change
* Working software is the primary measure of success



#### Q18: Have you ever used Scrum Task Board? ⭐⭐
**Answer:**
In Scrum the *task board* is a visual display of the progress of the Scrum team during a sprint. It presents a snapshot of the current sprint backlog allowing everyone to see which tasks remain to be started, which are in progress and which are done.

Consider the following layout of the task board:
- Stories
- To Do
- In Progress
- Testing
- Done

**Source:** _manifesto.co.uk_

#### Q19: Explain what does it mean by product roadmap? ⭐⭐
**Answer:**
A **product roadmap** is referred for the holistic view of product features that create the product vision.

**Source:** _career.guru99.com_

#### Q20: Explain what is Velocity in Agile? ⭐⭐
**Answer:**
**Velocity** is a metric that is calculated by addition of all efforts estimates related with user stories completed in an iteration. It figures out how much work Agile can complete in a sprint and how much time will it need to finish a project.

**Source:** _career.guru99.com_

#### Q21: Mention what should a burndown chart should highlight? ⭐⭐
**Answer:**
The burn-down chart shows the remaining work to complete before the timebox (iteration) ends.

**Source:** _career.guru99.com_

#### Q22: What is test driven development? ⭐⭐
**Answer:**
**Test driven development (TDD)** is also known as test-driven design. In this method, developer first writes an automated test case which describes new function or improvement and then creates small codes to pass that test, and later re-factors the new code to meet the acceptable standards.

**Source:** _career.guru99.com_

#### Q23: Explain what is Scrum ban? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q24: What does project velocity mean? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q25: Can you explain the purpose of a burndown chart? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q26: What is the Agile Manifesto? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q27: What does the Scrum Framework consist from? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q28: What are four Agile Manifesto values? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q29: Explain the difference between Extreme programming and Scrum? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q30: What are some methodologies used to implement Agile? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q31: Mention what are the challenges involved in Agile software development? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q32: What are the qualities of a good Agile tester should have? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q33: What is a Sprint Review? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q34: What is Acceptance Criteria? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q35: Mention what are the advantages of maintaining consistent iteration length throughout the project? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q36: Mention in detail what are the role’s of Scrum Master? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q37: Mention what is the difference between Scrum and Agile? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q38: Mention what are the Agile quality strategies? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q39: Why Continuous Integration is important for Agile? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q40: What is a Sprint Retrospective? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q41: What are the Scrum values? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q42: What the Scrum theory is based on? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q43: When not to use Agile? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q44: In Agile mention what is the difference between the Incremental and Iterative development? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q45: Explain how you can measure the velocity of the sprint with varying team capacity? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q46: What is Scrum Increment? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q47: Explain main differences between Scrum and Agile? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q48: Name the 12 Agile Principles ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q49: What are the benefits of Burn Up chart? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q50: What is the Scrum's definition of "Done"? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q51: Provide some examples of burn-up chart ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q52: Explain what is Spike and Zero sprint in Agile? What is the purpose of it? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

## [[⬆]](#toc) <a name=Android>Android</a> Interview Questions
#### Q1: Mention the difference between RelativeLayout and LinearLayout? ⭐
**Answer:**
* **Linear Layout** — Arranges elements either vertically or horizontally. i.e. in a row or column.
* **Relative Layout** — Arranges elements relative to parent or other elements.

**Source:** _android.jlelse.eu_

#### Q2: What is the difference between Bitmap and Drawable in Android? ⭐
**Answer:**
* A **Bitmap** is a representation of a bitmap image (something like java.awt.Image).
* A **Drawable** is an abstraction of "something that can be drawn". It could be a Bitmap (wrapped up as a BitmapDrawable), but it could also be a solid color, a collection of other Drawable objects, or any number of other structures.

**Source:** _stackoverflow.com_

#### Q3: What is a difference between Spannable and String? ⭐
**Answer:**
A **Spannable** allows to attach formatting information like bold, italic, ... to sub-sequences ("spans", thus the name) of the characters. It can be used whenever you want to represent "rich text".

**Source:** _stackoverflow.com_

#### Q4: What is an Activity? ⭐
**Answer:**
An **activity** provides the window in which the app draws its UI. This window typically fills the screen, but may be smaller than the screen and float on top of other windows. Generally, one activity implements one screen in an app. For instance, one of an app’s activities may implement a Preferences screen, while another activity implements a Select Photo screen.

**Source:** _github.com_

#### Q5: What is Armv7? ⭐⭐
**Answer:**
There are 3 CPU architectures in Android:

* **_ARMv7_**  is the most common as it is optimised for battery consumption.
*  **_ARM64_**  is an evolved version of that that supports 64-bit processing for more powerful computing.
*  **_ARMx86_**, is the least used for these three, since it is not battery friendly. It is more powerful than the other two.

**Source:** _android.jlelse.eu_

#### Q6: Explain activity lifecycle ⭐⭐
**Answer:**
As a user navigates through, out of, and back to your app, the Activity instances in your app transition through different states in their lifecycle.

To navigate transitions between stages of the activity lifecycle, the Activity class provides a core set of six callbacks: `onCreate()`, `onStart()`, `onResume()`, `onPause()`, `onStop()`, and `onDestroy()`. The system invokes each of these callbacks as an activity enters a new state. 

<div class="text-center"/>
<img src="https://developer.android.com/guide/components/images/activity_lifecycle.png" class="img-fluid" />
</div>


**Source:** _developer.android.com_

#### Q7: How can I get the context in a fragment? ⭐⭐
**Answer:**
You can use `getActivity()`, which returns the activity associated with a fragment. The activity is a context (since Activity extends `Context`).

You can also override the `onAttach` method of fragment:

```java
public static class DummySectionFragment extends Fragment{
...
    @Override
    public void onAttach(Activity activity) {
        super.onAttach(activity);
        DBHelper = new DatabaseHelper(activity);
    }
}
```

**Source:** _stackoverflow.com_

#### Q8: What is View Group? How are they different from Views? ⭐⭐
**Answer:**
**View:** View objects are the basic building blocks of User Interface(UI) elements in Android. View is a simple rectangle box which responds to the user’s actions. Examples are EditText, Button, CheckBox etc. View refers to the `android.view.View` class, which is the base class of all UI classes.

**ViewGroup:** ViewGroup is the invisible container. It holds View and ViewGroup. For example, LinearLayout is the ViewGroup that contains Button(View), and other Layouts also. ViewGroup is the base class for Layouts.

**Source:** _android.jlelse.eu_

#### Q9: Is it possible to implement the model–view–controller pattern in Java for Android? ⭐⭐
**Answer:**
In Android you **don't have MVC**, but you have the following:

* You define your user interface in  various XML files by resolution, hardware, etc.
* You define your resources in various XML files by locale, etc.
* You extend clases like ListActivity, TabActivity and make use of the XML file by inflaters.
* You can create as many classes as you wish for your business logic.
* A lot of Utils have been already written for you - DatabaseUtils, Html.

**Source:** _stackoverflow.com_

#### Q10: What’s the difference between onCreate() and onStart()? ⭐⭐
**Answer:**
*   The `onCreate()` method is called once during the Activity lifecycle, either when the application starts, or when the Activity has been destroyed and then recreated, for example during a configuration change.
*   The `onStart()` method is called whenever the Activity becomes visible to the user, typically after `onCreate()` or `onRestart()`.

**Source:** _android.jlelse.eu_

#### Q11: Explain the build process in Android ⭐⭐
**Answer:**
1.  First step involves compiling the resources folder (/res) using the aapt (android asset packaging tool) tool. These are compiled to a single class file called R.java. This is a class that just contains constants.
2.  Second step involves the java source code being compiled to .class files by javac, and then the class files are converted to Dalvik bytecode by the “dx” tool, which is included in the sdk ‘tools’. The output is classes.dex.
3.  The final step involves the android apkbuilder which takes all the input and builds the apk (android packaging key) file.

**Source:** _android.jlelse.eu_

#### Q12: What is an Intent in Android? ⭐⭐
**Answer:**
An Intent is basically a message that is passed between components (such as Activities, Services, Broadcast Receivers, and Content Providers).So, it is almost equivalent to parameters passed to API calls. The fundamental differences between API calls and invoking components via intents are:

* API calls are synchronous while intent-based invocations are asynchronous.
* API calls are compile-time binding while intent-based calls are run-time binding.

To listen for an broadcast intent (like the phone ringing, or an SMS is received), you implement a **broadcast receiver**, which will be passed the intent. To declare that you can handle another's app intent like "take picture", you declare an intent filter in your app's manifest file.

If you want to fire off an intent to do something, like pop up the dialer, you fire off an intent saying you will.

An Intent provides a facility for performing late runtime binding between the code in different applications. 

**Source:** _stackoverflow.com_

#### Q13: What is the most appropriate way to store user settings in Android application? ⭐⭐
**Answer:**
In general **SharedPreferences** are your best bet for storing preferences, so in general I'd recommend that approach for saving application and user settings.

The only area of concern here is what you're saving. Passwords are always a tricky thing to store, and I'd be particularly wary of storing them as clear text. The Android architecture is such that your application's SharedPreferences are sandboxed to prevent other applications from being able to access the values so there's some security there, but physical access to a phone could potentially allow access to the values.

**Source:** _stackoverflow.com_

#### Q14: In what situation should one use RecyclerView over ListView? ⭐⭐
**Answer:**
**RecyclerView** was created as a **ListView** improvement, so yes, you can create an attached list with **ListView** control, but using **RecyclerView** is easier as it:

* Reuses cells while scrolling up/down - this is possible with implementing View Holder in the ListView adapter, but it was an optional thing, while in the RecycleView it's the default way of writing adapter.
* Decouples list from its container - so you can put list items easily at run time in the different containers (linearLayout, gridLayout) with setting LayoutManager.

To conclude, **RecyclerView** is a more flexible control for handling "list data" that follows patterns of delegation of concerns and leaves for itself only one task - recycling items.

**Source:** _stackoverflow.com_

#### Q15: Explain briefly all the Android application components ⭐⭐
**Answer:**
**App components** are the essential building blocks of an Android app. Each component is an entry point through which the system or a user can enter your app.

There are four different types of app components:

* **Activities** - An activity is the entry point for interacting with the user. It represents a single screen with a user interface.
* **Services** - A service is a general-purpose entry point for keeping an app running in the background for all kinds of reasons. It is a component that runs in the background to perform long-running operations or to perform work for remote processes.
* **Broadcast receivers** - A broadcast receiver is a component that enables the system to deliver events to the app outside of a regular user flow, allowing the app to respond to system-wide broadcast announcements.
* **Content providers** - A content provider manages a shared set of app data that you can store in the file system, in a SQLite database, on the web, or on any other persistent storage location that your app can access.

**Source:** _developer.android.com_

#### Q16: What is 'Context' on Android? ⭐⭐
**Answer:**
The documentation itself provides a rather straightforward explanation: The Context class is an “Interface to global information about an application environment".

We may assume a **Context** is a handle to the system; it provides services like resolving resources, obtaining access to databases and preferences, and so on. An Android app has activities. Context is like a handle to the environment your application is currently running in. The activity object inherits the Context object.

**Source:** _stackoverflow.com_

#### Q17: What is the Dalvik Virtual Machine? ⭐⭐
**Answer:**
The **Dalvik Virtual Machine (DVM)** is an android virtual machine optimized for mobile devices. It optimizes the virtual machine for memory, battery life and performance.

The Dex compiler converts the class files into the `.dex` file that run on the Dalvik VM. Multiple class files are converted into one dex file.

**Source:** _www.javatpoint.com_

#### Q18: Tell about Constraint Layout ⭐⭐
**Answer:**
**ConstraintLayout** allows you to create large and complex layouts with a flat view hierarchy (no nested view groups). It's similar to **RelativeLayout** in that all views are laid out according to relationships between sibling views and the parent layout, but it's more flexible than RelativeLayout and easier to use with Android Studio's Layout Editor.

Intention of ConstraintLayout is to optimize and flatten the view hierarchy of your layouts by applying some rules to each view to avoid nesting.

**Source:** _developer.android.com_

#### Q19: What is ADB and what is it used for? ⭐⭐
**Answer:**
**ADB** is the acronym for Android Debug Bridge, which is part of the Android SDK (Software Development Kit). It uses a client-server-model (i.e. adbd, the ADB daemon, is running on the device and can be connected to), and in most cases is used via an USB connection. It is also possible to use it via WiFi (wireless adb).

There's nothing you need to install on your Android device, as the ADB daemon (adbd) is already integrated into the Android OS. It is usually accessed via a command line interface from the PC, where either the full Android SDK is installed (several 30 MB download archive currently), or a massively stripped-down version for "non-developers", sometimes referred to as "Mini ADB" or "ADB essentials" (for Linux, this is only the adb executable; for Windows it's adb.exe plus two or three .dll files).

**Source:** _developer.android.com_

#### Q20: What is Dalvik? ⭐⭐
**Answer:**
**Dalvik** is a Just In Time (JIT) compiler. By the term JIT, we mean to say that whenever you run your app in your mobile device then that part of your code that is needed for execution of your app will only be compiled at that moment and rest of the code will be compiled in the future when needed. The JIT or Just In Time compiles only a part of your code and it has a smaller memory footprint and due to this, it uses very less physical space on your device.

**Source:** _blog.mindorks.com_

#### Q21: What types of Context do you know? ⭐⭐
**Answer:**
The are mainly two types of context:

* **Application Context**: It is an instance that is the singleton and can be accessed in activity via `getApplicationContext()`. This context is tied to the lifecycle of an application. The application context can be used where you need a context whose lifecycle is separate from the current context or when you are passing a context beyond the scope of activity.

* **Activity Contex**t: This context is tied to the lifecycle of an activity. The activity context should be used when you are passing the context in the scope of an activity or you need the context whose lifecycle is attached to the current context.

**Source:** _blog.mindorks.com_

#### Q22: How do I pass data between Activities in Android application? ⭐⭐
**Details:**
I have a scenario where, after logging in through a login page, there will be a sign-out button on each activity. Can you guide me on how to keep session id available to all activities?

**Answer:**
The easiest way to do this would be to pass the session id to the signout activity in the **Intent** you're using to start the activity:

```java
Intent intent = new Intent(getBaseContext(), SignoutActivity.class);
intent.putExtra("EXTRA_SESSION_ID", sessionId);
startActivity(intent);
```
Access that intent on next activity:
```java
String sessionId = getIntent().getStringExtra("EXTRA_SESSION_ID");
```

**Source:** _stackoverflow.com_

#### Q23: How does the OutOfMemory happens? ⭐⭐
**Answer:**
**Out of memory** error is very common error when you are developing for a application that deals with multiple images sets or large bitmaps or some Animation stuff. In Android, every application runs in a Linux Process. Each Linux Process has a Virtual Machine (Dalvik Virtual Machine) running inside it. There is a limit on the memory a process can demand and it is different for different devices and also differs for phones and tablets. When some process demands a higher memory than its limit it causes a error i.e **Out of memory** error.

There are number of reasons why we get a Out of memory errors. Some of those are:

1. You are doing some operation that continuously demands a lot of memory and at some point it goes beyond the max heap memory limit of a process.

2. You are leaking some memory i.e you didn’t make the previous objects you allocated eligible for Garbage Collection (GC). This is called Memory leak.

3. You are dealing with large bitmaps and loading all of them at run time. You have to deal very carefully with large bitmaps by loading the size that you need not the whole bitmap at once and then do scaling.

**Source:** _blogs.innovationm.com_

#### Q24: What is a ContentProvider and what is it typically used for? ⭐⭐
**Answer:**
A **content provider** manages access to a central repository of data. A provider is part of an Android application, which often provides its own UI for working with the data. However, content providers are primarily intended to be used by other applications, which access the provider using a provider client object.

Typically you work with content providers in one of two scenarios; 
* you may want to implement code to access an existing content provider in another application, or 
* you may want to create a new content provider in your application to share data with other applications.

**Source:** _developer.android.com_

#### Q25: What is an AsyncTask? ⭐⭐
**Answer:**
`AsyncTask` is one of the easiest ways to implement parallelism in Android without having to deal with more complex methods like Threads. Though it offers a basic level of parallelism with the UI thread, it should not be used for longer operations (of, say, not more than 2 seconds). 

AsyncTask has four methods 

- `onPreExecute()` 
- `doInBackground()`
- `onProgressUpdate()`
- `onPostExecute()`

where `doInBackground()` is the most important as it is where background computations are performed.

**Source:** _stackoverflow.com_

#### Q26: Why is it recommended to use only the default constructor to create a Fragment? ⭐⭐
**Answer:**
In short, Fragments need to have a no-args constructor for the Android system to instantiate them. Your Fragment subclasses need a public empty constructor as this is what's being called by the framework.

It is used in the case when device has to restore the state of a fragment. No data will be passed and a default fragment will be created and then the state will be restored. Since the system has no way to know what you passed in your constructor or your `newInstance`, default constructor will be used and saved bundle should be passed via onCreate after the fragment is actually instantiated with the default constructor.

**Source:** _www.quora.com_

#### Q27: How to persist data in an Android app? ⭐⭐
**Answer:**
There are basically four different ways to store data in an Android app:

1. Shared Preferences - to save primitive data in key-value pairs
2. Internal Storage - you need to store data to the device filesystem, but you do not want any other app (even the user) to read this data
3. External Storage -  you might want the user to view the files and data saved by your app
4. SQLite database


**Source:** _www.androidauthority.com_

#### Q28: Explain Android notification system ⭐⭐
**Answer:**
A **notification** is a message that Android displays outside your app's UI to provide the user with reminders, communication from other people, or other timely information from your app. Users can tap the notification to open your app or take an action directly from the notification.

Notifications appear to users in different locations and formats, such as an icon in the status bar, a more detailed entry in the notification drawer, as a badge on the app's icon, and on paired wearables automatically. Beginning with Android 5.0, notifications can appear on the lock screen.

Starting in Android 8.0 (API level 26), all notifications must be assigned to a channel or it will not appear. By categorizing notifications into channels, users can disable specific notification channels for your app (instead of disabling all your notifications), and users can control the visual and auditory options for each channel—all from the Android system settings.

**Source:** _developer.android.com_

#### Q29: What is Handler and what is it used for? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q30: Explain key differences between Service and IntentService ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q31: What is Explicit Intent? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q32: How would you support different screen sizes? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q33: What is Implicit Intent? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q34: What is Intent Filter? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q35: What does LayoutInflater in Android do? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q36: Android Log.v(), Log.d(), Log.i(), Log.w(), Log.e(). When to use each one? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q37: What are the differences between onCreate(), onCreateView(), and onActivityCreated() in fragments and what would they each be used for? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q38: What is the difference between onCreate() and onCreateView() lifecycle methods in Fragment? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q39: How to declare global variables in Android? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q40: What is the actual differences between a activity context and application context? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q41: What are the permission protection levels in Android? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q42: What is the difference between Activity and Context? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q43: How would you preserve Activity state during a screen rotation? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q44: When to use Android's ArrayMap instead of a HashMap? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q45: What are the differences between ArrayList and ArrayMap? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q46: What are dex files are used for? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q47: What is an Android PendingIntent? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q48: Explain how HashMap works ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q49: What is the difference between compileSdkVersion and targetSdkVersion? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q50: What are Android Annotations and what are they used for? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q51: How could you pass data between activities without Intent? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q52: What is the difference between invisible and gone for the View visibility status? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q53: What is ART? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q54: What is Android Data Binding? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q55: What is RenderScript and when should we (really) use it? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q56: Why fragments, and when to use fragments instead of activities? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q57: What are retained fragments? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q58: What is the difference between Service & Intent Service? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q59: Describe Different Types of Services in Android ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q60: What is the support library? Why was it introduced? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q61: What is DDMS and what can you do with it? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q62: What is the best way to update the screen periodically? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q63: What is a JobScheduler? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q64: What is the ViewHolder pattern? Why should we use it? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q65: What is the difference between ListView and RecyclerView? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q66: What is a LocalBroadcastManager? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q67: What is the difference between AsyncTask and Thread/Runnable? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q68: What is the difference between a Bundle and an Intent? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q69: What is the difference between Adapter and Loader in Android? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q70: When to use Android Loaders? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q71: Isn't android's Bundle functionally equivalent with a Map? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q72: What is Parcelable in Android? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q73: When to use Fragments vs Activities? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q74: How would you communicate between two Fragments? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q75: What is the difference between Handler vs AsyncTask vs Thread? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q76: How can two distinct Android apps interact? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q77: Explain String vs StringBuilder vs SpannedString vs SpannableString vs SpannableStringBuilder vs CharSequence  ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q78: Is a Dalvik virtual machine instance created for each application? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q79: What is the Android NDK? How can one use it? Why should one use it? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q80: What is the StrictMode? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q81: When is it necessary, or better to use a SurfaceView instead of a View? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q82: Can you manually call the Garbage collector? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q83: What is the difference between Android timer and a Handler to do action every N seconds? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q84: What is Broadcast Receiver? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q85: How to avoid reverse engineering of an APK file? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q86: What are some differences between ART and Dalvik? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q87: What are Android Architecture Components? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q88: Why to consider FlatBuffers over JSON? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q89: What is the difference between ANR and crash in Android? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q90: How do you handle Bitmaps in Android as it takes too much memory? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q91: Explain how ArrayMap works ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q92: What is the difference between ArrayMap vs HashMap?  ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q93: Discuss Singletons vs. Application Context for app-global state ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q94: What is the difference between getContext() , getApplicationContext() , getBaseContext() , and "this"? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q95: What is Doze? What about App Standby? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q96: What is a ThreadPool? And is it more effective than using several separate Threads? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q97: How can I use AsyncTask in different Activities? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q98: What is AIDL? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q99: What are some best practices to avoid memory leaks on Android? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q100: When to use SparseArray vs HashMap? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q101: Provide some tips to reduce battery usage in an android application ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q102: What are some difference between Parcelable and Serializable? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q103: What are best practices for storing and protecting private API keys in applications? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q104: What is a Sticky Broadcast? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q105: What is the relationship between Looper, Handler and MessageQueue in Android? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q106: When would you use AIDL? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q107:  Explain reasons why not to use getApplicationContext()? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q108: When to use AIDL vs Messenger Queue? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q109: What is the difference between Local, Normal, Ordered and Sticky broadcasts? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q110: Explain when would you call getApplicationContext() and why? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q111: What is Intent vs Sticky Intent vs Pending Intent?  ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q112: What happens if the user navigates away or closes the app while I still have a reference to the Activity the user just closed in my AsyncTask? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q113: What is the onTrimMemory method? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

## [[⬆]](#toc) <a name=Angular>Angular</a> Interview Questions
#### Q1: What is Routing Guard in Angular? ⭐
**Answer:**
Angular’s route guards are interfaces which can tell the router whether or not it should allow navigation to a requested route. They make this decision by looking for a true or false return value from a class which implements the given guard interface.

**Source:** _medium.com_

#### Q2: What is a module, and what does it contain? ⭐
**Answer:**
An Angular module is set of Angular basic building blocks like component, directives, services etc. An app can have more than one module.

A module can be created using `@NgModule` decorator.

```js
@NgModule({
  imports:      [ BrowserModule ],
  declarations: [ AppComponent ],
  bootstrap:    [ AppComponent ]
})
export class AppModule { }
```

**Source:** _stackoverflow.com_

#### Q3: What are pipes? Give me an example. ⭐
**Answer:**
A **pipe** takes in data as input and transforms it to a desired output. You can chain pipes together in potentially useful combinations. You can write your own custom pipes. Angular comes with a stock of pipes such as `DatePipe`, `UpperCasePipe`, `LowerCasePipe`, `CurrencyPipe`, and `PercentPipe`.

Consider:
```html
<p>The hero's birthday is {{ birthday | date }}</p>
```
In this page, you'll use pipes to transform a component's birthday property into a human-friendly date.

**Source:** _angular.io_

#### Q4: What is the minimum definition of a component? ⭐⭐
**Answer:**
The absolute minimal configuration for a `@Component` in Angular is a template. Both template properties are set to optional because you have to define either `template` or `templateUrl`.

When you don't define them, you will get an exception like this:
```sh
No template specified for component 'ComponentName'
```
A selector property is not required, as you can also use your components in a route.

**Source:** _stackoverflow.com_

#### Q5: What's the difference between an Angular component and module? ⭐⭐
**Answer:**
*Components* control views (html). They also communicate with other components and services to bring functionality to your app.

*Modules* consist of one or more components. They do not control any html. Your modules declare which components can be used by components belonging to other modules, which classes will be injected by the dependency injector and which component gets bootstrapped. Modules allow you to manage your components to bring modularity to your app.

**Source:** _stackoverflow.com_

#### Q6: How would you run unit test? ⭐⭐
**Answer:**
The Angular CLI downloads and install everything you need to test an Angular application with the Jasmine test framework.

The project you create with the CLI is immediately ready to test. Just run this one CLI command:

```sh
ng test
```

**Source:** _angular.io_

#### Q7: What is a service, and when will you use it? ⭐⭐
**Answer:**
*Angular services* are singleton objects which get instantiated only once during the lifetime of an application. They contain methods that maintain data throughout the life of an application, i.e. data does not get refreshed and is available all the time. The main objective of a service is to organize and share business logic, models, or data and functions with different components of an Angular application.

The *separation of concerns* is the main reason why Angular services came into existence. An Angular service is a stateless object and provides some very useful functions. 

**Source:** _dzone.com_

#### Q8: What is interpolation? ⭐⭐
**Answer:**
**Interpolation** is a special syntax that Angular converts into property binding. It’s a convenient alternative to property binding. It is represented by double curly braces({{}}). The text between the braces is often the name of a component property. Angular replaces that name with the string value of the corresponding component property.
Let's take an example,
```html
    <h3>
      {{title}}
      <img src="{{url}}" style="height:30px">
    </h3>
```
In the example above, Angular evaluates the title and url properties and fills in the blanks, first displaying a bold application title and then a URL.

**Source:** _github.com/sudheerj_

#### Q9: What is a bootstrapping module? ⭐⭐
**Answer:**
Every application has at least one Angular module, the root module that you bootstrap to launch the application is called as bootstrapping module. It is commonly known as AppModule. The default structure of AppModule generated by AngularCLI would be as follows,
```javascript
    /* JavaScript imports */
    import { BrowserModule } from '@angular/platform-browser';
    import { NgModule } from '@angular/core';
    import { FormsModule } from '@angular/forms';
    import { HttpClientModule } from '@angular/common/http';

    import { AppComponent } from './app.component';

    /* the AppModule class with the @NgModule decorator */
    @NgModule({
      declarations: [
        AppComponent
      ],
      imports: [
        BrowserModule,
        FormsModule,
        HttpClientModule
      ],
      providers: [],
      bootstrap: [AppComponent]
    })
    export class AppModule { }
```

**Source:** _github.com/sudheerj_

#### Q10: What is the equivalent of ngShow and ngHide in Angular? ⭐⭐
**Answer:**
Just bind to the `hidden` property

**Source:** _stackoverflow.com_

#### Q11: What are observables? ⭐⭐
**Answer:**
**Observables** are declarative which provide support for passing messages between publishers and subscribers in your application. They are mainly used for event handling, asynchronous programming, and handling multiple values. In this case, you define a function for publishing values, but it is not executed until a consumer subscribes to it. The subscribed consumer then receives notifications until the function completes, or until they unsubscribe.

**Source:** _github.com/sudheerj_

#### Q12: What is an observable? ⭐⭐
**Answer:**
 An Observable is a unique Object similar to a Promise that can help manage async code. Observables are not part of the JavaScript language so we need to rely on a popular Observable library called RxJS.
    The observables are created using new keyword. Let see the simple example of observable,
```javascript
    import { Observable } from 'rxjs';

    const observable = new Observable(observer => {
      setTimeout(() => {
        observer.next('Hello from a Observable!');
      }, 2000);
    });`
```

**Source:** _github.com/sudheerj_

#### Q13: What is a component? Why would you use it? ⭐⭐
**Answer:**
*Components* are the most basic building block of an UI in an Angular application. An Angular application is a tree of Angular components. Angular components are a subset of directives. Unlike directives, components always have a template and only one component can be instantiated per an element in a template.

A component must belong to an NgModule in order for it to be usable by another component or application. To specify that a component is a member of an NgModule, you should list it in the `declarations` field of that NgModule.

```js
@Component({selector: 'greet', template: 'Hello {{name}}!'})
class Greet {
  name: string = 'World';
}
```

**Source:** _angular.io_

#### Q14: What is an observer? ⭐⭐
**Answer:**
Observer is an interface for a consumer of push-based notifications delivered by an Observable. It has below structure,
```javascript
    interface Observer<T> {
      closed?: boolean;
      next: (value: T) => void;
      error: (err: any) => void;
      complete: () => void;
    }
```
A handler that implements the Observer interface for receiving observable notifications will be passed as a parameter for observable as below,
```javascript
    myObservable.subscribe(myObserver);
```
**Note:** If you don't supply a handler for a notification type, the observer ignores notifications of that type.

**Source:** _github.com/sudheerj_

#### Q15: What is the purpose of base href tag? ⭐⭐
**Answer:**
The routing application should add <base> element to the index.html as the first child in the <head> tag inorder to indicate how to compose navigation URLs. If app folder is the application root then you can set the href value as below
```html
    <base href="/">
```

**Source:** _github.com/sudheerj_

#### Q16: You have an HTML response I want to display. How do I do that?  ⭐⭐
**Answer:**
The correct syntax is the following:
```html
<div [innerHTML]="theHtmlString"></div>
```
Working in `5.2.6`

**Source:** _medium.com_

#### Q17: What is the difference between Structural and Attribute directives in Angular? ⭐⭐
**Answer:**
* **Structural directives** are used to alter the DOM layout by removing and adding DOM elements. It is far better in changing the structure of the view. Examples of Structural directives are NgFor and Nglf.

* **Attribute Directives** These are being used as characteristics of elements. For example, a directive such as built-in NgStyle in the template Syntax guide is an attribute directive.

**Source:** _onlineinterviewquestions.com_

#### Q18: How can I select an element in a component template? ⭐⭐
**Answer:**
You can get a handle to the DOM element via ElementRef by injecting it into your component's constructor:

```js
constructor(myElement: ElementRef) { ... }
```

**Source:** _medium.com_

#### Q19: What is the equivalent of "ngShow" and "ngHide" in Angular? ⭐⭐
**Answer:**
Just bind to the hidden property:

```js
[hidden]="!myVar"
```

**Source:** _medium.com_

#### Q20: What is the difference between *ngIf vs [hidden]? ⭐⭐
**Answer:**
`*ngIf` effectively removes its content from the DOM while `[hidden]` modifies the `display` property and only instructs the browser to not show the content but the DOM still contains it.

**Source:** _medium.com_

#### Q21: What are the differences between AngularJS (angular 1.x) and Angular (Angular 2.x and beyond)? ⭐⭐
**Answer:**
Angular and AngularJS is basically a different framework with the same name.

Angular is more ready for the current state of web standards and the future state of the web (ES6\7, immutiablity, components, shadow DOM, service workers, mobile compatibilty, modules, typescript and so on and so on... )

Angular killed many main features in AngularJS like - controllers, $scope, directives (replaced with `@component` annotations), the module definition, and much more, even simple things like ng-repeat has not left the same as it was.

Also: 
1. They added an angular `cli`.
2. Your angular code is written in ES6 Typescript and it compiles at runtime to Javascript in the browser.
3. You bind to your HTML similarly like how you would if in an Angular 1 directive. So variable like $scope and $rootScope have been deprecated.

**Source:** _stackoverflow.com_

#### Q22: What are some differences between Angular 2 and 4? ⭐⭐
**Answer:**
Just to name a few:
* Improvements in AOT, 
* allowing the "else" clause in ngIf, 
* support for TypeScript 2.1
* breaking out the animations package

**Source:** _github.com/WebPredict_

#### Q23: What is the difference between "@Component" and "@Directive" in Angular?  ⭐⭐
**Answer:**
* **Directives** add behaviour to an existing DOM element or an existing component instance.
* **A component**, rather than adding/modifying behaviour, actually creates its own view (hierarchy of DOM elements) with attached behaviour.

Write a component when you want to create a reusable set of DOM elements of UI with custom behaviour. Write a directive when you want to write reusable behaviour to supplement existing DOM elements.

**Source:** _medium.com_

#### Q24: How would you protect a component being activated through the router? ⭐⭐
**Answer:**
The Angular router ships with a feature called guards. These provide us with ways to control the flow of our application. We can stop a user from visitng certain routes, stop a user from leaving routes, and more. The overall process for protecting Angular routes:

* Create a guard service: `ng g guard auth`
* Create `canActivate()` or `canActivateChild()` methods
* Use the guard when defining routes

```js
// import the newly created AuthGuard
const routes: Routes = [
  {
    path: 'account',
    canActivate: [AuthGuard]
  }
];
```

Some other available guards:

* `CanActivate`: Check if a user has access
* `CanActivateChild`: Check if a user has access to any of the child routes
* `CanDeactivate`: Can a user leave a page? For example, they haven't finished editing a post
* `Resolve`: Grab data before the route is instantiated
* `CanLoad`: Check to see if we can load the routes assets

**Source:** _scotch.io_

#### Q25: What does this line do? ⭐⭐
**Details:**
```js
@HostBinding('[class.valid]') isValid;
```

**Answer:**
`@HostBinding` lets you set properties on the element or component that hosts the directive.

The code applies the css class `valid` to whatever is using this directive conditionally based on the value of isValid.

**Source:** _alligator.io_

#### Q26: What is router outlet? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q27: What is difference between "declarations", "providers" and "import" in NgModule? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q28: What's new in Angular 6 and why shall we upgrade to it? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q29: Why would you use a spy in a test? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q30: What is TestBed? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q31: What is Protractor? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q32: What is the point of calling "renderer.invokeElementMethod(rendererEl, methodName)"? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q33: How would you control size of an element on resize of the window in a component? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q34: What is AOT? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q35: What is Redux and how does it relate to an Angular app? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q36: What is the use of codelyzer? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q37: How to inject base href? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q38: How to bundle an Angular app for production? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q39: When would you use eager module loading? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q40: What are the Core Dependencies of Angular 7? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q41: Why Incremental DOM Has Low Memory Footprint? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q42: What are the ways to control AOT compilation? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q43: What is Angular Universal? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q44: Do I need a Routing Module always? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q45: What is the purpose of Wildcard route? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q46: What is activated route? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q47: What is router state? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q48: What is Reactive Programming and how to use one with Angular? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q49: Why should `ngOnInit` be used, if we already have a `constructor`? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q50: What are dynamic components? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q51: Explain how custom elements works internally? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q52: What are custom elements? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q53: What are the utility functions provided by RxJS? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q54: How do you perform error handling in observables? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q55: What is multicasting? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q56: What is the difference between promise and observable? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q57: Can you explain the difference between `Promise` and `Observable` in Angular? In what scenario can we use each case? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q58: What is subscribing? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q59: How do you perform Error handling for HttpClient? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q60: What is the difference between `@Component` and `@Directive` in Angular? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q61: Explain the difference between "Constructor" and "ngOnInit" ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q62: What is a parameterized pipe? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q63: How do you categorize data binding types? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q64:  Explain the difference between `Promise` and `Observable` in Angular? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q65: What happens if you use script tag inside template? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q66: What is the option to choose between inline and external template file? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q67: What's new in Angular 8? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q68: Angular 8: What is Bazel? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q69: Angular 8: What is Angular Ivy? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q70: Angular 8: Explain Lazy Loading in Angular 8? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q71: Name some security best practices in Angular ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q72: How to set headers for every request in Angular? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q73: What is ngUpgrage?  ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q74: What are the mapping rules between Angular component and custom element? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q75: Why would you use renderer methods instead of using native element methods? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q76: Angular 9: What are some new features in Angular 9? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q77: Do I need to bootstrap custom elements? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q78: How do you create application to use scss? What changed for Angular 6? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q79: Name and explain some Angular Module Loading examples ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q80: What does "detectChanges" do in Angular jasmine tests? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q81: Why would you use lazy loading modules in Angular app? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q82: When does a lazy loaded module is loaded? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q83: What are the lifecycle hooks for components and directives? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q84: When should I store the "Subscription" instances and invoke `unsubscribe()` during the NgOnDestroy life cycle and when can I simply ignore them? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q85: What would be a good use for NgZone service? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q86: What is Ivy Renderer? Is it supported by Angular 7? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q87: What is incremental DOM? How is it different from virtual DOM? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q88: What is the difference between pure and impure pipe? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q89: What is Zone in Angular? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q90: How to detect a route change in Angular? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q91: What are the advantages with AOT? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q92: Could I use jQuery with Angular? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q93: How would you insert an embedded view from a prepared TemplateRef? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q94: Are there any pros/cons (especially performance-wise) in using local storage to replace cookie functionality? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q95: What does a just-in-time (JIT) compiler do (in general)? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q96: Angular 8: Why we should use Bazel for Angular builds? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q97: What is the need for SystemJS in Angular? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q98: What is Reactive programming and how does it relate to Angular? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q99: Explain the purpose of Service Workers in Angular ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q100: Why do we need compilation process? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q101: Angular 9: How Would You Compare View Engine vs Ivy? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q102: What is the Angular equivalent to an AngularJS "$watch"? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q103: Why Incremental DOM is Tree Shakable? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q104: What is the difference between BehaviorSubject vs Observable? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q105: What's new in Angular 7? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q106: Name some differences between SystemJS vs WebPack? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q107: What are observable creation functions? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q108: Is there no equivalent to `$scope.emit()` or `$scope.broadcast()` in Angular? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q109: What is the default compilation for Angular 5? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q110: Could you provide some particular examples of using ngZone? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q111: Why angular uses url segment? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q112: When to use query parameters versus matrix parameters? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q113: Angular 8: How does Ivy affect the (Re)build time? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q114: Angular 8: What are some changes in Location module? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q115: Do you know how you can run angularJS and angular side by side? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q116: How would you extract webpack config from angular cli project? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q117: Just-in-Time (JiT) vs Ahead-of-Time (AoT) compilation. Explain the difference. ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q118: Angular 9: What is Locality principle for Ivy? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q119: Angular 9: Explain improvements in Tree-Shaking ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q120: Why did the Google team go with incremental DOM instead of virtual DOM? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

## [[⬆]](#toc) <a name=AngularJS>AngularJS</a> Interview Questions
#### Q1: Why to use AngularJS? ⭐
**Answer:**
There are following reasons to choose AngularJS as a web development framework:

1. It is based on MVC pattern which helps you to organize your web apps or web application properly.
2. It extends HTML by attaching directives to your HTML markup with new attributes or tags and expressions
in order to define very powerful templates.
3. It also allows you to create your own directives, making reusable components that fill your needs and
abstract your DOM manipulation logic.
4. It supports two-way data binding i.e. connects your HTML (views) to your JavaScript objects (models)
seamlessly. In this way any change in model will update the view and vice versa without any DOM
manipulation or event handling.
5. It encapsulates the behavior of your application in controllers which are instantiated with the help of
dependency injection.
6. It supports services that can be injected into your controllers to use some utility code to fullfil your need.
For example, it provides $http service to communicate with REST service.
7. It supports dependency injection which helps you to test your angular app code very easily.
8. Also, AngularJS is mature community to help you. It has widely support over the internet.

**Source:** _github.com/krosti_

#### Q2: What is the difference between "ng-show"/"ng-hide" and "ng-if" directives? ⭐
**Answer:**
`ng-show`/`ng-hide` will always insert the DOM element, but will display/hide it based on the condition. `ng-if` will not insert the DOM element until the condition is not fulfilled.

`ng-if` is better when we needed the DOM to be loaded conditionally, as it will help load page bit faster compared to `ng-show`/`ng-hide`.

We only need to keep in mind what the difference between these directives is, so deciding which one to use totally depends on the task requirements.


**Source:** _codementor.io_

#### Q3: Does AngularJS has dependency on jQuery? ⭐⭐
**Answer:**
AngularJS has no dependency on jQuery library. But it can be used with jQuery library.

**Source:** _ github.com/krosti_

#### Q4: How do you hide an HTML element via a button click in AngularJS? ⭐⭐
**Answer:**
This can be done by using the `ng-hide` directive in conjunction with a controller to hide an HTML element on button click.

```html
<div ng-controller="MyCtrl">
    <button ng-click="hide()">Hide element</button>
    <p ng-hide="isHide">Hello World!</p>
</div>
```

```js
function MyCtrl($scope) {
	$scope.isHide = false;
	$scope.hide = function () {
		$scope.isHide = true;
	};
}
```
    

**Source:** _codementor.io_

#### Q5: What is a singleton pattern and where we can find it in AngularJS? ⭐⭐
**Answer:**
Is a great pattern that restricts the use of a class more than once. We can find singleton pattern in angular in dependency injection and in the services.

In a sense, if the you do 2 times `new Object()` without this pattern, the you will be alocating 2 pieces of memory for the same object. With singleton pattern, if the object exists, it'll be reused.

**Source:** _codementor.io_

#### Q6: What are the AngularJS features? ⭐⭐
**Answer:**
The features of AngularJS are listed below:

1. Modules
2. Directives
3. Templates
4. Scope
5. Expressions
6. Data Binding
7. MVC (Model, View & Controller)
8. Validations
9. Filters
10. Services
11. Routing
12. Dependency Injection
13. Testing

**Source:** _github.com/krosti_

#### Q7: When dependent modules of a module are loaded? ⭐⭐
**Answer:**
A module might have dependencies on other modules. The dependent modules are loaded by angular
before the requiring module is loaded.

In other words the configuration blocks of the dependent modules execute before the configuration blocks of the requiring module. The same is true for the run blocks. Each module can only be loaded once, even if multiple other modules require it.

**Source:** _github.com/krosti_

#### Q8: What is Angular’s prefixes $ and $$? ⭐⭐
**Answer:**
To prevent accidental name collisions with your code, Angular prefixes names of public objects with $ and names of private objects with `$$`. So, do not use the `$` or `$$` prefix in your code.

**Source:** _github.com/krosti_

#### Q9: What are Filters in AngularJS? ⭐⭐
**Answer:**
*Filters* are used to format data before displaying it to the user. They can be used in view templates, controllers, services and directives. There are some built-in filters provided by AngularJS like as `Currency`, `Date`, `Number`, `OrderBy`, `Lowercase`, `Uppercase` etc. You can also create your own filters.

Filter Syntax:

```{{ expression | filter}}```

**Source:** _github.com/krosti_

#### Q10: What are Directives in AngularJS? ⭐⭐
**Answer:**
AngularJS directives are a combination of AngularJS template markups (HTML attributes or elements, or CSS classes) and supporting JavaScript code. The JavaScript directive code defines the template data and behaviors of the HTML elements.

AngularJS directives are used to extend the HTML vocabulary i.e. they decorate html elements with new behaviors and help to manipulate html elements attributes in interesting way.

There are some built-in directives provided by AngularJS like as ng-app, ng-controller, ng-repeat, ng-model etc.


**Source:** _github.com/krosti_

#### Q11: What are Directives? ⭐⭐
**Answer:**
**Directives** are markers on a DOM element (such as an attribute, element name, comment or CSS class) that tell AngularJS’s HTML compiler ($compile) to attach a specified behavior to that DOM element (e.g. via event listeners), or even to transform the DOM element and its children. 

Angular comes with a set of these directives built-in, like `ngBind`, `ngModel`, and `ngClass`. Much like you create controllers and services, you can create your own directives for Angular to use. When Angular bootstraps your application, the HTML compiler traverses the DOM matching directives against the DOM elements.

**Source:** _codementor.io_

#### Q12: Explain what is a "$scope" in AngularJS ⭐⭐
**Answer:**
**Scope** is an object that refers to the application model. It is an execution context for expressions. Scopes are arranged in hierarchical structure which mimic the DOM structure of the application. Scopes can watch expressions and propagate events. Scopes are objects that refer to the model. They act as glue between controller and view.

**Source:** _codementor.io_

#### Q13: What directive would you use to hide elements from the HTML DOM by removing them from that DOM not changing their styling? ⭐⭐
**Answer:**
The `ngIf` Directive, when applied to an element, will remove that element from the DOM if it’s condition is false.

**Source:** _codementor.io_

#### Q14: What is the difference between one-way binding and two-way binding? ⭐⭐
**Answer:**
* One way binding implies that the scope variable in the html will be set to the first value its model is bound to (i.e. assigned to)  
* Two way binding implies that the scope variable will change it’s value everytime its model is assigned to a different value

**Source:** _codementor.io_

#### Q15: What is auto bootstrap process in AngularJS? ⭐⭐
**Answer:**
Angular initializes automatically upon ```DOMContentLoaded``` event or when the angular.js script is downloaded to the browser and the ```document.readyState``` is set to ```complete```. At this point AngularJS looks for the ```ng-app``` directive which is the root of angular app compilation and tells about AngularJS part within DOM. When the ```ng-app``` directive is found then Angular will:

1. Load the module associated with the directive.
2. Create the application injector.
3. Compile the DOM starting from the ng-app root element.
This process is called auto-bootstrapping.

```html
<html>
<body ng-app="myApp">
<div ng-controller="Ctrl"> Hello {{msg}}!
</div>
    <script src="lib/angular.js"></script>
    <script>
var app = angular.module('myApp', []); app.controller('Ctrl', function ($scope) {
              $scope.msg = 'World';
          });
    </script>
</body>
</html>
```

**Source:** _github.com/krosti_

#### Q16: How would you specify that a scope variable should have one-time binding only? ⭐⭐
**Answer:**
By using “`::`” in front of it. 

**Source:** _codementor.io_

#### Q17: What is scope in AngularJS? ⭐⭐
**Answer:**
Scope is a JavaScript object that refers to the application model. It acts as a context for evaluating angular expressions. Basically, it acts as glue between controller and view.

Scopes are hierarchical in nature and follow the DOM structure of your AngularJS app. AngularJS has two scope objects: **$rootScope** and **$scope**.

**Source:** _github.com/krosti_

#### Q18: How do you disable a button depending on a checkbox’s state? ⭐⭐
**Answer:**
We can use the `ng-disabled` directive and bind its condition to the checkbox’s state.

```html
<body ng-app>
    <label>
        <input type="checkbox" ng-model="checked" />Disable Button
    </label>
    <button ng-disabled="checked">Select me</button>
</body>
```
    

**Source:** _codementor.io_

#### Q19: What is scope hierarchy? ⭐⭐
**Answer:**
The **$scope** object used by views in AngularJS are organized into a hierarchy. There is a root scope, and the **$rootScope** can has one or more child scopes. Each controller has its own **$scope** (which is a child of the **$rootScope**), so whatever variables you create on $scope within controller, these variables are accessible by the view based on this controller.

For example, suppose you have two controllers: ParentController and ChildController as given below:
```html
<html>
  <head>
    <script src="lib/angular.js"></script>
    <script>
      var app = angular.module('ScopeChain', []); app.controller("parentController", function ($scope) {
      	$scope.managerName = 'Shailendra Chauhan';
      	$scope.$parent.companyName = 'Dot Net Tricks'; //attached to $rootScope
      });
      app.controller("childController", function ($scope, $controller) {
                 $scope.teamLeadName = 'Deepak Chauhan';
             });
         
    </script>
  </head>
  <body ng-app="ScopeChain">
    <div ng-controller="parentController ">
      <table style="border:2px solid #e37112">
        <caption>Parent Controller</caption>
        <tr>
          <td>Manager Name</td>
          <td>{{managerName}}</td>
        </tr>
        <tr>
          <td>Company Name</td>
          <td>{{companyName}}</td>
        </tr>
        <tr>
          <td>
            <table ng-controller="childController" style="border:2px solid #428bca">
              <caption>Child Controller</caption>
              <tr>
                <td>Team Lead Name</td>
                <td>{{ teamLeadName }}</td>
              </tr>
              <tr>
                <td>Reporting To</td>
                <td>{{managerName}}</td>
              </tr>
              <tr>
                <td>Company Name</td>
                <td>{{companyName}}</td>
              </tr>
            </table>
          </td>
        </tr>
      </table>
    </div>
  </body>
</html>
```


**Source:** _github.com/krosti_

#### Q20: How do you share data between controllers? ⭐⭐
**Answer:**
Create an AngularJS service that will hold the data and inject it inside of the controllers.

Using a service is the cleanest, fastest and easiest way to test. However, there are couple of other ways to implement data sharing between controllers, like:

– Using `events`  
– Using `$parent`, `nextSibling`, `controllerAs`, etc. to directly access the controllers  
– Using the `$rootScope` to add the data on (not a good practice)

The methods above are all correct, but are not the most efficient and easy to test.

**Source:** _codementor.io_

#### Q21: What are the basic steps to unit test an AngularJS filter? ⭐⭐
**Answer:**
* Inject the module that contains the filter.
* Provide any mocks that the filter relies on.
* Get an instance of the filter using `$filter('yourFilterName')`.
* Assert your expectations.

**Source:** _codementor.io_

#### Q22: What are the basic steps to unit test an AngularJS filter? ⭐⭐
**Answer:**
1.  Inject the module that contains the filter.
2.  Provide any mocks that the filter relies on.
3.  Get an instance of the filter using `$filter('yourFilterName')`.
4.  Assert your expectations.

**Source:** _codementor.io_

#### Q23:  What are the advantage of AngularJS? ⭐⭐
**Answer:**
There are following advantages of AngularJS:

1. **Data Binding** - AngularJS provides a powerful data binding mechanism to bind data to HTML elements by using scope.
2. **Customize & Extensible** - AngularJS is customized and extensible as per you requirement. You can create your own custom components like directives, services etc.
3. **Code Reusability** - AngularJS allows you to write code which can be reused. For example custom directive which you can reuse.
4. **Support** – AngularJS is mature community to help you. It has widely support over the internet. Also, AngularJS is supported by Google which gives it an advantage.
5. **Compatibility** - AngularJS is based on JavaScript which makes it easier to integrate with any other JavaScript library and runnable on browsers like IE, Opera, FF, Safari, Chrome etc.
6. **Testing** - AngularJS is designed to be testable so that you can test your AngularJS app components as easy as possible. It has dependency injection at its core, which makes it easy to test.

**Source:** _github.com/krosti_

#### Q24: Explain what is services in AngularJS ⭐⭐
**Answer:**
In AngularJS *services* are the singleton objects or functions that are used for carrying out specific tasks.  It holds some business logic and these function can be called as controllers, directive, filters and so on.

**Source:** _github.com/krosti_

#### Q25: Explain what is directive and mention what are the different types of Directive? ⭐⭐
**Answer:**
During compilation process when specific HTML constructs are encountered a behaviour or function is triggered, this function is referred as *directive*.  It is executed when the compiler encounters it in the DOM.

Different types of directives are:

* Element directives
* Attribute directives
* CSS class directives
* Comment directives

**Source:** _guru99.com_

#### Q26: How would you validate a text input field for a twitter username, including the @ symbol? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q27: Explain what is the difference between link and compile in AngularJS? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q28: How would you react on model changes to trigger some further action?  ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q29: What is jQLite/jQuery Lite? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q30: What should be the maximum number of concurrent “watches”? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q31: What is a digest cycle in AngularJS? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q32: Where should we implement the DOM manipulation in AngularJS? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q33: Is it a good or bad practice to use AngularJS together with jQuery? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q34: If you were to migrate from Angular 1.4 to Angular 1.5, what is the main thing that would need refactoring? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q35:  Explain what Angular JS routes does? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q36: Explain what is Angular Expression? Explain what is key difference between angular expressions and JavaScript expressions? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q37: What is restrict option in directive? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q38: How would you make an Angular service return a promise? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q39: What is the role of services in AngularJS and name any services made available by default? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q40: How do you reset a "$timeout", "$interval()", and disable a "$watch()"? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q41: What are different ways to invoke a directive? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q42: What is the role of ng-app, ng-init and ng-model directives? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q43: How to access jQLite? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q44: What is an interceptor? What are common uses of it? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q45: What is manual bootstrap process in AngularJS? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q46: What makes the `angular.copy()` method so powerful? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q47: Explain what is linking function and type of linking function? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q48: Explain what is injector? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q49: When creating a directive, it can be used in several different ways in the view. Which ways for using a directive do you know? How do you define the way your directive will be used? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q50: When should you use an attribute versus an element? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q51: Explain what is DI (Dependency Injection ) and how an object or function can get a hold of its dependencies? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q52: Explain how `$scope.$apply()` works? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q53: How AngularJS is compiled? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q54: What is DDO (Directive Definition Object)? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q55: Can you define multiple restrict options on a directive? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q56: What is the difference between $scope and scope? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q57: How would you implement application-wide exception handling in your Angular app? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q58:  What is $scope and $rootScope? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q59: How would you programatically change or adapt the template of a directive before it is executed and transformed? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q60: How AngularJS compilation is different from other JavaScript frameworks? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q61: How Directives are compiled? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q62: What are Compile, Pre and Post linking in AngularJS? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

## [[⬆]](#toc) <a name=Azure>Azure</a> Interview Questions
#### Q1: What are the benefits of severless applications? ⭐
**Answer:**
* Avoid managing servers
* Flexible scaling by demand
* Pay for time and resources it takes to execute your code

#### Q2: What is Azure Cloud Service? ⭐
**Answer:**
By creating a cloud service, you can deploy a multi-tier web application in Azure, defining multiple roles to distribute processing and allow flexible scaling of your application. A cloud service consists of one or more web roles and/or worker roles, each with its own application files and configuration. Azure Websites and Virtual Machines also enable web applications on Azure. The main advantage of cloud services is the ability to support more complex multi-tier architectures

**Source:** _mindmajix.com_

#### Q3: What is a web role? ⭐
**Answer:**
A web role provides a dedicated Internet Information Services (IIS) web-server used for hosting front-end web applications.

**Source:** _mindmajix.com_

#### Q4: What is Azure Functions? ⭐
**Answer:**
Azure Functions is a solution for easily running small pieces of code, or "functions," in the cloud. We can write just the code we need for the problem at hand, without worrying about a whole application or the infrastructure to run it and use language of our choice such as C#, F#, Node.js, Java, or PHP. Azure Functions lets us develop serverless applications on Microsoft Azure.

#### Q5: What is serverless computing? ⭐
**Answer:**
Serverless computing is the abstraction of servers, infrastructure, and operating systems. When you build serverless apps you don’t need to provision and manage any servers, so you can take your mind off infrastructure concerns. Serverless computing is driven by the reaction to events and triggers happening in near-real-time—in the cloud. 

As a fully managed service, server management and capacity planning are invisible to the developer and billing is based just on resources consumed or the actual time your code is running.

#### Q6: Is Azure Table Storage Nosql? ⭐⭐
**Answer:**
**Azure Table storage** is a service that stores structured NoSQL data in the cloud, providing a key/attribute store with a schemaless design.

**Source:** _docs.microsoft.com_

#### Q7: What is Kudu? ⭐⭐
**Answer:**
Every Azure App Service web application includes a "hidden" service site called **Kudu**.

Kudu Console for example is a debugging service for Azure platform which allows you to explore your web app and surf the bugs present on it, like deployment logs, memory dump, and uploading files to your web app, and adding JSON endpoints to your web apps, etc.


#### Q8: What is a role instance? ⭐⭐
**Answer:**
A role instance is a virtual machine on which the application code and role configuration run. A role can have multiple instances, defined in the service configuration file.

**Source:** _mindmajix.com_

#### Q9: What is a guest operating system? ⭐⭐
**Answer:**
The guest operating system for a cloud service is the operating system installed on the role instances (virtual machines) on which your application code runs.

**Source:** _mindmajix.com_

#### Q10: What is Azure Blob Storage? ⭐⭐
**Answer:**
*Azure Blob storage* is Microsoft's object storage solution for the cloud. Blob storage is optimized for storing massive amounts of unstructured data, such as text or binary data. Azure Storage offers three types of blobs:
* **Block blobs** store text and binary data, up to about 4.7 TB. Block blobs are made up of blocks of data that can be managed individually.
* **Append blobs** are made up of blocks like block blobs, but are optimized for append operations. Append blobs are ideal for scenarios such as logging data from virtual machines.
* **Page blobs** store random access files up to 8 TB in size. Page blobs store the VHD files that back VMs.


**Source:** _docs.microsoft.com_

#### Q11: How to include external dll into Azure Function? ⭐⭐
**Answer:**
* Add the assembly to the BIN directory using KUDU
* Include the assembly and code the Azure Function to use it
* Add the using declaration so that the methods within the DLL can be accessed. 

```cs
#r "D:\home\site\wwwroot\GreetingsAssemblyReference\bin\benjamin.dll"

using benjamin;
```

#### Q12: What is an Azure subscription? ⭐⭐
**Answer:**
A Windows **Azure subscription** grants you access to Windows Azure services and to the Windows Azure Platform Management Portal. A Windows Azure subscription has two aspects: 
* The Windows Azure account, through which resource usage is reported
* Services are billed.

**Source:** _blogs.msdn.microsoft.com_

#### Q13: What is Azure ARM? ⭐⭐
**Answer:**
The **Azure Resource Manager (ARM)** is the service used to provision resources in your Azure subscription. It was first announced at Build 2014 when the new Azure portal ( portal.azure.com) was announced and provides a new set of API's that are used to provision resources. The ARM is:

* Template-driven – Using templates to deploy all resources.
* Declarative – You declare the resources you want to have instead of imperative where you need to make rules.
* Idempotent – You can deploy the template over and over again without affecting the current state of resources.
* Multi-service – All services can be deployed using Azure Resource Manager, Website, Storage, VMs etc.
* Multi region - You can choose in which region you would like to deploy the resources.
* Extensible – Azure Resource Manager is extensible with more resource providers and thus resources.


**Source:** _azurestack.blog_

#### Q14: Explain the Azure ARM Templates ⭐⭐
**Answer:**
An Azure Resource Template is a JSON file used to deploy resources with Azure Resource Manager. It defines:
* Parameters
* Variables
* Resources - the actual resources that you are going to deploy or update
* Outputs

**Source:** _onlinetech.com_

#### Q15: What is a cloud service role? ⭐⭐
**Answer:**
A cloud service role is comprised of application files and a configuration. A cloud service can have two types of roles:
* web role
* worker role

**Source:** _mindmajix.com_

#### Q16: What is Azure Redis Cache? ⭐⭐
**Answer:**
*Redis* is an open source (BSD licensed), in-memory data structure store, used as a database, cache and message broker. **Azure Redis Cache** is based on the popular open-source Redis cache. It gives you access to a secure, dedicated Redis cache, managed by Microsoft, and accessible from any application within Azure. It supports data structures such as strings, hashes, lists, sets, sorted sets with range queries, bitmaps, hyperloglogs and geospatial indexes with radius queries.

**Source:** _quora.com_

#### Q17: What is Azure Service Fabric? ⭐⭐
**Answer:**
**Azure Service Fabric** is a distributed systems platform that makes it easy to package, deploy, and manage scalable and reliable micro-services. Service Fabric also addresses the significant challenges in developing and managing cloud applications. Developers and administrators can avoid complex infrastructure problems and focus on implementing mission-critical, demanding workloads that are scalable, reliable, and manageable. Service Fabric represents the next-generation middleware platform for building and managing these enterprise-class, tier-1, cloud-scale applications.

**Source:** _quora.com_

#### Q18: How can I use applications with Azure AD that I’m using on-premises? ⭐⭐
**Answer:**
*Azure AD* gives you an easy and secure way to connect to the web applications you choose. You can access these applications in the same way you access your SaaS apps in Azure AD, no need for a VPN to change your network infrastructure.

**Source:** _quora.com_

#### Q19: What is Azure Resource Group? ⭐⭐
**Answer:**
Resource groups (RG) in Azure is an approach to group a collection of assets in logical groups for easy or even automatic provisioning, monitoring, and access control, and for more effective management of their costs. The underlying technology that powers resource groups is the Azure Resource Manager (ARM).

**Source:** _onlinetech.com_

#### Q20: What Is Azure Key Vault? ⭐⭐
**Answer:**
**Key Vault** help you safeguard cryptographic keys and other secrets used by your applications whenever they are On-Premise or in the cloud. More and more services on Azure are now integrating Azure Key Vault as their secret/key source for things like deployments, data or even disk encryption.

**Source:** _codeisahighway.com_

#### Q21: What is a Blob Container? ⭐⭐
**Answer:**
A container organizes a set of blobs, similar to a folder in a file system. All blobs reside within a container. A storage account can contain an unlimited number of containers, and a container can store an unlimited number of blobs.

**Source:** _docs.microsoft.com_

#### Q22: How can you stop a VM using Power Shell? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q23: How can you retrieve the state of a particular VM? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q24: How can one create a VM in Azure CLI? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q25: What do you know about Azure WebJobs? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q26: What is Azure MFA? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q27: How can one create a Virtual Machine in Powershell? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q28: How much storage can I use with a virtual machine? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q29: Is it possible to add an existing VM to an availability set? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q30: What is a worker role? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q31: What is Azure VPN? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q32: What is the difference between Service Bus Queues and Storage Queues? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q33: What are the differences between Subscription Administrator and Directory Administrator? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q34: What is a VNet? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q35: What is key vault in Azure? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q36: What are stateful and stateless microservices for Service Fabric? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q37: Do scale sets work with Azure availability sets? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q38: What are Network Security Groups? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q39: What are Update Domains? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q40: What are Fault Domains? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q41: What is an Availability Set? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q42: What are virtual machine scale sets in Azure? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q43: What is deployment environments? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q44: What are Cloud Service Roles and why do we use them? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q45: What is Azure Table Storage? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q46: What is Azure Resource Manager and why we need to use one? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q47: What is Azure Search? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q48: What are Redis databases? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q49: Is it possible to create a Virtual Machine using Azure Resource Manager in a Virtual Network that was created using classic deployment? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q50: How to create a new storage account and container using Power Shell? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q51:  What is the meaning of application partitions? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q52: What is the difference between “price,” “software price,” and “total price” in the cost structure for Virtual Machine offers in the Azure Marketplace? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q53: What is Azure VNET? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q54: How to create a Network Security Group and a Network Security Group Rule? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q55: How are Azure Marketplace subscriptions priced? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q56: What are special Azure Regions? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q57: Explain Azure NSG ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q58: What VPN types are supported by Azure? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

## [[⬆]](#toc) <a name=Behavioral>Behavioral</a> Interview Questions
#### Q1: How do you spend your time outside work? ⭐
**Answer:**


#### Q2: Why are you interested in this opportunity? ⭐
**Answer:**


#### Q3: Why do you want to work for X company? ⭐
**Answer:**
The interviewer is looking for similar things whether asking about company or position. The hiring manager wants to:

* Learn about your career goals and how this position fits into your plan
* Make sure that you are sincerely interested in the job and will be motivated to perform if hired
* Find out what you know about the company, industry, position (and if you took the time to research)
* Understand your priorities and preferences — which aspects of the company and/or job are appealing to you and why?

**Source:** _github.com/yangshun/tech-interview-handbook_

#### Q4: Why do you want to leave your current/last company? ⭐
**Answer:**
Here are some things your interviewer is likely looking for:

* Did you leave for a good reason?
* Did you leave voluntarily?
* Did you leave on good terms?
* What are your work values?

**Source:** _biginterview.com_

#### Q5: A hammer and a nail cost $1.10 together, and the hammer costs one dollar more than the nail. How much does the nail cost? ⭐
**Answer:**


**Source:** _startups.co_

#### Q6: What are you looking for in your next role? ⭐
**Answer:**


**Source:** _github.com/yangshun/tech-interview-handbook_

#### Q7: How large was the last team that you worked on? ⭐
**Answer:**


#### Q8: Do you plan to advance your education while working here? ⭐
**Answer:**


#### Q9: What are your hobbies? ⭐
**Answer:**


#### Q10: Tell me the story of how you became who you are today and what made you apply to X. ⭐
**Answer:**


#### Q11: Why do you think you’re a good fit for this company? ⭐⭐
**Answer:**


#### Q12: What’s are your favorite five apps? ⭐⭐
**Answer:**


#### Q13: Why do you want to come work at a startup, as opposed to an established company? ⭐⭐
**Answer:**


#### Q14: Share one of your trips with us. ⭐⭐
**Answer:**


#### Q15: What project are you currently working on? ⭐⭐
**Answer:**


#### Q16: Do prefer to work at a single company for a long time or would you rather take a job that suits you at the time? ⭐⭐
**Answer:**


#### Q17: Can you give an example of a career goal that you set and how you went about meeting it? ⭐⭐
**Answer:**


#### Q18: How quickly can you learn to use a new technology? ⭐⭐
**Answer:**


#### Q19: What does "belong anywhere" mean to you? ⭐⭐
**Answer:**


#### Q20: Can you list any deal breakers that would deter you from working for an employer? ⭐⭐
**Answer:**


#### Q21: Are you more interested in a career that offers great compensation, flexibility or the chance to do something meaningful? ⭐⭐
**Answer:**


#### Q22: What are you excited about? ⭐⭐
**Answer:**


#### Q23: Why do people resist change? ⭐⭐
**Answer:**


**Source:** _github.com_

#### Q24:  Can you tell me what part of your resume you are most proud of? ⭐⭐
**Answer:**


#### Q25: Tell me about your last project - what worked and what didn’t? ⭐⭐
**Answer:**


#### Q26: What would your previous boss say your biggest strength was? ⭐⭐
**Answer:**


#### Q27: How do you stay up to date with the latest technologies? ⭐⭐
**Answer:**


#### Q28: What is the hardest technical problem you have run into? ⭐⭐
**Answer:**


#### Q29: What have you built as your side project? ⭐⭐
**Answer:**


#### Q30: If someone has a different viewpoint to do a project like different programming language, how would handle this situation? ⭐⭐
**Answer:**


#### Q31: What are your personal goals? ⭐⭐
**Answer:**


#### Q32: What was the most fun thing you did recently? ⭐⭐
**Answer:**


#### Q33: How do you deal with difficult coworkers? Think about specific instances where you resolved conflicts. ⭐⭐
**Answer:**


#### Q34: State an experience about how you solved a technical problem. Be specific about the diagnosis and process. ⭐⭐
**Answer:**


#### Q35: What is your biggest strength and area of growth? ⭐⭐
**Answer:**


#### Q36: Have you worked in a distributed team before? What challenges did you face? ⭐⭐
**Answer:**


#### Q37: What’s the most difficult part of being a member of a team for you? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q38: Tell me about a time your work responsibilities got a little overwhelming. What did you do? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q39: Where do you want to be in five years? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q40: Tell me about a time in which you had a conflict and needed to influence somebody else. ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q41:  What can you actually do for us? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q42: How did you win over the difficult employees? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q43: What are your three strengths and three weaknesses? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q44: What does it mean to be a "Professional Developer"? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q45: Would you prefer working on Green Field or Brown Field projects? Why? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q46: Describe company X to your grandmother. ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q47: Tell me a time when you predicted something. ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q48: Tell me a situation where you would have done something differently from what you actually did. ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q49: In my professional experience have you worked on something without getting approval from your manager? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q50: Explain me your toughest project and the working architecture. ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q51: What makes good code good? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q52: If you were to open your own business in the future, what kind of business will you open and why? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q53: Would you rather be good at a lot of things or an expert at one thing? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q54: Tell me something you are learning right now. ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q55: Tell me about a challenge you faced recently in your role. How did you tackle it? What was the outcome? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q56: What does your best day of work look like? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q57: Tell me about a time when you had a conflict with a co-worker. ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q58: What is the best gift you have ever given or received? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q59: What is something that you had to push for in your previous projects? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q60: What’s the best advice you’ve recently received? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q61: Can you explain this gap in your resume? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q62: What is something that you don't want from your last internship/job? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q63: If you had an unlimited budget and you could go somewhere, where would you go? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q64: What large problems in the world would you solve today? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q65: What frustrates you? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q66: If you had an unlimited budget and you could buy one gift for one person, what would you buy and who would you buy it for? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q67: Tell me about a time you needed information from someone who wasn't responsive. What did you do? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q68: What is the most exceedingly bad misstep you've made at any point? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q69: What books have inspired you in you live? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q70:  What is the biggest mistake that you made in your last position? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q71: What is something new that you can teach your interviewer in a few minutes? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q72: What are some of the new ideas you would implement in this position? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q73: Are you comfortable assuming responsibilities outside your job description? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q74: What is the most challenging aspect of your current project? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q75: Tell me something about yourself and why you'd be a good fit for the position. ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q76: What are some of the best and worst things about your current company? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q77: How do you respond to constructive criticism? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q78: Explain streaming and how you would implement it. ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q79: Apart from technical knowledge, what did you learn during your work at Y? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q80: Talk about a project you are most passionate about, or one where you did your best work. ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q81: What was the most difficult bug that you fixed in the past 6 months? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q82: Imagine it is your first day here at the company. What do you want to work on? What features would you improve on? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q83: How do you deal with a failed deadline? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q84: Do you prefer to work in a team or individually? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q85: How do you tackle challenges? Name a difficult challenge you faced while working on a project, how you overcame it, and what you learned. ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q86: What are the most interesting projects you have worked on and how might they be relevant to this company's environment? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q87: What is the craziest thing you’ve ever done? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q88: What is your superpower? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q89: What is something you had to persevere at for multiple months? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q90: Tell me about a time you had to give someone terrible news. ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q91: Imagine there's a perfect clone of yourself. Imagine that that clone is your boss. Would you like to work for him/her? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q92: Interview me ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q93: Why are Quora's answers better than Yahoo Answers' ones? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q94: Let's play a game: defend Cobol against modern languages, and try to find as many reasonable arguments as you can. ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q95: Where will you be in 10 years? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q96: You are my boss and I'm fired. Inform me. ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q97: I want to refactor a legacy system. You want to rewrite it from scratch. Argument. Then, switch our roles. ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q98: Your boss asks you to lie to the Company. What's your reaction? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q99: Tell me about a time you had a disagreement with your manager. ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q100: What would happen if you put a mirror in a scanner? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q101: As a software engineer you want both to innovate and to be predictable. How those 2 goals can coexist in the same strategy? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q102: Name a situation where you were impressed by a company's customer service. ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q103: If you were given $1 million dollars every year for the rest of your life, what would you do? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q104: What risks do you feel you should never take? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q105: What is something 90% of people disagree with you about? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q106: Is developing software an art, a craftsmanship or an engineering endeavour? Your opinion. ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q107: Tell me about a time you were uncomfortable and how you dealt with it. ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q108:  In one word, describe yourself. ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q109: Who do you look to as a role model? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q110: What is the most constructive feedback you have received in your career? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q111: What is broken around you? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q112: If you could travel back in time, which advice would you give to your younger self? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

## [[⬆]](#toc) <a name=BigData>Big Data</a> Interview Questions
#### Q1: What is the meaning of big data and how is it different? ⭐
**Answer:**
Big data is the term to represent all kind of data generated on the internet. On the internet over hundreds of GB of data is generated only by online activity. Here, online activity implies web activity, blogs, text, video/audio files, images, email, social network activity, and so on. Big data can be referred to data created from all these activities. Data generated online is mostly in unstructured form. Big data will also include transactions data in the database, system log files, along with data generated from smart devices such as sensors, IoT, RFID tags, and so on in addition to online activities.

Big data needs specialized systems and software tools to process all unstructured data. In fact, according to some industry estimates almost 85% of data generated on the internet is unstructured. Usually, relational databases have a structured format and the database is centralized. Hence, with RDBMS processing can be quickly done using a query language such as SQL. On the other hand, big data is very large and is distributed across the internet and hence processing big data will need distributed systems and tools to extract information from them. Big data needs specialized tools such as Hadoop, Hive, or others along with high-performance hardware and networks to process them.


**Source:** _www.educba.com_

#### Q2: What are the characteristics of big data? ⭐
**Answer:**
Big data has three main characteristics: Volume, Variety, and Velocity.
Volume characteristic refers to the size of data. Estimates show that over 3 million GB of data is generated every day. Processing this volume of data is not possible in a normal personal computer or in a client-server network in an office environment with limited compute bandwidth and storage capacities. However, cloud services provide solutions to handle big data volumes and process them efficiently using distributed computing architectures.

Variety characteristic refers to the format of big data – structured or unstructured. Traditional RDBMS fits into the structured format. An example of unstructured data format is, a video file format, image files, plain text format, from web document or standard MS Word documents, all have unique formats, and so on. Also to note, RDBMS does not have the capacity to handle unstructured data formats. Further, all this unstructured data must be grouped and consolidated which creates the need for specialized tools and systems. In addition new, data is added each day, or each minute and data grows continuously. Hence big data is more synonymous with variety.

The velocity characteristic refers to the speed at which data is created and the efficiency required to process all the data. For example, Facebook is accessed by over 1.6 billion users in a month. Likewise, there are other social network sites, YouTube, Google services, etc. Such data streams must be processed using queries in real time and must be stored without data loss. Thus, velocity characteristic is important in big data processing.
In addition, other characteristics include veracity and value. Veracity will determine the dependability and reliability of data and value is the value derived by organizations from big data processing.

**Source:** _www.educba.com_

#### Q3: Why is big data important for organizations? ⭐
**Answer:**
This is the basic Big Data interview question asked in an interview. Big data is important because by processing big data, organizations can obtain insight information related to:

 * Cost reduction
 * Improvements in products or services
 * To understand customer behaviour and markets
 * Effective decision making
 * To become more competitive

**Source:** _www.educba.com_

#### Q4: Name some tools or systems used in big data processing? ⭐
**Answer:**
Big data processing and analysis can be done using:
 * Hadoop
 * Hive
 * Pig
 * Mahout
 * Flume

**Source:** _www.educba.com_

#### Q5: How can big data support organizations? ⭐⭐
**Answer:**
Big data has the potential to support organizations in many ways. Information extracted from big data can be used in:
 * Better coordination with customers and stakeholders and to resolve problems
 * Improve reporting and analysis for product or service improvements
 * Customize products and services to selected markets
 * Ensure better information sharing
 * Support in management decisions
 * Identify new opportunities, product ideas, and new markets
 * Gather data from multiple sources and archive them for future reference
 * Maintain databases, systems
 * Determine performance metrics
 * Understand interdependencies between business functions
 * Evaluate organizational performance

**Source:** _www.educba.com_

#### Q6: Explain how big data can be used to increase business value? ⭐⭐
**Answer:**
While understanding the need for analyzing big data, such analysis will help businesses to identify their position in markets, and help businesses to differentiate themselves from their competitors. For example, from the results of big data analysis, organizations can understand the need for customized products or can understand potential markets towards increasing revenue and value. Analyzing big data will involve grouping data from various sources to understand trends and information related to business. When big data analysis is done in a planned manner by gathering data from the right sources, organizations can easily generate business value and revenue by almost 5% to 20%. Some examples of such organizations are Amazon, Linkedin, WalMart, and many others.

**Source:** _www.educba.com_

#### Q7: What is big data solution implementation? ⭐⭐
**Answer:**
Big data solutions are implemented at a small scale first, based on a concept as appropriate for the business. From the result, which is a prototype solution, the business solution is scaled further. This is the most popular Big Data interview questions asked in a Big Data interview Some of the best practices followed in the industry include:
 * To have clear project objectives and to collaborate wherever necessary
 * Gathering data from the right sources
 * Ensure the results are not skewed because this can lead to wrong conclusions
 * Be prepared to innovate by considering hybrid approaches in processing by including data from structured and unstructured types, include both internal and external data sources
 * Understand the impact of big data on existing information flows in the organization

**Source:** _www.educba.com_

#### Q8: What are the steps involved in big data solutions? ⭐⭐
**Answer:**
Big data solutions follow three standard steps in its implementation. They are:

**Data ingestion**: This step will define the approach to extract and consolidate data from multiple sources. For example, data sources can be social network feeds, CRM, RDBMS, etc. The data extracted from different sources is stored in a Hadoop distributed file system (HDFS).

**Data storage**: This is the second step, the extracted data is stored. This storage can be in HDFS or HBase (NoSQL database).

**Process the data**: This is the last step. The data stored must be processed. Processing is done using tools such as Spark, Pig, MapReduce, and others.

**Source:** _www.educba.com_

## [[⬆]](#toc) <a name=Blockchain>Blockchain</a> Interview Questions
#### Q1: What is blockchain? ⭐
**Answer:**
**Blockchain** is a secure distributed ledger (data structure or database) that maintains a continuously growing list of ordered records, called “blocks”,  that are linked using cryptography. Each block contains a cryptographic hash of the previous block, a timestamp, and transaction data.

By design, a blockchain is resistant to modification of the data. It is "an open, distributed ledger that can record transactions between two parties efficiently and in a verifiable and permanent way".

Once recorded, the data in any given block cannot be altered retroactively without alteration of all subsequent blocks, which requires consensus of the network majority. 

**Source:** _en.wikipedia.org_

#### Q2: Explain the common structure of blockchains ⭐⭐
**Answer:**
Blockchains are composed of three core parts:
* **Block**: A list of transactions recorded into a ledger over a given period. The size, period, and triggering event for blocks is different for every blockchain.
* **Chain**: A hash that links one block to another, mathematically “chaining” them together. 
* **Network**: The network is composed of “full nodes.” Think of them as the computer running an algorithm that is securing the network. Each node contains a complete record of all the transactions that were ever recorded in that blockchain.

**Source:** _dummies.com_

#### Q3: What is the blockchain data structure? ⭐⭐
**Answer:**
Basically **the blockchain data structure** is explained as a back-linked record of blocks of transactions, which is ordered. It can be saved as a file or in a plain database. Each block can be recognized by a hash, created utilizing the SHA256 cryptographic hash algorithm on the header of the block. Each block mentions a former block, also identified as the parent block, in the “previous block hash” field, in the block header.

<div class="text-center"/>
<img src="https://vitalflux.com/wp-content/uploads/2018/06/Blockchain-represented-as-Linked-List-Data-Structure.png" class="img-fluid" style="max-width: 500px" />
</div>


**Source:** _cryptoticker.io_

#### Q4: What is the Genesis Block? ⭐⭐
**Answer:**
The **first block in any blockchain **is termed the **genesis block**. If you start at any block and follow the chain backwards chronologically, you will arrive at the genesis block. The genesis block is statically encoded within the client software, that it cannot be changed. Every node can identify the genesis block’s hash and structure, the fixed time of creation, and the single transactions within. Thus every node has a secure “root” from which is possible to build a trusted blockchain on.

**Source:** _linkedin.com_

#### Q5: What is blockchain transaction? ⭐⭐
**Answer:**
**Transactions** are the things that give a blockchain purpose. They are the smallest building blocks of a blockchain system. Transactions generally consist of:
* a recipient address, 
* a sender address, 
* and a value. 

This is not too different from a standard transaction that you would find on a credit card statement.

A transaction _changes the state_ of the agreed-correct blockchain. A blockchain is a shared, decentralized, distributed state machine. This means that all nodes (users of the blockchain system) independently hold their own copy of the blockchain, and the current known "state" is calculated by processing each transaction in order as it appears in the blockchain.

**Source:** _pluralsight.com_

#### Q6: What is the purpose of a blockchain node? ⭐⭐
**Answer:**
A blockchain exists out of blocks of data. These blocks of data are stored on nodes (compare it to small servers). **Nodes** can be any kind of device (mostly computers, laptops or even bigger servers). Nodes form the infrastructure of a blockchain. 

All nodes on a blockchain are connected to each other and they constantly exchange the latest blockchain data with each other so all nodes stay up to date. They store, spread and preserve the blockchain data, so theoretically a blockchain exists on nodes. 

A **full node** is basically a device (like a computer) that contains a full copy of the transaction history of the blockchain.

**Source:** _lisk.io_

#### Q7: Why does Blockchain need coins or tokens? ⭐⭐
**Answer:**
_Tokens/Coins are used as a medium of exchange between the states_. They are digital assets built in to perform a specific function within a blockchain.

When someone does a transaction, there is a _change of state_, and coins are moved from one address to another address. Apart from that, transactions contain some additional data; this data can be mutated through the change of state. For this reason, blockchains need coins or tokens to incentivize the participants to join their networks.

**Source:** _mindmajix.com_

#### Q8: What is proof-of-work? ⭐⭐
**Answer:**
A **proof of work** is a piece of data which is difficult (costly, time-consuming) to produce but easy for others to verify and which satisfies certain requirements. Producing a proof of work can be a random process with low probability so that a lot of trial and error is required on average before a valid proof of work is generated. Difficulty is a measure of how difficult it is to find a hash below a given target.

**Source:** _en.bitcoin.it_

#### Q9: What is deterministic behavior? ⭐⭐
**Answer:**
If A + B = C, then no matter what the circumstances, A+B will always be equal to C. That is called deterministic behavior.

Hash functions are deterministic, meaning A’s hash will always be H(A).

**Source:** _blockgeeks.com_

#### Q10: Explain what do nodes do?  ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q11: Why is the blockchain immutable? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q12: What are the core components of blockchain architecture? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q13: What is mining difficulty? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q14: What is a smart contract? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q15: How Are Blockchain And Distributed Ledger Different? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q16: What are some advantages of using Merke Trees? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q17: Explain why there is a fixed supply of bitcoins? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q18: What is a hashing function? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q19: What is RSA algorithm? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q20: What are the major elements of the blockchain ecosystem? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q21: What is DApp or Decentralised Application? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q22: What is Merkle Trees? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q23: How do verifiers check if a block is valid? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q24: Explain why a blockchain needs tokens to operate ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q25: What is a trapdoor function, and why is it needed in blockchain development? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q26: What is block data structure in blockchain? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q27: What's the difference between distributed hashtable technology and the bitcoin blockchain? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q28: What is a stealth address? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q29: What is nonce? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q30: What Is a Blockchain Consensus Algorithm? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q31: What Is a Proof of Stake? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q32: What is the difference between PoW and PoS? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q33: Explain what is target hash? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q34: What is off-chain transaction? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q35: Name some widespread platforms for developing blockchain applications ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q36: How is hard fork different from the soft fork in blockchain? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q37: What determines the mining difficulty? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q38: What is a 51% attack? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q39: What are miners really solving? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q40: Is it possible to brute force bitcoin address creation in order to steal money? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q41: What can an attacker with 51% of hash power do? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q42: Why is Git not considered a “block chain”? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

## [[⬆]](#toc) <a name=Bootstrap>Bootstrap</a> Interview Questions
#### Q1: Explain Bootstrap? ⭐
**Answer:**
Bootstrap is a platform for web development that is based on front-end framework
and creates exceptional responsive designs. It is fast, easy and has multiple
templates designed using HTML, and CSS. These templates are used for forms,
tables, buttons, typography, modals, tables, navigation, carousels and images.
Bootstrap also has Javascript plugins, which are optional. Bootstrap is
preferred for developing mobile web applications.

**Source:** _medium.com/@onlineinerview_

#### Q2: Explain what is Bootstrap? ⭐
**Answer:**
Bootstrap is CSS/Javascript framework for building the rich web applications with
minimal effort. This framework emphasis more on building mobile web
applications.

**Source:** _medium.com/@alisonbenhar_

#### Q3: Explain the two codes that are used for code display in Bootstrap? ⭐⭐
**Answer:**
There are two simple ways to display a code in Bootstrap:

* `<code>` tag: In case you wish to display an inline code
* `<pre>` tag: In case you have a code with several lines or even a block element

**Source:** _medium.com/@onlineinerview_

#### Q4: What are the types of layout available in Bootstrap? ⭐⭐
**Answer:**
In Bootstrap there are two types of Layout available

* Fluid Layout: Fluid layout is used when you want to create a app that is 100%
wide and use up all the width of the screen
* Fixed Layout: For a standard screen you will use fixed layout (940 px) option

**Source:** _medium.com/@alisonbenhar_

#### Q5: What will be the output of the following HTML code ⭐⭐
**Answer:**
**Consider:**
```js
<ul class="list-unstyled">
  <li>Item 1</li>
  <li>Item 2</li>
    <ul>
      <li>Nested item 2.1</li>
      <li>Nested item 2.2</li>
      <li>Nested item 2.3</li>
    </ul>     
  <li>Item 3</li>
</ul>
```
What will be the output of the following HTML code?

**Answer:**

If we apply `.list-unstyled` to a list, it will remove the default list-style and left margin on the list items. But *only* for the immediate children. Main list items will be without any style, and nested list items will still have default unordered nested list-style.

**Source:** _toptal.com_

#### Q6: Explain why you prefer Bootstrap for website development? ⭐⭐
**Answer:**
Bootstrap has features that are way better than other web development platforms.
It provides an extensive browser support for almost every known browser such as
Opera, Chrome, Firefox, Safari etc. With adequate knowledge of CSS and HTML, web
development becomes easy on Bootstrap. Also, it supports mobile applications
with the help of responsive design. It can adjust CSS as per the device, screen
size etc. Instead of creating multiple files, it creates only a single file,
which reduces any extra effort by the developer.

**Source:** _medium.com/@onlineinerview_

#### Q7: What are the key components of Bootstrap? ⭐⭐
**Answer:**
In total, there are five key components of Bootstrap i.e. **CSS** (multiple CSS
files), **Scaffolding (**essential for the basic system that consist of Grid
system, background and link styles), **Layout Components:** (shares a list of
all layouts), **JavaScript Plugins** (includes jQuery and JavaScript plugins)
and **Customization **(Allows customization of all components for a desired
framework)

**Source:** _medium.com/@onlineinerview_

#### Q8: How many types of layout are available in Bootstrap? ⭐⭐
**Answer:**
There are two major layouts for Bootstrap i.e. Fluid Layout and Fixed Layout.
Fluid layout is necessary for creating an app that is 100 % wider and covers all
the screen width. Fixed Layout is used only for a standard screen (940px). Both
layouts can be used for creating a responsive design.

**Source:** _medium.com/@onlineinerview_

#### Q9: Why do we use Jumbotron in Bootstrap? ⭐⭐
**Answer:**
*Jumbotron* has a very basic function in bootstrap i.e. highlighting a content. It
could either be a slogan/uvp (unique value proposition) or probably a headline. It increases the heading size
and gives a margin for content of the landing page. In order to implement
Jumbotron in a Bootstrap use:

```html
 <div class=”jumbotron”>
```

Jumbotron can have any valid HTML along with other functions and classes.

**Source:** _medium.com/@onlineinerview_

#### Q10: What is Twitter Bootstrap? ⭐⭐
**Answer:**
Bootstrap is a sleek, intuitive, and powerful mobile first front-end framework
for faster and easier web development. It uses HTML, CSS and Javascript.

**Source:** _medium.com/@alisonbenhar_

#### Q11: Explain why to choose Bootstrap for building the websites? ⭐⭐
**Answer:**
There are few reason why we choose Bootstrap for building websites

* Mobile Support: For mobile devices it provides full support in one single file
rather than in separate file. It supports the responsive design including
adjusting the CSS based on the different types of device, size of the screen
etc. It reduces extra effort for developers.
* Easy to learn: Writing application in bootstrap is easy if you know CSS and HTML
* Browser Support: It supports all the popular browsers like Firefox, Opera,
Safari, IE etc.

**Source:** _medium.com/@alisonbenhar_

#### Q12: What global styles are applied as a part of Bootstrap’s default typography? ⭐⭐
**Answer:**
Bootstrap sets the global default font-size to `14px`, with a line-height of `1.428`. The default font is changed to `Helvetica` and `Arial` with `sans serif` fallback. 

All these styles are applied to the `<body>` and all paragraphs, with the addition that `<p>` (paragraphs) receive a bottom margin of half their computed line-height, which is `10px` by default.

**Source:** _toptal.com_

#### Q13: What is the procedure to create Nav elements in Bootstrap? ⭐⭐
**Answer:**
There are several styling navigation elements available on bootstrap and every
style uses the same function i.e. class `.nav`. In order to create tabs or a
tabular navigation, you can begin with a simple or rather basic unordered list
using the function class `.nav`. To add the tabs the function class `.nav-tabs` can
be used.

**Source:** _medium.com/@onlineinerview_

#### Q14:  What are Glyphicons? ⭐⭐
**Answer:**
Glyphicons are icon fonts which you can use in your web projects. Glyphicons
Halflings are not free and require licensing, however their creator has made
them available for Bootstrap projects free of cost.

To use the icons, simply use the following code just about anywhere in your
code. Leave a space between the icon and text for proper padding.

```html
<span class="glyphicon glyphicon-search"></span>
```

**Source:** _medium.com/@alisonbenhar_

#### Q15: When to use "lead" in Bootstrap? ⭐⭐
**Answer:**
To add some emphasis to a paragraph, add class `.lead`. This will give you
larger font size, lighter weight, and a taller line height.

**Source:** _medium.com/@alisonbenhar_

#### Q16: Explain the typography and links in Bootstrap. ⭐⭐
**Answer:**
Bootstrap sets a basic global display (background), typography, and link styles:

* **Basic Global display** − sets *background-color: #fff;* on the *<body>*
* **Typography** − uses the *@font-family-base*, *@font-size-base*,
and *@line-height-base* attributes as the typographic base
* **Link styles** − sets the global link color via attribute *@link-color* and
apply link underlines only on *:hover*.

**Source:** _medium.com/@alisonbenhar_

#### Q17: How do you make images responsive? ⭐⭐
**Answer:**
Bootstrap 3 allows to make the images responsive by adding a class
`.img-responsive` to the `<img>` tag. This class applies `max-width: 100%;` and
`height: auto;` to the image so that it scales nicely to the parent element.

**Source:** _medium.com/@alisonbenhar_

#### Q18: What is missing for a tooltip to show properly? ⭐⭐
**Answer:**
Consider:
```html
<button type="button" class="btn btn-default" data-toggle="tooltip" data-placement="top" title="Example tooltip">Hover over me</button>
```
What is missing for a tooltip to show properly?

**Answer**

Bootstrap’s Tooltip plugin is not CSS-only, like other plugins are. For performance reasons, the Tooltip plugin is opt-in, and to use it you must initialize it using JavaScript with the following example code:
```js
$(function () {
  $('[data-toggle="tooltip"]').tooltip();
});
```

**Source:** _medium.com/@alisonbenhar_

#### Q19: What do you mean by Bootstrap collapsing elements? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q20: What is a list group in Bootstrap and where does it finds its application? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q21: Explain Modal plugin in Bootstrap? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q22: What is a Bootstrap Container? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q23: Why do we use Bootstrap Carousel plugin? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q24: What is the role of media object in Bootstrap and how many types are available? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q25: What are the key components of Bootstrap? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q26: What is the step-wise procedure for creating basic or vertical forms? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q27: What do you mean by Bootstrap "well"? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q28: What is the difference between the following two lines of code? Explain your answer. ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q29: What will be the default Bootstrap look of the alert created with this following code? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q30: Explain what the following code does, and where they are useful ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q31: What is the role of pagination in bootstrap and what are their classifications? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q32: What is Normalize in Bootstrap? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q33: Consider the HTML code snippet below. What will the output be, and why? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q34: Explain column ordering in Bootstrap? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q35: What is screen reader in bootstrap documentation? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q36: How can you differentiate between Bootstrap and Foundation? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q37: How many different media queries are used by the Bootstrap grid system by default? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q38: What is the class sr-only used for? Is it important or can I remove it? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

## [[⬆]](#toc) <a name=C#>C#</a> Interview Questions
#### Q1: What is C#? ⭐
**Answer:**
C# is the programming language for writing Microsoft .NET applications. C# provides the rapid application development found in Visual Basic with the power of C++. Its syntax is similar to C++ syntax and meets 100% of the requirements of OOPs like the following: 
* Abstraction
* Encapsulation
* Polymorphism
* Inheritance

**Source:** _c-sharpcorner.com_

#### Q2: What is the difference between "continue" and "break" statements in C#? ⭐
**Answer:**
* using **break** statement, you can jump out of a loop
* using **continue** statement, you can jump over one iteration and then resume your loop execution

**Source:** _c-sharpcorner.com_

#### Q3: What are property Accessors? ⭐
**Answer:**
The _get_ and _set_ portions or blocks of a property are called accessors. These are useful to restrict the accessibility of a property, the set accessor specifies that we can assign a value to a private field in a property and without the set accessor property it is like a read-only field. By the get accessor we can access the value of the private field, in other words it returns a single value. A Get accessor specifies that we can access the value of a field publically.

**Source:** _c-sharpcorner.com_

#### Q4: What is an Object? ⭐
**Answer:**
According to MSDN, "_a class or struct definition is like a blueprint that specifies what the type can do. An object is basically a block of memory that has been allocated and configured according to the blueprint. A program may create many objects of the same class. Objects are also called instances, and they can be stored in either a named variable or in an array or collection. Client code is the code that uses these variables to call the methods and access the public properties of the object. In an object-oriented language such as C#, a typical program consists of multiple objects interacting dynamically"._

Objects helps us to access the member of a class or struct either they can be fields, methods or properties, by using the dot. 

**Source:** _c-sharpcorner.com_

#### Q5: What is enum in C#? ⭐⭐
**Answer:**
An **enum** is a value type with a set of related named constants often referred to as an enumerator list. The enum keyword is used to declare an enumeration. It is a primitive data type, which is user defined. An enum is used to create numeric constants in .NET framework. All the members of enum are of enum type. Their must be a numeric value for each enum type.

**Some points about enum**

* Enums are enumerated data type in C#.  
* Enums are strongly typed constant. They are strongly typed, i.e. an enum of one type may not be implicitly assigned to an enum of another type even though the underlying value of their members are the same.  
* Enumerations (enums) make your code much more readable and understandable.  
* Enum values are fixed. Enum can be displayed as a string and processed as an integer.  
* The default type is int, and the approved types are byte, sbyte, short, ushort, uint, long, and ulong.  
* Every enum type automatically derives from System.Enum and thus we can use System.Enum methods on enums.  
* Enums are value types and are created on the stack and not on the heap.

**Source:** _c-sharpcorner.com_

#### Q6: How is Exception Handling implemented in C#? ⭐⭐
**Answer:**
Exception handling is done using four keywords in C#:

*   **try** – Contains a block of code for which an exception will be checked.
*   **catch** – It is a program that catches an exception with the help of exception handler.
*   **finally** – It is a block of code written to execute regardless whether an exception is caught or not.
*   **Throw** – Throws an exception when a problem occurs.

**Source:** _softwaretestinghelp.com_

#### Q7: Can "this" be used within a static method? ⭐⭐
**Answer:**
We can't use _this_ in static method because keyword _this_ returns a reference to the current instance of the class containing it. Static methods (or any static member) do not belong to a particular instance. They exist without creating an instance of the class and call with the name of a class not by instance so we can't use this keyword in the body of static Methods, but in case of Extension Methods we can use it as the functions parameters.

**Source:** _c-sharpcorner.com_

#### Q8: Define Property in C#? ⭐⭐
**Answer:**
**Properties** are members that provide a flexible mechanism to read, write or compute the values of private fields, in other words by the property we can access private fields. In other words we can say that a property is a return type function/method with one parameter or without a parameter. These are always public data members. It uses methods to access and assign values to private fields called accessors.

**Source:** _c-sharpcorner.com_

#### Q9: What is Boxing and Unboxing? ⭐⭐
**Answer:**
Boxing and Unboxing both are used for type conversion but have some difference:

* **Boxing** - Boxing is the process of converting a value type data type to the object or to any interface data type which is implemented by this value type. When the CLR boxes a value means when CLR is converting a value type to Object Type, it wraps the value inside a System.Object and stores it on the heap area in application domain.

* **Unboxing** - Unboxing is also a process which is used to extract the value type from the object or any implemented interface type. Boxing may be done implicitly, but unboxing have to be explicit by code. 

The concept of boxing and unboxing underlines the C# unified view of the type system in which a value of any type can be treated as an object.

**Source:** _c-sharpcorner.com_

#### Q10: What is the difference between string and StringBuilder in c#? ⭐⭐
**Answer:**
**String**
* It's an immutable object that hold string value.
* Performance wise string is slow because its' create a new instance to override or change the previous value.
* String belongs to System namespace.

**StringBuilder**
* StringBuilder is a mutable object.  
* Performance wise StringBuilder is very fast because it will use same instance of StringBuilder object to perform any operation like insert value in existing string.  
* StringBuilder belongs to System.Text.Stringbuilder namespace.

**Source:** _c-sharpcorner.com_

#### Q11: What are partial classes? ⭐⭐
**Answer:**
A **partial** class is only use to splits the definition of a class in two or more classes in a same source code file or more than one source files. You can create a class definition in multiple files but it will be compiled as one class at run time and also when you'll create an instance of this class so you can access all the methods from all source file with a same object. Partial classes can be create in the same namespace it's doesn't allowed to create a partial class in different namespace. 

**Source:** _c-sharpcorner.com_

#### Q12: Filter out the first 3 even numbers from the list using LINQ ⭐⭐
**Answer:**
```csharp
var evenNumbers = List
   .Where(x => x % 2 ==0)
   .Take(3)
```

**Source:** _medium.com/_

#### Q13: Why to use “finally” block in C#? ⭐⭐
**Answer:**
**Finally** block will be executed irrespective of exception. So while executing the code in try block when exception is occurred, control is returned to catch block and at last `finally` block will be executed. So closing connection to database / releasing the file handlers can be kept in `finally` block.

**Source:** _a4academics.com_

#### Q14: What are nullable types in C#? ⭐⭐
**Answer:**
C# provides a special data types, the **nullable types**, to which you can assign normal range of values as well as null values.

For example, you can store any value from -2,147,483,648 to 2,147,483,647 or null in a `Nullable<Int32>` variable. Similarly, you can assign true, false, or null in a `Nullable<bool>` variable.

**Source:** _tutorialspoint.com_

#### Q15: What are generics in C#? ⭐⭐
**Answer:**
**Generics** allow you to delay the specification of the data type of programming elements in a class or a method, until it is actually used in the program. In other words, generics allow you to write a class or method that can work with any data type.

**Source:** _c-sharpcorner.com_

#### Q16: What is Managed or Unmanaged Code? ⭐⭐
**Answer:**
* **Managed Code**  - The code, which is developed in .NET framework is known as managed code. This code is directly executed by CLR with the help of managed code execution. Any language that is written in .NET Framework is managed code.
* **Unmanaged Code** - The code, which is developed outside .NET framework is known as unmanaged code. Applications that do not run under the control of the CLR are said to be unmanaged, and certain languages such as C++ can be used to write such applications, which, for example, access low - level functions of the operating system. Background compatibility with the code of VB, ASP and COM are examples of unmanaged code.


**Source:** _c-sharpcorner.com_

#### Q17: What are reference types in C#? ⭐⭐
**Answer:**
The **reference types** do not contain the actual data stored in a variable, but they contain a reference to the variables.

In other words, they refer to a memory location. Using multiple variables, the reference types can refer to a memory location. If the data in the memory location is changed by one of the variables, the other variable automatically reflects this change in value. Example of built-in reference types are: object, dynamic, and string.

**Source:** _tutorialspoint.com_

#### Q18: What you understand by Value types and Reference types in C#.Net? ⭐⭐
**Answer:**
In C# data types can be of two types: **Value Types** and **Reference Types**. Value type variables contain their object (or data) directly. If we copy one value type variable to another then we are actually making a copy of the object for the second variable. Value Type member will located into Stack and reference member will located in Heap always.  

**Source:** _stackoverflow.com_

#### Q19: What is namespace in C#? ⭐⭐
**Answer:**
A **namespace** is designed for providing a way to keep one set of names separate from another. The class names declared in one namespace does not conflict with the same class names declared in another.

**Source:** _tutorialspoint.com_

#### Q20: What is Serialization? ⭐⭐
**Answer:**
**Serialization** means saving the state of your object to secondary memory, such as a file.

1.  Binary serialization (Save your object data into binary format).  
2.  Soap Serialization (Save your object data into binary format; mainly used in network related communication).  
3.  XmlSerialization (Save your object data into an XML file).

**Source:** _c-sharpcorner.com_

#### Q21: In how many ways you can pass parameters to a method? ⭐⭐
**Answer:**
There are three ways that parameters can be passed to a method:

*   **Value parameters** − This method copies the actual value of an argument into the formal parameter of the function. In this case, changes made to the parameter inside the function have no effect on the argument.
*   **Reference parameters** − This method copies the reference to the memory location of an argument into the formal parameter. This means that changes made to the parameter affect the argument.
*   **Output parameters** − This method helps in returning more than one value.

**Source:** _tutorialspoint.com_

#### Q22: Can you return multiple values from a function in C#? ⭐⭐
**Answer:**
Yes! Using output parameters. A return statement can be used for returning only one value from a function. However, using output parameters, you can return two values from a function.

**Source:** _tutorialspoint.com_

#### Q23: What is LINQ in C#? ⭐⭐
**Answer:**
**LINQ** stands for Language Integrated Query. LINQ has a great power of querying on any source of data. The data source could be collections of objects, database or XML files. We can easily retrieve data from any object that implements the `IEnumerable<T>` interface. 

**Source:** _c-sharpcorner.com_

#### Q24: Can multiple catch blocks be executed? ⭐⭐
**Answer:**
No, Multiple catch blocks can't be executed. Once the proper catch code executed, the control is transferred to the finally block and then the code that follows the finally block gets executed.

**Source:** _guru99.com_

#### Q25: What is an Abstract Class? ⭐⭐
**Answer:**
An **Abstract class** is a class which is denoted by abstract keyword and can be used only as a Base class. An Abstract class should always be inherited. An instance of the class itself cannot be created. If we do not want any program to create an object of a class, then such classes can be made abstract.

Any method in the abstract class does not have implementations in the same class. But they must be implemented in the child class.

**Source:** _softwaretestinghelp.com_

#### Q26: What are Custom Exceptions? ⭐⭐
**Answer:**
Sometimes there are some errors that need to be handeled as per user requirements. Custom exceptions are used for them and are used defined exceptions.

**Source:** _guru99.com_

#### Q27: What is the difference between a struct and a class in C#? ⭐⭐
**Answer:**
Class and struct both are the user defined data type but have some major difference:  
**  
Struct**

* The struct is value type in C# and it inherits from System.Value Type.
* Struct is usually used for smaller amounts of data.
* Struct can't be inherited to other type.
* A structure can't be abstract.
* No need to create object by new keyword.
* Do not have permission to create any default constructor.

**Class**

* The class is reference type in C# and it inherits from the System.Object Type.
* Classes are usually used for large amounts of data.
* Classes can be inherited to other class.
* A class can be abstract type.
* We can't use an object of a class with using new keyword.
* We can create a default constructor.

**Source:** _c-sharpcorner.com_

#### Q28: Why can't you specify the accessibility modifier for methods inside the interface? ⭐⭐
**Answer:**
In an interface, we have virtual methods that do not have method definition. All the methods are there to be overridden in the derived class. That's why they all are public.

**Source:** _guru99.com_

#### Q29: What are the different types of classes in C#? ⭐⭐
**Answer:**
The different types of class in C# are:

*   **Partial class** – Allows its members to be divided or shared with multiple .cs files. It is denoted by the keyword _Partial._
*   **Sealed class** – It is a class which cannot be inherited. To access the members of a sealed class, we need to create the object of the class.  It is denoted by the keyword _Sealed_.
*   **Abstract class** – It is a class whose object cannot be instantiated. The class can only be inherited. It should contain at least one method.  It is denoted by the keyword _abstract._
*   **Static class** – It is a class which does not allow inheritance. The members of the class are also static.  It is denoted by the keyword _static_. This keyword tells the compiler to check for any accidental instances of the static class.

**Source:** _softwaretestinghelp.com_

#### Q30: What are dynamic type variables in C#? ⭐⭐
**Answer:**
You can store any type of value in the dynamic data type variable. Type checking for these types of variables takes place at run-time.

**Source:** _tutorialspoint.com_

#### Q31: What is the difference between Equality Operator (==) and Equals() Method in C#? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q32: How encapsulation is implemented in C#? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q33: What is the difference between dynamic type variables and object type variables? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q34:  What is extension method in C# and how to use them? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q35: What is lambda expressions in C#? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q36: What is Virtual Method in C#? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q37: What is the difference between ref and out keywords? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q38: What is delegates in C# and uses of delegates? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q39: What is sealed class in C#? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q40: What is an anonymous function in C#? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q41: What are the uses of “using” in C# ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q42: What is the difference between overloading and overriding? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q43: What is a Destructor in C#? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q44: Explain Anonymous type in C# ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q45: Refactor the code ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q46: What is Reflection in C#.Net? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q47: What is the output of the program below? Explain your answer. ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q48: What is difference between constants and readonly? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q49: Given an array of ints, write a C# method to total all the values that are even numbers. ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q50: What is the difference between Interface and Abstract Class? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q51: What is difference between Throw Exception and Throw Clause? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q52: What is the use of Null Coalescing Operator (??) in C#? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q53: What is the difference between constant and readonly in c#? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q54: Explain Code compilation in C# ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q55: What is the difference between Virtual method and Abstract method? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q56: What is scope of a Internal member variable of a C# class? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q57: Can Multiple Inheritance implemented in C# ? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q58: What are the different ways a method can be overloaded? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q59: Describe the accessibility modifier "protected internal". ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q60: What are the differences between a multidimensional array and an array of arrays in C#? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q61: Explain what is short-circuit evaluation in C# ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q62: Explain the difference between Select and Where ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q63: When to use ArrayList over array[] in c#? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q64: What is an Object Pool in .Net? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q65: Name difference between "is" and "as" operator in C# ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q66: What is the difference between Func<string,string> and delegate? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q67: What are pointer types in C#? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q68: What is marshalling and why do we need it? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q69: What is the difference between dispose and finalize methods in c#? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q70: What is scope of a Protected Internal member variable of a C# class? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q71: IEnumerable vs List - What to Use? How do they work? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q72: What is Indexer in C#? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q73: Can you create a function in C# which can accept varying number of arguments? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q74: Is operator overloading supported in C#? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q75: What interface should your data structure implement to make the "Where" method work? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q76: What is the use of conditional preprocessor directive in C#? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q77: What is the difference between System.ApplicationException class and System.SystemException class? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q78: What is difference between late binding and early binding in C#? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q79: Can we have only “try” block without “catch” block in C#? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q80: In try block if we add return statement whether finally block is executed in C#? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q81: What's the difference between StackOverflowError and OutOfMemoryError? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q82: What are the uses of delegates in C#? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q83: Why to use lock statement in C#? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q84: What is the "yield" keyword used for in C#? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q85: What is the output of the program below? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q86: What is the Constructor Chaining in C#? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q87: What is the output of the short program below? Explain your answer. ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q88: Is the comparison of time and null in the if statement below valid or not? Why or why not? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q89: What is the output of the program below? Explain your answer. ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q90: What is the best practice to have best performance using Lazy<T> objects?  ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q91: Calculate the circumference of the circle ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q92: Could you explain the difference between destructor, dispose and finalize method? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q93: What are the differences between IEnumerable and IQueryable? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q94: What is the use of static constructors? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q95: What's the difference between the System.Array.CopyTo() and System.Array.Clone()? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q96: What is a preprocessor directives in C#? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q97: What is multicast delegate in C#? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q98: What are the benefits of a Deferred Execution in LINQ? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q99: What is the method MemberwiseClone() doing? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q100: List some different ways for equality check in .Net ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q101: What is deep or shallow copy concept in C#? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q102: Can you create sealed abstract class in C#? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q103: Could you explain the difference between Func vs. Action vs. Predicate? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q104: What are circular references? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q105: Explain the difference between IQueryable, ICollection, IList & IDictionary interfaces? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q106:  in C#, when should we use abstract classes instead of interfaces with extension methods? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q107: Can you add extension methods to an existing static class? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q108: Implement the "Where" method in C# ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q109: What is the “volatile” keyword used for? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q110: What is jagged array in C#.Net and when to prefer jagged arrays over multi-dimensional arrays? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q111: Explain what is weak reference in C#? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q112: What is the difference between lambdas and delegates? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

## [[⬆]](#toc) <a name=CSS>CSS</a> Interview Questions
#### Q1: Explain the three main ways to apply CSS styles to a web page ⭐
**Answer:**
Using the inline style attribute on an element
```html
<div>
    <p style="color: maroon;"></p>
</div>
```
Using a `<style>` block in the `<head>` section of your HTML
```html
<head>
    <title>CSS Refresher</title>
    <style>
        body {
            font-family: sans-serif;
            font-size: 1.2em;
        }
    </style>
</head>
```
Loading an external CSS file using the `<link>` tag
```html
<head>
    <title>CSS Refresher</title>
    <link rel="stylesheet" href="/css/styles.css" />
</head>
```

**Source:** _goskills.com_

#### Q2: What is CSS? ⭐
**Answer:**
**CSS** stands for **Cascading Style Sheets**. CSS is used to define styles for your web pages, including the design, layout and variations in display for different devices and screen sizes.

CSS was intended to allow web professionals to separate the content and structure of a website's code from the visual design.

**Source:** _w3schools.com_

#### Q3: How to use variables in Sass? ⭐
**Answer:**
Think of variables as a way to store information that you want to reuse throughout your stylesheet. You can store things like colors, font stacks, or any CSS value you think you'll want to reuse. Sass uses the `$` symbol to make something a variable.

```css
$font-stack:    Helvetica, sans-serif;
$primary-color: #333;

body {
  font: 100% $font-stack;
  color: $primary-color;
}
```


**Source:** _sass-lang.com_

#### Q4: What is variable interpolation in Sass? Provide some examples.  ⭐⭐
**Answer:**
 If you want to use variables inside a string, you will have to use a process called **variable interpolation**. To use it you will have to wrap your variables in `#{}`. 

Consider:
```css
$name: 'Gajendar';
$author: 'Author : $name'; // 'Author : $name'

$author: 'Author : #{$name}';
// 'Author : Gajendar'
```

The interpolation method could be useful in situations where the value of a variable is determined by some conditional statements. 

**Source:** _sitepoint.com_

#### Q5: What is a CSS rule? ⭐⭐
**Answer:**
Web browsers apply **CSS rules** to a document to affect how they are displayed. A CSS rule is formed from:

* A **set of properties**, which have values set to update how the HTML content is displayed,
* A **selector**, which selects the element(s) you want to apply the updated property values to.

A set of CSS rules contained within a stylesheet determines how a webpage should look. 

**Source:** _developer.mozilla.org_

#### Q6: What is DOM (Document Object Model) and how is it linked to CSS? ⭐⭐
**Answer:**
The *Document Object Model (DOM)* is a cross-platform and language-independent *application programming interface* that treats an HTML, XHTML, or XML document as a tree structure wherein each node is an object representing a part of the document. 

With the Document Object Model, programmers can create and build documents, navigate their structure, and add, modify, or delete elements and content. The DOM specifies interfaces which may be used to manage XML or HTML documents. 

When a browser displays a document, it must combine the document's content with its style information. The browser converts HTML and CSS into the DOM (Document Object Model). The DOM represents the document in the computer's memory. It combines the document's content with its style.

**Source:** _en.wikipedia.org_

#### Q7: Have you played around with the new CSS Flexbox or Grid specs? ⭐⭐
**Answer:**
Yes. Flexbox is mainly meant for 1-dimensional layouts while Grid is meant for 2-dimensional layouts.

Flexbox solves many common problems in CSS, such as vertical centering of elements within a container, sticky footer, etc. Bootstrap and Bulma are based on Flexbox, and it is probably the recommended way to create layouts these days. Have tried Flexbox before but ran into some browser incompatibility issues (Safari) in using `flex-grow`, and I had to rewrite my code using `inline-blocks` and math to calculate the widths in percentages, it wasn't a nice experience.

Grid is by far the most intuitive approach for creating grid-based layouts (it better be!) but browser support is not wide at the moment.

**Source:** _codeburst.io_

#### Q8: What is Sass? ⭐⭐
**Answer:**
**Sass** or **Syntactically Awesome StyleSheets** is a *CSS* preprocessor that adds power and elegance to the basic language. It allows you to use variables, nested rules, mixins, inline imports, and more, all with a fully CSS-compatible syntax. Sass helps keep large stylesheets well-organized, and get small stylesheets up and running quickly.

A *CSS preprocessor* is a scripting language that extends CSS by allowing developers to write code in one language and then compile it into CSS. 


**Source:** _sass-lang.com_

#### Q9: List out the key features for Sass? ⭐⭐
**Answer:**
Key features for Sass include

* Full CSS3-compatible
* Language extensions such as nesting, variables, and mixins
* Many useful functions for manipulating colors and other values
* Advanced features like control directives for libraries
* Well-formatted, customizable output

**Source:** _career.guru99.com_

#### Q10: What existing CSS frameworks have you used locally, or in production? How would you change/improve them? ⭐⭐
**Answer:**
* **Bootstrap** - Slow release cycle. Bootstrap 4 has been in alpha for almost 2 years. Add a spinner button component, as it is widely used.
* **Semantic UI** - Source code structure makes theme customization extremely hard to understand. Its unconventional theming system is a pain to customize. Hardcoded config path within the vendor library. Not well-designed for overriding variables unlike in Bootstrap.
* **Bulma** - A lot of non-semantic and superfluous classes and markup required. Not backward compatible. Upgrading versions breaks the app in subtle manners.

**Source:** _codeburst.io_

#### Q11: List out the data types that Sass supports ⭐⭐
**Answer:**
Sass supports seven main data types:

* **Numbers** - most of the time they are accompanied by a unit of some sort but they are still technically numbers. You can perform basic mathematical operations on these values.

```css
$size: 18;                  // A number
$px-unit: $size * 1px;      // A pixel measurement
$px-string: $size + px;     // A string
$px-number: $px-unit / 1px; // A number
```
* **Strings** - just like CSS, accepts both quoted and unquoted strings, even if they contain spaces

```css
$website: 'SitePoint'; // Stores SitePoint
$name: 'Gajendar' + ' Singh';  // 'Gajendar Singh'
$date:  'Month/Year : ' + 3/2016; // 'Month/Year : 3/2016'
$date:  'Month/Year : ' + (3/2016); // 'Month/Year : 0.00149' 
// This is because 3/2016 is evaluated first.
$variable: 3/2016;      // Evaluated to 0.00149
```
* **Colors** - CSS color expressions come under the `color` data type. You can refer to the colors in hexadecimal notation, as `rgb`, `rgba`, `hsl` and `hsla` values or use native keywords like `pink`, `blue`, etc. 

```css
$color: yellowgreen;           // #9ACD32
color: lighten($color, 15%);    // #b8dc70
color: darken($color, 15%);     // #6c9023
color: saturate($color, 15%);   // #a1e01f
color: desaturate($color, 15%); // #93ba45
color: (green + red);           // #ff8000
```
* **Booleans** - has only two possible values: `true` and `false`

```css
$i-am-true: true;

body {
  @if not $i-am-true {
    background: rgba(255, 0, 0, 0.6);
  } @else {
    background: rgba(0, 0, 255, 0.6); // expected
  }
}
```

* **Null** -  is commonly used to define an empty state, neither `true` or `false`. This is typically the value you want to set when defining a variable without a value, only to prevent the parser from crashing.

```css
.foo {
  content: type-of(null); // null
  content: type-of(NULL); // string
  $bar: 'foo' + null; // invalid null operation: "foo plus null”.
}
```

* **Lists** - are just the Sass version of arrays. You can store multiple types of values in a list.

```css
$font-list: 'Raleway','Dosis','Lato'; // Three comma separated elements
$pad-list: 10px 8px 12px; // Three space separated elements
$multi-list: 'Roboto',15px 1.3em; // This multi-list has two lists.
```
* **Maps** -  Sass maps are like associative arrays. A map stores both keys and values associated with those keys.

```css
$styling: (
  'font-family': 'Lato',
  'font-size': 1.5em,
  'color': tomato,
  'background': black
);

h1 {
  color: map-get($styling, 'color');
  background: map-get($styling, 'background');
}
```

**Source:** _career.guru99.com_

#### Q12: Explain CSS sprites, and how you would implement them on a page or site. ⭐⭐
**Answer:**
*CSS sprites* combine multiple images into one single larger image. It is commonly used technique for icons (Gmail uses it). 

* Use a sprite generator that packs multiple images into one and generate the appropriate CSS for it.
* Each image would have a corresponding CSS class with `background-image`, `background-position` and `background-size` properties defined.
* To use that image, add the corresponding class to your element.

**Advantages**:

* Reduce the number of HTTP requests for multiple images (only one single request is required per spritesheet). But with HTTP2, loading multiple images is no longer much of an issue.
* Advance downloading of assets that won’t be downloaded until needed, such as images that only appear upon `:hover` pseudo-states. Blinking wouldn't be seen.

**Source:** _codeburst.io_

#### Q13: What Selector Nesting in Sass is used for? ⭐⭐
**Answer:**
Sass *let you nest* your CSS selectors in a way that follows the same visual hierarchy of your HTML.  CSS, on the other hand, doesn't have any visual hierarchy.

Consider example (scss):
```css
.parent {
  color: red;

  .child {
    color: blue;
  }
}
```
Result (css):
```css
.parent {
  color: red;
}

.parent .child {
  color: blue;
}
```


**Source:** _sass-lang.com_

#### Q14: Explain what is a @extend directive used for in Sass? ⭐⭐
**Answer:**
Using `@extend` lets you share a set of CSS properties from one selector to another. It helps keep your Sass very dry.

Consider:
```css
%message-shared {
  border: 1px solid #ccc;
  padding: 10px;
  color: #333;
}

.message {
  @extend %message-shared;
}

.success {
  @extend %message-shared;
  border-color: green;
}

.error {
  @extend %message-shared;
  border-color: red;
}

.warning {
  @extend %message-shared;
  border-color: yellow;
}
```
CSS output:
```css
.message, .success, .error, .warning {
  border: 1px solid #cccccc;
  padding: 10px;
  color: #333;
}

.success {
  border-color: green;
}

.error {
  border-color: red;
}

.warning {
  border-color: yellow;
}
```

 

**Source:** _career.guru99.comsass-lang.com_

#### Q15: Explain the CSS “box model” and the layout components that it consists of ⭐⭐
**Answer:**
The CSS box model is a rectangular layout paradigm for HTML elements that consists of the following:

* **Content** - The content of the box, where text and images appear
* **Padding** - A transparent area surrounding the content (i.e., the amount of space between the border and the content)
* **Border** - A border surrounding the padding (if any) and content
* **Margin** - A transparent area surrounding the border (i.e., the amount of space between the border and any neighboring elements)

**Source:** _toptal.com_

#### Q16: What is the difference between classes and IDs in CSS? ⭐⭐
**Answer:**
* **IDs** — Meant to be unique within the document. Can be used to identify an element when linking using a fragment identifier. Elements can only have one id attribute.

* **Classes** — Can be reused on multiple elements within the document. Mainly for styling and targeting elements.

**Source:** _codeburst.io_

#### Q17: Describe floats and how they work ⭐⭐
**Answer:**
*Float* is a CSS positioning property. Floated elements remain a part of the flow of the web page. This is distinctly different than page elements that use absolute positioning. Absolutely positioned page elements are removed from the flow of the webpage.

```css
#sidebar {
  float: right; // left right none inherit			
}
```
The CSS clear property can be used to be positioned below `left`/`right`/`both` floated elements.

**Source:** _css-tricks.com_

#### Q18: Explain the usage of "table-layout" property ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q19: How to create a zebra striped table with CSS? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q20: Have you ever worked with retina graphics? If so, when and what techniques did you use? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q21: What is a Mixin and how to use on? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q22: How is responsive design different from adaptive design? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q23: Explain your understanding of the box model and how you would tell the browser in CSS to render your layout in different box models. ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q24: What's the difference between SCSS and Sass? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q25: Describe pseudo-elements and discuss what they are used for. ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q26: How does CSS actually work (under the hood of browser)? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q27: What is CSS selectors? Name some. ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q28: What’s the difference between “resetting” and “normalizing” CSS? Which would you choose, and why? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q29: What's the difference between a `relative`, `fixed`, `absolute` and `static`ally positioned element? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q30: What are the advantages/disadvantages of using CSS preprocessors? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q31: What is CSS preprocessor and why to user one? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q32: How would you approach fixing browser-specific styling issues? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q33: What is a Grid System in CSS? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q34: What does Accessibility (a11y) mean? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q35: What does * { box-sizing: border-box; } do? What are its advantages? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q36: Have you ever used a grid system, and if so, what do you prefer? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q37: Explain the purpose of clearing floats in CSS ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q38: Can you explain the difference between coding a website to be responsive versus using a mobile-first strategy? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q39: How do you optimize your webpages for print? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q40: Describe z-index and how a stacking context is formed ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q41: Explain the basic rules of CSS Specificity ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q42: What is the '@content' directive used for? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q43: What are the different ways to visually hide content (and make it available only for screen readers)? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q44: What will be the CSS output for the following Sass code? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q45: Is there any reason you'd want to use `translate()` instead of `absolute` positioning, or vice-versa? And why? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q46: What the code fragment has the greater CSS specificity?  ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q47: What’s wrong with Sass nesting? Provide some example. ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q48: What clearfix methods do you know? Provide some examples. ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q49: How to style every element which has an adjacent item right before it? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q50: Write down a selector that will match any links end in .zip, .ZIP, .Zip etc... ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

## [[⬆]](#toc) <a name=Career>Career</a> Interview Questions
#### Q1: career test ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

## [[⬆]](#toc) <a name=Clojure>Clojure</a> Interview Questions
#### Q1: What is Clojure? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q2: What is Data-oriented programming? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q3: What does it mean "Clojure is immutable-first"? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q4: How do you make a web application using Clojure? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

## [[⬆]](#toc) <a name=CodeProblems>Code Problems</a> Interview Questions
#### Q1: Test divisors of three ⭐
**Details:**
You will be given 2 parameters: a low and high number. Your goal is to print all numbers between low and high, and for each of these numbers print whether or not the number is divisible by 3. If the number is divisible by 3, print the word "div3" directly after the number.

**Answer:**
We'll solve this problem by first creating a loop that will print each number from low to high. Once we have the code for that written, we'll add a conditional that will check if the number is evenly divisible by 3 by using the mod operator.

```js
function test_divisors(low, high) {
  
  // we'll store all numbers and strings within an array
  // instead of printing directly to the console
  var output = [];
  
  for (var i = low; i <= high; i++) {
    
    // simply store the current number in the output array
    output.push(i);
    
    // check if the current number is evenly divisible by 3
    if (i % 3 === 0) { output.push('div3'); }
    
  }
  
  // return all numbers and strings
  return output;
  
}

test_divisors(2, 10);
```

**Source:** _coderbyte.com_

#### Q2: Sum of Array Plus One ⭐
**Details:**
Write a function that takes an array of integers and returns the sum of the integers after adding 1 to each.

**Answer:**
```js
// ES5 method is nice and clean
exports.es5 = function (array) {
  return array.reduce(function (memo, num) {
    return memo + num;
  }, array.length);
};

// Without array.reduce method isn't much different
exports.iterative = function (array) {
  var result = array.length;

  for (var i = 0; i < array.length; i++) {
    result += array[i];
  }

  return result;
};
```

**Source:** _github.com/blakeembrey_

#### Q3: String Rotation ⭐
**Details:**
Find out if a string is a rotation of another string. E.g. `ABCD` is a rotation of `BCDA` but not `ACBD`.

**Answer:**
First make sure `a` and `b` are of the same length. Then check to see if `b` is a substring of `a` concatenated with `a`:

```js
module.exports = function (a, b) {
  return a.length === b.length && (a + a).indexOf(b) > -1;
};
```



**Source:** _github.com/blakeembrey_

#### Q4: Oddball sum ⭐
**Details:**
Write a function called `oddball_sum` which takes in a list of numbers and returns the sum of all the odd elements. Try to solve with and without `reduce` function.

**Answer:**
To solve this challenge we'll simply loop through the array while maintaining a final count, and every time an odd number is encountered we'll add it to the count.

Without `reduce`:
```js
function oddball_sum(nums) {
 
  // final count of all odd numbers added up
  var final_count = 0;
  
  // loop through entire list
  for (var i = 0; i < nums.length; i++) {
    
    // we divide by 2, and if there is a remainder then
    // the number must be odd so we add it to final_count
    if (nums[i] % 2 === 1) {
      final_count += nums[i]
    }
    
  }
  
  return final_count;
  
}

oddball_sum([1, 2, 3, 4, 5]); 
```

With `reduce`:

```js
function oddball_sum(nums) {
  return nums.reduce(function(total, item){
  	if (item % 2 === 1) {
  		return total += item;
  	}
  	return total;
  });
}
```

**Source:** _prepwork.appacademy.io_

#### Q5: Simple clock angle ⭐
**Details:**
You will be given a number `N` that represents where the minute hand currently is on a clock. Your program should return the angle that is formed by the minute hand and the `12` o'clock mark on the clock.

**Answer:**
If the input is `15` then your program should return `90` because a `90`-degree angle is formed by the minute hand and the `12` o'clock mark on the clock. We'll solve this challenge by first calculating what angle is created by each minute passing on a clock. Once we calculate this number, we multiply it by the input to determine the final angle. 

A method to solve such problems is to consider the rate of change of the angle in degrees per minute. The hour hand of a normal `12-hour` analogue clock turns `360°` in `12` hours (`720` minutes) or `0.5°` per minute. The minute hand rotates through `360°` in `60` minutes or `6°` per minute.

```js
function simpleClockAngle(num) {

  // we got 6 because 360/60 = 6
  // 360 represents the full number of a degrees in a circle and
  // 60 is the number of minutes on a clock, so dividing these two numbers
  // gives us the number of degrees for one minute
  return 6 * num;

}

simpleClockAngle(15);
```



**Source:** _coderbyte.com_

#### Q6: Sum of several arrays ⭐
**Details:**
You will be given an array of several arrays that each contain integers and your goal is to write a function that will sum up all the numbers in all the arrays. For example, if the input is `[[3, 2], [1], [4, 12]]` then your program should output `22` because `3 + 2 + 1 + 4 + 12 = 22`. Solve without and with `reduce`.

**Answer:**
We will solve this challenge by looping through the entire array, and then looping through each inner array adding up all the numbers.

```js
function sum_array(arr) {
  // store our final answer
  var sum = 0;
  // loop through entire array
  for (var i = 0; i < arr.length; i++) {
    // loop through each inner array
    for (var j = 0; j < arr[i].length; j++) {
      // add this number to the current final sum
      sum += arr[i][j];
    }
  }
  
  return sum;
}

sum_array([[3, 2], [1], [4, 12]]);
```

With `reduce`:

```js
function sumArray(arr) {
  return arr.reduce((t, e) => t.concat(e)).reduce((t, e) => t + e)
}
```

**Source:** _coderbyte.com_

#### Q7: Lucky sevens ⭐
**Details:**
Write a function called `lucky_sevens` which takes an array of integers and returns true if any three consecutive elements sum to 7.

**Answer:**
To solve this challenge we'll simply loop through the array starting at the 3rd position, and checking if the number at this index plus the two previous elements sums to 7. We continue doing this as we loop through the entire array. Once we find three elements that sum to 7, we simply return `true`. If we reach the end of the array without finding elements that sum to 7, we return `false`.

```js
function lucky_sevens(arr) {
  
  // if less than 3 elements then this challenge is not possible
  if (arr.length < 3) {
    return "not possible";
  }
  
  // because we know there are at least 3 elements we can
  // start the loop at the 3rd element in the array (i=2)
  // and check it along with the two previous elements (i-1) and (i-2)
  for (var i = 2; i < arr.length; i++) {
    if (arr[i] + arr[i-1] + arr[i-2] === 7) {
      return true; 
    }
  }
  
  // if loop is finished and no elements summed to 7
  return false;
  
}

lucky_sevens([2, 1, 5, 1, 0]);
``` 



**Source:** _coderbyte.com_

#### Q8: Two sum problem ⭐⭐
**Details:**
Given an integer `x` and a sorted array a of `N` distinct integers, design a linear-time algorithm to determine if there exists two distinct indices `i` and `j` such that `a[i] + a[j] == x`

For example, if the array is `[3, 5, 2, -4, 8, 11]` and the sum is `7`, 
your program should return `[[11, -4], [2, 5]]` because `11 + -4 = 7` and `2 + 5 = 7`.

**Answer:**
The algorithm below makes use of hash tables which have a constant lookup time. As we pass through each element in the array, we check to see if S minus the current element exists in the hash table. We only need to loop through the array once, resulting in a running time of `O(n)` since each lookup and insertion in a hash table is `O(1)`.

```js
// our two sum function which will return
// all pairs in the array that sum up to S
function twoSum(arr, S) {

  var sums = [];
  var hashTable = {};

  // check each element in array
  for (var i = 0; i < arr.length; i++) {
 
    // calculate S - current element
    var sumMinusElement = S - arr[i];

    // check if this number exists in hash table
    // if so then we found a pair of numbers that sum to S
    if (hashTable[sumMinusElement.toString()] !== undefined) { 
      sums.push([arr[i], sumMinusElement]);
    }

    // add the current number to the hash table
    hashTable[arr[i].toString()] = arr[i];

  }

  // return all pairs of integers that sum to S
  return sums;

}

twoSum([3, 5, 2, -4, 8, 11], 7);
```



**Source:** _coderbyte.com_

#### Q9: Implement a queue using a linked list ⭐⭐
**Answer:**
We will store a reference to the front and back of the queue in order to make enqueuing and dequeuing run in `O(1)` constant time. Every time we want to insert into the queue, we add the new element to the end of the linked list and update the back pointer. When we want to dequeue we return the first node in the linked list and update the front pointer.

```js
// queue is initially empty
var Queue = {front: null, back: null};

// we will use a node to keep track of the elements
// in the queue which is represented by a linked list
function Node(data, next) {
  this.data = data;
  this.next = next;
} 

// add elements to queue in O(1) time
function Enqueue(element) {
  var N = new Node(element, null);
  if (Queue.back === null) {
    Queue.front = N;
    Queue.back = N; 
  } else { 
    Queue.back.next = N; 
    Queue.back = Queue.back.next;
  } 
}

// remove first element from queue in O(1) time
function Dequeue() {
  if (Queue.front !== null) { 
    var first = Queue.front;
    Queue.front = Queue.front.next; 
    return first.data;
  } else {
    if (Queue.back !== null) { Queue.back = null; }
    return 'Cannot dequeue because queue is empty';
  }
}

Enqueue('a'); 
Enqueue('b'); 
Enqueue('c'); 
Dequeue();
```

**Source:** _codeisahighway.com_

#### Q10: Tree Level Order Print ⭐⭐
**Details:**
Given a binary tree of integers, print it in level order. The output will contain space between the numbers in the same level, and new line between different levels.

**Answer:**
```js
module.exports = function (root) {
  // Doing a breadth first search using recursion.
  (function walkLevel (children) {
    // Create a new queue for the next level.
    var queue = [],
        output;

    // Use the map function to easily join all the nodes together while pushing
    // it's children into the next level queue.
    output = children.map(function (node) {
      // Assuming the node has children stored in an array.
      queue = queue.concat(node.children || []);
      return node.value;
    }).join(' ');

    // Log the output at each level.
    console.log(output);

    // If the queue has values in it, recurse to the next level and walk
    // along it.
    queue.length && walkLevel(queue);
  })([root]);
};
```


**Source:** _ardendertat.com_

#### Q11: Stock maximum profit ⭐⭐
**Details:**
You will be given a list of stock prices for a given day and your goal is to return the maximum profit that could have been made by buying a stock at the given price and then selling the stock later on. 

For example if the input is: 

```js
[45, 24, 35, 31, 40, 38, 11] 
```

then your program should return 16 because if you bought the stock at $24 and sold it at $40, a profit of $16 was made and this is the largest profit that could be made. If no profit could have been made, return -1.

**Answer:**
We'll solve the challenge the following way:

1. Iterate through each number in the list.
2. At the ith index, get the `i+1` index price and check if it is larger than the ith index price.
3. If so, set `buy_price = i` and `sell_price = i+1`. Then calculate the profit: `sell_price - buy_price`.
4. If a stock price is found that is cheaper than the current `buy_price`, set this to be the new buying price and continue from step 2.
5. Otherwise, continue changing only the `sell_price` and keep `buy_price` set.

This algorithm runs in linear time, making only one pass through the array, so the running time in the worst case is `O(n)`.

```js
function StockPicker(arr) { 
  
  var max_profit = -1;
  var buy_price = 0;
  var sell_price = 0;
  
  // this allows our loop to keep iterating the buying
  // price until a cheap stock price is found
  var change_buy_index = true;
  
  // loop through list of stock prices once
  for (var i = 0; i < arr.length-1; i++) {
    
    // selling price is the next element in list
    sell_price = arr[i+1]; 
    
    // if we have not found a suitable cheap buying price yet
    // we set the buying price equal to the current element
    if (change_buy_index) { buy_price = arr[i]; }
    
    // if the selling price is less than the buying price
    // we know we cannot make a profit so we continue to the 
    // next element in the list which will be the new buying price
    if (sell_price < buy_price) {
      change_buy_index = true; 
      continue;
    }
    
    // if the selling price is greater than the buying price
    // we check to see if these two indices give us a better 
    // profit then what we currently have
    else { 
      var temp_profit = sell_price - buy_price;
      if (temp_profit > max_profit) { max_profit = temp_profit; }
      change_buy_index = false;
    }
    
  }
  
  return max_profit;
         
}

StockPicker([44, 30, 24, 32, 35, 30, 40, 38, 15]);  
```

**Source:** _coderbyte.com_

#### Q12: Find Word Positions in Text ⭐⭐
**Details:**
Given a text file and a word, find the positions that the word occurs in the file. We’ll be asked to find the positions of many words in the same file.

**Answer:**
Since we’ll have to answer multiple queries, precomputation would be useful. We’ll build a data structure that stores the positions of all the words in the text file. This is known as inverted index.

```js
module.exports = function (text) {
  var trie   = {},
      pos    = 0,
      active = trie; // Start the active structure as the root trie structure

  // Suffix a space after the text to make life easier
  text += ' ';

  // Loop through the input text adding it to the trie structure
  for (var i = 0; i < text.length; i++) {
    // When the character is a space, restart
    if (text[i] === ' ') {
      // If the current active doesn't equal the root, set the position
      if (active !== trie) {
        (active.positions = active.positions || []).push(pos);
      }
      // Reset the positions and the active part of the data structure
      pos    = i;
      active = trie;
      continue;
    }

    // Set the next character in the structure up
    active[text[i]] = (active[text[i]] || {});
    active = active[text[i]];
  }

  // Return a function that accepts a word and looks it up in the trie structure
  return function (word) {
    var i      = -1,
        active = trie;

    while (word[++i]) {
      if (!active[word[i]]) { return []; }
      active = active[word[i]];
    }

    return active.positions;
  };
};
```

**Source:** _github.com/blakeembrey_

#### Q13: Determine overlapping numbers in ranges ⭐⭐
**Details:**
You will be given an array with `5` numbers. The first 2 numbers represent a range, and the next two numbers represent another range. The final number in the array is `X`. The goal of your program is to determine if both ranges overlap by at least `X` numbers. For example, in the array `[4, 10, 2, 6, 3]` the ranges `4` to `10` and `2` to `6` overlap by at least `3` numbers `(4, 5, 6)`, so your program should return `true`. Solve with and without looping.

If the array is `[10, 20, 4, 14, 4]` then the ranges are:

```sh
10 11 12 13 14 15 16 17 18 19 20
4 5 6 7 8 9 10 11 12 13 14
```

These ranges overlap by at least `4` numbers, namely: `10, 11, 12, 13, 14` so your program should return `true`.

**Answer:**
With loop:
```js
function OverlappingRanges(arr) {

  // keep a count of how many numbers overlap
  var counter = 0;
  
  // loop through one of the ranges
  for (var i = arr[0]; i < arr[1]; i++) {

    // check if a number within the first range exists
    // in the second range
    if (i >= arr[2] && i <= arr[3]) { 
      counter += 1;
    }

  }
 
  // check if the numbers that overlap is equal to or greater
  // than the last number in the array
  return (counter >= arr[4]) ? true : false;
}

OverlappingRanges([4, 10, 2, 6, 3]); 
```

Without loop:

```js
function overlapping(input){
  var nums1 = listOfNums(input[0], input[1]);
  var nums2 = listOfNums(input[2], input[3]);
  var overlappingNum = 0;

  if(nums1[0] >= nums2[0] && nums1[0] <= nums2[1]){
    overlappingNum =  nums2[1] - nums1[0] + 1;
  } else {
    overlappingNum =  nums1[1] - nums2[0] + 1;
  }
  if(overlappingNum >= input[4]){
    return true;
  }
}

function listOfNums(a, b){
  var start = a;
  var end = b;
  if(a > b){
    start = b;
    end = a;
  }

  return [a, b];
}

var a = [4, 10, 2, 6, 3];
overlapping(a)
```


**Source:** _coderbyte.com_

#### Q14: Throttle Function Implementation ⭐⭐
**Details:**
Write a function that accepts a function and timeout, `x`, in number of milliseconds. It returns a function that can only be executed once per `x` milliseconds. This can be useful for limiting the number of time and computation heavy function that are run. For example, making AJAX requests to an autocompletion API.

Once written, add a third parameter that will allow the function to be executed immediately if set to true. Otherwise the function will run at the end of the timeout period.

**Answer:**
```js
module.exports = function (fn, delay, execAsap) {
  var timeout; // Keeps a reference to the timeout inside the returned function

  return function () {
    // Continue to pass through the function execution context and arguments
    var that = this,
        args = arguments;

    // If there is no timeout variable set, proceed to create a new timeout
    if (!timeout) {
      execAsap && fn.apply(that, args);

      timeout = setTimeout(function () {
        execAsap || fn.apply(that, args);
        // Remove the old timeout variable so the function can run again
        timeout = null;
      }, delay || 100);
    }
  };
};
```


**Source:** _github.com/blakeembrey_

#### Q15: Dutch national flag sorting problem ⭐⭐
**Details:**
For this problem, your goal is to sort an array of `0`, `1`, `2` but you must do this in place, in linear time and without any extra space (such as creating an extra array). This is called the *Dutch national flag sorting problem*. For example, if the input array is `[2,0,0,1,2,1]` then your program should output `[0,0,1,1,2,2]` and the algorithm should run in `O(n)` time.

**Answer:**
The solution to this algorithm will require 3 pointers to iterate throughout the array, swapping the necessary elements.

1. Create a low pointer at the beginning of the array and a high pointer at the end of the array.
2. Create a mid pointer that starts at the beginning of the array and iterates through each element.
3. If the element at `arr[mid]` is a `2`, then swap `arr[mid]` and `arr[high]` and decrease the high pointer by `1`.
4. If the element at `arr[mid]` is a `0`, then swap `arr[mid]` and `arr[low]` and increase the low and mid pointers by `1`.
5. If the element at `arr[mid]` is a `1`, don't swap anything and just increase the mid pointer by `1`.

```js
function swap(arr, i1, i2) {
  var temp = arr[i1];
  arr[i1] = arr[i2];
  arr[i2] = temp;
}

function dutchNatFlag(arr) {
  
  var low = 0;
  var mid = 0;
  var high = arr.length - 1;
  
  // one pass through the array swapping
  // the necessary elements in place
  while (mid <= high) {
    if      (arr[mid] === 0) { swap(arr, low++, mid++); }
    else if (arr[mid] === 2) { swap(arr, mid, high--); }
    else if (arr[mid] === 1) { mid++; }
  }
  
  return arr;
  
}

dutchNatFlag([2,2,2,0,0,0,1,1]); 
```

**Source:** _coderbyte.com_

#### Q16: Step-by-step solution for step counting using recursion ⭐⭐
**Details:**

Suppose you want climb a staircase of N steps, and on each step you can take either 1 or 2 steps. How many distinct ways are there to climb the staircase? For example, if you wanted to climb 4 steps, you can take the following distinct number of steps:

```sh
1) 1, 1, 1, 1
2) 1, 1, 2
3) 1, 2, 1
4) 2, 1, 1
5) 2, 2
```

So there are 5 distinct ways to climb 4 steps. We want to write a function, using recursion, that will produce the answer for any number of steps. 


**Answer:**
The solution to this problem requires recursion, which means to solve for a particular `N`, we need the solutions for previous N's. The solution for N steps is equal to the solutions for `N - 1` steps plus `N - 2` steps.

```js
function countSteps(N) {
  
  // just as in our solution explanation above, we know that to climb 1 step
  // there is only 1 solution, and for 2 steps there are 2 solutions
  if (N === 1) { return 1; }
  if (N === 2) { return 2; }
  
  // for all N > 2, we add the previous (N - 1) + (N - 2) steps to get
  // an answer recursively
  return countSteps(N - 1) + countSteps(N - 2);
  
}

// the solution for N = 6 will recursively be solved by calculating
// the solution for N = 5, N = 4, N = 3, and N = 2 which we know is 2
countSteps(6); 
```


**Source:** _coderbyte.com_

#### Q17: Implement Bubble Sort ⭐⭐
**Answer:**
The steps in the bubble sort algorithm are:

1. Loop through the whole array starting from index `1`
2. If the number in the array at index `i-1` is greater than i, swap the numbers and continue
3. Once the end of the array is reached, start looping again from the beginning
4. Once no more elements can be swapped, the sorting is complete

```js
function swap(arr, i1, i2) {
  var temp = arr[i1];
  arr[i1] = arr[i2];
  arr[i2] = temp;
}

function bubblesort(arr) {
  
  var swapped = true;
  
  // keep going unless no elements can be swapped anymore
  while (swapped) {
    
    // set swapped to false so that the loop stops
    // unless two element are actually swapped
    swapped = false;

    // loop through the whole array swapping adjacent elements
    for (var i = 1; i < arr.length; i++) {
      if (arr[i-1] > arr[i]) {
        swap(arr, i-1, i);
        swapped = true;
      }
    }
    
  }
  
  return arr;
         
}

bubblesort([103, 45, 2, 1, 97, -4, 67]); 
```

**Source:** _coderbyte.com_

#### Q18: Implement a queue using two stacks ⭐⭐
**Answer:**
Suppose we push `a`, `b`, `c` to a stack. If we are trying to implement a queue and we call the dequeue method 3 times, we actually want the elements to come out in the order: `a`, `b`, `c`, which is in the opposite order they would come out if we popped from the stack. So, basically, we need to access the elements in the reverse order that they exist in the stack. 

*Algorithm* for queue using two stacks:

1. When calling the enqueue method, simply push the elements into the stack 1.
2. If the dequeue method is called, push all the elements from stack 1 into stack 2, which reverses the order of the elements. Now pop from stack 2.

The worst case running time for implementing these operations using stacks is `O(n)` because you need to transfer n elements from stack 1 to stack 2 when a dequeue method is called. Pushing to stack 1 is simply `O(1)`.

```js
// implement stacks using plain arrays with push and pop functions
var Stack1 = [];
var Stack2 = [];

// implement enqueue method by using only stacks
// and the push and pop functions
function Enqueue(element) {
  Stack1.push(element);
}

// implement dequeue method by pushing all elements
// from stack 1 into stack 2, which reverses the order
// and then popping from stack 2
function Dequeue() {
  if (Stack2.length === 0) {
    if (Stack1.length === 0) { return 'Cannot dequeue because queue is empty'; }
    while (Stack1.length > 0) {
      var p = Stack1.pop();
      Stack2.push(p);
    }
  }
  return Stack2.pop();
}

Enqueue('a');
Enqueue('b');
Enqueue('c');
Dequeue(); 
```

**Source:** _coderbyte.com_

#### Q19: Implement pow(a,b) without multiplication or division ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q20: Generate all balanced bracket combinations ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q21: All Permutations (Anagrams) of a String ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q22: Merge two sorted linked lists ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q23: Insert an interval into a list of sorted disjoint intervals ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q24: Find all string combinations consisting only of 0, 1 and ? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q25: Quickly calculate the cube root of 6 digit numbers ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q26: Transform Word ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

## [[⬆]](#toc) <a name=DataScience>Data Science</a> Interview Questions
#### Q1: What is Data Science? ⭐
**Answer:**
Data Science is an interdisciplinary field of different scientific methods, techniques, processes, and knowledge that is used to transform the data of different types such as structured, unstructured and semi-structured data into the required format or representation.

Data Science concepts include different concepts such as statistics, regression, mathematics, computer science, algorithms, data structures and information science with also including some subfields such as data mining, machine learning, and databases etc.,

Data Science concept has recently evolved to a greater extent in the area of computing technology in order to perform data analysis on the existing data where the growth of data is in terms of an exponential with respect to time.

Data Science is the study of various types of data such as structured, semi-structured and unstructured data in any form or formats available in order to get some information out of it.

Data Science consists of different technologies used to study data such as data mining, data storing, data purging, data archival, data transformation etc., in order to make it efficient and ordered. Data Science also includes the concepts like Simulation, modeling, analytics, machine learning, computational mathematics etc.

**Source:** _www.educba.com_

#### Q2: What is the best Programming Language to use in Data Science? ⭐
**Answer:**
Data Science can be handled by using programming languages like Python or R programming language. These two are the two most popular languages being used by the Data Scientists or Data Analysts. R and Python are open source and are free to use and came into existence during the 1990s.

Python and R have different advantages depending on the applications and required a business goal. Python is better to be used in the cases of repeated tasks or jobs and for data manipulations whereas R programming can be used for querying or retrieving datasets and customized data analysis.

Mostly Python is preferred for all types of data science applications where some time R programming is preferred in the cases of high or complex data applications. Python is easier to learn and has less learning curve whereas R has a deep learning curve.

Python is mostly preferred in all the cases which is a general-purpose programming language and can be found in many applications other than Data Science too. R is mostly seen in Data Science area only where it is used for data analysis in standalone servers or computing separately.

**Source:** _www.educba.com_

#### Q3: Why is data cleaning essential in Data Science? ⭐
**Answer:**
Data cleaning is more important in Data Science because the end results or the outcomes of the data analysis come from the existing data where useless or unimportant need to be cleaned periodically as of when not required. This ensures the data reliability & accuracy and also memory is freed up.

Data cleaning reduces the data redundancy and gives good results in data analysis where some large customer information exists and that should be cleaned periodically. In the businesses like e-commerce, retail, government organizations contain large customer transaction information which is outdated and needs to be cleaned.

Depending on the amount or size of data, suitable tools or methods should be used to clean the data from the database or big data environment. There are different types of data existing in a data source such as dirty data, clean data, mixed clean and dirty data and sample clean data.

Modern data science applications rely on machine learning model where the learner learns from the existing data. So, the existing data should always be cleanly and well maintained to get sophisticated and good outcomes during the optimization of the system.

**Source:** _www.educba.com_

#### Q4: What is Linear Regression in Data Science? ⭐⭐
**Answer:**
Linear Regression is a technique used in supervised machine learning algorithmic process in the area of Data Science. This method is used for predictive analysis.

Predictive analytics is an area within Statistical Sciences where the existing information will be extracted and processed to predict the trends and outcomes pattern. The core of the subject lies in the analysis of existing context to predict an unknown event.

The process of Linear Regression method is to predict a variable called target variable by making the best relationship between the dependent variable and an independent variable. Here dependent variable is outcome variable and also response variable whereas the independent variable is predictor variable or explanatory variable.

For example in real life, depending on the expenses occurred in this financial year or monthly expenses, the predictions happen by calculating the approximate upcoming months or financial years expenses.

In this method, the implementation can be done by using Python programming technique where this is the most important method used in Machine Learning technique under the area of Data Science.

Linear regression is also called Regression analysis that comes under the area of Statistical Sciences which is integrated together with Data Science.

**Source:** _www.educba.com_

#### Q5: What is A/B testing in Data Science? ⭐⭐
**Answer:**
A/B testing is also called as Bucket Testing or Split Testing. This is the method of comparing and testing two versions of systems or applications against each other to determine which version of application performs better. This is important in the cases where multiple versions are shown to the customers or end users in order to achieve the goals.

In the area of Data Science, this A/B testing is used to know which variable out of the existing two variables in order to optimize or increase the outcome of the goal. A/B testing is also called Design of Experiment. This testing helps in establishing a cause and effect relationship between the independent and dependent variables.

This testing is also simply a combination of design experimentation or statistical inference. Significance, Randomization and Multiple Comparisons are the key elements of the A/B testing.

The significance is the term for the significance of statistical tests conducted. Randomization is the core component of the experimental design where the variables will be balanced. Multiple comparisons are the way of comparing more variables in the case of customer interests that causes more false positives resulting in the requirement of correction in the confidence level of a seller in the area of e-commerce.

A/B testing is the important one in the area of Data Science in predicting the outcomes.

**Source:** _www.educba.com_

## [[⬆]](#toc) <a name=DataStructures>Data Structures</a> Interview Questions
#### Q1: What is data-structure? ⭐
**Answer:**
Data structure availability may vary by programming languages. Commonly available data structures are:
* list, 
* arrays, 
* stack, 
* queues, 
* graph, 
* tree etc.

**Source:** _tutorialspoint.com_

#### Q2: What is a graph? ⭐
**Answer:**
A **graph** is a pictorial representation of a set of objects where some pairs of objects are connected by links. The interconnected objects are represented by points termed as vertices, and the links that connect the vertices are called edges.

**Source:** _tutorialspoint.com_

#### Q3: What is linear searching? ⭐
**Answer:**
**Linear search** or sequential search is a method for finding a target value within a list. It sequentially checks each element of the list for the target value until a match is found or until all the elements have been searched. Linear search runs in at worst *linear time* and makes at most `n` comparisons, where `n` is the length of the list. 

* Worst-case performance	`O(n)`
* Best-case performance	`O(1)`
* Average performance	`O(n)`
* Worst-case space complexity	`O(1)` iterative

In theory other search algorithms may be faster than linear search (for instance binary search), in practice even on medium-sized arrays (around 100 items or less) it might be infeasible to use anything else. 

**Source:** _wikipedia.org_

#### Q4: What is algorithm? ⭐
**Answer:**
**Algorithm** is a step by step procedure, which defines a set of instructions to be executed in certain order to get the desired output.

**Source:** _tutorialspoint.com_

#### Q5: What is linear data structure and what are common operations to perform on it? ⭐⭐
**Answer:**
A *linear data-structure* has sequentially arranged data items. The next item can be located in the next memory address. It is stored and accessed in a sequential manner. **Array** and **list** are example of linear data structure.

The following operations are commonly performed on any data-structure:

*   **Insertion** − adding a data item
*   **Deletion** − removing a data item
*   **Traversal** − accessing and/or printing all data items
*   **Searching** − finding a particular data item
*   **Sorting** − arranging data items in a pre-defined sequence

**Source:** _tutorialspoint.com_

#### Q6: What is an average case complexity of Bubble Sort? ⭐⭐
**Answer:**
**Bubble sort**, sometimes referred to as sinking sort, is a simple sorting algorithm that repeatedly steps through the list to be sorted, compares each pair of adjacent items and swaps them if they are in the wrong order. The pass through the list is repeated until no swaps are needed, which indicates that the list is sorted. 

Bubble sort has a worst-case and average complexity of `О(n2)`, where `n` is the number of items being sorted. Most practical sorting algorithms have substantially better worst-case or average complexity, often `O(n log n)`. Therefore, bubble sort is not a practical sorting algorithm.



**Source:** _wikipedia.org_

#### Q7: What examples of greedy algorithms do you know? ⭐⭐
**Answer:**
The below given problems find their solution using greedy algorithm approach:

*   Travelling Salesman Problem
*   Prim's Minimal Spanning Tree Algorithm
*   Kruskal's Minimal Spanning Tree Algorithm
*   Dijkstra's Minimal Spanning Tree Algorithm
*   Graph - Map Coloring
*   Graph - Vertex Cover
*   Knapsack Problem
*   Job Scheduling Problem

**Source:** _tutorialspoint.com_

#### Q8: What are some examples of divide and conquer algorithms? ⭐⭐
**Answer:**
The below given problems find their solution using divide and conquer algorithm approach:

*   Merge Sort
*   Quick Sort
*   Binary Search
*   Strassen's Matrix Multiplication
*   Closest pair (points)

**Source:** _tutorialspoint.com_

#### Q9: What are some examples of dynamic programming algorithms? ⭐⭐
**Answer:**
The below given problems find their solution using divide and conquer algorithm approach:

*   Fibonacci number series
*   Knapsack problem
*   Tower of Hanoi
*   All pair shortest path by Floyd-Warshall
*   Shortest path by Dijkstra
*   Project scheduling

**Source:** _tutorialspoint.com_

#### Q10: Why do we use stacks? ⭐⭐
**Answer:**
In data-structure, **stack** is an Abstract Data Type (ADT) used to store and retrieve values in Last In First Out (LIFO) method.

Stacks follows LIFO method and addition and retrieval of a data item takes only `Ο(n)` time. Stacks are used where we need to access data in the reverse order or their arrival. Stacks are used commonly in recursive function calls, expression parsing, depth first traversal of graphs etc.

The below operations can be performed on a stack:

*   **push()** − adds an item to stack
*   **pop()** − removes the top stack item
*   **peek()** − gives value of top item without removing it
*   **isempty()** − checks if stack is empty
*   **isfull()** − checks if stack is full

**Source:** _tutorialspoint.com_

#### Q11: Why do we use queues? ⭐⭐
**Answer:**
**Queue** is an abstract data structure (ADS), somewhat similar to stack. In contrast to stack, queue is opened at both end. One end is always used to insert data (enqueue) and the other is used to remove data (dequeue). Queue follows First-In-First-Out (FIFO) methodology, i.e., the data item stored first will be accessed first.

As queues follows FIFO method, they are used when we need to work on data-items in exact sequence of their arrival. Every operating system maintains queues of various processes. Priority queues and breadth first traversal of graphs are some examples of queues.

The below operations can be performed on a queue:
*   **enqueue()** − adds an item to rear of the queue
*   **dequeue()** − removes the item from front of the queue
*   **peek()** − gives value of front item without removing it
*   **isempty()** − checks if stack is empty
*   **isfull()** − checks if stack is full

**Source:** _tutorialspoint.com_

#### Q12: What is Selection Sort? ⭐⭐
**Answer:**
**Selection sort** is in-place sorting technique. It divides the data set into two sub-lists: sorted and unsorted. Then it selects the minimum element from unsorted sub-list and places it into the sorted list. This iterates unless all the elements from unsorted sub-list are consumed into sorted sub-list.

**Source:** _tutorialspoint.com_

#### Q13: Why we need to do algorithm analysis? ⭐⭐
**Answer:**
A problem can be solved in more than one ways. So, many solution algorithms can be derived for a given problem. We analyze available algorithms to find and implement the best suitable algorithm.

An algorithm are generally analyzed on two factors − time and space. That is, how much **execution** time and how much **extra space** required by the algorithm.

**Source:** _tutorialspoint.com_

#### Q14: What is the difference between Linear Search and Binary Search? ⭐⭐
**Answer:**
* A **linear search** looks down a list, one item at a time, without jumping. In complexity terms this is an `O(n)` search - the time taken to search the list gets bigger at the same rate as the list does.

* A **binary search** is when you start with the middle of a sorted list, and see whether that's greater than or less than the value you're looking for, which determines whether the value is in the first or second half of the list. Jump to the half way through the sublist, and compare again etc. In complexity terms this is an `O(log n)` search - the number of search operations grows more slowly than the list does, because you're halving the "search space" with each operation.

Comparing the two:

- Binary search requires the input data to be sorted; linear search doesn't
- Binary search requires an *ordering* comparison; linear search only requires equality comparisons
- Binary search has complexity `O(log n)`; linear search has complexity O(n)
- Binary search requires random access to the data; linear search only requires sequential access (this can be very important - it means a linear search can *stream* data of arbitrary size)

**Source:** _wikipedia.org_

#### Q15: What is asymptotic analysis of an algorithm? ⭐⭐
**Answer:**
**Asymptotic analysis** of an algorithm, refers to defining the mathematical boundation/framing of its run-time performance. Using asymptotic analysis, we can very well conclude the best case, average case and worst case scenario of an algorithm.

Asymptotic analysis can provide three levels of mathematical binding of execution time of an algorithm:

*   Best case is represented by Ω(n) notation.
*   Worst case is represented by Ο(n) notation.
*   Average case is represented by Θ(n) notation.

**Source:** _tutorialspoint.com_

#### Q16: Name some approaches to develop algorithms ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q17: What is Circular Queue and why will you use one? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q18: Why is Insertion sort better than Quick sort for small list of elements? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q19: Tell me something about Insertion sort? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q20: List some advantages of Insertion Sort ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q21: How Insertion sort and Selection sorts are different? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q22: What is Merge Sort and how it works? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q23: How Quick Sort works? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q24: What is Shell Sort? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q25: Is there ever a good reason to use Insertion Sort? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q26: Is there any advantages of Bubble Sort? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q27: What is Bucket Sort? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q28: What is Tim Sort and how would you compare it with Quick Sort? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q29: Why is Quick Sort better than Merge Sort? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q30: What is stability in sorting algorithms and why is it important? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

## [[⬆]](#toc) <a name=DesignPatterns>Design Patterns</a> Interview Questions
#### Q1: What are the main categories of Design Patterns? ⭐
**Answer:**
The Design patterns can be classified into three main categories:

* Creational Patterns
* Behavioral Patterns
* Functional Patterns

**Source:** _www.educba.com_

#### Q2: What is a pattern? ⭐
**Answer:**
*Patterns* in programming are like recipes in cooking. They are not ready dishes, but instructions for slicing and dicing products, cooking them, serving them and so forth.

**Pattern content**
As a rule, a pattern description consists of the following:

* a problem that the pattern solves;
* motivation for solving the the problem using the method suggested by the pattern;
* structures of classes comprising the solution;
* an example in one of the programming languages;
* a description of the nuances of pattern implementation in various contexts;
relations with other patterns.

**Source:** _refactoring.guru_

#### Q3: What is Singleton pattern? ⭐
**Answer:**
**Singleton pattern** comes under *creational* patterns category and introduces a single class which is responsible to create an object while making sure that only single object gets created. This class provides a way to access its only object which can be accessed directly without need to instantiate the object of the class.

<div class="text-center">
<img src="https://upload.wikimedia.org/wikipedia/commons/thumb/f/fb/Singleton_UML_class_diagram.svg/220px-Singleton_UML_class_diagram.svg.png" class="img-fluid"/>
</div>


**Source:** _refactoring.guru_

#### Q4: What is Design Patterns and why anyone should use them? ⭐
**Answer:**
Design patterns are a well-described solution to the most commonly encountered problems which occur during software development. 

Design pattern represents the best practices evolved over a period of time by experienced software developers. They promote reusability which leads to a more robust and maintainable code.

**Source:** _www.educba.com_

#### Q5: What is Factory pattern? ⭐⭐
**Answer:**
**Factory pattern** is one of most used design pattern and comes under *creational* patterns category.

In Factory pattern, we create object without exposing the creation logic to the client and refer to newly created object using a *common interface*.

<div class="text-center">
<img src="https://www.tutorialspoint.com/design_pattern/images/factory_pattern_uml_diagram.jpg" class="img-fluid"/>
</div>

<br/>
**Pro's**:  

*   Allows you to hide implementation of an application seam (the core interfaces that make up your application)
*   Allows you to easily test the seam of an application (that is to mock/stub) certain parts of your application so you can build and test the other parts
*   Allows you to change the design of your application more readily, this is known as loose coupling

**Con's**  

*   Makes code more difficult to read as all of your code is behind an abstraction that may in turn hide abstractions.
*   Can be classed as an anti-pattern when it is incorrectly used, for example some people use it to wire up a whole application when using an IOC container, instead use Dependency Injection.

**Source:** _tutorialspoint.com_

#### Q6: What is Iterator pattern? ⭐⭐
**Answer:**
**Iterator pattern** is very commonly used design pattern in Java and .Net programming environment. This pattern is used to get a way to access the elements of a collection object in sequential manner without any need to know its underlying representation. Iterator pattern falls under _behavioral_ pattern category.

<div class="text-center">
<img src="https://upload.wikimedia.org/wikipedia/commons/c/c5/W3sDesign_Iterator_Design_Pattern_UML.jpg" class="img-fluid"/>
</div>

**Source:** _tutorialspoint.com_

#### Q7: What is Inversion of Control? ⭐⭐
**Answer:**

*Inversion of control* is a broad term but for a software developer it's most commonly described as a pattern used for decoupling components and layers in the system. 

For example, say your application has a text editor component and you want to provide spell checking. Your standard code would look something like this:
```js
public class TextEditor {

    private SpellChecker checker;

    public TextEditor() {
        this.checker = new SpellChecker();
    }
}
```
What we've done here creates a dependency between the TextEditor and the SpellChecker. In an IoC scenario we would instead do something like this:
```js
public class TextEditor {

    private IocSpellChecker checker;

    public TextEditor(IocSpellChecker checker) {
        this.checker = checker;
    }
}
```

You have *inverted control* by handing the responsibility of instantiating the spell checker from the TextEditor class to the caller.

```js
SpellChecker sc = new SpellChecker; // dependency
TextEditor textEditor = new TextEditor(sc);
```


**Source:** _stackoverflow.com_

#### Q8: Can we create a clone of a singleton object? ⭐⭐
**Answer:**
Yesl, we can but the purpose of Singleton Object creation is to have single instance serving all requests. 

**Source:** _tutorialspoint.com_

#### Q9: Name types of Design Patterns? ⭐⭐
**Answer:**
Design patterns can be classified in three categories: Creational, Structural and Behavioral patterns.

-   Creational Patterns - These design patterns provide a way to create objects while hiding the creation logic, rather than instantiating objects directly using new opreator. This gives program more flexibility in deciding which objects need to be created for a given use case.

-   Structural Patterns - These design patterns concern class and object composition. Concept of inheritance is used to compose interfaces and define ways to compose objects to obtain new functionalities.

-   Behavioral Patterns - These design patterns are specifically concerned with communication between objects.

**Source:** _tutorialspoint.com_

#### Q10: What is Template pattern? ⭐⭐
**Answer:**
In **Template pattern**, an abstract class exposes defined way(s)/template(s) to execute its methods. Its subclasses can override the method implementation as per need but the invocation is to be in the same way as defined by an abstract class. This pattern comes under _behavior_ pattern category.

<div class="text-center">
<img src="https://upload.wikimedia.org/wikipedia/commons/2/2a/W3sDesign_Template_Method_Design_Pattern_UML.jpg" class="img-fluid"/>
</div>

**Source:** _tutorialspoint.com_

#### Q11: What is Filter pattern? ⭐⭐
**Answer:**
**Filter pattern** or **Criteria pattern** is a design pattern that enables developers to filter a set of objects using different criteria and chaining them in a decoupled way through logical operations. This type of design pattern comes under *structural* pattern as this pattern combines multiple criteria to obtain single criteria.

**Filter design pattern** is useful where you want to add filters dynamically or you are implementing multiple functionalities and most of them require different filter criteria to filter something. In that case instead of hard coding the filters inside the functionalities, you can create filter criteria and re-use it wherever required.

```js
List<Laptop> laptops = LaptopFactory.manufactureInBulk();
AndCriteria searchCriteria = new AndCriteria(
  new HardDisk250GBFilter(), 
  new MacintoshFilter(), 
  new I5ProcessorFilter());
List<Laptop> filteredLaptops = searchCriteria.meets(laptops);
```

**Source:** _tutorialspoint.com_

#### Q12: What is Strategy pattern? ⭐⭐
**Answer:**
In **Strategy pattern**, a class behavior or its algorithm can be changed at run time. This type of design pattern comes under _behavior_ pattern.

In Strategy pattern, we create objects which represent various strategies and a context object whose behavior varies as per its strategy object. The strategy object changes the executing algorithm of the context object.

<div class="text-center">
<img src="https://upload.wikimedia.org/wikipedia/commons/4/45/W3sDesign_Strategy_Design_Pattern_UML.jpg" class="img-fluid"/>
</div>



**Source:** _tutorialspoint.com_

#### Q13: What is Dependency Injection? ⭐⭐
**Answer:**
*Dependency injection* makes it easy to create loosely coupled components, which typically means that components consume functionality defined by interfaces without having any first-hand knowledge of which implementation classes are being used.

*Dependency injection* makes it easier to change the behavior of an application by changing the components that implement the interfaces that define application features. It also results in components that are easier to isolate for unit testing.

**Source:** _Pro ASP.NET Core MVC 2_

#### Q14: What is Null Object pattern? ⭐⭐
**Answer:**
In **Null Object pattern**, a null object replaces check of NULL object instance. Instead of putting if check for a null value, Null Object reflects a do nothing relationship. Such Null object can also be used to provide default behaviour in case data is not available.

In Null Object pattern, we create an abstract class specifying various operations to be done, concrete classes extending this class and a null object class providing do nothing implementation of this class and will be used seamlessly where we need to check null value.

<div class="text-center">
<img src="https://www.tutorialspoint.com/design_pattern/images/null_pattern_uml_diagram.jpg" class="img-fluid"/>
</div>


**Source:** _tutorialspoint.com_

#### Q15: What is State pattern? ⭐⭐
**Answer:**
In **State pattern** a class behavior changes based on its state. This type of design pattern comes under _behavior_ pattern. In State pattern, we create objects which represent various states and a context object whose behavior varies as its state object changes.

<div class="text-center">
<img src="https://upload.wikimedia.org/wikipedia/commons/e/ec/W3sDesign_State_Design_Pattern_UML.jpg" class="img-fluid"/>
</div>

**Source:** _tutorialspoint.com_

#### Q16: What is Proxy pattern? ⭐⭐
**Answer:**
In **proxy pattern**, a class represents functionality of another class. This type of design pattern comes under _structural_ pattern.

In proxy pattern, we create object having original object to interface its functionality to outer world.

<div class="text-center">
<img src="https://upload.wikimedia.org/wikipedia/commons/thumb/7/75/Proxy_pattern_diagram.svg/439px-Proxy_pattern_diagram.svg.png" class="img-fluid"/>
</div>

**Source:** _tutorialspoint.com_

#### Q17: What is Builder pattern? ⭐⭐
**Answer:**
*Builder pattern* builds a complex object using simple objects and using a step by step approach. This builder is independent of other objects.


<div class="text-center"/>
<img src="https://www.plantuml.com/plantuml/svg/TOux3i8m343tdC9ZE_G234YqIAo86mJ7WqMQLeupS7kSqY90iCJsU_4dtpZDNlm8MU-Hx1L6BMDqHfMHPvyK_12PQio0d-B8GgYJL1M-UgQ4GafzuHXe-O5NvunvfPeYTDtU4jZ14sukh2gy6LXhcset5jIcTG6s_cN7sROVcXP-yVuF7oh75p-HNYYNQDCV" class="img-fluid" style="max-width: 500px" />
</div>

*The Director* class is optional and is used to make sure that the building steps are executed in the *right order* with the right data by the right builder. It's about validation and delegation.

Builder/Director pattern's steps invocations could be semantically presented by *method chaining* or so called *Fluent Interface* syntax. 

```js
Pizza pizza = new Pizza.Builder()
                       .cheese(true)
                       .pepperoni(true)
                       .bacon(true)
                       .build();
```

**Source:** _tutorialspoint.com_

#### Q18: What are the difference between a static class and a singleton class? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q19: When should I use composite design pattern? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q20: What does “program to interfaces, not implementations” mean? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q21: What is Abstract Factory pattern? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q22: What is Decorator pattern? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q23: What is Prototype pattern? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q24: What is Memento pattern? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q25: Can you give any good explanation what is the difference between Proxy and Decorator? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q26: What is Adapter Pattern? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q27: What is Bridge pattern? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q28: What is the Chain of Responsibility pattern? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q29: What is Observer pattern? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q30: What is Command pattern? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q31: What is Interpreter pattern? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q32: What is Facade pattern? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q33: What is Mediator pattern? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q34: When would you use the Builder Pattern? Why not just use a Factory Pattern? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q35: Why would I ever use a Chain of Responsibility over a Decorator? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q36: What is Flyweight pattern? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q37: Explain usage of Service Locator Pattern ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q38: What is the difference between Strategy design pattern and State design pattern? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q39: How is Bridge pattern is different from Adapter pattern? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q40: Explain what is Composition over inheritance? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q41: Could you explain the difference between Façade vs. Mediator? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q42: Explain difference between the Facade, Proxy, Adapter and Decorator design patterns? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q43: What is the difference between the template patterns and the strategy pattern? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q44: What's the difference between the Dependency Injection and Service Locator patterns? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q45: Could you explain what is the "deadly diamond of death"? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

## [[⬆]](#toc) <a name=DevOps>DevOps</a> Interview Questions
#### Q1: Explain what is DevOps ? ⭐
**Answer:**
**DevOps** is a newly emerging term in IT field, which is nothing but a practice that emphasizes the collaboration and communication of both software developers and other information-technology (IT) professionals. It focuses on delivering software product faster and lowering the failure rate of releases.

**Source:** _quora.com_

#### Q2: What is the most important thing DevOps helps us achieve? ⭐
**Answer:**
The most important thing that DevOps helps us achieve is to get the changes into production as quickly as possible while minimising risks in software quality assurance and compliance. This is the primary objective of DevOps.

**Source:** _edureka.co_

#### Q3: What is meant by Continuous Integration? ⭐
**Answer:**
*Continuous Integration (CI)* is a development practice that requires developers to integrate code into a shared repository several times a day. Each check-in is then verified by an automated build, allowing teams to detect problems early. 

**Source:** _edureka.co_

#### Q4: What is the need for DevOps? ⭐
**Answer:**
Nowadays instead of releasing big sets of features, companies are trying to see if small features can be transported to their customers through a series of release trains. This has many advantages like quick feedback from customers, better quality of software etc. which in turn leads to high customer satisfaction. To achieve this, companies are required to:

1.  Increase deployment frequency
2.  Lower failure rate of new releases
3.  Shortened lead time between fixes
4.  Faster mean time to recovery in the event of new release crashing

DevOps fulfills all these requirements and helps in achieving seamless software delivery. 

**Source:** _edureka.co_

#### Q5: Are you more Dev or Ops? ⭐
**Answer:**
What the interview means is do you do more sysadmin work, or do you spend a lot of time working with developers on coding?

**Source:** _vminstall.com_

#### Q6: What is post mortem meetings? ⭐⭐
**Answer:**
*Post mortem meeting* is a meeting where we discuss what went wrong and what steps should be taken so that failure doesn't happen again. Post mortem meetings are not about finding the one to be blamed, they are for preventing outages from reoccurring and planing redesign of the infrastructure so that downtime can be minimised. It is about learning from mistakes.

**Source:** _linoxide.com_

#### Q7: How is DevOps different from Agile/SDLC? ⭐⭐
**Answer:**
* Agile software development methodology focuses on the development of software.
* DevOps on the other hand is responsible for development as well as deployment of the software in the safest and most reliable way possible.


**Source:** _edureka.co_

#### Q8: What are the success factors for Continuous Integration? ⭐⭐
**Answer:**
*   Maintain a code repository
*   Automate the build
*   Make the build self-testing
*   Everyone commits to the baseline every day
*   Every commit (to baseline) should be built
*   Keep the build fast
*   Test in a clone of the production environment
*   Make it easy to get the latest deliverables
*   Everyone can see the results of the latest build
*   Automate deployment

**Source:** _edureka.co_

#### Q9: How have you handled failed deployments? ⭐⭐
**Answer:**


**Source:** _logz.io_

#### Q10: Why is Continuous monitoring necessary? ⭐⭐
**Answer:**
*Continuous Monitoring* allows timely identification of problems or weaknesses and quick corrective action that helps reduce expenses of an organization. Continuous monitoring provides solution that addresses three operational disciplines known as:

* continuous audit
* continuous controls monitoring
* continuous transaction inspection

**Source:** _quora.com_

#### Q11: Which are the top DevOps tools? Which tools have you worked on? ⭐⭐
**Answer:**
The most popular DevOps tools are:

*   **Git**: Version Control System tool
*   **Jenkins**: Continuous Integration tool
*   **Selenium**: Continuous Testing tool
*   **Puppet, Chef, Ansible**: Configuration Management and Deployment tools
*   **Nagios**: Continuous Monitoring tool
*   **Docker**: Containerization tool

**Source:** _edureka.co_

#### Q12: Mention what are the key aspects or principle behind DevOps? ⭐⭐
**Answer:**
The key aspects or principle behind DevOps are:

* Infrastructure as code
* Continuous deployment
* Automation
* Monitoring
* Security

**Source:** _quora.com_

#### Q13: What's the next thing you would automate in your current workflow? ⭐⭐
**Answer:**


**Source:** _github.com_

#### Q14: Can we consider DevOps as an Agile methodology? ⭐⭐
**Answer:**
*DevOps* is a movement to reconcile and synchronize development and production start through a set of good practices . Its emergence is motivated by a deep changing demands of business, who want to speed up the changes to stick closer to the requirements of business and the customer.

**Source:** _linoxide.com_

#### Q15: What is DevOps engineer's duty with regards to Agile development? ⭐⭐
**Answer:**
DevOps engineer work very closely with Agile development teams to ensure they have an environment necessary to support functions such as automated testing, continuous Integration and continuous Delivery. DevOps engineer must be in constant contact with the developers and make all required parts of environment work seamlessly.

**Source:** _linoxide.com_

#### Q16: What does Containerization mean? ⭐⭐
**Answer:**
*Containerisation* is a type of *virtualization* strategy that emerged as an alternative to traditional hypervisor-based virtualization. 

In containerization, the operating system is shared by the different containers rather than cloned for each virtual machine. For example Docker provides a container virtualization platform that serves as a good alternative to hypervisor-based arrangements.

**Source:** _linoxide.com_

#### Q17: What is the function of CI (Continuous Integration) server? ⭐⭐
**Answer:**
CI server function is to continuously integrate all changes being made and committed to repository by different developers and check for compile errors. It needs to build code several times a day, preferably after every commit so it can detect which commit made the breakage if the breakage happens.

**Source:** _linoxide.com_

#### Q18: What are the advantages of DevOps? ⭐⭐
**Answer:**
Technical benefits:

*   Continuous software delivery
*   Less complex problems to fix
*   Faster resolution of problems

Business benefits:

*   Faster delivery of features
*   More stable operating environments
*   More time available to add value (rather than fix/maintain)

**Source:** _edureka.co_

#### Q19: What is the role of a configuration management tool in DevOps? ⭐⭐
**Answer:**
*Configuration Management* tools' purpose is to automatize deployment and configuration of software on big number of servers. Most CM tools usually use agent architecture which means that every machine being manged needs to have agent installed. 

One tool that uses agentless architecture is Ansible. It only requires SSH and Python. And if raw module is being used, not even Python is required because it can run raw bash commands. Other available and popular CM tools are Puppet, Chef, SaltStack.

**Source:** _linoxide.com_

#### Q20: Tell me about the worst-run/best-run outage you’ve been a part of. What made it bad/well-run? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q21: How would you make key aspects of a software system traceable? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q22: If something breaks in production, how do you know about it? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q23: What is the difference between resource allocation and resource provisioning? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q24: What is Chef? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q25: How do all DevOps tools work together? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q26: What are the differences between continuous integration, continuous delivery, and continuous deployment? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q27: Explain a use case for Docker ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q28: Explain Blue-Green Deployment Technique ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q29: How would you assess how “deployable” a system is? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q30: How would you prepare for a migration from one platform to another? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q31: Classify Cloud Platforms by category ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q32: What's the difference between a blue/green deployment and a rolling deployment? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q33: What do you know about serverless model? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q34: What is Vagrant and what is it used for? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q35: How is container different from a virtual machine? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q36: How would you deploy software to 5000 nodes? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q37: What is Continuous Monitoring? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q38: How would you introduce Continuous Delivery in a successful, huge company for which the change from Waterfall to Continuous Delivery would be not trivial, because of the size and complexity of the business? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q39: What is Canary Releasing? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

## [[⬆]](#toc) <a name=Docker>Docker</a> Interview Questions
#### Q1: What is Docker? ⭐
**Answer:**
* Docker is a containerization platform which packages your application and all its dependencies together in the form of containers so as to ensure that your application works seamlessly in any environment be it development or test or production.
* Docker containers, wrap a piece of software in a complete filesystem that contains everything needed to run: code, runtime, system tools, system libraries etc. anything that can be installed on a server.
* This guarantees that the software will always run the same, regardless of its environment.

**Source:** _edureka.co_

#### Q2: What is Build Cache in Docker? ⭐⭐
**Answer:**
When we build an Image, Docker will process each line in Dockerfile. It will execute the commands on each line in the order that is mentioned in the file. But at each line, before running any command, Docker will check if there is already an existing image in its cache that can be reused rather than creating a new image.

**Source:** _mindmajix.com_

#### Q3: What’s the difference between a repository and a registry? ⭐⭐
**Answer:**
* **Docker registry** is a service for hosting and distributing images (the default one is the Docker Hub). 
* **Docker repository** is a collection of related Docker images (the same name but with different tags).

**Source:** _rafalgolarz.com_

#### Q4: What is the difference between ‘docker run’ and ‘docker create’? ⭐⭐
**Answer:**
The primary difference is that using **‘docker create’** creates a container in a stopped state.

**Bonus point:** You can use **‘docker create’** and store an outputed container ID for later use. The best way to do it is to use **‘docker run’** with -**\-cidfile FILE\_NAME** as running it again won’t allow to overwrite the file. A good practice is to keep well ogranised directory structure: /containers/web/server1/ws.cid containers/web/server3/ws.cid

**Source:** _rafalgolarz.com_

#### Q5: Can you remove (‘docker rm’) a container that is paused? ⭐⭐
**Answer:**
No, to remove a container it must be stopped first.

**Source:** _rafalgolarz.com_

#### Q6: When would you use ‘docker kill’ or ‘docker rm -f’? ⭐⭐
**Answer:**
If you must stop the container really quickly… (someone pushed something to production on Friday evening?… ;) )

**Source:** _rafalgolarz.com_

#### Q7:  How to link containers? ⭐⭐
**Answer:**
The simplest way is to use network port mapping. There’s also the **\- -link** flag which is deprecated.

**Source:** _rafalgolarz.com_

#### Q8: What is the difference between a Docker image and a container? ⭐⭐
**Answer:**
An instance of an image is called a container. You have an image, which is a set of layers. If you start this image, you have a running container of this image. You can have many running containers of the same image.

You can see all your images with `docker images` whereas you can see your running containers with `docker ps` (and you can see all containers with `docker ps -a`).

So a running instance of an image is a container.

**Source:** _stackoverflow.com_

#### Q9: What type of applications - Stateless or Stateful are more suitable for Docker Container? ⭐⭐
**Answer:**
It is preferable to create Stateless application for Docker Container. We can create a container out of our application and take out the configurable state parameters from application. Now we can run same container in Production as well as QA environments with different parameters. This helps in reusing the same Image in different scenarios. Also a stateless application is much easier to scale with Docker Containers than a stateful application.

**Source:** _mindmajix.com_

#### Q10: What are the most common instructions in Dockerfile? ⭐⭐
**Answer:**

Some of the common instructions in Dockerfile are as follows:
*   **FROM**: We use FROM to set the base image for subsequent instructions. In every valid Dockerfile, FROM is the first instruction.
*   **LABEL**: We use LABEL to organize our images as per project, module, licensing etc. We can also use LABEL to help in automation.  
    In LABEL we specify a key value pair that can be later used for programmatically handling the Dockerfile.
*   **RUN**: We use RUN command to execute any instructions in a new layer on top of the current image. With each RUN command we add something on top of the image and use it in subsequent steps in Dockerfile.
*   **CMD**: We use CMD command to provide default values of an executing container. In a Dockerfile, if we include multiple CMD commands, then only the last instruction is used.

**Source:** _knowledgepowerhouse.com_

#### Q11: How to build envrionment-agnostic systems with Docker? ⭐⭐
**Answer:**
There are three main features helping to achieve that:

*   Volumes
*   Environment variable injection
*   Read-only file systems

**Source:** _rafalgolarz.com_

#### Q12: What is the difference between the `COPY` and `ADD` commands in a Dockerfile? ⭐⭐
**Answer:**
Although `ADD` and `COPY` are functionally similar, generally speaking, `COPY` is preferred. 

That’s because it’s more transparent than ADD. COPY only supports the basic copying of local files into the container, while ADD has some features (like local-only tar extraction and remote URL support) that are not immediately obvious. Consequently, the best use for ADD is local tar file auto-extraction into the image, as in ADD rootfs.tar.xz /.

**Source:** _stackoverflow.com_

#### Q13: What is the difference between CMD and ENTRYPOINT in a Dockerfile? ⭐⭐
**Answer:**
Both `CMD` and `ENTRYPOINT` instructions define what command gets executed when running a container. There are few rules that describe their co-operation.
 
1. Dockerfile should specify at least one of `CMD` or `ENTRYPOINT` commands.
2. `ENTRYPOINT` should be defined when using the container as an executable.
3. `CMD` should be used as a way of defining default arguments for an `ENTRYPOINT` command or for executing an ad-hoc command in a container.
4. `CMD` will be overridden when running the container with alternative argumen

**Source:** _stackoverflow.com_

#### Q14: How do I transfer a Docker image from one machine to another one without using a repository, no matter private or public? ⭐⭐
**Answer:**
You will need to save the Docker image as a tar file:

```sh
docker save - o <path for generated tar file> <image name>
```

Then copy your image to a new system with regular file transfer tools such as `cp` or `scp`. After that you will have to load the image into Docker:

```sh
docker load -i <path to image tar file>
```

**Source:** _stackoverflow.com_

#### Q15: Is there a way to identify the status of a Docker container? ⭐⭐
**Answer:**
We can identify the status of a Docker container by running the command 

```sh
docker ps –a
```

which will in turn list down all the available docker containers with its corresponding statuses on the host. From there we can easily identify the container of interest to check its status correspondingly.

**Source:** _mindmajix.com_

#### Q16: What is Docker image? ⭐⭐
**Answer:**
**Docker image** is the source of Docker container. In other words, Docker images are used to create containers. Images are created with the build command, and they’ll produce a container when started with run. Images are stored in a Docker registry such as ` registry.hub.docker.com` because they can become quite large, images are designed to be composed of layers of other images, allowing a minimal amount of data to be sent when transferring images over the network.

**Source:** _edureka.co_

#### Q17: What is Docker container? ⭐⭐
**Answer:**
**Docker containers** include the application and all of its dependencies, but share the kernel with other containers, running as isolated processes in user space on the host operating system. Docker containers are not tied to any specific infrastructure: they run on any computer, on any infrastructure, and in any cloud.

**Source:** _edureka.co_

#### Q18: What is Docker hub? ⭐⭐
**Answer:**
**Docker hub** is a cloud-based registry service which allows you to link to code repositories, build your images and test them, stores manually pushed images, and links to Docker cloud so you can deploy images to your hosts. It provides a centralized resource for container image discovery, distribution and change management, user and team collaboration, and workflow automation throughout the development pipeline.

**Source:** _edureka.co_

#### Q19: Do I lose my data when the Docker container exits? ⭐⭐
**Answer:**
There is no loss of data when any of your Docker containers exits as any of the data that your application writes to the disk in order to preserve it. This will be done until the container is explicitly deleted. The file system for the Docker container persists even after the Docker container is halted.

**Source:** _mindmajix.com_

#### Q20: What are the various states that a Docker container can be in at any given point in time? ⭐⭐
**Answer:**
There are four states that a Docker container can be in, at any given point in time. Those states are as given as follows:

* Running
* Paused
* Restarting
* Exited

**Source:** _mindmajix.com_

#### Q21: What is the difference between “expose” and “publish” in Docker? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q22: Explain basic Docker usage workflow ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q23: Should I use Vagrant or Docker for creating an isolated environment? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q24: What is the difference between Docker Image and Layer? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q25: What happens if you add more than one CMD instruction to a Dockerfile? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q26: What is virtualisation? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q27: What is the difference between CMD and ENTRYPOINT in a Dockerfile? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q28: Can you create containers wihout their own PID namespace? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q29: Docker Compose vs. Dockerfile - which is better? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q30: What is Hypervisor? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q31: Could you explain what is Emulation? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q32: What is the default CPU limit set for a container? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q33: What is the purpose of EXPOSE command in Dockerfile? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q34: What is Docker Swarm? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q35: How will you monitor Docker in production? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q36: What is the preferred way of removing containers - ‘docker rm -f’ or ‘docker stop’ then followed by a ‘docker rm’? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q37: How can we control the startup order of services in Docker compose? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q38: What exactly do you mean by “Dockerized node”? Can this node be on-premises or in the cloud? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q39: How is Docker different from a virtual machine? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q40: Is it possible to generate a Dockerfile from an image? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q41: Can you explain dockerfile ONBUILD instruction? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q42: When you limit the memory for a container, does it reserve (guarantee) the memory? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q43: What is the difference between Docker RUN, CMD and ENTRYPOINT? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q44: What is an orphant volume and how to remove it? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q45: What are the different kinds of namespaces available in a Container? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q46: Is it good practice to run stateful applications on Docker? What are the scenarios where Docker best fits in? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q47: How virtualization works at low level? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q48: What is Paravirtualization? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q49: Can you run Docker containers natively on Windows? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q50: Name some limitations of containers vs VM ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q51: How does Docker run containers in non-Linux systems? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q52: How containers works at low level? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q53: Why did Docker jump from version 1.13 to 17.03? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q54: Why Docker compose does not wait for a container to be ready before moving on to start next service in dependency order? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q55: How to use Docker with multiple environments? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

## [[⬆]](#toc) <a name=EntityFramework>Entity Framework</a> Interview Questions
#### Q1: Explain what is ADO.NET entity framework? ⭐
**Answer:**
**ADO.NET Entity Framework** is an ORM (Object Relational Mapping) framework developed by Microsoft. It is an extension of ADO.NET that provides an automated mechanism to access and store data in the database. With the help of ADO.NET, database can be accessed without much required programming or code.

**Source:** _career.guru99.com_

#### Q2: What are the benefits of using EF? ⭐
**Answer:**
The main and the only benefit of EF is it auto-generates code for the Model (middle layer), Data Access Layer, and mapping code, thus reducing a lot of development time.

**Source:** _codeproject.com_

#### Q3: What is Entity Framework? ⭐
**Answer:**
ADO.NET EF is an ORM (object-relational mapping) which creates a higher abstract object model over ADO.NET components. So rather than getting into dataset, datatables, command, and connection objects as shown in the below code, you work on higher level domain objects like customers, suppliers, etc.

**Source:** _codeproject.com_

#### Q4: What are scalar and navigation properties in Entity Framework? ⭐⭐
**Answer:**
* _Scalar properties_ are those where actual values are contained in the entities. Normally a scalar property will map to a database field.
* _Navigation properties_ help to navigate from one entity to another entity directly in the code.

**Source:** _codeproject.com_

#### Q5: What are the different ways of creating these domain / entity objects? ⭐⭐
**Answer:**
Entity objects can be created in two ways: from a database structure, or by starting from scratch by creating a model.

**Source:** _codeproject.com_

#### Q6: What is pluralize and singularize in the Entity Framework? ⭐⭐
**Answer:**
“Pluralize” and “Singularize” give meaningful naming conventions to objects. In simple words it says do you want to represent your objects with the below naming convention:

*   One Customer record means “Customer” (singular).
*   Lot of customer records means “Customer’s” (plural, watch the “s”)

**Source:** _codeproject.com_

#### Q7: What is migration in Entity Framework? ⭐⭐
**Answer:**
Entity Framework introduced a migration tool that automatically updates the database schema when your model changes without losing any existing data or other database objects.

There are two kinds of Migration:

* Automated Migration
* Code-based Migration

**Source:** _entityframeworktutorial.net_

#### Q8: What is Code First approach in Entity Framework? ⭐⭐
**Answer:**
In **Code First** approach we avoid working with the Visual Designer of Entity Framework. In other words the EDMX file is excluded from the solution. So you now have complete control over the context class as well as the entity classes.

**Source:** _codeproject.com_

#### Q9: How can we read records using Entity Framework classes? ⭐⭐
**Answer:**
In order to browse through records you can create the object of the context class and inside the context class you will get the records.

For instance, in the below code snippet we are looping through a customer object collection. This customer collection is the output given by the context class `CustomermytextEntities`.

```csharp
CustomermytestEntities obj = new CustomermytestEntities();
foreach (Customer objCust in obj.Customers)
{}
```

**Source:** _codeproject.com_

#### Q10: What is the purpose of a DBContext class? ⭐⭐
**Answer:**
You can think of `DbContext` as the database connection and a set of tables, and `DbSet` as a representation of the tables themselves. The `DbContext` allows you to link your model properties (presumably using the Entity Framework) to your database with a connection string. 

Later, when you wish to refer to a database in your controller to handle data, you reference the `DbContext`.

**Source:** _stackoverflow.com_

#### Q11: What is Mapping? ⭐⭐
**Answer:**
The Mapping will have the information on how the Conceptual Models are mapped to Storage Models.

**Source:** _a4academics.com_

#### Q12: What is Conceptual Model? ⭐⭐
**Answer:**
**Conceptual Models** are the model classes which contain the relationships. These are independent of the database design.

**Source:** _a4academics.com_

#### Q13: What is Storage Model? ⭐⭐
**Answer:**
**Storage Models** are our database design models, which contains database tables, views, stored procs and keys with relationships.

**Source:** _a4academics.com_

#### Q14: Mention in what all scenarios Entity Framework can be applicable? ⭐⭐
**Answer:**
Entity Framework can be applicable in three scenarios

* If you have an existing database already or you want to build your database first than other parts of the application
* If your prime focus is your domain classes and then create the database from your domain classes
* If you want to design your database schema on the visual designer and create the classes and database

**Source:** _career.guru99.com_

#### Q15: Mention what is Code First approach and Model First Approach in Entity Framework? ⭐⭐
**Answer:**
In Entity Framework,

*   **Model First Approach:** In this approach we create entities, relationships directly on the design surface of EDMX.
*   **Code Approach:** For code approach we avoid working with the visual designer or entity framework.

**Source:** _career.guru99.com_

#### Q16: What are the components of Entity Framework Architecture? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q17: What are the advantages of Model First Approach? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q18: What are the advantages and disadvantages of Database First Approach? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q19: How can we handle concurrency in Entity Framework? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q20: What are the different approaches supported in the Entity Framework to create Entity Model? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q21: What is EF Data Access Architecture? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q22: What is the importance of EDMX file in Entity Framework? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q23: Can you explain lazy loading in a detailed manner? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q24: What is the role of Entity Client Data Provider? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q25: What is eager loading? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q26: What are POCO classes in Entity Framework? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q27: How do I delete multiple rows in Entity Framework (without foreach)? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q28: What are complex types in Entity Framework? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q29: Could you explain the difference between Optimistic vs Pessimistic locking? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q30: What are the advantages/disadvantages of Code First Approach? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q31: Explain Lazy loading, Eager Loading, and Explicit Loading? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q32: Explain how you can load related entities in EF? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q33: What is Optimistic locking? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q34: What’s the difference between LINQ to SQL and Entity Framework? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q35: Name some differences between Express vs Recoverable messages ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q36: What is faster - ADO.NET or ADO.NET Entity Framework? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q37: Is DbContext thread safe? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q38: What are the disadvantages of using static DbContext? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q39: Can you explain CSDL, SSDL and MSL sections in an EDMX file? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q40: What is the difference between ObjectContext and DbContext? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q41: What is the difference between Code First, Model First and Database First? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q42: How can you enhance the performance of Entity Framework? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q43: Which type of loading is good in which scenario? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q44: When would you use EF6 vs EF Core? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q45: What is the difference between POCO, Code First, and simple EF approach? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q46: What type of system generated messages do you know? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q47: What are T4 templates? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q48: Could you explain pessimistic locking? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q49: What is the difference between Automatic Migration vs Code-base Migration? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q50: How can we do pessimistic locking in Entity Framework? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q51: How do I view the SQL generated by the Entity Framework? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q52: What difference does .AsNoTracking() make? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q53: What's the difference between .SaveChanges() and .AcceptAllChanges()? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q54: When would you use SaveChanges(false) + AcceptAllChanges()? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q55: What are the advantages and disadvantages of creating a global entities context for the application (i.e. one static instance)? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q56: What is client wins and store wins mode in Entity Framework concurrency? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q57: Can I use Entity Framework 6 (not core) in .Net Core? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

## [[⬆]](#toc) <a name=Flutter>Flutter</a> Interview Questions
#### Q1: When to use main Axis Alignment and cross Axis Alignment? ⭐
**Answer:**
**For Row:**  
`mainAxisAlignment` = Horizontal Axis   
`crossAxisAlignment` = Vertical Axis

![enter image description here](https://i.stack.imgur.com/aypHr.png)

**For Column:**
  
`mainAxisAlignment` = Vertical Axis      
`crossAxisAlignment` = Horizontal Axis

![enter image description here](https://i.stack.imgur.com/eseWF.png)


[Image source](https://flutter.dev/docs/development/ui/layout#aligning-widgets)

**Source:** _stackoverflow.com_

#### Q2: What is Flutter? ⭐
**Answer:**
**Flutter** is an open-source UI toolkit from *Google* for crafting beautiful, natively compiled applications for desktop, web, and mobile from a single codebase. Flutter apps are built using the *Dart* programming language.


**Source:** _flutter.dev_

#### Q3: What is the pubspec.yaml file and what does it do? ⭐⭐
**Answer:**
- The `pubspec.yaml` file allows you to define the packages your app relies on, declare your assets like images, audio, video, etc. 
- It allows you to set constraints for your app. 
- For Android developers, this is roughly similar to a `build.gradle` file.

**Source:** _medium.com_

#### Q4: When should you use WidgetsBindingObserver? ⭐⭐
**Answer:**
WidgetsBindingObserver should be used when we want to listen to the `AppLifecycleState` and call stop/start on our services.

**Source:** _www.filledstacks.com_

#### Q5: What is the difference between "main()" and "runApp()" functions in Flutter? ⭐⭐
**Answer:**
- `main ()` function came from *Java*-like languages so it's where all program started, without it, you can't write any program on Flutter even without UI.
- `runApp()` function should return *Widget* that would be attached to the screen as a root of the *Widget Tree* that will be rendered.

**Source:** _stackoverflow.com_

#### Q6: What is the difference between Expanded and Flexible widgets? ⭐⭐
**Answer:**
`Expanded` is just a shorthand for `Flexible`

Using expanded this way:
```dart
Expanded(
	child: Foo(),
);
```
is strictly equivalent to:
```dart
Flexible(
	fit: FlexFit.tight,
	child: Foo(),
);
```

You may want to use `Flexible` over `Expanded` when you want a different `fit`, useful in some responsive layouts.

The difference between `FlexFit.tight` and `FlexFit.loose` is that loose will allow its child to have a maximum size while tight forces that child to fill all the available space.

**Source:** _stackoverflow.com_

#### Q7: How is Flutter different from a WebView based application? ⭐⭐
**Answer:**
- Code you write for a **WebView** or an app that runs similarly has to go through multiple layers to finally get executed (like Cordova for Ionic).** In essence, Flutter leapfrogs that by **compiling down to native **ARM** code to execute on both platforms. 
- “Hybrid” apps are slow, sluggish and look different from the platform they run on. *Flutter* apps run much, much faster than their hybrid counterparts. 
- It’s much easier to access native components and sensors using plugins rather than using **WebView** which can’t take full use of their platform.

**Source:** _medium.com_

#### Q8: What is the pubspec.yaml file and what does it do? ⭐⭐
**Answer:**
The `Pubspec.yaml` allows you to define the packages your app relies on, declare your assets like images, audio, video, etc. It also allows you to set constraints for your app. For Android developers, this is roughly similar to a `build.gradle` file, but the differences between the two are also evident.

**Source:** _medium.com_

#### Q9: What is a "widget" and mention its importance in Flutter? ⭐⭐
**Answer:**
- Widgets are basically the UI components in Flutter.
- It is a way to describe the configuration of an *Element*.
- They are inspired from components in **React**.

Widgets are important in Flutter because everything within a Flutter application is a  **Widget**  , from a simple “_Text”_  to “_Buttons”_  to “_Screen Layouts”_.

**Source:** _stackoverflow.com_

#### Q10: What is Dart and why does Flutter use it? ⭐⭐
**Answer:**
**Dart** is an *object-oriented*, *garbage-collected* programming language that you use to develop Flutter apps.
It was also created by Google, but is open-source, and has community inside and outside Google.
Dart was chosen as the language of **Flutter** for the following reason: 
- Dart is **AOT** (Ahead Of Time) compiled to fast, predictable, native code, which allows almost all of Flutter to be written in Dart. This not only makes Flutter fast, virtually everything (including all the widgets) can be customized.
- Dart can also be **JIT** (Just In Time) compiled for exceptionally fast development cycles and game-changing workflow (including Flutter’s popular sub-second stateful hot reload).
- Dart allows Flutter to avoid the need for a separate declarative layout language like *JSX* or *XML*, or separate visual interface builders, because Dart’s declarative, programmatic layout is easy to read and visualize. And with all the layout in one language and in one place, it is easy for Flutter to provide advanced tooling that makes layout a snap.

**Source:** _hackernoon.com_

#### Q11: What is an App state?  ⭐⭐
**Answer:**
- State that is not *ephemeral*, that you want to share across many parts of your app, and that you want to keep between user sessions, is what we call **application state** (sometimes also called *shared state*).
- Examples of application state:
	-   User preferences
	-   Login info
	-   Notifications in a social networking app
	-   The shopping cart in an e-commerce app
	-   Read/unread state of articles in a news app

**Source:** _flutter.dev_

#### Q12: How many types of widgets are there in Flutter? ⭐⭐
**Answer:**
There are two types of widgets:
1.  **StatelessWidget** : A widget that does not require mutable state.
2.  **StatefulWidget**: A widget that has mutable state.

**Source:** _proandroiddev.com_

#### Q13: What are the different build modes in Flutter? ⭐⭐
**Answer:**
- The Flutter tooling supports three modes when compiling your app, and a headless mode for testing. 
- You choose a compilation mode depending on where you are in the development cycle.
- The modes are:
	- Debug
	- Profile
	- Release

**Source:** _flutter.dev_

#### Q14: What is Fat Arrow Notation in Dart and when do you use it? ⭐⭐
**Answer:**
The fat arrow syntax is simply a short hand for returning an expression and is similar to `(){ return expression; }`.

The fat arrow is for returning a single line, braces are for returning a code block.

Only an expression—not a statement—can appear between the arrow (`=>`) and the semicolon (`;`). For example, you can’t put an *if* statement there, but you can use a *conditional* expression
```dart
// Normal function
void function1(int a) {
  if (a == 3) {
    print('arg was 3');
  } else {
    print('arg was not 3');
  }
}

// Arrow Function
void function2(int a) => print('arg was ${a == 3 ? '' : 'not '}3');
```


**Source:** _stackoverflow.com_

#### Q15: Does Flutter work like a browser? How is it different from a WebView based application? ⭐⭐
**Answer:**
To answer this question simply: **Code you write for a WebView or an app that runs similarly has to go through multiple layers to finally get executed.** In essence, Flutter leapfrogs that by **compiling down to native ARM** code to execute on both platforms. “Hybrid” apps are slow, sluggish and look different from the platform they run on. Flutter apps run much, much faster than their hybrid counterparts. Also, it’s much easier to access native components and sensors using plugins rather than using WebViews which can’t take full use of their platform.

**Source:** _medium.com_

#### Q16: Do you know what Ephemeral state means?  ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q17: What is Streams in Flutter/Dart? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q18: Explain the different types of Streams? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q19: Why is the build() method on State and not Stateful Widget? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q20: Differentiate  StatelessWidget and StatefulWidget? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q21: What are packages and plugins in Flutter? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q22: What are keys in Flutter and when to use it? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q23: Explain Navigator Widget and its push pop functions in Flutter? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q24: When do we use double.INFINITY? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q25: How to get difference of lists in Flutter/Dart? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q26: Differentiate between required and optional parameters in Dart ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q27: What are Null-aware operators? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q28: What is debug mode and when do you use it? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q29: What is profile mode and when do you use it? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q30: What is release mode and when do you use it? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q31: Differentiate between named parameters and positional parameters in Dart? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q32: How would you execute code only in debug mode? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q33: What is the difference between Scaffold and Container in Flutter? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q34: What is ScopedModel / BLoC Pattern? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q35: How is InheritedWidget different from Provider? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q36: What are some pros of Flutter? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q37: Name some cons of using Flutter? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q38: Where are the layout files? Why doesn’t Flutter have layout files? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q39: Why do we pass functions to widgets? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q40: Differentiate between Hot Restart and Hot Reload? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q41: How do you check if an async void method is completed in Dart? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q42: How to declare async function as a variable in Dart? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q43: How to duplicate repeating items inside a Dart list? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q44: How is whenCompleted() different from then() in Future? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q45: When would you use App state or Ephemeral state over another?  ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q46: What is Future in Flutter/Dart? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q47: What is the purpose of SafeArea in Flutter? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q48: How do you convert a List into a Map in Dart? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q49: What is a difference between these operators "?? and ?." ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q50: What is the difference between React Native and Flutter in-depth? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q51: How does Dart AOT work? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q52: What are some pros and cons of Scoped Model vs BLoC and vice versa? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q53: What are Global Keys? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q54: What is a MediaQuery in Flutter and when do we use it? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q55: Why is exit(0) not preferred for closing an app? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q56: What's the difference between async and async* in Dart? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q57: What is the difference between double.INFINITY and MediaQuery? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q58: What are the similarities and differences of Future and Stream? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q59: Explain async, await in Flutter/Dart? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q60: How to compare two dates that are constructed differently in Dart? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q61: What does "non-nullable by default" mean in Dart? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q62: What does a class with a method named ._() mean in Dart/Flutter? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q63: Why should you use kReleaseMode instead of assert? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q64: How is AnimationController different from Timer? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q65: What is the difference between debug mode and profile mode? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q66: Why Are StatefulWidget and State Separate Classes? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q67: List some approaches for State management in Flutter ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q68: Explain Stateful Widget Lifecycle in details ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

## [[⬆]](#toc) <a name=Git>Git</a> Interview Questions
#### Q1: What is the command to write a commit message in Git? ⭐
**Answer:**
Use:
```sh
git commit -a
```

 -a on the command line instructs git to commit the new content of all tracked files that have been modified. You can use 
```sh
git add <file>
```
or 
```sh
git add -A
```

before git commit -a if new files need to be committed for the first time.


**Source:** _edureka.co_

#### Q2: What is difference between Git vs SVN? ⭐
**Answer:**
The main point in Git vs SVN debate boils down to this: Git is a distributed version control system (DVCS), whereas SVN is a centralized version control system.

**Source:** _medium.com_

#### Q3: What is Git? ⭐
**Answer:**
Git is a Distributed Version Control system (DVCS). It can track changes to a file and allows you to revert back to any particular change.

Its distributed architecture provides many advantages over other Version Control Systems (VCS) like SVN one major advantage is that it does not rely on a central server to store all the versions of a project’s files. 

**Source:** _edureka.co_

#### Q4: What's the difference between a "pull request" and a "branch"? ⭐⭐
**Answer:**
* A **branch** is just a separate version of the code.

* A **pull request** is when someone take the repository, makes their own branch, does some changes, then tries to merge that branch in (put their changes in the other person's code repository).

**Source:** _stackoverflow.com_

#### Q5: What is Git fork? What is difference between fork, branch and clone? ⭐⭐
**Answer:**
* A **fork** is a remote, server-side copy of a repository, distinct from the original. A fork isn't a Git concept really, it's more a political/social idea. 
* A **clone** is not a fork; a clone is a local copy of some remote repository.  When you clone, you are actually copying the entire source repository, including all the history and branches.
* A **branch** is a mechanism to handle the changes within a single repository in order to eventually merge them with the rest of code. A branch is something that is within a repository. Conceptually, it represents a thread of development.

**Source:** _stackoverflow.com_

#### Q6: What is the difference between "git pull" and "git fetch"? ⭐⭐
**Answer:**
In the simplest terms, `git pull` does a `git fetch` followed by a `git merge`.

* When you use `pull`, Git tries to automatically do your work for you. **It is context sensitive**, so Git will merge any pulled commits into the branch you are currently working in.  `pull` **automatically merges the commits without letting you review them first**. If you don’t closely manage your branches, you may run into frequent conflicts.

* When you `fetch`, Git gathers any commits from the target branch that do not exist in your current branch and **stores them in your local repository**. However, **it does not merge them with your current branch**. This is particularly useful if you need to keep your repository up to date, but are working on something that might break if you update your files. To integrate the commits into your master branch, you use `merge`.

**Source:** _stackoverflow.com_

#### Q7: How does the Centralized Workflow work? ⭐⭐
**Answer:**
The **Centralized Workflow** uses a central repository to serve as the single point-of-entry for all changes to the project. The default development branch is called master and all changes are committed into this branch.

Developers start by cloning the central repository. In their own local copies of the project, they edit files and commit changes. These new commits are stored locally.

To publish changes to the official project, developers *push* their local master branch to the central repository. Before the developer can publish their feature, they need to *fetch* the updated central commits and rebase their changes on top of them. 

Compared to other workflows, the Centralized Workflow has no defined pull request or forking patterns. 

**Source:** _atlassian.com_

#### Q8: You need to update your local repos. What git commands will you use? ⭐⭐
**Answer:**
It’s a two steps process. First you fetch the changes from a remote named origin:

```sh
git fetch origin
```
Then you merge a branch master to local:

```sh
git merge origin/master
```
Or simply:

```sh
git pull origin master
```
If origin is a default remote and ‘master’ is default branch, you can drop it eg. `git pull`.

**Source:** _samwize.com_

#### Q9: How to undo the most recent commits in Git? ⭐⭐
**Details:**
You accidentally committed wrong files to Git, but haven't pushed the commit to the server yet.
How can you undo those commits from the local repository?

**Answer:**
```sh
$ git commit -m "Something terribly misguided"      
$ git reset HEAD~                                   # copied the old head to .git/ORIG_HEAD
<< edit files as necessary >>                       
$ git add ...                                       
$ git commit -c ORIG_HEAD                           # will open an editor, which initially contains the log message from the old commit and allows you to edit it
```

**Source:** _stackoverflow.com_

#### Q10: Tell me the difference between HEAD, working tree and index, in Git? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q11: When should I use "git stash"? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q12: Explain the advantages of Forking Workflow ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q13: Could you explain the Gitflow workflow? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q14: You need to rollback to a previous commit and don't care about recent changes. What commands should you use? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q15: How to revert previous commit in git? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q16: What is "git cherry-pick"? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q17: What is a "bare git" repository? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q18: When would you use "git clone --bare" over "git clone --mirror" ? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q19: What is the "HEAD" in Git? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q20: How to remove a file from git without removing it from your file system? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q21: Can you explain what “git reset” does in plain english? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q22: Write down a sequence of git commands for a "Rebase Workflow" ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q23: What is difference between "git stash pop" and "git stash apply"? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q24: How do you make an existing repository bare? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q25: What is the difference between "git clone", "git clone --bare" and "git clone --mirror"? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q26: When would you use "git clone" over "git clone --bare" ? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q27: When would you use "git clone" over "git clone --mirror" ? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q28: Write down a git command to check difference between two commits ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q29: When do you use "git rebase" instead of "git merge"? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q30: Do you know how to easily undo a git rebase?  ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q31: How to amend older Git commit? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q32: What git command do you need to use to know who changed certain lines in a specific file? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q33: What are "git hooks"? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q34: What are the type of git hooks? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q35: What is "git bisect"? How can you use it to determine the source of a (regression) bug? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q36: How can you use "git bisect" to determine the source of a (regression) bug? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

## [[⬆]](#toc) <a name=Golang>Golang</a> Interview Questions
#### Q1: What is Go? ⭐
**Answer:**
**Go** is a general-purpose language designed with systems programming in mind. It was initially developed at Google in year 2007 by Robert Griesemer, Rob Pike, and Ken Thompson. It is strongly and statically typed, provides inbuilt support for garbage collection and supports concurrent programming. Programs are constructed using packages, for efficient management of dependencies. Go programming implementations use a traditional compile and link model to generate executable binaries.

**Source:** _tutorialspoint.com_

#### Q2: Is Go a new language, framework or library? ⭐
**Answer:**
**Go** isn't a library and not a framework, it's a new language. 

Go is mostly in the C family (basic syntax), with significant input from the Pascal/Modula/Oberon family (declarations, packages). Go does have an extensive library, called the runtime, that is part of every Go program. Although it is more central to the language, Go's runtime is analogous to libc, the C library. It is important to understand, however, that Go's runtime does not include a virtual machine, such as is provided by the Java runtime. Go programs are compiled ahead of time to native machine code.

**Source:** _golang.org_

#### Q3: Can you declared multiple types of variables in single declaration in Go? ⭐⭐
**Answer:**
Yes. Variables of different types can be declared in one go using type inference.

```go
var a, b, c =  3,  4,  "foo"  
```

**Source:** _tutorialspoint.com_

#### Q4: What is a pointer? ⭐⭐
**Answer:**
A **pointer variable** can hold the *address* of a variable.

Consider:
```go
var x =  5  var p *int p =  &x
fmt.Printf("x = %d",  *p)
```

Here `x` can be accessed by `*p`.

**Source:** _tutorialspoint.com_

#### Q5: Can you return multiple values from a function? ⭐⭐
**Answer:**
A Go function can return multiple values.

Consider:
```go
package main
import "fmt"

func swap(x, y string) (string, string) {
   return y, x
}
func main() {
   a, b := swap("Mahesh", "Kumar")
   fmt.Println(a, b)
}
```

**Source:** _tutorialspoint.com_

#### Q6: What are some advantages of using Go? ⭐⭐
**Answer:**
**Go** is an attempt to introduce a new, concurrent, garbage-collected language with fast compilation and the following benefits: 
* It is possible to compile a large Go program in a few seconds on a single computer.
* Go provides a model for software construction that makes dependency analysis easy and avoids much of the overhead of C-style include files and libraries.
* Go's type system has no hierarchy, so no time is spent defining the relationships between types. Also, although Go has static types, the language attempts to make types feel lighter weight than in typical OO languages.
* Go is fully garbage-collected and provides fundamental support for concurrent execution and communication.
* By its design, Go proposes an approach for the construction of system software on multicore machines.

**Source:** _golang.org_

#### Q7: Why the Go language was created? ⭐⭐
**Answer:**
**Go** was born out of frustration with existing languages and environments for systems programming. 

Go is an attempt to have:
* an interpreted, dynamically typed language with 
* the efficiency and safety of a statically typed, compiled language
* support for networked and multicore computing
* be fast in compilation

To meet these goals required addressing a number of linguistic issues: an expressive but lightweight type system; concurrency and garbage collection; rigid dependency specification; and so on. These cannot be addressed well by libraries or tools so a new language was born.


**Source:** _golang.org_

#### Q8: Explain this code ⭐⭐
**Details:**
In Go there are various ways to return a struct value or slice thereof. Could you explain the difference?

```go
type MyStruct struct {
    Val int
}

func myfunc() MyStruct {
    return MyStruct{Val: 1}
}

func myfunc() *MyStruct {
    return &MyStruct{}
}

func myfunc(s *MyStruct) {
    s.Val = 1
}
```

**Answer:**
Shortly: 
* the first returns a copy of the struct, 
* the second a pointer to the struct value created within the function, 
* the third expects an existing struct to be passed in and overrides the value.

**Source:** _stackoverflow.com_

#### Q9: What is dynamic type declaration of a variable in Go? ⭐⭐
**Answer:**
A *dynamic type variable declaration* requires compiler to interpret the type of variable based on value passed to it. Compiler don't need a variable to have type statically as a necessary requirement.

**Source:** _tutorialspoint.com_

#### Q10: What are Goroutines? ⭐⭐
**Answer:**
**Goroutines** are functions or methods that run concurrently with other functions or methods. Goroutines can be thought of as light weight threads. The cost of creating a Goroutine is tiny when compared to a thread. Its common for Go applications to have thousands of Goroutines running concurrently.

**Source:** _golangbot.com_

#### Q11: Let's talk variable declaration in Go. Could you explain what is a variable "zero value"? ⭐⭐
**Answer:**
Variable is the name given to a memory location to store a value of a specific type. There are various syntaxes to declare variables in go.

```go
// 1 - variable declaration, then assignment
var age int
age = 29

// 2 - variable declaration with initial value
var age2 int = 29

// 3 - Type inference
var age3 = 29

// 4 - declaring multiple variables
var width, height int = 100, 50

// 5 - declare variables belonging to different types in a single statement
var (  
      name1 = initialvalue1,
      name2 = initialvalue2
)
// 6 - short hand declaration
name, age4 := "naveen", 29 //short hand declaration
```

If a variable is not assigned any value, go automatically initialises it with the **zero value of the variable's type**. Go is strongly typed, so variables declared as belonging to one type cannot be assigned a value of another type.

**Source:** _golangbot.com_

#### Q12: What kind of type conversion is supported by Go? ⭐⭐
**Answer:**
Go is very strict about **explicit typing**. There is no automatic type promotion or conversion. Explicit type conversion is required to assign a variable of one type to another. 

Consider:
```go
i := 55      //int
j := 67.8    //float64
sum := i + int(j) //j is converted to int
```

**Source:** _golangbot.com_

#### Q13: What is static type declaration of a variable in Go? ⭐⭐
**Answer:**
*Static type variable declaration* provides assurance to the compiler that there is one variable existing with the given type and name so that compiler proceed for further compilation without needing complete detail about the variable. A variable declaration has its meaning at the time of compilation only, compiler needs actual variable declaration at the time of linking of the program.

**Source:** _tutorialspoint.com_

#### Q14: How to efficiently concatenate strings in Go? ⭐⭐
**Details:**
In Go, a `string` is a primitive type, which means it is read-only, and every manipulation of it will create a new string.

So if I want to concatenate strings many times without knowing the length of the resulting string, what's the best way to do it?

**Answer:**
Beginning with Go 1.10 there is a `strings.Builder`. A Builder is used to efficiently build a string using Write methods. It minimizes memory copying. The zero value is ready to use.

```go
package main

import (
    "strings"
    "fmt"
)

func main() {
    var str strings.Builder

    for i := 0; i < 1000; i++ {
        str.WriteString("a")
    }

    fmt.Println(str.String())
}
```

**Source:** _stackoverflow.com_

#### Q15: What are the benefits of using Go programming? ⭐⭐
**Answer:**
Following are the benefits of using Go programming:

*   Support for environment adopting patterns similar to dynamic languages. For example type inference (`x := 0` is valid declaration of a variable `x` of type `int`).
*   Compilation time is fast.
*   In built concurrency support: light-weight processes (via goroutines), channels, select statement.
*   Conciseness, Simplicity, and Safety.
*   Support for Interfaces and Type embedding.
*   The go compiler supports static linking. All the go code can be statically linked into one big fat binary and it can be deployed in cloud servers easily without worrying about dependencies.

**Source:** _tutorialspoint.com_

#### Q16: Does Go have exceptions? ⭐⭐
**Answer:**
No, Go takes a different approach. For plain error handling, Go's **multi-value returns** make it easy to report an error without overloading the return value. Go code uses error values to indicate an abnormal state. 

Consider:
```go
func Open(name string) (file *File, err error)
```
```go
f, err := os.Open("filename.ext")
if err != nil {
    log.Fatal(err)
}
// do something with the open *File f
```

**Source:** _golang.org_

#### Q17: What is "rune" type in Go? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q18: Name some advantages of Goroutines over threads ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q19: How to initialise a struct in Go? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q20: Is Go an object-oriented language? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q21: How to check if a map contains a key in Go? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q22: Is there a foreach construct in the Go language? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q23: Implement a function that reverses a slice of integers ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q24: Can Go have optional parameters?  ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q25: Have you worked with Go 2? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q26: What is the preferred way to handle configuration parameters for a Go program? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q27: What is the difference between the = and := operator?  ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q28: What would you do if you need a hash displayed in a fixed order? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q29: What is the difference between C.sleep() and time.Sleep()? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q30: What are the differences between unbuffered and buffered channels? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q31: How to copy map in Go? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q32: Why would you prefer to use an empty struct{}? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q33: How do you swap two values? Provide a few examples. ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q34: What is so special about constants in Go? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q35: How does Go compile so quickly? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q36: What might be wrong with the following small program? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q37: How to find a type of an object in Go? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q38: When is the init() function run? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q39: Briefly describe how GC works in GO? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q40: What is the difference, if any, in the following two slice declarations, and which one is more preferable? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q41: List the functions can stop or suspend the execution of current goroutine, and explain their differences. ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q42: What is $GOROOT and $GOPATH? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q43: What is the idiomatic Go equivalent of C's ternary operator? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q44: What are the use(s) for tags in Go? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q45: How can I check if two slices are equal? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q46: What is an idiomatic way of representing enums in Go? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q47: What is the malloc threshold of Map object? How to modify it? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q48: How to compare two interfaces in Go? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q49: When go runtime allocates memory from heap, and when from stack? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

## [[⬆]](#toc) <a name=GraphQL>GraphQL</a> Interview Questions
#### Q1: Is GraphQL a Database Technology? ⭐
**Answer:**
No. GraphQL is often confused with being a database technology. This is a misconception, GraphQL is a _query language_ for APIs - not databases. In that sense it’s database agnostic and can be used with any kind of database or even no database at all.

**Source:** _howtographql.com_

#### Q2: What is GraphQL? ⭐
**Answer:**
GraphQL is a query language created by [Facebook](http://facebook.github.io/) in 2012 which provides a **common interface between the client and the server for data fetching and manipulations**.

The client asks for various data from the GraphQL server via queries. The response format is described in the query and defined by the client instead of the server: they are called **client‐specified queries**.  
The structure of the data is not hardcoded as in traditional REST APIs - this makes retrieving data from the server more efficient for the client.

**Source:** _howtographql.com_

#### Q3: Is GraphQL only for React / Javascript Developers? ⭐
**Answer:**
No. GraphQL is an API technology so it can be used in any context where an API is required.

On the _backend_, a GraphQL server can be implemented in any programming language that can be used to build a web server. Next to Javascript, there are popular reference implementations for Ruby, Python, Scala, Java, Clojure, Go and .NET.

Since a GraphQL API is usually operated over HTTP, any client that can speak HTTP is able to query data from a GraphQL server.

*Note*: GraphQL is actually transport layer agnostic, so you could choose other protocols than HTTP to implement your server.

**Source:** _howtographql.com_

#### Q4: What is an exclamation point in GraphQL? ⭐
**Answer:**
That means that the field is non-nullable. By default, all types in GraphQL are nullable. When non-null is applied to the type of a field, it means that if the server resolves that field to `null`, the response will _fail validation_.

**Source:** _stackoverflow.com_

#### Q5: How to do Error Handling? ⭐⭐
**Answer:**
A successful GraphQL query is supposed to return a JSON object with a root field called `"data"`. If the request fails or partially fails (e.g. because the user requesting the data doesn’t have the right access permissions), a second root field called `"errors"` is added to the response:
```js
    {
      "data": { ... },
      "errors": [ ... ]
    }
```   

**Source:** _howtographql.com_

#### Q6: Where is GraphQL useful? ⭐⭐
**Answer:**
GraphQL helps where your **client needs a flexible response** format to avoid extra queries and/or massive data transformation with the overhead of keeping them in sync.

Using a GraphQL server makes it very easy for a client side developer to change the response format without any change on the backend.

With GraphQL, you can describe the required data in a more natural way. It can speed up development, because in application structures like **top-down rendering** in React, the required data is more similar to your component structure.

**Source:** _blog.risingstack.com_

#### Q7: What is difference between Mutation and Query? ⭐⭐
**Answer:**
Technically any GraphQL _query_ could be implemented to cause a data write. But there is a convention that any operations that cause writes should be sent explicitly via a _mutation_.

Besides the difference in the semantic, there is one important technical difference:

Query fields can be executed in parallel by the GraphQL engine while Mutation top-level fields MUST execute serially according to the spec.

**Source:** _stackoverflow.com_

#### Q8: What is GraphQL schema? ⭐⭐
**Answer:**
Every GraphQL server has two core parts that determine how it works: a schema and resolve functions.

The *schema* is a model of the data that can be fetched through the GraphQL server. It defines what queries clients are allowed to make, what types of data can be fetched from the server, and what the relationships between these types are. 

Consider:

```css
type Author {
  id: Int
  name: String
  posts: [Post]
}
type Post {
  id: Int
  title: String
  text: String
  author: Author
}
type Query {
  getAuthor(id: Int): Author
  getPostsByTitle(titleContains: String): [Post]
}
schema {
  query: Query
}
```

**Source:** _dev-blog.apollodata.com_

#### Q9: How to do Authentication and Authorization? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q10: What kind of operations could GraphQL schema have? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q11: Explain the main difference between REST and GraphQL ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q12: Does GraphQL Support Offline Usage? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q13: How to do Server-side Caching? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q14: How to query all the GraphQL type fields without writing a long query? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q15: List the key concepts of the GraphQL query language ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q16: Can you make a GraphQL type both an input and output type? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q17: Are there any disadvantages to GraphQL? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q18: How to implement a set of GraphQL mutations in single transaction? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q19: How do you prevent nested attack on GraphQL server? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q20: Is it possible to use inheritance with GraphQL input types? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q21: What is AST in GraphQL? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q22: How to respond with different status code in GraphQL? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q23: What the criteria set is for deciding when to use GraphQL vs. HATEOAS? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q24: How would you model recursive data structures in GraphQL? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

## [[⬆]](#toc) <a name=HTML5>HTML5</a> Interview Questions
#### Q1: What is an iframe and how it works? ⭐
**Answer:**
An **iframe** is an **HTML document** which can be embedded inside another HTML page.

**Example**:

```html
<iframe src="https://github.com" height="300px" width="300px"></iframe>
```

**Source:** _github.com/FuelFrontend_

#### Q2: Explain meta tags in HTML ⭐
**Answer:**
- **Meta tags** always go inside **head tag** of the HTML page
- **Meta tags** is always passed as name/value pairs
- **Meta tags** are not displayed on the page but intended for the browser
- **Meta tags** can contain information about **character encoding**, **description**, **title** of the document etc,

**Example**:

```html
<!DOCTYPE html>
<html>
<head>
  <meta name="description" content="I am a web page with description"> 
  <title>Home Page</title>
</head>
<body>
  
</body>
</html>
```


**Source:** _github.com/FuelFrontend_

#### Q3: What is the purpose of the alt attribute on images? ⭐
**Answer:**
The `alt` attribute provides alternative information for an image if a user cannot view it. The `alt` attribute should be used to describe any images except those which only serve a decorative purposes, in which case it should be left empty.


**Source:** _developer.mozilla.org_

#### Q4: Write a HTML table tag sequence that outputs the following ⭐
**Answer:**
Write a HTML table tag sequence that outputs the following:
```
50 pcs 100 500
10 pcs 5 50
```

**Answer:**
```html
<table>
  <tr>
    <td>50 pcs</td>
    <td>100</td>
    <td>500</td>
  </tr>
  <tr>
    <td>10 pcs</td>
    <td>5</td>
    <td>50</td>
  </tr>
</table>
```

**Source:** _toptal.com_

#### Q5: What were some of the key goals and motivations for the HTML5 specification? ⭐⭐
**Answer:**
HTML5 was designed to replace HTML 4, XHTML, and the HTML DOM Level 2. The key goals and motivations behind the HTML5 specification were to:

* Deliver rich content (graphics, movies, etc.) without the need for additional plugins, such as Flash.
* Provide better semantic support for web page structure through new structural element tags.
* Provide a stricter parsing standard to simplify error handling, ensure more consistent cross-browser behaviour, and simplify compatibility with documents written to older standards.
* Provide better cross-platform support whether running on a PC, Tablet, or Smartphone.

**Source:** _toptal.com_

#### Q6: hat's the difference between an "attribute" and a "property" in HTML? ⭐⭐
**Answer:**
Attributes are defined on the HTML markup but properties are defined on the DOM. To illustrate the difference, imagine we have this text field in our HTML: `<input type="text" value="Hello">`.

```js
const input = document.querySelector('input');
console.log(input.getAttribute('value')); // Hello
console.log(input.value); // Hello
```

But after you change the value of the text field by adding "World!" to it, this becomes:

```js
console.log(input.getAttribute('value')); // Hello
console.log(input.value); // Hello World!
```

**Source:** _github.com/yangshun_

#### Q7: Briefly describe the correct usage of the following HTML5 semantic elements: <header>, <article>, <section>, <footer> ⭐⭐
**Answer:**
* `<header>` is used to contain introductory and navigational information about a section of the page. This can include the section heading, the author’s name, time and date of publication, table of contents, or other navigational information.

* `<article>` is meant to house a self-contained composition that can logically be independently recreated outside of the page without losing it’s meaining. Individual blog posts or news stories are good examples.

* `<section>` is a flexible container for holding content that shares a common informational theme or purpose.

* `<footer>` is used to hold information that should appear at the end of a section of content and contain additional information about the section. Author’s name, copyright information, and related links are typical examples of such content.


**Source:** _w3schools.com_

#### Q8: How Can I Get Indexed Better by Search Engines? ⭐⭐
**Answer:**
It is possible to get indexed better by placing the following two statements in the `<HEAD>` part of your documents:

```html
<META NAME="keywords" CONTENT="keyword keyword keyword keyword">
<META NAME="description" CONTENT="description of your site">
```
Both may contain up to 1022 characters. If a keyword is used more than 7 times, the keywords tag will be ignored altogether. Also, you cannot put markup (other than entities) in the description or keywords list.

**Source:** _freejavaguide.com_

#### Q9: What is Character Encoding? ⭐⭐
**Answer:**
To display an HTML page correctly, a web browser must know which character set (character encoding) to use. This is specified in the <meta> tag:

**HTML4:**
```html
<meta http-equiv="Content-Type" content="text/html;charset=ISO-8859-1">
```

**HTML5:**
```html
<meta charset="UTF-8">
```


**Source:** _w3schools.com_

#### Q10: What is the difference between span and div? ⭐⭐
**Answer:**
* `div` is a block element
* `span` is inline element 

For bonus points, you could point out that it’s illegal to place a block element inside an inline element, and that while `div` can have a `p` tag, and a `p` tag can have a `span`, it is not possible for `span` to have a `div` or `p` tag inside.

**Source:** _thatjsdude.com_

#### Q11: What is a self closing tag?  ⭐⭐
**Answer:**
In HTML5 it is not strictly necessary to close certain HTML tags. The tags that aren’t required to have specific closing tags are called “self closing” tags.

An example of a self closing tag is something like a line break (`<br />`) or the meta tag (`<meta>`). This means that the following are both acceptable:

```html
<meta charset="UTF-8">
...
<meta charset="UTF-8" />
```

**Source:** _blog.teamtreehouse.com_

#### Q12: How can you highlight text in HTML? ⭐⭐
**Answer:**
If you are working with an HTML5 page, the `<mark>` tag can be a quick and easy way of highlighting or marking text on a page:

```html
<mark>highlighted text</mark>
```

To highlight text with just HTML code and support for all browsers, set the background-color style, as shown in the example below, using the <span> HTML tag.
```html
<span style="background-color: #FFFF00">Yellow text.</span>
```

**Source:** _computerhope.com_

#### Q13: Can a web page contain multiple <header> elements? What about <footer> elements? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q14: What are `data-` attributes good for? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q15: Have you used different HTML templating languages before? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q16: How do you change the direction of html text? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q17: What is WebSQL? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q18: What is an optional tag? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q19: How do you serve a page with content in multiple languages? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q20: What is the difference between <section> and <div>? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q21: What does a DOCTYPE do? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q22: Explain almost standard, full standard and quirks mode ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q23: When is it appropriate to use the small element? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q24: What is the purpose of cache busting and how can you achieve it? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q25: Describe the difference between a 'cookie', 'sessionStorage' and 'localStorage'. ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q26: What are `defer` and `async` attributes on a `<script>` tag? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q27: What is the DOM? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q28: Discuss the differences between an HTML specification and a browser’s implementation thereof. ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q29: What are some differences that XHTML has compared to HTML? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q30: Where and why is the `rel="noopener"` attribute used? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q31: What is HTML5 Web Storage? Explain `localStorage` and `sessionStorage`. ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q32: What is WebSQL? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q33: Explain the difference between block elements and inline elements ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q34: How do you set IE compatibility mode? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q35: What's new in HTML 5? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q36: Explain the difference between cookies, session and local storage ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q37: What are Web Workers? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q38: Describe the difference between <script>, <script async> and <script defer>. ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q39: Why to use HTML5 semantic tags? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q40: What is WebP? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q41: What kind of things must you be wary of when designing or developing for multilingual sites? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q42: What is progressive rendering? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q43: What are the building blocks of HTML5? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q44: What's the difference between Full Standard, Almost Standard and Quirks Mode? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q45: Why you would use a `srcset` attribute in an image tag? Explain the process the browser uses when evaluating the content of this attribute. ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q46: HTML Markup Validity ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q47: How would you select svg or canvas for your site? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q48: What is an HTML preprocessor and are you using it? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q49: Why do I need a doctype and what does it do? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q50: What is the purpose of 'main' element? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q51: What are Web Components? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q52: What is accessibility & ARIA role means in a web application? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q53: Could you generate a public key in HTML? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q54: Why is it generally a good idea to position CSS <link>s between <head></head> and JS <script>s just before </body>? Do you know any exceptions? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q55: What is an IndexedDB? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

## [[⬆]](#toc) <a name=Ionic>Ionic</a> Interview Questions
#### Q1: What is Ionic Framework? ⭐
**Answer:**
**Ionic Framework** is an open source UI toolkit for building performant, high-quality mobile and desktop apps using web technologies (HTML, CSS, and JavaScript). Ionic Framework is focused on the frontend user experience, or UI interaction of an app (controls, interactions, gestures, animations). Currently, Ionic Framework has official integrations with Angular and React, and support for Vue is in development.

**Source:** _ionicframework.com_

#### Q2: How can you test Ionic applications? ⭐⭐
**Answer:**
Ionic v.1 applications are built using AngularJS. Angular has a rich set of test libraries and frameworks such as Jasmine and Karma test runner. These frameworks can be used to write unit tests for Ionic applications. Also, `ionic-CLI` provides `live reload` feature so the application can be tested in the browser. For example, the `ionic serve` command can be used to load the application in any browser. Thus, we can use Chrome Developer Tools or Mozilla Firefox with Firebug to debug and inspect Ionic applications.

**Source:** _toptal.com_

#### Q3: What is hybrid app development? ⭐⭐
**Answer:**
**Hybrid apps** are developed using web technologies like HTML, CSS and Javascript, and then wrapped in a native application using platforms like Cordova. The apps are shown in its own embedded browser, like UIWebView in iOS and WebView in Android (not Safari or Chrome). This allows you to use any web-native framework for mobile app development.

**Source:** _netguru.com_

#### Q4: Can we work with Ionic > 1 and AngularJS? ⭐⭐
**Answer:**
Unfortunately, **no**. Ionic (1) at a very high-level is essentially just a wrapper & directive/component library for AngularJS (1). In that same regard, Ionic 2 is built in the same way, utilizing all the benefits of Angular 2+.

Ionic 2 breaks away from being tied to the DOM in the browser, by using angular 2 which is the reason for the massive change between ionic 1.x and ionic 2.x. ( Angular 2.x architecture is not tied down to the DOM unlike the Angular 1.x ).

**Source:** _toptal.com_

#### Q5: How do you pass data from one view to another in Ionic applications? ⭐⭐
**Answer:**
Ionic v.1 uses AngularJS and UI-router. It means you can use Angular services or UI-router’s state `resolve` to pass data from one view to another. Since Angular services are singletons, data stored in services can be accessed across other Angular controllers.

As mentioned, UI-router provides a `resolve` configuration. For example:
```js
$stateProvider
  .state('todos', {
    url: '/todos',
    controller: 'TodosCtrl',
    templateUrl: 'todos.html',
    resolve: {
      todos: function(TodosService) {
        return TodosService.getTodos()
      }
    }
  })
```

One advantage of `resolve` over stateful services is better testing: as `resolve` injects dependencies in the controller, it is easy to test them.

When using Ionic v.4 you have 3 options:
1. Using Query Params (bad)
2. Service and Resolve Function (legit)
3. Using Router Extras State (new since Angular 7.2)

```js
 openDetailsWithState() {
    let navigationExtras: NavigationExtras = {
      state: {
        user: this.user
      }
    };
    this.router.navigate(['details'], navigationExtras);
  }
```

**Source:** _toptal.com_

#### Q6: What is the difference between Cordova and Ionic? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q7: How would you compare Ionic vs Flutter? When would you choose one? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q8: How do you persist data between application launches using Ionic? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q9: What are some possible security issues with Ionic apps? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q10: What is the advantage of caching the views in Ionic apps? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q11: How can you detect a platform (Android or iOS) at runtime in Ionic application? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q12: How can you access mobile phone native functionality in Ionic applications, for example the camera? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q13: What is the difference between PhoneGap, Cordova, and Ionic? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q14: What’s the difference between “ionic build” and “ionic prepare”? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q15: What are the most prominent advantages and disadvantages of building applications using the Ionic framework? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q16: How many Types of Storage Available in Ionic Framework? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q17: What is Capacitor? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q18: How to use observables in the Ionic framework? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q19: What is Ionic Native? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q20: What is the difference between Capacitor and Cordova? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q21:  What does it mean that Ionic became framework-agnostic? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q22: How can you render a 5000 item list in Ionic, without affecting scroll performance? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q23: How is the Ionic Framework v4 different from v3? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q24: If more than one component is trying to make an HTTP call to same URL, then how can you restrict making 2 network calls? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q25: What are the new features in Ionic 4? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q26: What Are The Ionic Lifecycle Events? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q27: What AOT and JIT and which is used by Ionic? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q28: Performance of Ionic application is bad on older Android devices. Why is this, and what can be done to improve it? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q29: What are some security measures should be made for Ionic app? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

## [[⬆]](#toc) <a name=JSON>JSON</a> Interview Questions
#### Q1: What is JSON and why would I use it? ⭐
**Answer:**
**JSON** (JavaScript Object Notation) is a lightweight format that is used for data interchanging. It is based on a subset of JavaScript language (the way objects are built in JavaScript). Some JavaScript is not JSON, and some JSON is not JavaScript.

**Source:** _stackoverflow.com_

#### Q2: What is the correct JSON content type? ⭐⭐
**Answer:**
The MIME media type for JSON text is **application/json**. The default encoding is UTF-8. (Source: RFC 4627).

**Source:** _stackoverflow.com_

#### Q3: How should I parse a JSON string in JavaScript? ⭐⭐
**Answer:**
The standard way to parse JSON in JavaScript is `JSON.parse()`

The JSON API was introduced with ES5 (2011) and has since been implemented in >99% of browsers by market share, and Node.js. Its usage is simple:

```js
const json = '{ "fruit": "pineapple", "fingers": 10 }';
const obj = JSON.parse(json);
console.log(obj.fruit, obj.fingers);
```

**Source:** _stackoverflow.com_

#### Q4: What are the limitations and uses of JSON? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q5: Can I use comments inside a JSON file? If so, how? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q6: Why must one use JSON over XML? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q7: Are Javascript objects and JSON equivalent? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q8: Explain the structure of JSON ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q9: What are the differences between JSON and JSONP? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q10: Explain the difference between JSON.stringify() and JSON.parse() ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q11: What is the difference between YAML and JSON? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q12: Which data format is the right one for JSON? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q13: Is there a standard on JSON naming?  ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q14: What is JSONP, and why was it created? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q15: How could I parse a JSON string in older browser? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

## [[⬆]](#toc) <a name=Java>Java</a> Interview Questions
#### Q1: What is JVM? Why is Java called the “Platform Independent Programming Language”?  ⭐
**Answer:**
A Java virtual machine (JVM) is a process virtual machine that can execute Java bytecode. Each Java source file is compiled into a bytecode file, which is executed by the JVM. Java was designed to allow application programs to be built that could be run on any platform, without having to be rewritten or recompiled by the programmer for each separate platform. A Java virtual machine makes this possible, because it is aware of the specific instruction lengths and other particularities of the underlying hardware platform.

**Source:** _github.com/snowdream_

#### Q2: What is a Servlet? ⭐
**Answer:**
The servlet is a Java programming language class used to process client requests and generate dynamic web content. Servlets are mostly used to process or store data submitted by an HTML form, provide dynamic content and manage state information that does not exist in the stateless HTTP protocol.

**Source:** _github.com/snowdream_

#### Q3: What is the Difference between JDK and JRE?  ⭐
**Answer:**
* **The Java Runtime Environment (JRE) **is basically the Java Virtual Machine (**JVM**) where your Java programs are being executed. It also includes browser plugins for applet execution. 

* **The Java Development Kit (JDK)** is the full featured Software Development Kit for Java, including the JRE, the compilers and tools (like JavaDoc, and Java Debugger), in order for a user to develop, compile and execute Java applications.

**Source:** _github.com/snowdream_

#### Q4: What is a JSP Page? ⭐
**Answer:**
A **Java Server Page (JSP)** is a text document that contains two types of text: 
* static data and 
* JSP elements. 

Static data can be expressed in any text-based format, such as HTML or XML. JSP is a technology that mixes static content with dynamically-generated content.

**Source:** _github.com/snowdream_

#### Q5: What is the difference between an Applet and a Java Application? ⭐
**Answer:**
* Applets are executed within a Java enabled browser, but a 
* Java application is a standalone Java program that can be executed outside of a browser. 

However, they both require the existence of a Java Virtual Machine (JVM). Furthermore, a Java application requires a main method with a specific signature, in order to start its execution. Java applets don’t need such a method to start their execution. Finally, Java applets typically use a restrictive security policy, while Java applications usually use more relaxed security policies.

**Source:** _github.com/snowdream_

#### Q6: What are the two types of Exceptions in Java? Which are the differences between them?  ⭐
**Answer:**
Java has two types of exceptions: checked exceptions and unchecked exceptions. 

1. **Unchecked exceptions **do not need to be declared in a method or a constructor’s throws clause, if they can be thrown by the execution of the method or the constructor, and propagate outside the method or constructor boundary. 

2. On the other hand, **checked exceptions** must be declared in a method or a constructor’s throws clause.

**Source:** _github.com/snowdream_

#### Q7: How do I efficiently iterate over each entry in a Java Map? ⭐⭐
**Answer:**
Consider:
```java
Map<String, String> map = ...
for (Map.Entry<String, String> entry : map.entrySet()) {
    System.out.println(entry.getKey() + "/" + entry.getValue());
}
```
In Java 8 you can do it clean and fast using the new lambdas features:
```java
final long[] i = {0};
map.forEach((k, v) -> i[0] += k + v);
```


**Source:** _stackoverflow.com_

#### Q8: Explain Serialization and Deserialization.  ⭐⭐
**Answer:**
Java provides a mechanism, called object serialization where an object can be represented as a sequence of bytes and includes the object’s data, as well as information about the object’s type, and the types of data stored in the object. Thus, serialization can be seen as a way of flattening objects, in order to be stored on disk, and later, read back and reconstituted. Deserialisation is the reverse process of converting an object from its flattened state to a live object.

**Source:** _github.com/snowdream_

#### Q9: What is the difference between an Interface and an Abstract class?  ⭐⭐
**Answer:**
Java provides and supports the creation both of **abstract** classes and **interfaces**. Both implementations share some common characteristics, but they differ in the following features:

* All methods in an interface are implicitly abstract. On the other hand, an abstract class may contain both abstract and non-abstract methods.
* A class may implement a number of Interfaces, but can extend only one abstract class.
* In order for a class to implement an interface, it must implement all its declared methods. However, a class may not implement all declared methods of an abstract class. Though, in this case, the sub-class must also be declared as abstract.
* Abstract classes can implement interfaces without even providing the implementation of interface methods.
* Variables declared in a Java interface is by default final. An abstract class may contain non-final variables.
* Members of a Java interface are public by default. A member of an abstract class can either be private, protected or public.
* An interface is absolutely abstract and cannot be instantiated. An abstract class also cannot be instantiated, but can be invoked if it contains a main method.

**Source:** _github.com/snowdream_

#### Q10: What are pass by reference and pass by value?  ⭐⭐
**Answer:**
* When an object is **passed by value**, this means that a copy of the object is passed. Thus, even if changes are made to that object, it doesn’t affect the original value. 
* When an object is **passed by reference**, this means that the actual object is not passed, rather a reference of the object is passed. Thus, any changes made by the external method, are also reflected in all places.

**Source:** _github.com/snowdream_

#### Q11: What is the difference between processes and threads? ⭐⭐
**Answer:**
The main difference between them is that 
* a **Process** is a program which is executing some code and 
* a **Thread** is an independent path of execution in the process. 

A process can have more than one thread for doing independent task e.g. a thread for reading data from disk, a thread for processing that data and another thread for sending that data over the network.

**Source:** _github.com/snowdream_

#### Q12: What’s the difference between sendRedirect and forward methods? ⭐⭐
**Answer:**
The sendRedirect method creates a new request, while the forward method just forwards a request to a new target. The previous request scope objects are not available after a redirect, because it results in a new request. On the other hand, the previous request scope objects are available after forwarding. FInally, in general, the sendRedirect method is considered to be slower compare to the forward method.

**Source:** _github.com/snowdream_

#### Q13: Explain the architechure of a Servlet. ⭐⭐
**Answer:**
The core abstraction that must be implemented by all servlets is the javax.servlet.Servlet interface. Each servlet must implement it either directly or indirectly, either by extending javax.servlet.GenericServlet or javax.servlet.http.HTTPServlet. Finally, each servlet is able to serve multiple requests in parallel using multithreading.

**Source:** _github.com/snowdream_

#### Q14: What are JSP actions? ⭐⭐
**Answer:**
JSP actions use constructs in XML syntax to control the behavior of the servlet engine. JSP actions are executed when a JSP page is requested. They can be dynamically inserted into a file, re-use JavaBeans components, forward the user to another page, or generate HTML for the Java plugin.Some of the available actions are listed below:

* jsp:include – includes a file, when the JSP page is requested.
* jsp:useBean – finds or instantiates a JavaBean.
* jsp:setProperty – sets the property of a JavaBean.
* jsp:getProperty – gets the property of a JavaBean.
* jsp:forward – forwards the requester to a new page.
* jsp:plugin – generates browser-specific code.


**Source:** _github.com/snowdream_

#### Q15: What are Expressions? ⭐⭐
**Answer:**
A JSP expression is used to insert the value of a scripting language expression, converted into a string, into the data stream returned to the client, by the web server. Expressions are defined between <% = and %> tags.

**Source:** _github.com/snowdream_

#### Q16: What are Decalarations? ⭐⭐
**Answer:**
Declarations are similar to variable declarations in Java. Declarations are used to declare variables for subsequent use in expressions or scriptlets. To add a declaration, you must use the sequences to enclose your declarations.

**Source:** _github.com/snowdream_

#### Q17: What does the “static” keyword mean? Can you override private or static method in Java? ⭐⭐
**Answer:**
The `static` keyword denotes that a member variable or method can be accessed, _without requiring an instantiation of the class to which it belongs_. 

A user cannot override static methods in Java, because method overriding is based upon dynamic binding at runtime and static methods are statically binded at compile time. A static method is not associated with any instance of a class so the concept is not applicable.

**Source:** _github.com/snowdream_

#### Q18: What are the basic interfaces of Java Collections Framework?  ⭐⭐
**Answer:**
**Java Collections Framework** provides a well designed set of interfaces and classes that support operations on a collections of objects. The most basic interfaces that reside in the Java Collections Framework are:

* **Collection**, which represents a group of objects known as its elements.
* **Set**, which is a collection that cannot contain duplicate elements.
* **List**, which is an ordered collection and can contain duplicate elements.
* **Map**,  which is an object that maps keys to values and cannot contain duplicate keys.

**Source:** _github.com/snowdream_

#### Q19: What are Directives? ⭐⭐
**Answer:**
What are the different types of Directives available in JSP ? Directives are instructions that are processed by the JSP engine, when the page is compiled to a servlet. Directives are used to set page-level instructions, insert data from external files, and specify custom tag libraries. Directives are defined between < %@ and % >.The different types of directives are shown below:

* Include directive: it is used to include a file and merges the content of the file with the current page.
* Page directive: it is used to define specific attributes in the JSP page, like error page and buffer.
* Taglib: it is used to declare a custom tag library which is used in the page.

**Source:** _github.com/snowdream_

#### Q20: What is an Iterator?  ⭐⭐
**Answer:**
The [Iterator](http://docs.oracle.com/javase/7/docs/api/java/util/Iterator.html) interface provides a number of methods that are able to iterate over any [Collection](http://docs.oracle.com/javase/7/docs/api/java/util/Collection.html). Each Java [Collection](http://docs.oracle.com/javase/7/docs/api/java/util/Collection.html) contains the [Iterator](http://docs.oracle.com/javase/7/docs/api/java/util/Iterator.html)  method that returns an [Iterator](http://docs.oracle.com/javase/7/docs/api/java/util/Iterator.html)  instance. Iterators are capable of removing elements from the underlying collection during the iteration.

**Source:** _github.com/snowdream_

#### Q21: How are the JSP requests handled? ⭐⭐
**Answer:**
On the arrival of a JSP request, the browser first requests a page with a .jsp extension. Then, the Web server reads the request and using the JSP compiler, the Web server converts the JSP page into a servlet class. Notice that the JSP file is compiled only on the first request of the page, or if the JSP file has changed.The generated servlet class is invoked, in order to handle the browser’s request. Once the execution of the request is over, the servlet sends a response back to the client. See [how to get Request parameters in a JSP](http://examples.javacodegeeks.com/enterprise-java/jsp/get-request-parameter-in-jsp-page/).

**Source:** _github.com/snowdream_

#### Q22: What is Function Overriding and Overloading in Java? ⭐⭐
**Answer:**
* Method **overloading** in Java occurs when two or more methods in the same class have the exact same name, but different parameters. 

```java
class Dog{
    public void bark(){
        System.out.println("woof ");
    }
 
    //overloading method
    public void bark(int num){
    	for(int i=0; i<num; i++)
    		System.out.println("woof ");
    }
}
```

* On the other hand, method **overriding** is defined as the case when a child class redefines the same method as a parent class. Overridden methods must have the same name, argument list, and return type. The overriding method may not limit the access of the method it overrides.

```java
class Dog{
    public void bark(){
        System.out.println("woof ");
    }
}
class Hound extends Dog{
    public void sniff(){
        System.out.println("sniff ");
    }
 
    public void bark(){
        System.out.println("bowl");
    }
}
 
public class OverridingTest{
    public static void main(String [] args){
        Dog dog = new Hound();
        dog.bark();
    }
}
```


**Source:** _github.com/snowdream_

#### Q23: How HashMap works in Java?  ⭐⭐
**Answer:**
[A HashMap in Java stores key-value pairs](http://www.javacodegeeks.com/2014/03/how-hashmap-works-in-java.html). The [HashMap](http://docs.oracle.com/javase/7/docs/api/java/util/HashMap.html) requires a hash function and uses hashCode and equals methods, in order to put and retrieve elements to and from the collection respectively. When the put method is invoked, the [HashMap](http://docs.oracle.com/javase/7/docs/api/java/util/HashMap.html) calculates the hash value of the key and stores the pair in the appropriate index inside the collection. If the key exists, its value is updated with the new value. Some important characteristics of a [HashMap](http://docs.oracle.com/javase/7/docs/api/java/util/HashMap.html) are its capacity, its load factor and the threshold resizing.

**Source:** _github.com/snowdream_

#### Q24: What differences exist between HashMap and Hashtable?  ⭐⭐
**Answer:**
There are several differences between `HashMap` and `Hashtable` in Java:

 1. `Hashtable` is synchronized, whereas `HashMap` is not. This makes `HashMap` better for non-threaded applications, as unsynchronized Objects typically perform better than synchronized ones.

 2. `Hashtable` does not allow `null` keys or values.  `HashMap` allows one `null` key and any number of `null` values.

 3. One of HashMap's subclasses is `LinkedHashMap`, so in the event that you'd want predictable iteration order (which is insertion order by default), you could easily swap out the `HashMap` for a `LinkedHashMap`.  This wouldn't be as easy if you were using `Hashtable`.

**Source:** _stackoverflow.com_

#### Q25: What is the purpose Class.forName method? ⭐⭐
**Answer:**
This method is used to method is used to load the driver that will establish a connection to the database.

**Source:** _github.com/snowdream_

#### Q26: What is JDBC? ⭐⭐
**Answer:**
JDBC is an abstraction layer that allows users to choose between databases. [JDBC enables developers to write database applications in Java](http://www.javacodegeeks.com/2014/03/java-8-friday-java-8-will-revolutionize-database-access.html), without having to concern themselves with the underlying details of a particular database.

**Source:** _github.com/snowdream_

#### Q27: What is the design pattern that Java uses for all Swing components? ⭐⭐
**Answer:**
The design pattern used by Java for all Swing components is the Model View Controller (MVC) pattern.

**Source:** _github.com/snowdream_

#### Q28: How does Garbage Collection prevent a Java application from going out of memory? ⭐⭐
**Answer:**
It doesn’t! Garbage Collection simply cleans up unused memory when an object goes out of scope and is no longer needed. However an application could create a huge number of large objects that causes an `OutOfMemoryError`.

**Source:** _codementor.io_

#### Q29: What do you know about the big-O notation and can you give some examples with respect to different data structures? ⭐⭐
**Answer:**
The Big-O notation simply describes how well an algorithm scales or performs in the worst case scenario as the number of elements in a data structure increases. The Big-O notation can also be used to describe other behavior such as memory consumption. Since the collection classes are actually data structures, we usually use the Big-O notation to chose the best implementation to use, based on time, memory and performance. Big-O notation can give a good indication about performance for large amounts of data.

**Source:** _github.com/snowdream_

#### Q30: What are the Data Types supported by Java? What is Autoboxing and Unboxing? ⭐⭐
**Answer:**
The eight primitive data types supported by the Java programming language are:

* byte
* short
* int
* long
* float
* double
* boolean
* char

**Autoboxing** is the automatic conversion made by the Java compiler between the primitive types and their corresponding object wrapper classes. If the conversion goes the other way, this operation is called **unboxing**.

**Source:** _github.com/snowdream_

#### Q31: What is an Java Applet? ⭐⭐
**Answer:**
A Java Applet is program that can be included in a HTML page and be executed in a java enabled client browser. Applets are used for creating dynamic and interactive web applications.

**Source:** _github.com/snowdream_

#### Q32: What will happen to the Exception object after exception handling? ⭐⭐
**Answer:**
The [Exception](http://docs.oracle.com/javase/7/docs/api/java/lang/Exception.html) object will be garbage collected in the next garbage collection.

**Source:** _github.com/snowdream_

#### Q33: What is the importance of finally block in exception handling? ⭐⭐
**Answer:**
A *finally* block will always be executed, whether or not an exception is actually thrown. Even in the case where the catch statement is missing and an exception is thrown, the finally block will still be executed. Last thing to mention is that the finally block is used to release resources like I/O buffers, database connections, etc.

**Source:** _github.com/snowdream_

#### Q34:  What is the purpose of garbage collection in Java, and when is it used? ⭐⭐
**Answer:**
The purpose of garbage collection is to identify and discard those objects that are no longer needed by the application, in order for the resources to be reclaimed and reused.

**Source:** _github.com/snowdream_

#### Q35: What does System.gc() and Runtime.gc() methods do? ⭐⭐
**Answer:**
These methods can be used as a hint to the JVM, in order to start a garbage collection. However, this it is up to the Java Virtual Machine (JVM) to start the garbage collection immediately or later in time.


**Source:** _github.com/snowdream_

#### Q36: What is the difference between Exception and Error in java? ⭐⭐
**Answer:**
* An **Error** "indicates serious problems that a reasonable application should not try to catch."
* An **Exception** "indicates conditions that a reasonable application might want to catch."

**Source:** _github.com/snowdream_

#### Q37: What is reflection and why is it useful? ⭐⭐
**Answer:**
The name **reflection** is used to describe code which is able to inspect other code in the same system (or itself) and to make modifications at runtime.

For example, say you have an object of an unknown type in Java, and you would like to call a 'doSomething' method on it if one exists. Java's static typing system isn't really designed to support this unless the object conforms to a known interface, but using reflection, your code can look at the object and find out if it has a method called 'doSomething' and then call it if you want to.

```java
Method method = foo.getClass().getMethod("doSomething", null);
method.invoke(foo, null);
```

**Source:** _stackoverflow.com_

#### Q38: When does an Object becomes eligible for Garbage collection in Java ?  ⭐⭐
**Answer:**
A Java object is subject to garbage collection when it becomes unreachable to the program in which it is currently used.

**Source:** _github.com/snowdream_

#### Q39: Compare the sleep() and wait() methods in Java ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q40: Is there anything like static class in java? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q41: What is the importance of hashCode() and equals() methods?  ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q42: If an object reference is set to null, will the Garbage Collector immediately free the memory held by that object? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q43: When is the finalize() called? What is the purpose of finalization?  ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q44: What is the difference between throw and throws? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q45: What is the Java Classloader? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q46: What’s the difference between Enumeration and Iterator interfaces?  ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q47: How does finally block differ from finalize() method? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q48: Explain the life cycle of an Applet.  ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q49: What happens when an applet is loaded? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q50: What is the tradeoff between using an unordered array versus an ordered array?  ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q51: What are the restrictions imposed on Java applets? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q52: What are untrusted applets? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q53: What is the applet security manager, and what does it provide? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q54: Can an enum be extended? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q55: Which Swing methods are thread-safe? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q56: What is the relationship between an event-listener interface and an event-adapter class? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q57: What’s the difference between a ClassNotFoundException and NoClassDefFoundError? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q58: What is Java Priority Queue? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q59: What is Comparable and Comparator interface? List their differences. ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q60: What is difference between ArrayList and LinkedList ?  ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q61: Explain the role of Driver in JDBC.  ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q62: What is difference between Array and ArrayList ? When will you use Array over ArrayList? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q63: What is the advantage of PreparedStatement over Statement? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q64: What is the use of CallableStatement? Name the method, which is used to prepare a CallableStatement. ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q65: What is difference between fail-fast and fail-safe?  ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q66: What differences exist between Iterator and ListIterator?  ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q67: What are the advantages of JSP? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q68: Why Collection doesn’t extend Cloneable and Serializable interfaces?  ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q69: What are Scriptlets? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q70: What’s a deadlock?  ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q71: What is structure of Java Heap? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q72: What is meant by JSP implicit objects and what are they? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q73: What is the difference between an Applet and a Servlet? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q74: What is the difference between GenericServlet and HttpServlet? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q75: Explain the life cycle of a Servlet. ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q76: What is the difference between doGet() and doPost()? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q77: What is the difference between final, finalize and finally? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q78:  What is a Server Side Include (SSI)? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q79: Explain different ways of creating a thread. Which one would you prefer and why? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q80: How and where are Annotations used in Java? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q81: What are the steps involved to make work a RMI program?  ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q82: What is the role of stub in RMI? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q83: Does Java support multiple inheritance?  ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q84: Is Java “pass-by-reference” or “pass-by-value”? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q85: How do I read/convert an InputStream into a String in Java? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q86: What is the volatile keyword useful for? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q87: What is a Constructor, Constructor Overloading in Java and Copy-Constructor?  ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q88: What is the difference between public, protected, package-private and private in Java? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q89: How threadsafe is enum in Java? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q90: What is the JIT? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q91: Can you access non static variable in static context? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q92: What do the ... dots in the method parameters mean? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q93: How can I synchornize two Java processes? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q94: How do I break out of nested loops in Java? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q95: What is a JavaBean exactly? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q96: Can == be used on enum? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q97: What are the differences between == and equals? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q98: What is the main difference between StringBuffer and StringBuilder? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q99: What's the advantage of using getters and setters? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q100: Why does Java have transient fields? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q101: What is static initializer? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q102: What is the difference between HashMap, LinkedHashMap and TreeMap in Java? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q103: What is the role of Remote Interface in RMI? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q104:  What is the difference between applets loaded over the internet and applets loaded via the file system? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q105: What is the applet class loader, and what does it provide? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q106: What are the differences between a HashMap and a Hashtable in Java? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q107: What are some of the best practices relating to the Java Collection framework? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q108: What is Servlet Chaining? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q109: How do you find out what client machine is making a request to your servlet? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q110: When to use LinkedList over ArrayList in Java? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q111: What is the difference between a synchronized method and a synchronized block? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q112: What is Double Brace initialization in Java? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q113: What is RMI? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q114: How do I test a private function or a class that has private methods, fields or inner classes? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q115: What is the basic principle of RMI architecture? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q116: Explain the available thread states in a high-level. ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q117: Is it possible to call one constructor from another in Java? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q118: What is the difference between Serial and Throughput Garbage collector? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q119: What is the role of the java.rmi.Naming Class?  ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q120: What is the main difference between an inner class and a static nested class in Java? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q121: What is meant by binding in RMI? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q122: Given two double values d1, d2, what is the most reliable way to test their equality?  ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q123: How do you ensure that N threads can access N resources without deadlock?  ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q124: Does Java support default parameter values? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q125: Explain a use case for the Builder Design Pattern ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q126: What exactly is marker interface in Java? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q127: What is the purpose of using RMISecurityManager in RMI? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q128: Explain Marshalling and demarshalling. ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q129: Is null check needed before calling instanceof? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q130: What is Perm Gen space in Heap? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q131: Why is Spring MVC better than Servlets / JSP ? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q132: Why is char[] preferred over String for passwords? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q133: What does Connection pooling mean? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q134: What is an efficient way to implement a singleton pattern in Java? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q135: What's the difference between SoftReference and WeakReference in Java? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q136: Provide some examples when a finally block won't be executed in Java? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q137: Why isn’t String‘s .length() accurate? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q138: What's wrong with Double Brace initialization in Java? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q139: Why ArrayList are preferable in many more use-cases than LinkedList? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q140: Explain what will the code return ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q141: Compare volatile vs static variables in Java ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q142: What is DGC ? And how does it work? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q143: What are the layers of RMI Architecture? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q144: How does thread synchronization occurs inside a monitor? What levels of synchronization can you apply?  ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q145: What is the difference between HashSet and TreeSet? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q146: Does Garbage collection occur in permanent generation space in JVM? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q147: What does 'synchronized' mean? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

## [[⬆]](#toc) <a name=JavaScript>JavaScript</a> Interview Questions
#### Q1: What is Coercion in JavaScript? 
**Answer:**
In JavaScript conversion between different two build-in types called `coercion`.  Coercion comes in two forms in JavaScript: *explicit* and *implicit*.

Here's an example of explicit coercion:
```js
var a = "42";

var b = Number( a );

a;				// "42"
b;				// 42 -- the number!
```
And here's an example of implicit coercion:
```js
var a = "42";

var b = a * 1;	// "42" implicitly coerced to 42 here

a;				// "42"
b;				// 42 -- the number!
``` 

#### Q2: Explain equality in JavaScript ⭐
**Answer:**
JavaScript has both strict and type–converting comparisons: 
* **Strict comparison (e.g., ===)** checks for value equality without allowing *coercion*
* **Abstract comparison (e.g. ==)** checks for value equality with *coercion* allowed

```js
var a = "42";
var b = 42;

a == b;			// true
a === b;		// false
```
Some simple equalityrules:
* If either value (aka side) in a comparison could be the `true` or `false` value, avoid `==` and use `===`.
* If either value in a comparison could be of these specific values (`0`, `""`, or `[]` -- empty array), avoid `==` and use `===`.
* In all other cases, you're safe to use `==`. Not only is it safe, but in many cases it simplifies your code in a way that improves readability.

#### Q3: What is typeof operator? ⭐
**Answer:**
JavaScript provides a `typeof` operator that can examine a value and tell you what type it is:
```js
var a;
typeof a;				// "undefined"

a = "hello world";
typeof a;				// "string"

a = 42;
typeof a;				// "number"

a = true;
typeof a;				// "boolean"

a = null;
typeof a;				// "object" -- weird, bug

a = undefined;
typeof a;				// "undefined"

a = { b: "c" };
typeof a;				// "object"
```


#### Q4: What is the object type? ⭐
**Answer:**
The object type refers to a compound value where you can set properties (named locations) that each hold their own values of any type. 

```js
var obj = {
	a: "hello world", // property
	b: 42,
	c: true
};

obj.a;		// "hello world", accessed with doted notation
obj.b;		// 42
obj.c;		// true

obj["a"];	// "hello world", accessed with bracket notation
obj["b"];	// 42
obj["c"];	// true
```
Bracket notation is also useful if you want to access a property/key but the name is stored in another variable, such as:
```js
var obj = {
	a: "hello world",
	b: 42
};

var b = "a";

obj[b];			// "hello world"
obj["b"];		// 42
```

#### Q5: Explain arrays in JavaScript ⭐
**Answer:**
An `array` is an object that holds values (of any type) not particularly in named properties/keys, but rather in numerically indexed positions:

```js
var arr = [
	"hello world",
	42,
	true
];

arr[0];			// "hello world"
arr[1];			// 42
arr[2];			// true
arr.length;		// 3

typeof arr;		// "object"
```


#### Q6: What is Scope in JavaScript? ⭐
**Answer:**
In JavaScript, each function gets its own *scope*. Scope is basically a collection of variables as well as the rules for how those variables are accessed by name. Only code inside that function can access that function's scoped variables.

A variable name has to be unique within the same scope. A scope can be nested inside another scope. If one scope is nested inside another, code inside the innermost scope can access variables from either scope.

#### Q7: What does "use strict" do? ⭐⭐
**Answer:**
The `use strict` literal is entered at the top of a JavaScript program or at the top of a function and it helps you write safer JavaScript code by throwing an error if a global variable is created by mistake. For example, the following program will throw an error:

```js
function doSomething(val) {
  "use strict"; 
  x = val + 10;
}`
```

It will throw an error because `x` was not defined and it is being set to some value in the global scope, which isn't allowed with `use strict` The small change below fixes the error being thrown:

```js
function doSomething(val) {
  "use strict"; 
  var x = val + 10;
}
```

**Source:** _coderbyte.com_

#### Q8: Explain Null and Undefined in JavaScript ⭐⭐
**Answer:**
JavaScript (and by extension TypeScript) has two bottom types: `null` and `undefined`. They are *intended* to mean different things:
* Something hasn't been initialized : `undefined`.
* Something is currently unavailable: `null`.

#### Q9: What's the difference between throw Error('msg') vs throw new Error('msg')? ⭐⭐
**Details:**
```js
var err1 = Error('message');
var err2 = new Error('message');
```
Which one is correct and why?

**Answer:**
Both are fine; the function call `Error(…)` is equivalent to the object creation expression `new Error(…)` with the same arguments.

**Source:** _stackoverflow.com_

#### Q10: Is there anyway to force using strict mode in Node.js? ⭐⭐
**Answer:**
you can place

```js
"use strict";
```

at the top of your file in **node >= 0.10.7**, but if you want your whole app to run in strict (**including external modules**) you can do this

```sh
node --use_strict
```

**Source:** _stackoverflow.com_

#### Q11: What's the difference between host objects and native objects? ⭐⭐
**Answer:**
* Native objects are objects that are part of the JavaScript language defined by the ECMAScript specification, such as `String`, `Math`, `RegExp`, `Object`, `Function`, etc.
* Host objects are provided by the runtime environment (browser or Node), such as `window`, `XMLHTTPRequest`, etc.

**Source:** _github.com/yangshun_

#### Q12: What is strict mode? ⭐⭐
**Answer:**
*Strict Mode* is a new feature in ECMAScript 5 that allows you to place a program, or a function, in a "strict" operating context. This strict context prevents certain actions from being taken and throws more exceptions.

```js
// Non-strict code...

(function(){
  "use strict";

  // Define your library strictly...
})();

// Non-strict code...
```

#### Q13: What is the difference between `==` and `===`? ⭐⭐
**Answer:**
`==` is the abstract equality operator while `===` is the strict equality operator. The `==` operator will compare for equality after doing any necessary type conversions. The `===` operator will not do type conversion, so if two values are not the same type `===` will simply return `false`. When using `==`, funky things can happen, such as:

```js
1 == '1'; // true
1 == [1]; // true
1 == true; // true
0 == ''; // true
0 == '0'; // true
0 == false; // true
```

My advice is never to use the `==` operator, except for convenience when comparing against `null` or `undefined`, where `a == null` will return `true` if `a` is `null` or `undefined`.

```js
var a = null;
console.log(a == null); // true
console.log(a == undefined); // true
```

**Source:** _github.com/yangshun_

#### Q14: Explain the same-origin policy with regards to JavaScript. ⭐⭐
**Answer:**
The same-origin policy prevents JavaScript from making requests across domain boundaries. An origin is defined as a combination of URI scheme, hostname, and port number. This policy prevents a malicious script on one page from obtaining access to sensitive data on another web page through that page's Document Object Model.

**Source:** _github.com/yangshun_

#### Q15: Make this work ⭐⭐
**Details:**
```js
duplicate([1, 2, 3, 4, 5]); // [1,2,3,4,5,1,2,3,4,5]
```

**Answer:**
```js
function duplicate(arr) {
  return arr.concat(arr);
}

duplicate([1, 2, 3, 4, 5]); // [1,2,3,4,5,1,2,3,4,5]
```

**Source:** _github.com/yangshun_

#### Q16: FizzBuzz Challenge ⭐⭐
**Details:**
Create a for loop that iterates up to `100` while outputting **"fizz"** at multiples of `3`, **"buzz"** at multiples of `5` and **"fizzbuzz"** at multiples of `3` and `5`.

**Answer:**
Check out this version of FizzBuzz:

```js
for (let i = 1; i <= 100; i++) {
  let f = i % 3 == 0,
    b = i % 5 == 0;
  console.log(f ? (b ? 'FizzBuzz' : 'Fizz') : b ? 'Buzz' : i);
}
```

**Source:** _github.com/yangshun_

#### Q17: What is a Polyfill? ⭐⭐
**Answer:**
A polyfill is essentially the specific code (or plugin) that would allow you to have some specific functionality that you expect in current or “modern” browsers to also work in other browsers that do not have the support for that functionality built in.
* Polyfills are not part of the HTML5 standard
* Polyfilling is not limited to Javascript

**Source:** _programmerinterview.com_

#### Q18: Why would you use something like the `load` event? Does this event have disadvantages? Do you know any alternatives, and why would you use those? ⭐⭐
**Answer:**
The `load` event fires at the end of the document loading process. At this point, all of the objects in the document are in the DOM, and all the images, scripts, links and sub-frames have finished loading.

The DOM event `DOMContentLoaded` will fire after the DOM for the page has been constructed, but do not wait for other resources to finish loading. This is preferred in certain cases when you do not need the full page to be loaded before initializing.

**Source:** _github.com/yangshun_

#### Q19: Why is it, in general, a good idea to leave the global scope of a website as-is and never touch it? ⭐⭐
**Answer:**
Every script has access to the global scope, and if everyone uses the global namespace to define their variables, collisions will likely occur. Use the module pattern (IIFEs) to encapsulate your variables within a local namespace.

**Source:** _github.com/yangshun_

#### Q20: What are some of the advantages/disadvantages of writing JavaScript code in a language that compiles to JavaScript? ⭐⭐
**Answer:**
Some examples of languages that compile to JavaScript include CoffeeScript, Elm, ClojureScript, PureScript, and TypeScript.

Advantages:

* Fixes some of the longstanding problems in JavaScript and discourages JavaScript anti-patterns.
* Enables you to write shorter code, by providing some syntactic sugar on top of JavaScript, which I think ES5 lacks, but ES2015 is awesome.
* Static types are awesome (in the case of TypeScript) for large projects that need to be maintained over time.

Disadvantages:

* Require a build/compile process as browsers only run JavaScript and your code will need to be compiled into JavaScript before being served to browsers.
* Debugging can be a pain if your source maps do not map nicely to your pre-compiled source.
* Most developers are not familiar with these languages and will need to learn it. There's a ramp up cost involved for your team if you use it for your projects.
* Smaller community (depends on the language), which means resources, tutorials, libraries, and tooling would be harder to find.
* IDE/editor support might be lacking.
* These languages will always be behind the latest JavaScript standard.
* Developers should be cognizant of what their code is being compiled to — because that is what would actually be running, and that is what matters in the end.

Practically, ES2015 has vastly improved JavaScript and made it much nicer to write. I don't really see the need for CoffeeScript these days.

**Source:** _github.com/yangshun_

#### Q21: What language constructions do you use for iterating over object properties and array items? ⭐⭐
**Answer:**
For objects:

* `for` loops - `for (var property in obj) { console.log(property); }`. However, this will also iterate through its inherited properties, and you will add an `obj.hasOwnProperty(property)` check before using it.
* `Object.keys()` - `Object.keys(obj).forEach(function (property) { ... })`. `Object.keys()` is a static method that will lists all enumerable properties of the object that you pass it.
* `Object.getOwnPropertyNames()` - `Object.getOwnPropertyNames(obj).forEach(function (property) { ... })`. `Object.getOwnPropertyNames()` is a static method that will lists all enumerable and non-enumerable properties of the object that you pass it.

For arrays:

* `for` loops - `for (var i = 0; i < arr.length; i++)`. The common pitfall here is that `var` is in the function scope and not the block scope and most of the time you would want block scoped iterator variable. ES2015 introduces `let` which has block scope and it is recommended to use that instead. So this becomes: `for (let i = 0; i < arr.length; i++)`.
* `forEach` - `arr.forEach(function (el, index) { ... })`. This construct can be more convenient at times because you do not have to use the `index` if all you need is the array elements. There are also the `every` and `some` methods which will allow you to terminate the iteration early.

Most of the time, I would prefer the `.forEach` method, but it really depends on what you are trying to do. `for` loops allow more flexibility, such as prematurely terminate the loop using `break` or incrementing the iterator more than once per loop.

**Source:** _github.com/yangshun_

#### Q22: What is let keyword in JavaScript? ⭐⭐
**Answer:**
In addition to creating declarations for variables at the function level, ES6 lets you declare variables to belong to individual blocks (pairs of { .. }), using the `let` keyword. 

**Source:** _github.com/getify_

#### Q23: Explain what a callback function is and provide a simple example. ⭐⭐
**Answer:**
A `callback` function is a function that is passed to another function as an argument and is executed after some operation has been completed. Below is an example of a simple callback function that logs to the console *after* some operations have been completed.

```js
function modifyArray(arr, callback) {
  // do something to arr here
  arr.push(100);
  // then execute the callback function that was passed
  callback();
}

var arr = [1, 2, 3, 4, 5];

modifyArray(arr, function() {
  console.log("array has been modified", arr);
});
```

**Source:** _coderbyte.com_

#### Q24: Being told that an unsorted array contains (n - 1) of n consecutive numbers (where the bounds are defined), find the missing number in O(n) time ⭐⭐
**Answer:**
```js
// The output of the function should be 8
var arrayOfIntegers = [2, 5, 1, 4, 9, 6, 3, 7];
var upperBound = 9;
var lowerBound = 1;

findMissingNumber(arrayOfIntegers, upperBound, lowerBound); // 8

function findMissingNumber(arrayOfIntegers, upperBound, lowerBound) {
  // Iterate through array to find the sum of the numbers
  var sumOfIntegers = 0;
  for (var i = 0; i < arrayOfIntegers.length; i++) {
    sumOfIntegers += arrayOfIntegers[i];
  }

  // Find theoretical sum of the consecutive numbers using a variation of Gauss Sum.
  // Formula: [(N * (N + 1)) / 2] - [(M * (M - 1)) / 2];
  // N is the upper bound and M is the lower bound

  upperLimitSum = (upperBound * (upperBound + 1)) / 2;
  lowerLimitSum = (lowerBound * (lowerBound - 1)) / 2;

  theoreticalSum = upperLimitSum - lowerLimitSum;

  return theoreticalSum - sumOfIntegers;
}
```

**Source:** _https://github.com/kennymkchan_

#### Q25: Remove duplicates of an array and return an array of only unique elements ⭐⭐
**Answer:**
```js
// ES6 Implementation
var array = [1, 2, 3, 5, 1, 5, 9, 1, 2, 8];

Array.from(new Set(array)); // [1, 2, 3, 5, 9, 8]

// ES5 Implementation
var array = [1, 2, 3, 5, 1, 5, 9, 1, 2, 8];

uniqueArray(array); // [1, 2, 3, 5, 9, 8]

function uniqueArray(array) {
  var hashmap = {};
  var unique = [];

  for(var i = 0; i < array.length; i++) {
    // If key returns undefined (unique), it is evaluated as false.
    if(!hashmap.hasOwnProperty(array[i])) {
      hashmap[array[i]] = 1;
      unique.push(array[i]);
    }
  }

  return unique;
}
```

**Source:** _https://github.com/kennymkchan_

#### Q26: Explain Values and Types in JavaScript ⭐⭐
**Answer:**
JavaScript has typed values, not typed variables. The following built-in types are available:
* `string`
* `number`
* `boolean`
* `null` and `undefined`
* `object`
* `symbol` (new to ES6)

#### Q27: How would you check if a number is an integer? ⭐⭐
**Answer:**
A very simply way to check if a number is a decimal or integer is to see if there is a remainder left when you divide by 1.

```js
function isInt(num) {
  return num % 1 === 0;
}

console.log(isInt(4)); // true
console.log(isInt(12.2)); // false
console.log(isInt(0.3)); // false
```

**Source:** _coderbyte.com_

#### Q28: Given a string, reverse each word in the sentence ⭐⭐
**Details:**
For example `Welcome to this Javascript Guide!` should be become `emocleW ot siht tpircsavaJ !ediuG`

**Answer:**
```js
var string = "Welcome to this Javascript Guide!";

// Output becomes !ediuG tpircsavaJ siht ot emocleW
var reverseEntireSentence = reverseBySeparator(string, "");

// Output becomes emocleW ot siht tpircsavaJ !ediuG
var reverseEachWord = reverseBySeparator(reverseEntireSentence, " ");

function reverseBySeparator(string, separator) {
  return string.split(separator).reverse().join(separator);
}
```

**Source:** _https://github.com/kennymkchan_

#### Q29: Write a function that would allow you to do this. ⭐⭐
**Details:**
```js
var addSix = createBase(6);
addSix(10); // returns 16
addSix(21); // returns 27
```

**Answer:**
You can create a closure to keep the value passed to the function `createBase` even after the inner function is returned. The inner function that is being returned is created within an outer function, making it a closure, and it has access to the variables within the outer function, in this case the variable `baseNumber`.

```js
function createBase(baseNumber) {
  return function(N) {
    // we are referencing baseNumber here even though it was declared
    // outside of this function. Closures allow us to do this in JavaScript
    return baseNumber + N;
  }
}

var addSix = createBase(6);
addSix(10);
addSix(21);
```

**Source:** _coderbyte.com_

#### Q30: How would you use a closure to create a private counter? ⭐⭐
**Answer:**
You can create a function within an outer function (a closure) that allows you to update a private variable but the variable wouldn't be accessible from outside the function without the use of a helper function.

```js
function counter() {
  var _counter = 0;
  // return an object with several functions that allow you
  // to modify the private _counter variable
  return {
    add: function(increment) { _counter += increment; },
    retrieve: function() { return 'The counter is currently at: ' + _counter; }
  }
}

// error if we try to access the private variable like below
// _counter;

// usage of our counter function
var c = counter();
c.add(5); 
c.add(9); 

// now we can access the private variable in the following way
c.retrieve(); // => The counter is currently at: 14
```

**Source:** _coderbyte.com_

#### Q31: Implement enqueue and dequeue using only two stacks ⭐⭐
**Answer:**
*Enqueue* means to add an element, *dequeue* to remove an element.

```js
var inputStack = []; // First stack
var outputStack = []; // Second stack

// For enqueue, just push the item into the first stack
function enqueue(stackInput, item) {
  return stackInput.push(item);
}

function dequeue(stackInput, stackOutput) {
  // Reverse the stack such that the first element of the output stack is the
  // last element of the input stack. After that, pop the top of the output to
  // get the first element that was ever pushed into the input stack
  if (stackOutput.length <= 0) {
    while(stackInput.length > 0) {
      var elementToOutput = stackInput.pop();
      stackOutput.push(elementToOutput);
    }
  }

  return stackOutput.pop();
}
```

**Source:** _https://github.com/kennymkchan_

#### Q32: How to check if an object is an array or not? Provide some code. ⭐⭐
**Answer:**
> The best way to find whether an object is instance of a particular class or not using `toString` method from `Object.prototype`

```javascript
var arrayList = [1 , 2, 3];
```

One of the best use cases of type checking of an object is when we do method overloading in JavaScript. For understanding this let say we have a method called `greet` which take one single string and also a list of string, so making our `greet` method workable in both situation we need to know what kind of parameter is being passed, is it single value or list of value?

```javascript
function greet(param) {
  if() {
    // here have to check whether param is array or not
  }
  else {
  }
}
```

However, in above implementation it might not necessary to check type for array, we can check for single value string and put array logic code in else block, let see below code for the same.

```javascript
 function greet(param) {
   if(typeof param === 'string') {
   }
   else {
     // If param is of type array then this block of code would execute
   }
 }
```

Now it's fine we can go with above two implementations, but when we have a situation like a parameter can be `single value`, `array`, and `object` type then we will be in trouble.

Coming back to checking type of object, As we mentioned that we can use `Object.prototype.toString`

```javascript
if(Object.prototype.toString.call(arrayList) === '[object Array]') {
  console.log('Array!');
}
```

If you are using `jQuery` then you can also used jQuery `isArray` method:

```javascript
if($.isArray(arrayList)) {
  console.log('Array');
} else {
  console.log('Not an array');
}
```

FYI jQuery uses `Object.prototype.toString.call` internally to check whether an object is an array or not.

In modern browser, you can also use:

```javascript
Array.isArray(arrayList);
```

`Array.isArray` is supported by Chrome 5, Firefox 4.0, IE 9, Opera 10.5 and Safari 5

**Source:** _github.com/ganqqwerty_

#### Q33: How to empty an array in JavaScript? ⭐⭐
**Details:**
```js
var arrayList =  ['a', 'b', 'c', 'd', 'e', 'f'];
```
How could we empty the array above?

**Answer:**
**Method 1**

```javascript
arrayList = [];
```

Above code will set the variable `arrayList` to a new empty array. This is recommended if you don't have **references to the original array** `arrayList` anywhere else because It will actually create a new empty array. You should be careful with this way of empty the array, because if you have referenced this array from another variable, then the original reference array will remain unchanged, Only use this way if you have only referenced the array by its original variable `arrayList`.

For Instance:

```javascript
var arrayList = ['a', 'b', 'c', 'd', 'e', 'f']; // Created array
var anotherArrayList = arrayList;  // Referenced arrayList by another variable
arrayList = []; // Empty the array
console.log(anotherArrayList); // Output ['a', 'b', 'c', 'd', 'e', 'f']
```

**Method 2**

```javascript
arrayList.length = 0;
```

Above code will clear the existing array by setting its length to 0. This way of empty the array also update all the reference variable which pointing to the original array. This way of empty the array is useful when you want to update all the another reference variable which pointing to `arrayList`.

For Instance:

```javascript
var arrayList = ['a', 'b', 'c', 'd', 'e', 'f']; // Created array
var anotherArrayList = arrayList;  // Referenced arrayList by another variable
arrayList.length = 0; // Empty the array by setting length to 0
console.log(anotherArrayList); // Output []
```

**Method 3**

```javascript
arrayList.splice(0, arrayList.length);
```

Above implementation will also work perfectly. This way of empty the array will also update all the references of the original array.

```javascript
var arrayList = ['a', 'b', 'c', 'd', 'e', 'f']; // Created array
var anotherArrayList = arrayList;  // Referenced arrayList by another variable
arrayList.splice(0, arrayList.length); // Empty the array by setting length to 0
console.log(anotherArrayList); // Output []
```

**Method 4**

```javascript
while(arrayList.length) {
  arrayList.pop();
}
```

Above implementation can also empty the array. But not recommended to use often.

**Source:** _github.com/ganqqwerty_

#### Q34: Write a "mul" function which will properly when invoked as below syntax. ⭐⭐
**Details:**
```javascript
console.log(mul(2)(3)(4)); // output : 24
console.log(mul(4)(3)(4)); // output : 48
```

**Answer:**
```javascript
function mul (x) {
  return function (y) { // anonymous function
    return function (z) { // anonymous function
      return x * y * z;
    };
  };
}
```

Here `mul` function accept the first argument and return anonymous function which take the second parameter and return anonymous function which take the third parameter and return multiplication of arguments which is being passed in successive

In JavaScript function defined inside has access to outer function variable and function is the first class object so it can be returned by function as well and passed as argument in another function.
- A function is an instance of the Object type
- A function can have properties and has a link back to its constructor method
- Function can be stored as variable
- Function can be pass as a parameter to another function
- Function can be returned from function

**Source:** _github.com/ganqqwerty_

#### Q35: Explain event bubbling and how one may prevent it ⭐⭐
**Answer:**
**Event bubbling** is the concept in which an event triggers at the deepest possible element, and triggers on parent elements in nesting order. As a result, when clicking on a child element one may exhibit the handler of the parent activating.

One way to prevent event bubbling is using `event.stopPropagation()` or `event.cancelBubble` on IE < 9.

**Source:** _https://github.com/kennymkchan_

#### Q36: Provide some examples of non-bulean value coercion to a boolean one ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q37: How to compare two objects in JavaScript? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q38: What will be the output of the following code? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q39: What is the drawback of creating true private in JavaScript? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q40: Write a recursive function that returns the binary string of a given decimal number ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q41: What will be the output of the following code? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q42: What will be the output of the following code? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q43: When should we use generators in ES6? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q44: What is IIFEs (Immediately Invoked Function Expressions)? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q45: Given two strings, return true if they are anagrams of one another ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q46: Find the intersection of two arrays. An intersection would be the common elements that exists within both arrays. In this case, these elements should be unique! ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q47: What will the following code output? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q48: Write a function that would allow you to do this ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q49: Given an array of integers, find the largest difference between two elements such that the element of lesser value must come before the greater element ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q50: Given an array of integers, find the largest product yielded from three of the integers ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q51: Check if a given string is a palindrome. Case sensitivity should be taken into account. ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q52: What's the difference between using “let” and “var” to declare a variable in ES6? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q53: When should I use Arrow functions in ES6? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q54: What is the motivation for bringing Symbols to ES6? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q55: What is generator in JS? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q56: What are the benefits of using spread syntax in ES6 and how is it different from rest syntax? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q57: Explain the difference between "undefined" and "not defined" in JavaScript ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q58: What is 'Currying'? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q59: What is the definition of a higher-order function? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q60: What are the differences between ES6 class and ES5 function constructors? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q61: Explain the differences on the usage of `foo` between `function foo() {}` and `var foo = function() {}` ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q62: Could you explain the difference between ES5 and ES6 ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q63: What is the difference between a shim and a polyfill? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q64: What are the advantages and disadvantages of using "use strict"? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q65: Describe closure concept in JavaScript as best as you could ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q66: What is the difference between anonymous and named functions?  ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q67: What is the difference between document `load` event and document `DOMContentLoaded` event? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q68: Why is extending built-in JavaScript objects not a good idea? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q69: Explain `Function.prototype.bind`. ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q70: What's the difference between `.call` and `.apply`? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q71: What's a typical use case for anonymous functions? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q72: What is a closure, and how/why would you use one? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q73: What do you think of AMD vs CommonJS? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q74: Suggest one simple way of removing duplicates from an array using ES6 ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q75: Why should we use ES6 classes? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q76: What is the preferred syntax for defining enums in JavaScript? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q77: Explain the difference between Object.freeze() vs const ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q78: Can you give an example for destructuring an object or an array in ES6? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q79: Explain what is hoisting in Javascript ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q80: Explain prototype inheritance in JavaScript? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q81: What will the following code output? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q82: What does the term "Transpiling" stand for? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q83: How would you create a private variable in JavaScript? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q84: What is the "new" keyword in JavaScript? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q85: Explain the Prototype Design Pattern ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q86: How does the “this” keyword work? Provide some code examples. ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q87: What is the Temporal Dead Zone in ES6? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q88: Create a function that will evaluate if a given expression has balanced parentheses using stacks ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q89: Check if a given string is a isomorphic ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q90: When should you NOT use arrow functions in ES6? Name three or more cases. ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q91: Explain how JSONP works (and how it's not really Ajax) ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q92: What will be the output of the following code? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q93: What are the actual uses of ES6 WeakMap? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q94: Explain difference between: `function Person(){}`, `var person = Person()`, and `var person = new Person()`? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q95: What is Hoisting in JavaScript? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q96: What is “closure” in javascript? Provide an example? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q97: Can you describe the main difference between a `.forEach` loop and a `.map()` loop and why you would pick one versus the other? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q98: What's the difference between a variable that is: `null`, `undefined` or undeclared? How would you go about checking for any of these states? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q99: How can you share code between files? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q100: Explain why the following doesn't work as an IIFE. What needs to be changed to properly make it an IIFE? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q101: Write a recursive function that performs a binary search ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q102: What will be the output of the following code? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q103: Could you compare usage of Module Pattern vs Constructor/Prototype pattern? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q104: When would you use the "bind" function? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q105: Given an integer, determine if it is a power of 2. If so, return that number, else return -1 ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q106: Describe the JS module design pattern ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q107: How would you add your own method to the Array object so the following code would work? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q108: How to "deep-freeze" object in JavaScript? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q109: Is JavaScript a pass-by-reference or pass-by-value language? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q110: Can you give an example of a curry function and why this syntax offers an advantage? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q111: In JavaScript, why is the “this” operator inconsistent? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q112: What's the difference between ES6 Map and WeakMap? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q113: Describe the Revealing Module Pattern design pattern ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q114: What is the difference between the await keyword and the yield keyword?  ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q115: Is it possible to reset an ECMAScript 6 generator to its initial state? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q116: Compare Async/Await and Generators usage to achive same functionality ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

## [[⬆]](#toc) <a name=Kotlin>Kotlin</a> Interview Questions
#### Q1: How to initialize an array in Kotlin with values? ⭐⭐
**Details:**
In Java an array can be initialized such as:

```java
 int numbers[] = new int[] {10, 20, 30, 40, 50}
```

How does Kotlin's array initialization look like?

**Answer:**
```kotlin
val numbers: IntArray = intArrayOf(10, 20, 30, 40, 50)
```

**Source:** _stackoverflow.com_

#### Q2: How to correctly concatenate a String in Kotlin? ⭐⭐
**Answer:**
In Kotlin, you can concatenate 
1. using string interpolation / templates
 ```kotlin
val a = "Hello"
val b = "World"
val c = "$a $b"
 ```
2. using the + / `plus()` operator
 ```kotlin
 val a = "Hello"
 val b = "World" 
 val c = a + b   // same as calling operator function a.plus(b)
 val c = a.plus(b)
 
 print(c)
 ```
3. using the `StringBuilder`
 ```kotlin
 val a = "Hello"
 val b = "World"
 
 val sb = StringBuilder()
 sb.append(a).append(b)
 val c = sb.toString()
 
 print(c)
 ```

**Source:** _stackoverflow.com_

#### Q3: What is basic difference between fold and reduce in Kotlin? When to use which? ⭐⭐
**Answer:**
* `fold` takes an initial value, and the first invocation of the lambda you pass to it will receive that initial value and the first element of the collection as parameters.

 ```kotlin 
 listOf(1, 2, 3).fold(0) { sum, element -> sum + element }
 ```
 The first call to the lambda will be with parameters `0` and `1`.

 Having the ability to pass in an initial value is useful _if you have to provide some sort of default value or parameter for your operation_.

* `reduce` doesn't take an initial value, but instead starts with the first element of the collection as the accumulator (called `sum` in the following example)

 ```kotlin
 listOf(1, 2, 3).reduce { sum, element -> sum + element }
 ```

 The first call to the lambda here will be with parameters `1` and `2`.

**Source:** _stackoverflow.com_

#### Q4: What is the idiomatic way to remove duplicate strings from array? ⭐⭐
**Details:**
How to remove duplicates from an `Array<String?>` in Kotlin?

**Answer:**
Use the `distinct` extension function:

```kotlin
val a = arrayOf("a", "a", "b", "c", "c")
val b = a.distinct() // ["a", "b", "c"]
```

You can also use:
* `toSet`, `toMutableSet`
* `toHashSet` - if you don't need the original ordering to be preserved

These functions produce a `Set` instead of a `List` and should be a little bit more efficient than distinct.

**Source:** _stackoverflow.com_

#### Q5: What is the difference between var and val in Kotlin? ⭐⭐
**Answer:**
* **var** is like `general` variable and it's known as a _mutable_ variable in kotlin and can be assigned multiple times.

* **val** is like `Final` variable and it's known as _immutable_ in Kotlin and can be initialized only single time.

```sh
+----------------+-----------------------------+---------------------------+
|                |             val             |            var            |
+----------------+-----------------------------+---------------------------+
| Reference type | Immutable(once initialized  | Mutable(can able to change|
|                | can't be reassigned)        | value)                    |
+----------------+-----------------------------+---------------------------+
| Example        | val n = 20                  | var n = 20                |
+----------------+-----------------------------+---------------------------+
| In Java        | final int n = 20;           | int n = 20;               |
+----------------+-----------------------------+---------------------------+
```

**Source:** _stackoverflow.com_

#### Q6: Where should I use var and where val? ⭐⭐
**Answer:**
Use **var** where value is changing _frequently_. For example while getting location of android device:

```kotlin
var integerVariable : Int? = null
```

Use **val** where there is _no change_ in value in whole class. For example you want set textview or button's text programmatically.

```kotlin
val stringVariables : String = "Button's Constant or final Text"
```

**Source:** _stackoverflow.com_

#### Q7: What is a data class in Kotlin? ⭐⭐
**Answer:**
We frequently create classes whose main purpose is to hold data. In Kotlin, this is called a data class and is marked as `data`:

```kotlin
data class User(val name: String, val age: Int)
```

To ensure consistency and meaningful behavior of the generated code, data classes have to fulfill the following requirements:

* The primary constructor needs to have at least one parameter;
* All primary constructor parameters need to be marked as val or var;
* Data classes cannot be abstract, open, sealed or inner;

**Source:** _kotlinlang.org_

#### Q8: What is a primary constructor in Kotlin? ⭐⭐
**Answer:**
The **primary constructor** is part of the class header. Unlike Java, you don't need to declare a constructor in the body of the class. Here's an example:

```kotlin
class Person(val firstName: String, var age: Int) {
    // class body
}
```

The main idea is by removing the constructor keyword, our code gets simplified and easy to understand.

**Source:** _www.programiz.com_

#### Q9: How to create singleton in Kotlin? ⭐⭐
**Answer:**
Just use `object`.
```kotlin
object SomeSingleton
```
The above Kotlin object will be compiled to the following equivalent Java code:
```java
public final class SomeSingleton {
   public static final SomeSingleton INSTANCE;

   private SomeSingleton() {
      INSTANCE = (SomeSingleton)this;
      System.out.println("init complete");
   }

   static {
      new SomeSingleton();
   }
}
```
This is the preferred way to implement singletons on a JVM because it enables thread-safe lazy initialization without having to rely on a locking algorithm like the complex double-checked locking.

**Source:** _medium.com_

#### Q10: How to convert List to Map in Kotlin? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q11: What will be result of the following code execution? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q12: Why would you use apply in Kotlin? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q13: Explain what is wrong with that code? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q14: How are extensions resolved in Kotlin and what doest it mean? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q15: What is a purpose of Companion Objects in Kotlin? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q16: What is Lateinit in Kotlin and when would you use it? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q17: What are scope functions in Kotlin? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q18: When to use lateinit over lazy initialization in Kotlin? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q19: What is the purpose of Unit-returning in functions? Why is VALUE there? What is this VALUE? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q20: What is the Kotlin double-bang (!!) operator? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q21: May you briefly compare Kotlin vs Java? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q22: What are coroutines in Kotlin? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q23: What is the difference between suspending vs. blocking? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q24: What is suspending function in Kotlin? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q25: How would you create a singleton with parameter in Kotlin? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q26: What is the equivalent of Java static methods in Kotlin? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q27: Explain the Null safety in Kotlin ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q28: May you use IntArray and an Array<Int> is in Kotlin interchangeably? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q29: How is it recommended to create constants in Kotlin? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q30: Explain advantages of "when" vs "switch" in Kotlin ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q31: What are the advantages of Kotlin over Java? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q32: What are some disadvantages of Kotlin? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q33: What is the difference between "open" and "public" in Kotlin? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q34: What is the difference between “const” and “val”? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q35: Explain lazy initialization in Kotlin ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q36: val mutableList vs var immutableList. When to use which in Kotlin? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q37: What is the difference between List and Array types? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q38: What is the idiomatic way to deal with nullable values, referencing or converting them? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q39: When would you use Elvis operator in Kotlin? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q40: What is a difference between a class and object in Kotlin? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q41: Rewrite this code in Kotlin ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q42: How would you refactor this code using "apply"? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q43: Explain the difference between Inline classes vs type aliases ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q44: Rewrite this code using "run" extension function  ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q45: Why is there no static keyword in Kotlin? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q46: What is inline class in Kotlin and when do we need one? Provide an example. ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q47: Provide a real use case when inline classes may be useful ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q48: What is Kotlin backing field is used for? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q49: What are Object expressions in Kotlin and when to use them? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q50: How can I create “static” method for enum in Kotiln? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q51: How to create an instance of anonymous class of abstract class in Kotlin? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q52: How to create empty constructor for data class in Kotlin? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q53: What is Coroutine Scope and how is that different from Coroutine Context? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q54: How would you override default getter for Kotlin data class? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q55: How does the reified keyword in Kotlin work? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q56: Imagine you moving your code from Java to Kotlin. How would you rewrite this code in Kotlin? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q57: What is SAM Conversion in Kotlin? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q58: What is The Billion Dollar Mistake? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q59: What is the difference between “*” and “Any” in Kotlin generics? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q60: What is the difference between Java field and Kotlin property? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q61: How to implement Builder pattern in Kotlin? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q62: What's wrong with that code? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q63: What is a motivation to make classes final by default in Kotlin? Do you agree with that decision? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q64: Explain the difference between lateinit and lazy in details ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q65: What is the difference between launch/join and async/await in Kotlin coroutines? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q66: When to use and do not use an inline function in Kotlin? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q67: How Kotlin coroutines are better than RxKotlin/RxJava? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q68: Why do we use “companion object” as a kind of replacement for Java static fields in Kotlin? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

## [[⬆]](#toc) <a name=LINQ>LINQ</a> Interview Questions
#### Q1: What is LINQ? ⭐
**Answer:**
**LINQ** stands for Language INtegrated Query. LINQ allows us to write queries over local collection objects and remote data sources like SQL, XML documents etc. We can write LINQ query on any collection class which implements the `IEnumerable` interface.

**Source:** _stackoverflow.com_

#### Q2: Explain what is LINQ? Why is it required? ⭐
**Answer:**
**Language Integrated Query** or **LINQ** is the collection of standard query operators which provides query facilities into.NET framework language like C#, VB.NET. LINQ is required as it bridges the gap between the world of data and the world of objects.

**Source:** _career.guru99.com_

#### Q3: What are the types of LINQ? ⭐
**Answer:**
*   LINQ to Objects
*   LINQ to XML
*   LINQ to Dataset
*   LINQ to SQL
*   LINQ to Entities

**Source:** _career.guru99.com_

#### Q4: List out the three main components of LINQ? ⭐⭐
**Answer:**
Three main components of LINQ are

*   Standard Query Operators
*   Language Extensions
*   LINQ Providers

**Source:** _career.guru99.com_

#### Q5: What are Extension Methods? ⭐⭐
**Answer:**
**Extension methods** are static functions of a static class. These methods can be invoked just like instance method syntax. These methods are useful when we can not want to modify the class. Consider:

```csharp
public static class StringMethods
{
    public static bool IsStartWithLetterM(this string s)
    {
        return s.StartsWith("m");
    }
}
class Program
{
    static void Main(string[] args)
    {
        string value = "malslfds";
        Console.WriteLine(value.IsStartWithLetterM()); //print true;
 
        Console.ReadLine();
    }
}
```

**Source:** _stackoverflow.com_

#### Q6: Explain why SELECT clause comes after FROM clause in LINQ? ⭐⭐
**Answer:**
With other programming language and C#, LINQ is used, it requires all the variables to be declared first. “FROM” clause of LINQ query defines the range or conditions to select records. So, FROM clause must appear before SELECT in LINQ.

**Source:** _career.guru99.com_

#### Q7: What is Anonymous function? ⭐⭐
**Answer:**
An Anonymous function is a special function which does not have any name. We just define their parameters and define the code into the curly braces.

Consider:
```csharp
delegate int func(int a, int b);
static void Main(string[] args)
{
    func f1 = delegate(int a, int b)
    {
        return a + b;
    };
 
    Console.WriteLine(f1(1, 2));
}
```

**Source:** _stackoverflow.com_

#### Q8:  What are Anonymous Types? ⭐⭐
**Answer:**
Anonymous types are types that are generated by compiler at run time. When we create a anonymous type we do not specify a name. We just write properties names and their values. Compiler at runtime create these properties and assign values to them.

```csharp
var k = new { FirstProperty = "value1", SecondProperty = "value2" };
Console.WriteLine(k.FirstProperty);
```

Anonymous class is useful in LINQ queries to save our intermediate results.

There are some restrictions on Anonymous types as well:

*   Anonymous types can not implement interfaces.
*   Anonymous types can not specify any methods.
*   We can not define static members.
*   All defined properties must be initialized.
*   We can only define public fields.

**Source:** _stackoverflow.com_

#### Q9: Explain how LINQ is useful than Stored Procedures? ⭐⭐
**Answer:**
*   **Debugging:** It is difficult to debug a stored procedure but as LINQ is part of.NET, visual studio debugger can be used to debug the queries
*   **Deployment:** For stored procedure, additional script should be provided but with LINQ everything gets compiled into single DLL hence deployment becomes easy
*   **Type Safety:** LINQ is type safe, so queries errors are type checked at compile time

**Source:** _career.guru99.com_

#### Q10: In LINQ how will you find the index of the element using where() with Lambda Expressions? ⭐⭐
**Answer:**
In order to find the index of the element use the overloaded version of `where()` with the lambda expression:

```csharp
where(( i, ix ) => i == ix);
```

**Source:** _career.guru99.com_

#### Q11: Mention what is the role of DataContext classes in LINQ? ⭐⭐
**Answer:**
**DataContext** class acts as a bridge between SQL Server database and the LINQ to SQL. For accessing the database and also for changing the data in the database, it contains connections string and the functions. Essentially a DataContext class performs the following three tasks:

* Create connection to database.
* It submits and retrieves object to database.
* Converts objects to SQL queries and vice versa.

**Source:** _career.guru99.com_

#### Q12: Explain what is the purpose of LINQ providers in LINQ? ⭐⭐
**Answer:**
LINQ providers are set of classes that take an LINQ query which generates method that executes an equivalent query against a particular data source.

**Source:** _career.guru99.com_

#### Q13: Explain what is “LINQ to Objects”? ⭐⭐
**Answer:**
When LINQ queries any `IEnumerable(<T>)` collection or IEnumerable directly without the use of an intermediate LINQ provider or API such as LINQ to SQL or LINQ to XML is referred as **LINQ to Objects**.

**Source:** _career.guru99.com_

#### Q14: What is Expression Trees and how they used in LINQ? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q15: Using LINQ to remove elements from a List<T> ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q16: When to use First() and when to use FirstOrDefault() with LINQ? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q17: Explain what is the difference between Skip() and SkipWhile() extension method? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q18: What is the difference between First() and Take(1)? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q19: Explain how standard query operators useful in LINQ? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q20: Explain what is lambda expressions in LINQ? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q21: Could you explian what is the exact deference between deferred execution and Lazy evaluation in C#? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q22: Explain what are LINQ compiled queries? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q23: Could you compare Entity Framework vs LINQ to SQL vs ADO.NET with stored procedures? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q24: Get the indexes of top n items where item value = true ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q25: Define what is Let clause? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q26: When trying to decide between using the Entity Framework and LINQ to SQL as an ORM, what's the difference? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q27: What are the benefits of a Deferred Execution in LINQ? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q28: What is an equivalent to the "let" keyword in chained LINQ extension method calls? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q29: When should I use a CompiledQuery? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q30: Name some advantages of LINQ over Stored Procedures ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q31: Name some disadvantages of LINQ over sprocs ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q32: What is the difference between returning IQueryable<T> vs. IEnumerable<T>? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q33: Can you provide a concise distinction between anonymous method and lambda expressions? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q34: Why use .AsEnumerable() rather than casting to IEnumerable<T>? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q35: What is the difference between Select and SelectMany? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

## [[⬆]](#toc) <a name=Laravel>Laravel</a> Interview Questions
#### Q1: What is the Laravel? ⭐
**Answer:**
**Laravel** is a free, open-source PHP web framework, created by Taylor Otwell and intended for the development of web applications following the model–view–controller (MVC) architectural pattern.

**Source:** _codingcompiler.com_

#### Q2: Why do you prefer using Laravel? ⭐
**Answer:**
* Simple MVC that can be extended easily
* Clean and secure routing
* Powerful Eloquent ORM for database
* Migrations
* Third party plugins

**Source:** _linkedin.com_

#### Q3: Is there any CLI for Laravel? ⭐
**Answer:**
PHP artisan is the command line interface/tool included with Laravel. It provides a number of helpful commands that can help you while you build your application easily. Here are the list of some artisian commands:

* php artisan list
* php artisan help
* php artisan tinker
* php artisan make
* php artisan –versian
* php artisan make modal modal_name
* php artisan make controller controller_name

**Source:** _mytectra.com_

#### Q4: What are some benefits of Laravel over other Php frameworks? ⭐
**Answer:**
* Setup and customisation process is  easy and fast as compared to others.
* Inbuilt Authentication System
* Supports multiple file systems
* Pre-loaded packages like Laravel Socialite, Laravel cashier, Laravel elixir, Passport, Laravel Scout
* Eloquent ORM (Object Relation Mapping) with PHP active record implementation
* Built in command line tool “Artisan” for creating a code skeleton ,database structure and build their migration

**Source:** _mytectra.com_

#### Q5: What is Service Container? ⭐⭐
**Answer:**
The Laravel **service container** is a tool for managing class dependencies and performing dependency injection. 

**Source:** _laravel.com_

#### Q6: Why are migrations necessary? ⭐⭐
**Answer:**
Migrations are necessary because:

* Without migrations, database consistency when sharing an app is almost impossible, especially as more and more people collaborate on the web app.
* Your production database needs to be synced as well.

**Source:** _linkedin.com_

#### Q7: What is the purpose of the Eloquent cursor() method in Laravel ? ⭐⭐
**Answer:**
The **cursor** method allows you to iterate through your database records using a cursor, which will only execute a single query. When processing large amounts of data, the cursor method may be used to greatly reduce your memory usage.

```js
foreach (Product::where('name', 'bar')->cursor() as $flight) {
   //do some stuff
}
```

**Source:** _laravelinterviewquestions.com_

#### Q8: Explain Migrations in Laravel ⭐⭐
**Answer:**
**Laravel Migrations** are like version control for the database, allowing a team to easily modify and share the application’s database schema. Migrations are typically paired with Laravel’s schema builder to easily build the application’s database schema.

**Source:** _laravelinterviewquestions.com_

#### Q9: What is Eloquent Models? ⭐⭐
**Answer:**
The Eloquent ORM included with Laravel provides a beautiful, simple ActiveRecord implementation for working with your database. Each database table has a corresponding **Model** which is used to interact with that table. Models allow you to query for data in your tables, as well as insert new records into the table.

**Source:** _laravel.com_

#### Q10: List some official packages of Laravel ⭐⭐
**Answer:**
* **Cashier** - Laravel Cashier provides an expressive, fluent interface to Stripe's and Braintree's subscription billing services. 
* **Dusk** - Laravel Dusk provides an expressive, easy-to-use browser automation and testing API.
* **Envoy** - Laravel Envoy provides a clean, minimal syntax for defining common tasks you run on your remote servers. 
* **Horizon** - Horizon provides a dashboard and code-driven configuration for your Laravel powered Redis queues. 
* **Passport** - provides a full OAuth2 server implementation for your Laravel application in a matter of minutes.
* **Scout** - Laravel Scout provides a simple, driver based solution for adding full-text search to your Eloquent models. 
* **Socialite** - a simple, convenient way to authenticate with OAuth providers using Laravel Socialite. 

**Source:** _laravel.com_

#### Q11: What are Laravel events? ⭐⭐
**Answer:**
Laravel event provides a simple **observer pattern** implementation, that allow to subscribe and listen for events in the application. An event is an incident or occurrence detected and handled by the program.

Below are some events examples in Laravel:

* A new user has registered
* A new comment is posted
* User login/logout
* New product is added.

**Source:** _mytectra.com_

#### Q12: What is the Facade Pattern used for? ⭐⭐
**Answer:**
**Facades** provide a *static* interface to classes that are available in the application's service container. Laravel facades serve as *static proxies* to underlying classes in the service container, providing the benefit of a terse, expressive syntax while maintaining more testability and flexibility than traditional static methods.

All of Laravel's facades are defined in the `Illuminate\Support\Facades` namespace. 
Consider:
```js
use Illuminate\Support\Facades\Cache;

Route::get('/cache', function () {
    return Cache::get('key');
});
```

**Source:** _laravel.com_

#### Q13: How do you generate migrations? ⭐⭐
**Answer:**
Migrations are like version control for your database, allowing your team to easily modify and share the application's database schema. 

To create a migration, use:
```js
php artisan make:migration create_users_table
```

**Source:** _laravel.com_

#### Q14: Which template engine does Laravel use? ⭐⭐
**Answer:**
Laravel uses **Blade Templating Engine.**

Blade is the simple, yet powerful templating engine provided with Laravel. Unlike other popular PHP templating engines, Blade does not restrict you from using plain PHP code in your views. In fact, all Blade views are compiled into plain PHP code and cached until they are modified, meaning Blade adds essentially zero overhead to your application. Blade view files use the .blade.php file extension and are typically stored in the `resources/views` directory.

**Source:** _laravelinterviewquestions.com_

#### Q15: What are artisan commands? ⭐⭐
**Answer:**
Artisan is the name of the command-line interface included with Laravel. It provides a number of helpful commands for your use while developing your application for example:

```php
php artisan serve // To start Laravel project
```

**Source:** _laravel.comv_

#### Q16: How do you check “if not null” with Eloquent? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q17: What is Laravel Passport? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q18: What is reverse routing in Laravel? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q19: List some Aggregates methods provided by query builder in Laravel ? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q20: List types of relationships available in Laravel Eloquent? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q21: How to Rollback one specific migration in Laravel? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q22: How do you mock a static facade methods? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q23: What are Queues and Job workers? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q24: What is the benefit of eager loading, when do you use it? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q25: How do you generate event and listeners? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q26: How do you do soft deletes? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q27: What do you know about query builder in Laravel? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q28: What are query scopes? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q29: What are named routes in Laravel? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q30: What are the benefits of using Vue.js with Laravel? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q31: Where can you easily hook on validation in Laravel 5.x? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q32: How do you generate migrations? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q33: What is Closure in Laravel? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q34: Why do we need Traits in Laravel? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q35: Where can you inject authentication checks on an API request? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q36: How Do I Get the Query Builder to Output Its Raw SQL Query as a String? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q37: What is Autoloader in PHP? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q38: Explain the structure of the Migration Class ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q39: How does Laravel use IoC? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q40: What are some Differences and Similarities Between Lumen and Laravel? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q41: What do you know about service providers? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

## [[⬆]](#toc) <a name=MSMQ>MSMQ</a> Interview Questions
#### Q1: What is Message in MSMQ? ⭐
**Answer:**
Messages are just envelopes that are used to send data through the queues. They can be **application-generated** or **system-generated**. **Application-generated messages** are sent by queued messaging applications.

**Source:** _simpleorientedarchitecture.com_

#### Q2: Why do we use MSMQ? ⭐⭐
**Answer:**
**Microsoft Message Queuing**, or MSMQ, is technology for asynchronous messaging. Whenever there's need for two or more applications (processes) to send messages to each other without having to immediately know results, MSMQ can be used. MSMQ can communicate between remote machines, even over Internet. It's free and comes with Windows, but is not installed by default.

This mainly addresses the common use case of asynchronous message processing: you have a service `Service1` that communicates (send messages) with another part of your software architecture, say `Service2`.

Main problem: what if `Service2` becomes suddenly unavailable? Will messages be lost?
If you use MSMQ it won't: `Service1` will send messages into a queue, and `Service2` will dequeue when it is available.

MSMQ will resolve following common issues:

 - temporary unavailability of a service: messages are persisted on the disk and will be dequeued when the service becomes available again, so **no messages are lost**
 - as it's fully asynchronous, it'll help a lot in case of **punctual peak load**: your `Service2` won't die under the heavy load, it'll just dequeue and process messages, one after one

**Source:** _cogin.com_

#### Q3: What is Queue in MSMQ? ⭐⭐
**Answer:**
The queue is just a container that stores messages, decoupling the sender from the receiver. MSMQ Queues are not necessarily FIFO (First In, First Out), because messages can be prioritized.

Queues can be **transactional** or **nontransactional**. 
* Transactional Queues can only receive  messages sent within a transactional context. 
* Nontransactional queues can only receive messages sent outside of a transactional context. 

Messages sent in a transactional context are processed in the order in which they were sent.

**Source:** _simpleorientedarchitecture.com_

#### Q4: How to use MSMQ in Azure applications? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q5: Name different types of Application Queues in MSMQ ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q6: Name some benefits of MSMQ? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q7: What are the benefits and tradeoffs of using MSMQ over a SQL Table in this situation, and why should I choose one over the other? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q8: When would we use MSMQ? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q9: What types of timer provided by MSMQ? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q10: How to publish messages asynchronously to MSMQ in .NET Core? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q11: Is there any alternatives to MSMQ for Azure? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q12: What is the difference between Windows Service Bus and MSMQ? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q13: Is it possible for server A to access a private queue from server B? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q14:  If I have an application on windows machine A that wants to write to a queue on windows machine B, do I need to have MSMQ installed on machine A (even though there is no queue there)? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q15: Explain types of transaction in MSMQ ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q16: Would you choose MSMQ or Service Broker for mission critical applications? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

## [[⬆]](#toc) <a name=MachineLearning>Machine Learning</a> Interview Questions
#### Q1: What is Machine Learning? ⭐
**Answer:**
**Machine learning** is the study of algorithms and mathematical models that computer systems use to progressively improve their performance on a specific task. 

The name machine learning was coined in 1959 by *Arthur Samuel* as the science of getting computers to act without being explicitly programmed.

*Tom M. Mitchell* provided a widely quoted, more formal definition of the algorithms studied in the machine learning field: "A computer program is said to learn from experience E with respect to some class of tasks T and performance measure P if its performance at tasks in T, as measured by P, improves with experience E."

**Source:** _wikipedia.org_

#### Q2: What do you understand by Machine Learning? ⭐
**Answer:**

Machine learning is an application of artificial intelligence that provides systems the ability to automatically learn and improve from experience without being explicitly programmed. Machine learning focuses on the development of computer programs that can access data and use it learn for themselves.

**Source:** _www.educba.com_

#### Q3: Give an example that explains Machine Leaning in industry. ⭐
**Answer:**
Robots are replacing humans in many areas. It is because robots are programmed such that they can perform the task based on data they gather from sensors. They learn from the data and behaves intelligently

**Source:** _www.educba.com_

#### Q4: What are the different Algorithm techniques in Machine Learning? ⭐
**Answer:**
The different types of Algorithm techniques in Machine Learning are as follows:
 * Reinforcement Learning
 * Supervised Learning
 * Unsupervised Learning
 * Semi-supervised Learning
 * Transduction
 * Learning to Learn

**Source:** _www.educba.com_

#### Q5: What are Classification and Regression in ML? Explain the difference. ⭐⭐
**Answer:**
### Classification

Classification algorithms are used when the desired output is a discrete label. In other words, they’re helpful when the answer to your question about your business falls under a finite set of possible outcomes. Many use cases, such as determining whether an email is spam or not, have only two possible outcomes. This is called binary classification.

Multi-label classification captures everything else, and is useful for customer segmentation, audio and image categorization, and text analysis for mining customer sentiment. If these are the questions you’re hoping to answer with machine learning in your business, consider algorithms like naive Bayes, decision trees, logistic regression, kernel approximation, and K-nearest neighbors.

### Regression

On the other hand, regression is useful for predicting outputs that are continuous. That means the answer to your question is represented by a quantity that can be flexibly determined based on the inputs of the model rather than being confined to a set of possible labels. Regression problems with time-ordered inputs are called time-series forecasting problems, like ARIMA forecasting, which allows data scientists to explain seasonal patterns in sales, evaluate the impact of new marketing campaigns, and more.

Linear regression is by far the most popular example of a regression algorithm. Though it’s often underrated because of its relative simplicity, it’s a versatile method that can be used to predict housing prices, likelihood of customers to churn, or the revenue a customer will generate. For use cases like these, regression trees and support vector regression are good algorithms to consider if you’re looking for something more sophisticated than linear regression.

**Source:** _www.datascience.com_

#### Q6: What is Overfitting in Machine Learning? ⭐⭐
**Answer:**
Overfitting in Machine Learning is defined as when a statistical model describes random error or noise instead of underlying relationship or when a model is excessively complex.

**Source:** _www.educba.com_

#### Q7: What s Classification in Machine Learning? ⭐⭐
**Answer:**
In machine learning and statistics, classification is the problem of identifying to which of a set of categories (sub-populations) a new observation belongs, on the basis of a training set of data containing observations (or instances) whose category membership is known. Examples are assigning a given email to the "spam" or "non-spam" class, and assigning a diagnosis to a given patient based on observed characteristics of the patient (sex, blood pressure, presence or absence of certain symptoms, etc.). Classification is an example of pattern recognition.

In the terminology of machine learning, classification is considered an instance of supervised learning, i.e., learning where a training set of correctly identified observations is available. The corresponding unsupervised procedure is known as clustering, and involves grouping data into categories based on some measure of inherent similarity or distance.

**Source:** _wikipedia.org_

#### Q8: What is Regression Analysis? ⭐⭐
**Answer:**
In statistical modeling, regression analysis is a set of statistical processes for estimating the relationships among variables. It includes many techniques for modeling and analyzing several variables, when the focus is on the relationship between a dependent variable and one or more independent variables (or 'predictors'). More specifically, regression analysis helps one understand how the typical value of the dependent variable (or 'criterion variable') changes when any one of the independent variables is varied, while the other independent variables are held fixed.

**Source:** _wikipedia.org_

#### Q9: What is the difference between supervised and unsupervised machine learning? ⭐⭐
**Answer:**
Supervised learning is a process where it requires training labeled data While Unsupervised learning it doesn’t require data labeling.

**Source:** _www.educba.com_

#### Q10: What is the function of Unsupervised Learning? ⭐⭐
**Answer:**
The function of Unsupervised Learning are as below:
* Find clusters of the data
* Find low-dimensional representations of the data
* Find interesting directions in data
* Find interesting coordinates and correlations
* Find novel observations

**Source:** _www.educba.com_

#### Q11: What is the function of Supervised Learning? ⭐⭐
**Answer:**
The function of Supervised Learning are as below:
* Classifications
* Speech recognition
* Regression
* Predict time series
* Annotate strings

**Source:** _www.educba.com_

#### Q12: What are the disadvantages of neural networks? ⭐⭐
**Answer:**
Neural Network requires a large amount of training data to converge. It’s also difficult to pick the right architecture, and the internal “hidden” layers are incomprehensible.

**Source:** _www.educba.com_

#### Q13: What are the advantages of neural networks? ⭐⭐
**Answer:**
Neural networks have led to performance breakthroughs for unstructured datasets such as images, audio, and video. Their incredible flexibility allows them to learn patterns that no other Machine Learning algorithm can learn.

**Source:** _www.educba.com_

#### Q14: What are the disadvantages of decision trees? ⭐⭐
**Answer:**
Decision trees are prone to be overfit. However, this can be addressed by ensemble methods like random forests or boosted trees.

**Source:** _www.educba.com_

#### Q15: Explain the difference between Supervised Learning and Unsupervised Learning? ⭐⭐
**Answer:**
Supervised machine learning is the more commonly used between the two. It includes such algorithms as linear and logistic regression, multi-class classification, and support vector machines. Supervised learning is so named because the data scientist acts as a guide to teach the algorithm what conclusions it should come up with. It’s similar to the way a child might learn arithmetic from a teacher. Supervised learning requires that the algorithm’s possible outputs are already known and that the data used to train the algorithm is already labeled with correct answers. For example, a classification algorithm will learn to identify animals after being trained on a dataset of images that are properly labeled with the species of the animal and some identifying characteristics.

On the other hand, unsupervised machine learning is more closely aligned with what some call true artificial intelligence — the idea that a computer can learn to identify complex processes and patterns without a human to provide guidance along the way. Although unsupervised learning is prohibitively complex for some simpler enterprise use cases, it opens the doors to solving problems that humans normally would not tackle. Some examples of unsupervised machine learning algorithms include k-means clustering, principal and independent component analysis, and association rules.

While a supervised classification algorithm learns to ascribe inputted labels to images of animals, its unsupervised counterpart will look at inherent similarities between the images and separate them into groups accordingly, assigning its own new label to each group. In a practical example, this type of algorithm is useful for customer segmentation because it will return groups based on parameters that a human may not consider due to pre-existing biases about the company’s demographic.

Choosing to use either a supervised or unsupervised machine learning algorithm typically depends on factors related to the structure and volume of your data and the use case of the issue at hand. A well-rounded data science program will use both types of algorithms to build predictive data models that help stakeholders make decisions across a variety of business challenges.

**Source:** _www.datascience.com_

#### Q16: What are the conditions when Overfitting happens? ⭐⭐
**Answer:**
One of the important reason and possibility of overfitting is because the criteria used for training the model is not the same as the criteria used to judge the efficacy of a model.

**Source:** _www.educba.com_

#### Q17: How can you avoid overfitting? ⭐⭐
**Answer:**
We can avoid overfitting by using:
* Lots of data
* Cross-validation

**Source:** _www.educba.com_

#### Q18: What are the five popular algorithms for Machine Learning? ⭐⭐
**Answer:**
Below is the list of five popular algorithms of Machine Learning:
* Decision Trees
* Probabilistic networks
* Nearest Neighbor
* Support vector machines
* Neural Networks

**Source:** _www.educba.com_

#### Q19: What are the different use cases where machine learning algorithms can be used? ⭐⭐
**Answer:**
The different use cases where machine learning algorithms can be used are as follows:
* Fraud Detection
* Face detection
* Natural language processing
* Market Segmentation
* Text Categorization
* Bioinformatics

**Source:** _www.educba.com_

#### Q20: What are parametric models and Non-Parametric models? ⭐⭐
**Answer:**
Parametric models are those with a finite number of parameters and to predict new data, you only need to know the parameters of the model.
Non Parametric models are those with an unbounded number of parameters, allowing for more flexibility and to predict new data, you need to know the parameters of the model and the state of the data that has been observed.

**Source:** _www.educba.com_

#### Q21: What are the three stages to build the hypotheses or model in machine learning? ⭐⭐
**Answer:**
The three stages to build the hypotheses or model in machine learning are:
1. Model building
2. Model testing
3. Applying the model

**Source:** _www.educba.com_

#### Q22: What is Inductive Logic Programming in Machine Learning (ILP)? ⭐⭐
**Answer:**
Inductive Logic Programming (ILP) is a subfield of machine learning which uses logical programming representing background knowledge and examples.

**Source:** _www.educba.com_

#### Q23: What is the difference between classification and regression? ⭐⭐
**Answer:**
The difference between classification and regression are as follows:
* Classification is about identifying group membership while regression technique involves predicting a response.
* Classification and Regression techniques are related to prediction
* Classification predicts the belonging to a class whereas regression predicts the value from a continuous set
* Classification technique is preferred over regression when the results of the model need to return the belongingness of data points in a dataset with specific explicit categories


**Source:** _www.educba.com_

#### Q24: What are the difference between inductive machine learning and deductive machine learning? ⭐⭐
**Answer:**
The difference between inductive machine learning and deductive machine learning are as follows:
Inductive machine learning is where the model learns by examples from a set of observed instances to draw a generalized conclusion whereas in deductive learning the model first draws the conclusion and then the conclusion is drawn.

**Source:** _www.educba.com_

#### Q25: What are the advantages of decision trees? ⭐⭐
**Answer:**
The advantages decision trees are:
* Decision trees are easy to interpret
* Nonparametric
* There are relatively few parameters to tune

**Source:** _www.educba.com_

#### Q26: Why is Naive Bayes so naive? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q27: What are the disadvantages of Naive Bayes? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q28: What are the advantages of Naive Bayes? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q29: What is the difference between L1 and L2 regularization? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

## [[⬆]](#toc) <a name=Microservices>Microservices</a> Interview Questions
#### Q1: Why Would You Opt For Microservices Architecture? ⭐⭐
**Answer:**
There are plenty of pros that are offered by Microservices architecture. Here are a few of them:

* Microservices can adapt easily to other frameworks or technologies.
* Failure of a single process does not affect the entire system.
* Provides support to big enterprises as well as small teams.
* Can be deployed independently and in relatively less time.

**Source:** _lambdatest.com_

#### Q2: List down the advantages of Microservices Architecture ⭐⭐
**Answer:**
* **Independent Development**.	All microservices can be easily developed based on their individual functionality
* **Independent Deployment**.	Based on their services, they can be individually deployed in any application
* **Fault Isolation**.	Even if one service of the application does not work, the system still continues to function
* **Mixed Technology Stack**.	Different languages and technologies can be used to build different services of the same application
* **Granular Scaling**.	Individual components can scale as per need, there is no need to scale all components together

**Source:** _lambdatest.com_

#### Q3: Define Microservice Architecture ⭐⭐
**Answer:**
**Microservices**, aka **_Microservice Architecture_**, is an architectural style that structures an application as a collection of small autonomous services, modeled around a **business domain.**

**Source:** _lambdatest.com_

#### Q4: What is the difference between Monolithic, SOA and Microservices Architecture? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q5: What are the standard patterns of orchestrating microservices? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q6: What are the features of Microservices? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q7: How does Microservice Architecture work? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q8: What Are The Fundamentals Of Microservices Design? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q9: What are the challenges you face while working Microservice Architectures? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q10: Whether do you find GraphQL the right fit for designing microservice architecture? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q11: What is the difference between a proxy server and a reverse proxy server? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q12: How can we perform Cross-Functional testing? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q13: What are main differences between Microservices and Monolithic Architecture? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q14: What are smart endpoints and dumb pipes? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q15: What is the role of an architect in Microservices architecture? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q16: What is Materialized View pattern and when will you use it? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q17: What are the pros and cons of Microservice Architecture? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q18: Mention some benefits and drawbacks of an API Gateway ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q19: Can we create State Machines out of Microservices? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q20: Explain what is the API Gateway pattern ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q21: What is Idempotence? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q22: What do you understand by Distributed Transaction? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q23: What do you understand by Contract Testing? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q24: How should the various services share a common DB Schema and code? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q25: What does it mean that shifting to microservices creates a run-time problem? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q26: What is the most accepted transaction strategy for microservices ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q27: Provide an example of "smart pipes" and "dumb endpoint" ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q28: What are Reactive Extensions in Microservices? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q29: Why would one use sagas over 2PC and vice versa?  ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q30: What is a Consumer-Driven Contract (CDC)? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q31: What is the difference between cohesion and coupling? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q32: How would you implement SSO for Microservice Architecture? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q33: Name the main differences between SOA and Microservices? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q34: What Did The Law Stated By Melvin Conway Implied? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

## [[⬆]](#toc) <a name=MongoDB>MongoDB</a> Interview Questions
#### Q1: Does Mongodb Support Foreign Key Constraints? ⭐
**Answer:**
No. MongoDB does not support such relationships. The database does not apply any constraints to the system (i.e.: foreign key constraints), so there are no "cascading deletes" or "cascading updates". Basically, in a NoSQL database it is up to you to decide how to organise the data and its relations if there are any.

**Source:** _interviewbubble.com_

#### Q2: Which are the most important features of MongoDB? ⭐
**Answer:**
* Flexible data model in form of documents
* Agile and highly scalable database
* Faster than traditional databases
* Expressive query language

**Source:** _tutorialspoint.com_

#### Q3: Explain what is MongoDB? ⭐
**Answer:**
MongoDB is an open-source document database that provides high performance, high availability, and automatic scaling.
It's Key Features are:
* Document Oriented and NoSQL database.
* Supports Aggregation
* Uses BSON format
* Sharding (Helps in Horizontal Scalability)
* Supports Ad Hoc Queries
* Schema Less
* Capped Collection
* Indexing (Any field in MongoDB can be indexed)
* MongoDB Replica Set (Provides high availability)
* Supports Multiple Storage Engines

**Source:** _mongodb.com_

#### Q4: How many indexes does MongoDB create by default for a new collection? ⭐
**Answer:**
By default, MongoDB created the _id collection for every collection.

**Source:** _tutorialspoint.com_

#### Q5: Compare SQL databases and MongoDB at a high level. ⭐⭐
**Answer:**
SQL databases store data in form of tables, rows, columns and records. This data is stored in a pre-defined data model which is not very much flexible for today's real-world highly growing applications. MongoDB in contrast uses a flexible structure which can be easily modified and extended.

**Source:** _tutorialspoint.com_

#### Q6: What Is Replication In MongoDB? ⭐⭐
**Answer:**
**Replication** is the process of synchronizing data across multiple servers. Replication provides redundancy and increases data availability. With multiple copies of data on different database servers, replication protects a database from the loss of a single server. Replication also allows you to recover from hardware failure and service interruptions.

**Source:** _interviewbubble.com_

#### Q7: What is “Namespace” in MongoDB? ⭐⭐
**Answer:**
MongoDB stores BSON (Binary Interchange and Structure Object Notation) objects in the collection. The concatenation of the collection name and database name is called a namespace

**Source:** _medium.com/@hub4tech_

#### Q8: If you remove an object attribute, is it deleted from the database? ⭐⭐
**Answer:**
Yes, it be. Remove the attribute and then re-save () the object.

**Source:** _medium.com/@hub4tech_

#### Q9: Why does Profiler use in MongoDB? ⭐⭐
**Answer:**
MongoDB uses a database profiler to perform characteristics of each operation against the database. You can use a profiler to find queries and write operations

**Source:** _medium.com/@hub4tech_

#### Q10: What is BSON in MongoDB? ⭐⭐
**Answer:**
**BSON** is a binary serialization format used to store documents and make remote procedure calls in MongoDB. BSON extends the JSON model to provide additional data types, ordered fields, and to be efficient for encoding and decoding within different languages. 


**Source:** _mongodb.com_

#### Q11: Does MongoDB need a lot space of Random Access Memory (RAM)? ⭐⭐
**Answer:**
No. MongoDB can be run on small free space of RAM.

**Source:** _medium.com/@hub4tech_

#### Q12: How is data stored in MongoDB? ⭐⭐
**Answer:**
Data in MongoDB is stored in BSON documents – JSON-style data structures. Documents contain one or more fields, and each field contains a value of a specific data type, including arrays, binary data and sub-documents. Documents that tend to share a similar structure are organized as collections. It may be helpful to think of documents as analogous to rows in a relational database, fields as similar to columns, and collections as similar to tables.

The advantages of using documents are:

* Documents (i.e. objects) correspond to native data types in many programming languages.
* Embedded documents and arrays reduce need for expensive joins.
* Dynamic schema supports fluent polymorphism.

**Source:** _mongodb.com_

#### Q13: Mention the command to insert a document in a database called school and collection called persons. ⭐⭐
**Answer:**
```js
use school;
db.persons.insert( { name: "kadhir", dept: "CSE" } )
```

**Source:** _tutorialspoint.com_

#### Q14: What are Indexes in MongoDB? ⭐⭐
**Answer:**
Indexes support the efficient execution of queries in MongoDB. Without indexes, MongoDB must perform a collection scan, i.e. scan every document in a collection, to select those documents that match the query statement. If an appropriate index exists for a query, MongoDB can use the index to limit the number of documents it must inspect.

**Source:** _tutorialspoint.com_

#### Q15: What is a replica set? ⭐⭐
**Answer:**
It is a group of mongo instances that maintain same data set. Replica sets provide redundancy and high availability, and are the basis for all production deployments.

**Source:** _interviewbubble.com_

#### Q16: Can you create an index on an array field in MongoDB? If yes, what happens in this case? ⭐⭐
**Answer:**
Yes. An array field can be indexed in MongoDB. In this case, MongoDB would index each value of the array so you can query for individual items:

```js
> db.col1.save({'colors': ['red','blue']})
> db.col1.ensureIndex({'colors':1})

> db.col1.find({'colors': 'red'})
{ "_id" : ObjectId("4ccc78f97cf9bdc2a2e54ee9"), "colors" : [ "red", "blue" ] }
> db.col1.find({'colors': 'blue'})
{ "_id" : ObjectId("4ccc78f97cf9bdc2a2e54ee9"), "colors" : [ "red", "blue" ] }
```

**Source:** _stackoverflow.com_

#### Q17: When should we embed one document within another in MongoDB? ⭐⭐
**Answer:**
You should consider embedding documents for:

* *contains* relationships between entities
* One-to-many relationships
* Performance reasons

**Source:** _tutorialspoint.com_

#### Q18: How is MongoDB better than other SQL databases? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q19: Should I normalize my data before storing it in MongoDB? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q20: What is use of capped collection in MongoDB? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q21: What does MongoDB not being ACID compliant really mean? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q22: How to query MongoDB with %like%? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q23: How do I perform the SQL JOIN equivalent in MongoDB? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q24: When to use MongoDB or other document oriented database systems? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q25: What is the difference between MongoDB and MySQL? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q26: How can you achieve primary key - foreign key relationships in MongoDB? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q27: Does MongoDB pushes the writes to disk immediately or lazily? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q28: If you remove a document from database, does MongoDB remove it from disk? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q29: What is the difference b/w MongoDB and CouchDB? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q30: What is sharding? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q31: What are NoSQL databases? What are the different types of NoSQL databases? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q32: Explain the structure of ObjectID in MongoDB ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q33: What is a covered query in MongoDB? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q34: How can I combine data from multiple collections into one collection? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q35: Find objects between two dates MongoDB ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q36: How to query MongoDB with “like”? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q37: Is there an “upsert” option in the mongodb insert command? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q38: What is oplog? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q39: How can you achieve transaction and locking in MongoDB? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q40: What do you understand by NoSQL databases? Explain. ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q41: What is Sharding in MongoDB? Explain. ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q42: Can one MongoDB operation lock more than one databases? If yes, how? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q43: Mention the command to check whether you are on the master server or not. ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q44: Why are MongoDB data files large in size? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q45: Does MongoDB support ACID transaction management and locking functionalities? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q46: Why MongoDB is not preferred over a 32-bit system? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q47: What is Aggregation in MongoDB? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q48: How replication works in MongoDB? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q49: By default, MongoDB writes and reads data from both primary and secondary replica sets. True or False. ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q50: How does MongoDB provide concurrency? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q51: How can you isolate your cursors from intervening with the write operations? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q52: What are Primary and Secondary Replica sets? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q53: At what interval does MongoDB write updates to the disk? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q54: Mention the command to list all the indexes on a particular collection. ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q55: What happens if an index does not fit into RAM? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q56: Does MongoDB provide a facility to do text searches? How? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q57: Update MongoDB field using value of another field ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q58: How does Journaling work in MongoDB? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q59: Why is a covered query important? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q60: When to Redis or MongoDB? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q61: MongoDB relationships. What to use - embed or reference? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q62: Is MongoDB schema-less? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q63: How to get the last N records from find? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q64: How does MongoDB ensure high availability? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q65: How to find MongoDB records where array field is not empty? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q66: How to check if a field contains a substring? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q67: Where can I run MongoDB? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q68: What are alternatives to MongoDB? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q69: How to remove a field completely from a MongoDB document? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q70: What is a Storage Engine in MongoDB ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q71: How to find document with array that contains a specific value? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q72: What is splitting in mongodb? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q73: Is it possible to update MongoDB field using value of another field? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q74: Explain what is horizontal scalability? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q75: What are the differences between MongoDB and MySQL? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q76: How to condense large volumes of data in Mongo? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q77: Which are the two storage engines used by MongoDB? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q78: What's the advantage of the backup features in Ops Manager versus traditional backup strategies? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q79: What are three primary concerns when choosing a data management system? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

## [[⬆]](#toc) <a name=Node.js>Node.js</a> Interview Questions
#### Q1: What is Node.js? ⭐
**Answer:**
Node.js is a web application framework built on Google Chrome's JavaScript Engine (V8 Engine).

Node.js comes with runtime environment on which a Javascript based script can be interpreted and executed (It is analogus to JVM to JAVA byte code). This runtime allows to execute a JavaScript code on any machine outside a browser. Because of this runtime of Node.js, JavaScript is now can be executed on server as well.

*Node.js = Runtime Environment + JavaScript Library*

**Source:** _tutorialspoint.com_

#### Q2: What is npm? ⭐
**Answer:**
`npm` stands for Node Package Manager. npm provides following two main functionalities:

*   Online repositories for node.js packages/modules which are searchable on [search.nodejs.org](http://search.nodejs.org)
*   Command line utility to install packages, do version management and dependency management of Node.js packages.

**Source:** _tutorialspoint.com_

#### Q3: What are the two types of API functions in Node.js?  ⭐
**Answer:**
The two types of API functions in Node.js are: a) Asynchronous, non-blocking functions b) Synchronous, blocking functions

**Source:** _lazyquestion.com_

#### Q4: What is the difference between returning a callback and just calling a callback? ⭐⭐
**Answer:**
```js
return callback();
//some more lines of code; -  won't be executed

callback();
//some more lines of code; - will be executed
```

Of course returning will help the context calling async function get the value returned by callback.
```js
function do2(callback) {
    log.trace('Execute function: do2');
    return callback('do2 callback param');
}

var do2Result = do2((param) => {
    log.trace(`print ${param}`);
    return `return from callback(${param})`; // we could use that return
});

log.trace(`print ${do2Result}`);
```
Output:
```sh
C:\Work\Node>node --use-strict main.js
[0] Execute function: do2
[0] print do2 callback param
[0] print return from callback(do2 callback param)
```

**Source:** _stackoverflow.com_

#### Q5: What are Event Listeners?   ⭐⭐
**Answer:**
**Event Listeners** are similar to call back functions but are associated with some event. For example when a server listens to http request on a given port a event will be generated and to specify http server has received and will invoke corresponding event listener. Basically, Event listener's are also call backs for a corresponding event.

Node.js has built in event's and built in event listeners. Node.js also provides functionality to create Custom events and Custom Event listeners.

**Source:** _lazyquestion.com_

#### Q6: What is global installation of dependencies? ⭐⭐
**Answer:**
Globally installed packages/dependencies are stored in **<user-directory>**/npm directory. Such dependencies can be used in CLI (Command Line Interface) function of any node.js but can not be imported using require() in Node application directly. To install a Node project globally use -g flag.

**Source:** _tutorialspoint.com_

#### Q7: What is libuv? ⭐⭐
**Answer:**
**libuv** is a C library that is used to abstract non-blocking I/O operations to a consistent interface across all supported platforms. It provides mechanisms to handle file system, DNS, network, child processes, pipes, signal handling, polling and streaming. It also includes a thread pool for offloading work for some things that can't be done asynchronously at the operating system level.

**Source:** _nodejs.org_

#### Q8: What is V8? ⭐⭐
**Answer:**
The V8 library provides Node.js with a JavaScript engine (a program that converts Javascript code into lower level or machine code that microprocessors can understand), which Node.js controls via the V8 C++ API. V8 is maintained by Google, for use in Chrome.

The Chrome V8 engine :

* The V8 engine is written in C++ and used in Chrome and Nodejs.
* It implements ECMAScript as specified in ECMA-262.
* The V8 engine can run standalone we can embed it with our own C++ program.



**Source:** _nodejs.org_

#### Q9: What are the core modules of Node,js? ⭐⭐
**Answer:**
* EventEmitter
* Stream
* FS
* Net
* Global Objects

**Source:** _github.com/jimuyouyou_

#### Q10:  How you can monitor a file for modifications in Node.js ? ⭐⭐
**Answer:**
We can take advantage of File System `watch()` function which watches the changes of the file.

**Source:** _codingdefined.com_

#### Q11: Could we run an external process with Node.js? ⭐⭐
**Answer:**
Yes. *Child process module* enables us to access operating system functionaries or other apps. Scalability is baked into Node and child processes are the key factors to scale our application. You can use child process to run system commands, read large files without blocking event loop,  decompose the application into various “nodes” (That’s why it’s called Node).

Child process module has following three major ways to create child processes –

* spawn  - child_process.spawn launches a new process with a given command.
* exec  - child_process.exec method runs a command in a shell/console and buffers the output.
* fork - The child_process.fork method is a special case of the spawn() to create child processes.

**Source:** _codeforgeek.com_

#### Q12:  List out the differences between AngularJS and NodeJS? ⭐⭐
**Answer:**
AngularJS is a web application development framework. It’s a JavaScript and it is different from other web app frameworks written in JavaScript like jQuery. NodeJS is a runtime environment used for building server-side applications while AngularJS is a JavaScript framework mainly useful in building/developing client-side part of applications which run inside a web browser.

**Source:** _a4academics.com_

#### Q13: What do you mean by Asynchronous API? ⭐⭐
**Answer:**
All APIs of Node.js library are aynchronous that is non-blocking. It essentially means a Node.js based server never waits for a API to return data. Server moves to next API after calling it and a notification mechanism of Events of Node.js helps server to get response from the previous API call.

**Source:** _tutorialspoint.com_

#### Q14: What is Callback Hell? ⭐⭐
**Answer:**
The asynchronous function requires callbacks as a return parameter. When multiple asynchronous functions are chained together then callback hell situation comes up. 

**Source:** _codeforgeek.com_

#### Q15: If Node.js is single threaded then how it handles concurrency? ⭐⭐
**Answer:**
Node provides a single thread to programmers so that code can be written easily and without bottleneck. Node internally uses multiple POSIX threads for various I/O operations such as File, DNS, Network calls etc.

When Node gets I/O request it creates or uses a thread to perform that I/O operation and once the operation is done, it pushes the result to the event queue. On each such event, event loop runs and checks the queue and if the execution stack of Node is empty then it adds the queue result to execution stack.

This is how Node manages concurrency.

**Source:** _codeforgeek.com_

#### Q16: What are the benefits of using Node.js? ⭐⭐
**Answer:**
Following are main benefits of using Node.js

*   **Aynchronous and Event Driven** - All APIs of Node.js library are aynchronous that is non-blocking. It essentially means a Node.js based server never waits for a API to return data. Server moves to next API after calling it and a notification mechanism of Events of Node.js helps server to get response from the previous API call.
*   **Very Fast** - Being built on Google Chrome's V8 JavaScript Engine, Node.js library is very fast in code execution.
*   **Single Threaded but highly Scalable** - Node.js uses a single threaded model with event looping. Event mechanism helps server to respond in a non-bloking ways and makes server highly scalable as opposed to traditional servers which create limited threads to handle requests. Node.js uses a single threaded program and same program can services much larger number of requests than traditional server like Apache HTTP Server.
*   **No Buffering** \- Node.js applications never buffer any data. These applications simply output the data in chunks.

**Source:** _tutorialspoint.com_

#### Q17: Is Node a single threaded application? ⭐⭐
**Answer:**
Yes! Node uses a single threaded model with event looping.

**Source:** _tutorialspoint.com_

#### Q18: What is control flow function?   ⭐⭐
**Answer:**
It is a generic piece of code which runs in between several asynchronous function calls is known as control flow function.

**Source:** _lazyquestion.com_

#### Q19: What are the key features of Node.js? ⭐⭐
**Answer:**
Let’s look at some of the key features of Node.js.

*   **Asynchronous event driven IO helps concurrent request handling –** All APIs of Node.js are asynchronous. This feature means that if a Node receives a request for some Input/Output operation, it will execute that operation in the background and continue with the processing of other requests. Thus it will not wait for the response from the previous requests.
*   **Fast in Code execution –** Node.js uses the V8 JavaScript Runtime engine, the one which is used by Google Chrome. Node has a wrapper over the JavaScript engine which makes the runtime engine much faster and hence processing of requests within Node.js also become faster.
*   **Single Threaded but Highly Scalable –** Node.js uses a single thread model for event looping. The response from these events may or may not reach the server immediately. However, this does not block other operations. Thus making Node.js highly scalable. Traditional servers create limited threads to handle requests while Node.js creates a single thread that provides service to much larger numbers of such requests.
*   **Node.js library uses JavaScript –** This is another important aspect of Node.js from the developer’s point of view. The majority of developers are already well-versed in JavaScript. Hence, development in Node.js becomes easier for a developer who knows JavaScript.
*   **There is an Active and vibrant community for the Node.js framework –** The active community always keeps the framework updated with the latest trends in the web development.
*   **No Buffering –** Node.js applications never buffer any data. They simply output the data in chunks.

**Source:** _techbeamers.com_

#### Q20: What is an error-first callback? ⭐⭐
**Answer:**
*Error-first callbacks* are used to pass errors and data. The first argument is always an error object that the programmer has to check if something went wrong. Additional arguments are used to pass data.

```js
fs.readFile(filePath, function(err, data) {
  if (err) {
    //handle the error
  }
  // use the data object
});
```

**Source:** _tutorialspoint.com_

#### Q21: How to make Post request in Node.js? ⭐⭐
**Answer:**
Following code snippet can be used to make a Post Request in Node.js.

```js
var request = require('request');
request.post('http://www.example.com/action', {
  form: {
    key: 'value'
  }
}, function(error, response, body) {
  if (!error && response.statusCode == 200) {
    console.log(body)
  }
});
```

**Source:** _techbeamers.com_

#### Q22: What is the difference between Nodejs, AJAX, and jQuery? ⭐⭐
**Answer:**
The one common trait between Node.js, AJAX, and jQuery is that all of them are the advanced implementation of JavaScript. However, they serve completely different purposes.

* Node.js –It is a server-side platform for developing client-server applications. For example, if we’ve to build an online employee management system, then we won’t do it using client-side JS. But the Node.js can certainly do it as it runs on a server similar to Apache, Django not in a browser.

* AJAX (aka Asynchronous Javascript and XML) –It is a client-side scripting technique, primarily designed for rendering the contents of a page without refreshing it. There are a no. of large companies utilizing AJAX such as Facebook and Stack Overflow to display dynamic content.

* jQuery –It is a famous JavaScript module which complements AJAX, DOM traversal, looping and so on. This library provides many useful functions to help in JavaScript development. However, it’s not mandatory to use it but as it also manages cross-browser compatibility, so can help you produce highly maintainable web applications.

**Source:** _techbeamers.com_

#### Q23: What's the difference between operational and programmer errors? ⭐⭐
**Answer:**
Operation errors are not bugs, but problems with the system, like _request timeout_ or _hardware failure_. On the other hand programmer errors are actual bugs.

**Source:** _blog.risingstack.com_

#### Q24: What is Event Loop? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q25: What are the use cases for the Node.js "vm" core module? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q26: What is REPL in context of Node? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q27: Are you familiar with differences between Node.js nodules and ES6 nodules? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q28: Explain the concept of Domain in Node.js ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q29: How to avoid callback hell in Node.js? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q30: How can you avoid callback hells? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q31: What is N-API in Node.js? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q32: What is Callback? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q33: Explain how does Node.js work? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q34: What is a blocking code? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q35: When should we use Node.js? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q36: What is the purpose of setTimeout function? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q37: What is the relationship between Node.js and V8? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q38: What is Chaining in Node? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q39: Rewrite promise-based Node.js applications to Async/Await ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q40: How does Node.js handle child threads? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q41: What is the preferred method of resolving unhandled exceptions in Node.js? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q42: What are streams? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q43: What is difference between synchronous and asynchronous method of fs module? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q44: What is stream and what are types of streams available in Node.js? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q45: How do you debug Node.js applications? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q46: When should I use EventEmitter? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q47: What is purpose of Buffer class in Node? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q48: What is Event Emmitter? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q49: How to use Buffer in Node.js? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q50: What's the event loop? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q51: How Node prevents blocking code? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q52: What are the global objects of Node.js? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q53: What is the purpose of __filename variable? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q54: What are the timing features of Node.js? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q55: Why to use Buffers instead of binary strings to handle binary data ? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q56: Explain usage of NODE_ENV ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q57: What is LTS releases of Node.js why should you care? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q58: Provide some example of config file separation for dev and prod environments ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q59: How would you handle errors for async code in Node.js? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q60: What's the difference between dependencies, devDependencies and peerDependencies in npm package.json file? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q61: What is Piping in Node? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q62: How do you convert an existing callback API to promises? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q63: Name some of the events fired by streams. ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q64: What are async functions in Node? Provide some examples. ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q65: How to gracefully Shutdown Node.js Server? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q66: Can Node.js work without V8? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q67: When to not use Node.js? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q68: How the V8 engine works? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q69: Is Node.js entirely based on a single-thread? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q70: How does the cluster module work? What’s the difference between it and a load balancer? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q71: Is Node.js entirely based on a single-thread? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q72: How can you listen on port 80 with Node? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q73: Is it possible to use "Class" in Node.js? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q74: Does Node.js support multi-core platforms? And is it capable of utilizing all the cores? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q75: What's a stub? Name a use case. ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q76: What tools can be used to assure consistent code style? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q77: Explain what is Reactor Pattern in Node.js? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q78: Rewrite the code sample without try/catch block ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q79: What is the purpose of using hidden classes in V8? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q80: How V8 compiles JavaScript code? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q81: Can Node.js use other engines than V8? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q82: How does libuv work under the hood? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q83: How to solve "Process out of Memory Exception" in Node.js ? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q84: What is V8 Templates? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q85: Why do we need C++ Addons in Node.js? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q86: Explain some Error Handling approaches in Node.js you know about. Which one will you use? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q87: What will happen when that code will be executed? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q88: Consider following code snippet ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q89: How many threads does Node actually create? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q90: Why should you separate Express 'app' and 'server'? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q91: Why Node.js devs tend to lean towards the Module Requiring vs Dependency Injection? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q92: What is the difference between process.nextTick() and setImmediate() ? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q93: Explain the result of this code execution ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q94: Explain the result of this code execution ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q95: How would you scale Node application? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

## [[⬆]](#toc) <a name=OOP>OOP</a> Interview Questions
#### Q1: What is object-oriented programming (OOP)? ⭐
**Answer:**
OOP is a technique to develop logical modules, such as classes that contain properties, methods, fields, and events. An object is created in the program to represent a class. Therefore, an object encapsulates all the features, such as data and behavior that are associated to a class. OOP allows developers to develop modular programs and assemble them as software. Objects are used to access data and behaviors of different software modules, such as classes, namespaces, and sharable assemblies. .NET Framework supports only OOP languages, such as Visual Basic .NET, Visual C#, and Visual C++.

**Source:** _indiabix.com_

#### Q2: What is inheritance? ⭐
**Answer:**
**Inheritance** allows us to define a class in terms of another class, which makes it easier to create and maintain an application. This also provides an opportunity to reuse the code functionality and speeds up implementation time.

When creating a class, instead of writing completely new data members and member functions, the programmer can designate that the new class should inherit the members of an existing class. This existing class is called the base class, and the new class is referred to as the derived class.

The idea of inheritance implements the IS-A relationship. For example, mammal IS A animal, dog IS-A mammal hence dog IS-A animal as well, and so on.

**Source:** _tutorialspoint.com_

#### Q3: What is the difference between procedural and object-oriented programming? ⭐⭐
**Answer:**
Procedural programming is based upon the modular approach in which the larger programs are broken into procedures. Each procedure is a set of instructions that are executed one after another. On the other hand, OOP is based upon objects. An object consists of various elements, such as methods and variables.  
  
Access modifiers are not used in procedural programming, which implies that the entire data can be accessed freely anywhere in the program. In OOP, you can specify the scope of a particular data by using access modifiers - _public_, _private_, _internal_, _protected_, and _protected_ internal.

**Source:** _indiabix.com_

#### Q4: What is encapsulation? ⭐⭐
**Answer:**
**Encapsulation** is defined _as the process of enclosing one or more items within a physical or logical package_. Encapsulation, in object oriented programming methodology, prevents access to implementation details.

**Source:** _tutorialspoint.com_

#### Q5: What is a class? ⭐⭐
**Answer:**
A class describes all the attributes of objects, as well as the methods that implement the behavior of member objects. It is a comprehensive data type, which represents a blue print of objects. It is a template of object. 

A class can be defined as the primary building block of OOP. It also serves as a template that describes the properties, state, and behaviors common to a particular group of objects.

A class contains data and behavior of an entity. For example, the aircraft class can contain data, such as model number, category, and color and behavior, such as duration of flight, speed, and number of passengers. A class inherits the data members and behaviors of other classes by extending from them.

**Source:** _indiabix.com_

#### Q6: What is the relationship between a class and an object? ⭐⭐
**Answer:**
A class acts as a blue-print that defines the properties, states, and behaviors that are common to a number of objects. An object is an instance of the class. For example, you have a class called _Vehicle_ and _Car_ is the object of that class. You can create any number of objects for the class named _Vehicle_, such as _Van_, _Truck_, and _Auto_.  
      
The _new_ operator is used to create an object of a class. When an object of a class is instantiated, the system allocates memory for every data member that is present in the class.

**Source:** _indiabix.com_

#### Q7: What is an object? ⭐⭐
**Answer:**
Objeects are instance of classes. It is a basic unit of a system. An object is an entity that has attributes, behavior, and identity. Attributes and behavior of an object are defined by the class definition.

**Source:** _indiabix.com_

#### Q8: Explain the basic features of OOPs ⭐⭐
**Answer:**
The following are the four basic features of OOP:  
    
*   **Abstraction** - Refers to the process of exposing only the relevant and essential data to the users without showing unnecessary information.
*   **Polymorphism** - Allows you to use an entity in multiple forms.
*   **Encapsulation** - Prevents the data from unwanted access by binding of code and data in a single unit called object.
*   **Inheritance** - Promotes the reusability of code and eliminates the use of redundant code. It is the property through which a child class obtains all the features defined in its parent class. When a class inherits the common properties of another class, the class inheriting the properties is called a derived class and the class that allows inheritance of its common properties is called a base class.

**Source:** _indiabix.com_

#### Q9: What is the difference between a class and a structure? ⭐⭐
**Answer:**
**Class**:
* A class is a reference type.
* While instantiating a class, CLR allocates memory for its instance in heap.
* Classes support inheritance.
* Variables of a class can be assigned as null.
* Class can contain constructor/destructor.

**Structure**:
* A structure is a value type.
* In structure, memory is allocated on stack.
* Structures do not support inheritance.
* Structure members cannot have null values.
* Structure does not require constructor/destructor and members can be initialiazed automatically.

**Source:** _indiabix.com_

#### Q10: Why is the virtual keyword used in code? ⭐⭐
**Answer:**
The `virtual` keyword is used while defining a class to specify that the methods and the properties of that class can be overridden in derived classes.

**Source:** _indiabix.com_

#### Q11: Explain the concept of constructor? ⭐⭐
**Answer:**
**Constructor** is a special method of a class, which is called automatically when the instance of a class is created. It is created with the same name as the class and initializes all class members, whenever you access the class. The main features of a constructor are as follows:
* Constructors do not have any return type.
* Constructors can be overloaded.
* It is not mandatory to declare a constructor; it is invoked automatically by .NET Framework.

**Source:** _indiabix.com_

#### Q12: Can you inherit private members of a class? ⭐⭐
**Answer:**
No, you cannot inherit `private` members of a class because `private` members are accessible only to that class and not outside that class.

**Source:** _indiabix.com_

#### Q13: What is polymorphism? ⭐⭐
**Answer:**
The word polymorphism means having many forms. In object-oriented programming paradigm, polymorphism is often expressed as _one interface, multiple functions_.


**Source:** _tutorialspoint.com_

#### Q14: Interface or an Abstract Class: which one to use? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q15: Is it possible for a class to inherit the constructor of its base class? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q16: When should I use a struct instead of a class? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q17: What is polymorphism, what is it for, and how is it used? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q18: How could you defineAbstraction in OOP? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q19: Can you specify the accessibility modifier for methods inside the interface? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q20: How is method overriding different from method overloading? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q21: What are the different ways a method can be overloaded? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q22: A structure in C# can implement one or more interfaces. Is it true or false? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q23: How can you prevent your class to be inherited further? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q24: How can you prevent a class from overriding in C#? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q25: What do you mean by data encapsulation? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q26: What are similarities between a class and a structure? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q27: What are abstract classes? What are the distinct characteristics of an abstract class? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q28: Can you allow a class to be inherited, but prevent a method from being overridden in C#? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q29: State the features of an interface. ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q30: Explain the concept of destructor? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q31: What's the advantage of using getters and setters - that only get and set - instead of simply using public fields for those variables? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q32: When should I use an interface and when should I use a base class? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q33: Explain different types of inheritance. ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q34: What is a static constructor? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q35: Differentiate between an abstract class and an interface. ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q36: Can you declare an overridden method to be static if the original method is not static? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q37: What is the difference between an abstract function and a virtual function? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q38: What is Cohesion in OOP? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q39: What is Coupling in OOP? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q40: What is the difference between cohesion and coupling? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q41: What exactly is the difference between an interface and abstract class? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q42: Does .NET support multiple inheritance? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q43: In terms that an OOP programmer would understand (without any functional programming background), what is a monad? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q44: What is LSP (Liskov Substitution Principle) and what are some examples of its use (good and bad)? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q45: Can you provide a simple explanation of methods vs. functions in OOP context? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q46: You have defined a destructor in a class that you have developed by using the C# programming language, but the destructor never executed. Why did the destructor not execute? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q47: What is the difference between a mixin and inheritance? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q48: What does it mean to “program to an interface”? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q49: Why Doesn't C# Allow Static Methods to Implement an Interface? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q50: Can you declare a private class in a namespace? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q51: Why prefer composition over inheritance? What trade-offs are there for each approach? When should you choose inheritance over composition? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q52: What is the difference between association, aggregation and composition? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q53: Could you elaborate Polymorphism vs Overriding vs Overloading? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

## [[⬆]](#toc) <a name=PHP>PHP</a> Interview Questions
#### Q1: What is the return type of a function that doesn't return anything? ⭐
**Answer:**
`void` which mean nothing.

**Source:** _github.com/Bootsity_

#### Q2: What is the purpose of php.ini file? ⭐
**Answer:**
The PHP configuration file, _php.ini_, is the final and most immediate way to affect PHP's functionality. The php.ini file is read each time PHP is initialized.in other words, whenever httpd is restarted for the module version or with each script execution for the CGI version.

**Source:** _github.com/Bootsity_

#### Q3: What does $GLOBALS mean? ⭐
**Answer:**
`$GLOBALS` is associative array including references to all variables which are currently defined in the global scope of the script.

**Source:** _guru99.com_

#### Q4: How can you pass a variable by reference? ⭐
**Answer:**
To be able to pass a variable by **reference**, we use an _ampersand_ in front of it, as follows:
```php
$var1 = &$var2
```

**Source:** _guru99.com_

#### Q5: What is the use of ini_set()? ⭐
**Answer:**
PHP allows the user to modify some of its settings mentioned in php.ini using ini_set(). This function requires two string arguments. First one is the name of the setting to be modified and the second one is the new value to be assigned to it.

Given line of code will enable the display_error setting for the script if it’s disabled.

`ini_set('display_errors', '1');`

We need to put the above statement, at the top of the script so that, the setting remains enabled till the end. Also, the values set via ini_set() are applicable, only to the current script. Thereafter, PHP will start using the original values from php.ini.

**Source:** _github.com/Bootsity_

#### Q6: What are the keys & values in an indexed array? ⭐
**Answer:**

Consider:
```php
Array ( [0] => Hello [1] => world [2] => It's [3] => a [4] => beautiful [5] => day)
```

The keys of an indexed array are 0, 1, 2 etc. (the index values) and values are "Hello", "world", "It's", "beautiful", "day".

**Source:** _github.com/Bootsity_

#### Q7: What is the difference between == and ===? ⭐
**Answer:**
* The operator `==` casts between two different types if they are different
* The `===` operator performs a '_typesafe comparison_'

That means that it will only return true if both operands have the same type and the same value.

```php
1 === 1: true
1 == 1: true
1 === "1": false // 1 is an integer, "1" is a string
1 == "1": true // "1" gets casted to an integer, which is 1
"foo" === "foo": true // both operands are strings and have the same value
```

**Source:** _stackoverflow.com_

#### Q8: How can you enable error reporting in PHP? ⭐⭐
**Answer:**
Check if “`display_errors`” is equal “on” in the php.ini or declare “`ini_set('display_errors', 1)`” in your script.

Then, include “`error_reporting(E_ALL)`” in your code to display all types of error messages during the script execution.

**Source:** _codementor.io_

#### Q9: What are the main differences between const vs define ⭐⭐
**Answer:**
The fundamental difference between `const` vs `define` is that `const` defines constants at compile time, whereas `define` defines them at run time.

```php
const FOO = 'BAR';
define('FOO', 'BAR');

// but
if (...) {
    const FOO = 'BAR';    // Invalid
}
if (...) {
    define('FOO', 'BAR'); // Valid
}
```

Also until PHP 5.3, `const` could not be used in the global scope. You could only use this from within a class. This should be used when you want to set some kind of constant option or setting that pertains to that class. Or maybe you want to create some kind of enum. An example of good `const` usage is to get rid of magic numbers. 

`Define` can be used for the same purpose, but it can only be used in the global scope. It should only be used for global settings that affect the entire application.

Unless you need any type of conditional or expressional definition, use `consts` instead of `define() `- simply for the sake of readability!

**Source:** _stackoverflow.com_

#### Q10: What are the differences between die() and exit() functions in PHP? ⭐⭐
**Answer:**
There's no difference - they are the same. The only advantage of choosing `die()` over `exit()`, might be the time you spare on typing an extra letter.

**Source:** _stackoverflow.com_

#### Q11: What does the 'var' keyword mean in PHP? ⭐⭐
**Answer:**
It's for declaring class member variables in PHP4, and is no longer needed. It will work in PHP5, but will raise an **E_STRICT** warning in PHP from version 5.0.0 up to version 5.1.2, as of when it was deprecated. Since PHP 5.3, var has been un-deprecated and is a synonym for 'public'.

Consider:
```php
class foo {
    var $x = 'y'; // or you can use public like...
    public $x = 'y'; //this is also a class member variables.
    function bar() {
    }
}
```

**Source:** _stackoverflow.com_

#### Q12: What's the difference between isset() and array_key_exists()?  ⭐⭐
**Answer:**
* `array_key_exists` will tell you if a key exists in an array and complains when `$a` does not exist.
* `isset` will only return `true` if the key/variable exists **and is not `null`**. `isset` doesn't complain when `$a` does not exist.

Consider:
```js
$a = array('key1' => 'Foo Bar', 'key2' => null);

isset($a['key1']);             // true
array_key_exists('key1', $a);  // true

isset($a['key2']);             // false
array_key_exists('key2', $a);  // true
```

**Source:** _stackoverflow.com_

#### Q13: What are the different scopes of variables? ⭐⭐
**Answer:**
Variable scope is known as its boundary within which it can be visible or accessed from code. In other words, it is the context within which a variable is defined. There are only two scopes available in PHP namely local and global scopes.

- Local variables (local scope)
- Global variables (special global scope)
- Static variables (local scope)
- Function parameters (local scope)
When a variable is accessed outside its scope it will cause PHP error undefined variable.


**Source:** _github.com/Bootsity_

#### Q14: What is the difference between single-quoted and double-quoted strings in PHP? ⭐⭐
**Answer:**
* Single quoted strings will display things almost completely "as is." 
* Double quote strings will display a host of escaped characters (including some regexes), and variables in the strings will be evaluated.

Things get evaluated in **double quotes** but not in single:

```php
$s = "dollars";
echo 'This costs a lot of $s.'; // This costs a lot of $s.
echo "This costs a lot of $s."; // This costs a lot of dollars.
```

**Source:** _stackoverflow.com_

#### Q15: What do we mean by keys and values? ⭐⭐
**Answer:**
In associative arrays, we can use named keys that you assign to them.
There are two ways to create an associative array: 

```php
// first way -

$age = array("Peter"=>"35", "Ben"=>"37", "Joe"=>"43");`

// another method - 
$age['Peter'] = "35"; //Peter, Ben & Joe are keys
$age['Ben'] = "37"; //35, 37 & 43 are values
$age['Joe'] = "43";
```

**Source:** _github.com/Bootsity_

#### Q16: PHP array delete by value (not key) ⭐⭐
**Details:**
I have a PHP array as follows:

```php
$messages = [312, 401, 1599, 3, ...];
```

I want to delete the element containing the value `$del_val` (for example, `$del_val=401`), but I don't know its key. This might help: **each value can only be there once**.

I'm looking for the simplest function to perform this task please.


**Answer:**
Using `array_search()` and `unset`, try the following:

```js
if (($key = array_search($del_val, $messages)) !== false) {
   unset($messages[$key]);
}
```

`array_search()` returns the key of the element it finds, which can be used to remove that element from the original array using `unset()`. It will return `FALSE` on failure, however it can return a false-y value on success (your key may be `0` for example), which is why the strict comparison `!==` operator is used.

The `if()` statement will check whether `array_search()` returned a value, and will only perform an action if it did.

**Source:** _stackoverflow.com_

#### Q17: When should I use require vs. include? ⭐⭐
**Answer:**
The `require()` function is identical to `include()`, except that it handles errors differently. If an error occurs, the `include()` function generates a warning, but the script will continue execution. The `require()` generates a fatal error, and the script will stop.

My suggestion is to just use `require_once` 99.9% of the time.

Using `require` or `include` instead implies that your code is not **reusable** elsewhere, i.e. that the scripts you're pulling in actually execute code instead of making available a class or some function libraries.

**Source:** _stackoverflow.com_

#### Q18: What is the difference between var_dump() and print_r()? ⭐⭐
**Answer:**
* The `var_dump` function displays structured information about variables/expressions including its **type** and **value**. Arrays are explored recursively with values indented to show structure. It also shows which array values and object properties are references.

* The `print_r()` displays information about a variable in a way that's readable by humans. array values will be presented in a format that shows keys and elements. Similar notation is used for objects.

Consider:
```php
$obj = (object) array('qualitypoint', 'technologies', 'India');
```
`var_dump($obj) `will display below output in the screen:
```
object(stdClass)#1 (3) {
 [0]=> string(12) "qualitypoint"
 [1]=> string(12) "technologies"
 [2]=> string(5) "India"
}
```
And, `print_r($obj)` will display below output in the screen.
```
stdClass Object ( 
 [0] => qualitypoint
 [1] => technologies
 [2] => India
)
```

**Source:** _stackoverflow.com_

#### Q19: Is there a difference between isset and !empty? ⭐⭐
**Answer:**
`empty` is more or less shorthand for` !isset($foo) || !$foo`, and `!empty` is analogous to ` isset($foo) && $foo`.  `empty` is the same as `!$foo`, but doesn't throw warnings if the variable doesn't exist. That's the main point of this function: do a boolean comparison without worrying about the variable being set.

**Source:** _stackoverflow.com_

#### Q20: Explain what the different PHP errors are ⭐⭐
**Answer:**
* A `notice` is a non-critical error saying something went wrong in execution, something minor like an undefined variable.
* A `warning` is given when a more critical error like if an include() command went to retrieve a non-existent file. In both this and the error above, the script would continue.
* A `fatal error` would terminate the code. Failure to satisfy a require() would generate this type of error, for example.

**Source:** _pangara.com_

#### Q21: Differentiate between echo and print() ⭐⭐
**Answer:**
`echo` and `print` are more or less the same. They are both used to output data to the screen.

The differences are: 
- echo has no return value while print has a return value of 1 so it can be used in expressions. 
- echo can take multiple parameters (although such usage is rare) while print can take one argument. 
- echo is faster than print.

**Source:** _github.com/Bootsity_

#### Q22: Give me some real life examples when you had to use __destruct in your classes ⭐⭐
**Answer:**
We know that `__destruct` is called when the object is destroyed. Logically, what happens if the object is destroyed? Well, it means it's no longer available. So if it has resources open, it makes sense to close those resources as it's being destroyed or cleaning up after itself. Also because PHP will close resources on termination for you doesn't mean that it's bad to explicitly close them when you no longer need them (or good to not close them).

Some real examples are:
* Closing custom database connector/wrapper connection
* Deletion of temporary folders
* Cleaning up caching
* Spooling the queue of logging messages to db/file


**Source:** _stackoverflow.com_

#### Q23: Declare some function with default parameter ⭐⭐
**Answer:**
Consider:
```php
function showMessage($hello = false){
  echo ($hello) ? 'hello' : 'bye';
}
```

**Source:** _codementor.io_

#### Q24: What are PSRs? Choose 1 and briefly describe it. ⭐⭐
**Answer:**
**PSRs** are PHP Standards Recommendations that aim at standardising common aspects of PHP Development. An example of a PSR is PSR-2, which is a coding style guide.

**Source:** _codementor.io_

#### Q25: Explain how we handle exceptions in PHP? ⭐⭐
**Answer:**
When an exception is thrown, code following the statement will not be executed, and PHP will attempt to find the first matching catch block. If an exception is not caught, a PHP Fatal Error will be issued with an "Uncaught Exception".
An exception can be thrown, and caught within PHP. 

To handle exceptions, code may be surrounded in a `try` block.
Each try must have at least one corresponding `catch` block. Multiple catch blocks can be used to catch different classes of exceptions.
Exceptions can be thrown (or re-thrown) within a catch block.

Consider:

```php
try {
    print "this is our try block n";
    throw new Exception();
} catch (Exception $e) {
    print "something went wrong, caught yah! n";
} finally {
    print "this part is always executed n";
}
```

**Source:** _github.com/Bootsity_

#### Q26:  Is multiple inheritance supported in PHP? ⭐⭐
**Answer:**
PHP supports only single inheritance; it means that a class can be extended from only one single class using the keyword 'extended'.

**Source:** _guru99.com_

#### Q27: How is it possible to set an infinite execution time for PHP script? ⭐⭐
**Answer:**
The `set_time_limit(0) `added at the beginning of a script sets to infinite the time of execution to not have the PHP error 'maximum execution time exceeded.' It is also possible to specify this in the _php.ini_ file.

**Source:** _guru99.com_

#### Q28: What is stdClass in PHP? ⭐⭐
**Answer:**
`stdClass` is just a generic 'empty' class that's used when casting other types to objects. `stdClass` is **not** the base class for objects in PHP.  This can be demonstrated fairly easily:

```js
class Foo{}
$foo = new Foo();
echo ($foo instanceof stdClass)?'Y':'N'; // outputs 'N'
```

It is useful for anonymous objects, dynamic properties, etc. 

An easy way to consider the `StdClass` is as an alternative to associative array. See this example below that shows how `json_decode()` allows to get an StdClass instance or an associative array.
Also but not shown in this example, `SoapClient::__soapCall` returns an `StdClass` instance.

```js
//Example with StdClass
$json = '{ "foo": "bar", "number": 42 }';
$stdInstance = json_decode($json);

echo $stdInstance - > foo.PHP_EOL; //"bar"
echo $stdInstance - > number.PHP_EOL; //42

//Example with associative array
$array = json_decode($json, true);

echo $array['foo'].PHP_EOL; //"bar"
echo $array['number'].PHP_EOL; //42
```



**Source:** _stackoverflow.com_

#### Q29: In PHP, objects are they passed by value or by reference? ⭐⭐
**Answer:**
In PHP, objects passed by **value**.

**Source:** _guru99.com_

#### Q30: Explain usage of enumerations in PHP ⭐⭐
**Answer:**
PHP doesn't have native Enumerations. Depending upon use case, I would normally use something simple like the following:

```php
abstract class DaysOfWeek
{
    const Sunday = 0;
    const Monday = 1;
    // etc.
}

$today = DaysOfWeek::Sunday;
```

There is a native extension, too. **SplEnum** gives the ability to emulate and create enumeration objects natively in PHP.

**Source:** _stackoverflow.com_

#### Q31: What is the differences between $a != $b and $a !== $b? ⭐⭐
**Answer:**
`!=` means _inequality_ (TRUE if $a is not equal to $b) and `!==` means _non-identity_ (TRUE if $a is not identical to $b).

**Source:** _guru99.com_

#### Q32: What is PDO in PHP? ⭐⭐
**Answer:**
**PDO** stands for PHP Data Object.

It is a set of PHP extensions that provide a core PDO class and database, specific drivers. It provides a vendor-neutral, lightweight, data-access abstraction layer. Thus, no matter what database we use, the function to issue queries and fetch data will be same. It focuses on data access abstraction rather than database abstraction.

**Source:** _github.com/Bootsity_

#### Q33: Can you extend a Final defined class? ⭐⭐
**Answer:**
No, you cannot extend a `Final` defined class. A `Final` class or method declaration prevents child class or method overriding.

**Source:** _codementor.io_

#### Q34: Explain function call by reference ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q35: Differentiate between parameterised and non parameterised functions ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q36: Does PHP support method overloading? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q37: How would you create a Singleton class using PHP? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q38: How do I pass variables and data from PHP to JavaScript? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q39: Why do we use extract()? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q40: Is there any reason to use strcmp() for strings comparison? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q41: What will be returned by this code? Explain the result. ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q42: What is the difference between using self and $this? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q43: Let's create Enumerations for PHP. Prove some code examples. ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q44: What is the difference between MySQL, MySQLi and PDO?  ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q45: What are the exception class functions? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q46: Differentiate between exception and error ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q47: Is there a function to make a copy of a PHP array to another? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q48: What is the difference between PDO's query() vs execute()? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q49: Explain the difference between shell_exec() and exec() ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q50: Check if PHP array is associative ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q51: What will be returned by this code? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q52: What exactly is the the difference between array_map, array_walk and array_filter? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q53: Are Parent constructors called implicitly inside a class constructor? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q54: Explain the difference between exec() vs system() vs passthru()? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q55: When should I use require_once vs. require? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q56: What are some of the big changes PHP has gone through in the past few years? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q57: What is autoloading classes in PHP? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q58: What is the difference between a PHP interpreter and a PHP handler? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q59: What is use of Null Coalesce Operator? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q60: Maximum how many arguments are allowed in a function in PHP? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q61: What does the following code output? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q62: What is use of Spaceship Operator? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q63: Is PHP single or multi threaded? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q64: What does $$ mean? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q65: What are the disadvantages of using persistent connection in PDO? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q66: Compare mysqli or PDO - what are the pros and cons? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q67: Does PHP have threading? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q68: What does yield mean in PHP? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q69: Store an array as JSON or as a PHP serialized array? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q70: What is the best method to merge two PHP objects? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q71: What's better at freeing memory with PHP: unset() or $var = null? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q72: Explain the Exception Hierarchy introduced in PHP7 ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q73: How to turn errors into exceptions in PHP? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q74: explain what is a closure in PHP and why does it use the “use” identifier? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q75: What exactly are late static bindings in PHP? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q76: What is the crucial difference between using traits versus interfaces? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q77: How to measure execution times of PHP scripts? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q78: Explain the Order of Precedence for Traits in PHP ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q79: Provide some ways to mimic multiple constructors in PHP ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q80: How could we implement method overloading in PHP? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q81: Are PDO prepared statements sufficient to prevent SQL injection? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q82: What does a $$$ mean in PHP?  ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

## [[⬆]](#toc) <a name=PWA>PWA</a> Interview Questions
#### Q1: What is a progressive web app? ⭐
**Answer:**
The concept of the **progressive web app (PWA)** was approached by Google in late 2015. They are basically web applications (Website) but have look and feel like other native mobile apps. The progressive web app enabled websites can offer functionalities such as working offline, push notifications, and device hardware access.

**Source:** _stackoverflow.com_

#### Q2: Why do we need a web manifest for PWA? ⭐⭐
**Answer:**
A **web manifest **file lists all the information about the website in a JSON format. Having this file is one of the requirements **to make the website installable**.

It usually resides in the root folder of a web app. It contains useful information, such as the app’s title, paths to different-sized icons that can be used to represent the app on a mobile OS (for example, as the home screen icon), and a background color to use in loading or splash screens. This information is needed for the browser to present the web app properly when installing, and on the home screen.

**Source:** _developer.mozilla.org_

#### Q3: What makes an app a PWA? ⭐⭐
**Answer:**
There are some key principles a web app should try to observe to be identified as a PWA. It should be:

* **Discoverable**, so the contents can be found through search engines.
* **Installable**, so it's available on the device's home screen.
* **Linkable**, so you can share it by simply sending a URL. 
*** Network independent**, so it works offline or with a poor network connection.
* **Progressive**, so it's still usable on a basic level on older browsers, but fully-functional on the latest ones.
* **Re-engageable**, so it's able to send notifications whenever there's new content available.
* **Responsive**, so it's usable on any device with a screen and a browser — mobile phones, tablets, laptops, TVs, fridges, etc.
* **Safe**, so the connection between you and the app is secured against any third parties trying to get access to your sensitive data.

**Source:** _developer.mozilla.org_

#### Q4: What are some benefits of PWA? ⭐⭐
**Answer:**
Benefits of the progressive web app:

1. **Smaller and Faster:**
The progressive web apps are much smaller in size than native apps. They don’t even need to install. That’s they are not wasting disc space and load very fast.
2. **Responsive Interface:**
Progressive web app (PWA) supported web pages are capable to fit in every screen sizes automatically. It could be a smartphone, tablet, desktop or laptop.
3. **No Updates Required:**
Most of the mobile apps need regular weekly updates. Like the normal website, progressive web apps (PWA) are always loaded latest updated version whenever the user interaction happens and no App or Play Store approval required.
4. **Cost Effective:**
Native mobile apps need to be developed for both Android and iOS devices separately and their development cost is very high. On the other hand, progressive web apps are had the same features but the fraction of the prior price.
5. **SEO Advantage:**
Progressive web apps are discoverable by search engines and load super-fast. Just like other websites, their links are sharable too. This, in other words, gives good user experience and result in SEO rank boost.
5. **Offline capabilities:**
Due to the support of service worker API, PWAs are accessible in offline or low internet connections.
6. **Security:**
PWAs are delivered over HTTPS connection and secure user-data over each interaction.
8. **Push Notifications:**
By the support of push notifications, PWAs can interact easily with the users and provide a really amazing user experience.
9. **Bypass the  app stores:**
PWAs don’t need the App store or Google play store support. Their updated version can be directly loaded from the web server without the requirement of app store approval. On the other hand, native apps need days of approval if any new update required. There are possibilities of getting rejected or banned.
10. **Zero installation:**
During browsing, progressive web app gets its own icon on phones and tablets, just like a mobile application, but without the need to go through the tedious and slow App Store installation process.

**Source:** _stackoverflow.com_

#### Q5: What is a service worker? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q6: What is IndexedDB and how is it used by PWA? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q7: What are some requirements to make the website installable as PWA? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q8: What is CacheStorage? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q9: What are some disadvantages of PWA? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q10: What is the differences between a Hybrid Mobile App and a Progressive Web App? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q11: What features do Progressive Web Apps have that native apps lacks? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q12: What is a fetch event? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q13: What are some requirements to app shell? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q14: Explain the service worker lifecycle ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q15: What is App Shell? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q16: How to update a service worker? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q17: What are some service worker's caching strategies do you know? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q18: What can service workers do that web workers cannot? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q19: What are some benefits of an app shell architecture with a service worker? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q20: What about PWA for iOS? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q21: Is it possible to have truly persistent storage in a PWA and why may you want one? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q22: Is it possible to have multiple service workers? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

## [[⬆]](#toc) <a name=PowerShell>PowerShell</a> Interview Questions
#### Q1: What is PowerShell? ⭐
**Answer:**
**PowerShell** is a task-based command-line shell and scripting language built on .NET. PowerShell helps system administrators and power-users rapidly automate tasks that manage operating systems (Linux, macOS, and Windows) and processes.

The consistency of PowerShell is one of its primary assets. For example, if you learn how to use the `Sort-Object` cmdlet, you can use that knowledge to sort the output of any cmdlet. You don't have to learn the different sorting routines of each cmdlet. PowerShell combines an interactive shell and a scripting environment. PowerShell can access command-line tools, COM objects, and .NET class libraries. PowerShell is based on object not text. The output of a command is an object. You can send the output object, through the pipeline, to another command as its input.

**Source:** _docs.microsoft.com_

#### Q2: What would be the PowerShell equivalent of echo? ⭐⭐
**Answer:**
There are several ways:

* `Write-Host`: Write directly to the console, not included in function/cmdlet output. Allows foreground and background colour to be set.
* `Write-Debug`: Write directly to the console, if `$DebugPreference` set to Continue or Stop.
* `Write-Verbose`: Write directly to the console, if `$VerbosePreference` set to Continue or Stop.
* `echo` as an alias mapping to `Write-Output`

**Source:** _stackoverflow.com_

#### Q3: What is a PowerShell session? ⭐⭐
**Answer:**
A **session** is an environment in which PowerShell runs.

Each time you start PowerShell, a session is created for you, and you can run commands in the session. You can also add items to your session, such as modules and snap-ins, and you can create items, such as variables, functions, and aliases. These items exist only in the session and are deleted when the session ends.

**Source:** _docs.microsoft.com_

#### Q4: What is PowerShell execution policies? ⭐⭐
**Answer:**
The **PowerShell execution policy** is the setting that determines which type of PowerShell scripts (if any) can be run on the system. PowerShell's execution policy is a safety feature that controls the conditions under which PowerShell loads configuration files and runs scripts.





**Source:** _docs.microsoft.com_

#### Q5: What does $_ mean in PowerShell? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q6: Mention some types of Execution Policy? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q7: What's the difference between “Write-Host”, “Write-Output”, or “[console]::WriteLine”? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q8: How PowerShell is Object Oriented? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q9: What is the difference between `Start-Job` vs `Start-Process`? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q10: What is PowerShell Cmdlets? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q11: Whats is the difference between Session and PSSession? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q12: How Cmdlets Differ from Commands? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q13: When should I use Write-Error vs. Throw in PowerShell?  ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q14: Does PowerShell support OOP? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q15:  Is there an equivalent of bash ampersand (&) for forking/running background processes? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

## [[⬆]](#toc) <a name=Python>Python</a> Interview Questions
#### Q1: Name some characteristics of Python?  ⭐
**Answer:**
Here are a few key points:

*   Python is an **interpreted language**. That means that, unlike languages like C and its variants, Python does not need to be compiled before it is run. Other interpreted languages include _PHP_ and _Ruby_.
*   Python is **dynamically typed**, this means that you don't need to state the types of variables when you declare them or anything like that. You can do things like `x=111` and then `x="I'm a string"` without error
*   Python is well suited to **object orientated programming** in that it allows the definition of classes along with composition and inheritance. Python does not have access specifiers (like C++'s `public`, `private`), the justification for this point is given as "we are all adults here"
*   In Python, **functions are first-class objects**. This means that they can be assigned to variables, returned from other functions and passed into functions. Classes are also first class objects
*   Writing Python code is quick but running it is **often slower than compiled languages**. Fortunately, Python allows the inclusion of C based extensions so bottlenecks can be optimised away and often are. The `numpy` package is a good example of this, it's really quite quick because a lot of the number crunching it does isn't actually done by Python

**Source:** _codementor.io_

#### Q2: What are the built-in types available In Python? ⭐
**Answer:**
**Immutable** built-in datatypes of Python
* Numbers
* Strings
* Tuples

**Mutable** built-in datatypes of Python
* List
* Dictionaries
* Sets

**Source:** _techbeamers.com_

#### Q3: How do I modify a string? ⭐
**Answer:**
You can’t, because strings are immutable. In most situations, you should simply construct a new string from the various parts you want to assemble it from.

**Source:** _docs.python.org_

#### Q4: Why would you use the "pass" statement? ⭐⭐
**Answer:**
Python has the syntactical requirement that code blocks cannot be empty. Empty code blocks are however useful in a variety of different contexts, for example if you are designing a new class with some methods that you don't want to implement:

```python
class MyClass(object):
    def meth_a(self):
        pass

    def meth_b(self):
        print "I'm meth_b"
```
If you were to leave out the pass, the code wouldn't run and you'll get an error:
```python
IndentationError: expected an indented block
```

Other examples when we could use `pass`:
* Ignoring (all or) a certain type of `Exception`
* Deriving an exception class that does not add new behaviour
* Testing that code runs properly for a few test values, without caring about the results

**Source:** _stackoverflow.com_

#### Q5: What is pickling and unpickling? ⭐⭐
**Answer:**
The pickle module implements a fundamental, but powerful algorithm for serializing and de-serializing a Python object structure.

* **Pickling** - is the process whereby a Python object hierarchy is converted into a byte stream,
* **Unpickling** - is the inverse operation, whereby a byte stream is converted back into an object hierarchy.

**Source:** _stackoverflow.com_

#### Q6: What is negative index in Python? ⭐⭐
**Answer:**
Python sequences can be index in positive and negative numbers. For positive index, 0 is the first index, 1 is the second index and so forth. For negative index, (-1) is the last index and (-2) is the second last index and so forth.

**Source:** _guru99.com_

#### Q7: Name some benefits of Python ⭐⭐
**Answer:**
*   Python is a dynamic-typed language. It means that you don’t need to mention the data type of variables during their declaration.
*   Python supports object orientated programming as you can define classes along with the composition and inheritance.
*   Functions in Python are like first-class objects. It suggests you can assign them to variables, return from other methods and pass as arguments.
*   Developing using Python is quick but running it is often slower than compiled languages.
*   Python has several usages like web-based applications, test automation, data modeling, big data analytics and much more.

**Source:** _techbeamers.com_

#### Q8: What are local variables and global variables in Python? ⭐⭐
**Answer:**
* **Global Variables**: Variables declared outside a function or in global space are called global variables. These variables can be accessed by any function in the program.

* **Local Variables**: Any variable declared inside a function is known as a local variable. This variable is present in the local space and not in the global space.

**Source:** _edureka.co_

#### Q9: What are the rules for local and global variables in Python? ⭐⭐
**Answer:**
In Python, variables that are only referenced inside a function are implicitly global. If a variable is assigned a value anywhere within the function’s body, it’s assumed to be a local unless explicitly declared as global.

Requiring global for assigned variables provides a bar against unintended side-effects.

**Source:** _docs.python.org_

#### Q10: What is lambda functions in Python? ⭐⭐
**Answer:**
A **lambda function** is a small anonymous function. A lambda function can take any number of arguments, but can only have one expression.

Consider:
```python
x = lambda a : a + 10
print(x(5)) # Output: 15
```


**Source:** _stackoverflow.com_

#### Q11: When to use a tuple vs list vs dictionary in Python? ⭐⭐
**Answer:**
* Use a `tuple` to store a sequence of items that will not change.
* Use a `list` to store a sequence of items that may change.
* Use a `dictionary` when you want to associate pairs of two items.

**Source:** _stackoverflow.com_

#### Q12: What are some drawbacks of the Python language? ⭐⭐
**Answer:**
The two most common valid answers to this question (by no means intended as an exhaustive list) are:
- The Global Interpreter Lock (GIL). CPython (the most common Python implementation) is not fully thread safe. In order to support multi-threaded Python programs, CPython provides a global lock that must be held by the current thread before it can safely access Python objects. As a result, no matter how many threads or processors are present, only one thread is ever being executed at any given time. In comparison, it is worth noting that the PyPy implementation discussed earlier in this article provides a stackless mode that supports micro-threads for massive concurrency.
- Execution speed. Python can be slower than compiled languages since it is interpreted. (Well, sort of. See our earlier discussion on this topic.)

**Source:** _github.com_

#### Q13:  Does Python have a switch-case statement? ⭐⭐
**Answer:**
In Python, we do not have a switch-case statement. Here, you may write a switch function to use. Else, you may use a set of if-elif-else statements. To implement a function for this, we may use a dictionary.

```py
def switch_demo(argument):
    switcher = {
        1: "January",
        2: "February",
        3: "March",
        4: "April",
        5: "May",
        6: "June",
        7: "July",
        8: "August",
        9: "September",
        10: "October",
        11: "November",
        12: "December"
    }
    print switcher.get(argument, "Invalid month")
```

**Source:** _github.com_

#### Q14: What is PEP 8? ⭐⭐
**Answer:**
PEP 8 is the latest Python coding standard, a set of coding recommendations. It guides to deliver more readable Python code.

**Source:** _techbeamers.com_

#### Q15: What Is The Benefit Of Using Flask? ⭐⭐
**Answer:**
**Flask** is part of the micro-framework. Which means it will have little to no dependencies on external libraries. It makes the framework light while there is little dependency to update and less security bugs.

**Source:** _wisdomjobs.com_

#### Q16: Suppose lst is [2, 33, 222, 14, 25], What is lst[-1]? ⭐⭐
**Details:**
Suppose `lst` is `[2, 33, 222, 14, 25]`, What is `lst[-1]`?

**Answer:**
It's `25`. Negative numbers mean that you count from the right instead of the left. So, `lst[-1]` refers to the last element, `lst[-2]` is the second-last, and so on.

**Source:** _adevait.com_

#### Q17: Given variables a and b, switch their values so that b has the value of a, and a has the value of b without using an intermediary variable. ⭐⭐
**Answer:**
```py
a, b = b, a
```

**Source:** _adevait.com_

#### Q18: How do you list the functions in a module? ⭐⭐
**Answer:**
Use the `dir()` method to list the functions in a module:

```py
import some_module
print dir(some_module)
```

**Source:** _toptal.com_

#### Q19: What are descriptors? ⭐⭐
**Answer:**
Descriptors were introduced to Python way back in version 2.2. They provide the developer with the ability to add managed attributes to objects. The methods needed to create a descriptor are `__get__`, `__set__` and `__delete__`. If you define any of these methods, then you have created a descriptor.

Descriptors power a lot of the magic of Python’s internals. They are what make properties, methods and even the super function work. They are also used to implement the new style classes that were also introduced in Python 2.2.

**Source:** _blog.pythonlibrary.org_

#### Q20: Explain how does Python memory management work? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q21: What is monkey patching and is it ever a good idea? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q22: What does this stuff mean: *args, **kwargs? And why would we use it? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q23: What's the difference between lists and tuples? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q24: Explain the UnboundLocalError exception and how to avoid it? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q25: How to make a flat list out of list of lists? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q26: What is a None value? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q27: What's the difference between the list methods append() and extend()? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q28: How do I check if a list is empty? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q29: What is the most efficient way to concatenate many strings together? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q30: After executing the above code, what is the value of y? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q31: What are the key differences between Python 2 and 3? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q32: What is the difference between range and xrange? How has this changed over time? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q33: What are the wheels and eggs? What is the difference? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q34: Is it possible to have static methods in Python? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q35: What is namespace in Python? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q36: What Is Flask-WTF And What Are Their Features? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q37: What is a "callable"? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q38: How can I create a copy of an object in Python? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q39: Is this valid in Python and why? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q40: What are decorators in Python? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q41: What is introspection/reflection and does Python support it? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q42: What are the Dunder/Magic/Special methods in Python? Name a few. ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q43: What are virtualenvs? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q44: What is the python “with” statement designed for? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q45: How the string does get converted to a number? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q46: Write a program to check whether the object is of a class or its subclass. ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q47: What is the function of “self”? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q48: What is the process of compilation and linking in Python? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q49: What does the Python nonlocal statement do (in Python 3.0 and later)? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q50: What is the difference between range and xrange functions in Python 2.X? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q51: How can you share global variables across modules? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q52: What are immutable objects in Python? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q53: Why are default values shared between objects? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q54: How to make a chain of function decorators? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q55: Create function that similar to os.walk ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q56: How do I write a function with output parameters (call by reference) ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q57: Why are Python's 'private' methods not actually private? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q58: What is GIL? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q59: Is it a good idea to use multi-thread to speed your Python code? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q60: What is an alternative to GIL? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q61: Show me three different ways of fetching every third item in the list ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q62: What is the difference between @staticmethod and @classmethod? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q63: What is the difference between deep and shallow copy? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q64: What are the advantages of NumPy over regular Python lists? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q65: How to work with transitive dependencies? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q66: What are metaclasses in Python? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q67: How is memory managed in Python? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q68: Why Python (CPython and others) uses the GIL? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q69: Can you explain closures (as they relate to Python)? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q70: Why aren't python nested functions called closures? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q71: Is there a tool to help find bugs or perform static analysis? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q72: What's the difference between a Python module and a Python package? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q73: What does an 'x = y or z' assignment do in Python? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q74: What is the difference between old style and new style classes in Python? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q75: What will be the output of the code below? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q76: Will the code below work? Why or why not? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q77: What is Cython? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q78: What will be returned by this code? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q79: What is the purpose of the single underscore “_” variable in Python? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q80: Explain how you reverse a generator? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q81: What is monkey patching? How to use it in Python? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q82: What is MRO in Python? How does it work? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q83: How is set() implemented internally? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q84: Whenever you exit Python, is all memory de-allocated?  ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q85: Why use else in try/except construct in Python? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q86: What does Python optimization (-O or PYTHONOPTIMIZE) do? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q87: Why isn't all memory freed when Python exits? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q88: How should one access nonlocal variables in closures in python 2.x? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q89: What is a global interpreter lock (GIL) and why is it an issue? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q90: Is there any downside to the -O flag apart from missing on the built-in debugging information? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q91: How to read a 8GB file in Python? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q92: Describe Python's garbage collection mechanism in brief. ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q93: What will this code return? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q94: Why would you use metaclasses? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q95: How do I access a module written in Python from C? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q96: Is there a simple, elegant way to define singletons? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

## [[⬆]](#toc) <a name=QuestionstoAsk>Questions to Ask</a> Interview Questions
#### Q1: What would you change around here if you could? ⭐
**Answer:**


#### Q2: How do you measure individual performance? ⭐
**Answer:**


#### Q3: How do your clients and customers define success? ⭐
**Answer:**


#### Q4: How do you evaluate new technologies? Who makes the final decisions? ⭐
**Answer:**


#### Q5: How do you know what to work on each day? ⭐
**Answer:**


#### Q6: What is the most important/valuable thing you have learnt from working here? ⭐
**Answer:**


#### Q7: Do you tend to roll your own solutions more often or rely on third party tools? What's the rationale in a specific case? ⭐
**Answer:**


#### Q8: What is the most fulfilling/exciting/technically complex project that you've worked on here so far? ⭐⭐
**Answer:**


#### Q9: How do you train/ramp up engineers who are new to the team? ⭐⭐
**Answer:**


#### Q10: What does a typical day look like for you? ⭐⭐
**Answer:**


#### Q11: What do you think the company can improve at? ⭐⭐
**Answer:**


#### Q12: What is your policy on working from home/remotely? ⭐⭐
**Answer:**


#### Q13: What is your stack? What is the rationale for/story behind this specific stack? ⭐⭐
**Answer:**


#### Q14: What are the engineering challenges that the company/team is facing? ⭐⭐
**Answer:**


#### Q15: What do you measure? What are your most important product metrics? ⭐⭐
**Answer:**


#### Q16: What does the company do to nurture and train its employees? ⭐⭐
**Answer:**


#### Q17: If you hire person, what do you have for him to study product you're working on and processes in general? Do you have specifications, requirements, documentation? ⭐⭐
**Answer:**


#### Q18: Tell me about the main products of your company. ⭐⭐
**Answer:**


#### Q19: What are some weaknesses of the organization? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q20: What is your team's biggest challenge right now? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q21: Why did you choose to come to this company? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q22: How does the engineering team balance resources between feature requests and engineering maintenance? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q23: What makes your product competitive? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q24: What is the most frustrating part about working here? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q25: Is the team growing, and what sort of opportunities will there be in the next year/3 years? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q26: What is the current team composition like? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q27: There's "C++" (or Python, Swift or any other tech) in the job description. How will you estimate my proficiency in this tech in 3 months? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q28: Why have the last few people left? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q29: When was the last time you interacted with a founder? What was it regarding? Generally how involved are the founders in the day-to-day? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q30: How much time do you spend on new project development versus maintenance? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q31: What are your highest priorities right now? For example, new features, new products, solidifying existing code, reducing operations overhead? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q32: What has been the worst technical blunder that has happened in the recent past? How did you guys deal with it? What changes were implemented afterwards to make sure it didn't happen again? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q33: What is unique about working at this company that you have not experienced elsewhere? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q34: What is the most costly technical decision made early on that the company is living with now? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q35: How are you funded? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q36: Does the company culture encourage entrepreneurship? Could you give me any specific examples? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q37: What would I work on if I joined this team and who would I work most closely with? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q38: Are you profitable? If no, what's your plan for becoming profitable? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q39: How long does the average engineer stay at the company? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

## [[⬆]](#toc) <a name=React>React</a> Interview Questions
#### Q1: What is React? ⭐
**Answer:**
React is an open-source JavaScript library created by Facebook for building complex, interactive UIs in web and mobile applications. React’s core purpose is to build UI components; it is often referred to as just the “V” (View) in an “MVC” architecture. 

**Source:** _codementor.io_

#### Q2: How would you write an inline style in React? ⭐
**Answer:**
For example: 

```html
<div style={{ height: 10 }}>
```

**Source:** _github.com/WebPredict_

#### Q3: What is JEST? ⭐
**Answer:**
**Jest** is a JavaScript unit testing framework made by Facebook based on Jasmine and provides automated mock creation and a jsdom environment. It's often used for testing React components.

**Source:** _github.com/sudheerj_

#### Q4: What are the advantages of ReactJS? ⭐
**Answer:**
Below are the advantages of ReactJS:
1. Increases the application’s performance with Virtual DOM
2. JSX makes code is easy to read and write
3. It renders both on client and server side
4. Easy to integrate with other frameworks (Angular, BackboneJS) since it is only a view library
5. Easy to write UI Test cases and integration with tools such as JEST.

**Source:** _github.com/sudheerj_

#### Q5: How to write comments in ReactJS? ⭐
**Answer:**
The comments in ReactJS/JSX is similar to javascript multiline comments which are wrapped with curly braces:

**Single-line comments:**
```js
<div>
  {/* Single-line comments */}
  Welcome {user}, Let's play React
</div>
```

**Multi-line comments:**
```js
<div>
  {/* Multi-line comments for more than
   one line */}
  Welcome {user}, Let's play React
</div>
```

**Source:** _github.com/sudheerj_

#### Q6: What is context? ⭐
**Answer:**
**Context** provides a way to pass data through the component tree without having to pass props down manually at every level. For example, authenticated user, locale preference, UI theme need to be accessed in the application by many components.

```js
const {Provider, Consumer} = React.createContext(defaultValue);
```

**Source:** _github.com/sudheerj_

#### Q7: What is virtual DOM? ⭐
**Answer:**
**The virtual DOM (VDOM)** is an in-memory representation of Real DOM. The representation of a UI is kept in memory and synced with the “real” DOM. It’s a step that happens between the render function being called and the displaying of elements on the screen. This entire process is called reconciliation.

**Source:** _github.com/sudheerj_

#### Q8: How does React work? ⭐
**Answer:**
React creates a virtual DOM. When state changes in a component it firstly runs a "diffing" algorithm, which identifies what has changed in the virtual DOM. The second step is reconciliation, where it updates the DOM with the results of diff.

**Source:** _github.com/Pau1fitz_

#### Q9: What is the use of refs? ⭐
**Answer:**
The **ref** is used to return a reference to the element. They should be avoided in most cases, however, they can be useful when we need direct access to DOM element or an instance of a component.

**Source:** _github.com/sudheerj_

#### Q10: What is props in ReactJS? ⭐
**Answer:**
**Props** are inputs to a React component. They are single values or objects containing a set of values that are passed to React Components on creation using a naming convention similar to HTML-tag attributes. i.e, *They are data passed down from a parent component to a child component.*

The primary purpose of props in React is to provide following component functionality:

1. Pass custom data to your React component.
2. Trigger `state` changes.
3. Use via `this.props.reactProp` inside component's `render()` method.

For example, let us create an element with reactProp property,
```js
 <Element reactProp = "1" />
```

This `reactProp` (or whatever you came up with) name then becomes a property attached to React's native props object which originally already exists on all components created using React library.

```js
 props.reactProp;
```

**Source:** _https://github.com/sudheerj_

#### Q11: What are the major features of ReactJS? ⭐
**Answer:**
The major features of ReactJS are as follows,

- It uses **VirtualDOM** instead RealDOM considering that RealDOM manipulations are expensive.
- Supports **server-side rendering**
- Follows **Unidirectional** data flow or data binding
- Uses **reusable/composable** UI components to develop the view

**Source:** _https://github.com/sudheerj_

#### Q12: What is ReactJS? ⭐
**Answer:**
ReactJS is an **open-source frontend JavaScript library** which is used for building user interfaces especifically for single page applications. It is used for handling view layer for web and mobile apps. React was created by Jordan Walke, a software engineer working for Facebook. ReactJS was first deployed on Facebook’s newsfeed in 2011 and on Instagram.com in 2012.

**Source:** _https://github.com/sudheerj_

#### Q13: What are props in React? ⭐
**Answer:**
Props are properties that are passed into a child component from its parent, and are readonly.

**Source:** _github.com/WebPredict_

#### Q14: What is Flux? ⭐⭐
**Answer:**
Unidrectional application flow paradigm popular a few years back in React; mostly superceded by Redux these days.

**Source:** _github.com/WebPredict_

#### Q15: How error boundaries handled in React (15)? ⭐⭐
**Answer:**
React15 provided very basic support for error boundaries using the method name **unstable_handleError**. Later this has been renamed as **componentDidCatch** starting from React16 beta release.

**Source:** _github.com/sudheerj_

#### Q16: What are the limitations of ReactJS? ⭐⭐
**Answer:**
Below are the list of limitations:

1. React is just a view library, not a full-blown framework
2. There is a learning curve for beginners who are new to web development.
3. Integrating React.js into a traditional MVC framework requires some additional configuration
4. The code complexity increases with inline templating and JSX.
5. Too many smaller components leading to over-engineering or boilerplate

**Source:** _github.com/sudheerj_

#### Q17: What’s the difference between an "Element" and a "Component" in React? ⭐⭐
**Answer:**
Simply put, a React element describes what you want to see on the screen. Not so simply put, a React element is an object representation of some UI.

A React component is a function or a class which optionally accepts input and returns a React element (typically via JSX which gets transpiled to a createElement invocation).

**Source:** _medium.freecodecamp.org/_

#### Q18: What are stateful components? ⭐⭐
**Answer:**
If the behaviour of a component is dependent on the state of the component then it can be termed as _stateful component_. These Stateful components are always class components and have a state that gets initialized in the constructor.

```js
class App extends Component {
 constructor(props) {
  super(props);
  this.state = { count: 0 };
 }

 render() {
    // omitted for brevity
  }
}
```

**Source:** _github.com/sudheerj_

#### Q19: What are stateless components? ⭐⭐
**Answer:**
If the behaviour is independent of its state then it can be a _stateless component_. You can use either a function or a class for creating stateless components. But unless you need to use a lifecycle hook in your components, you should go for stateless functional components. There are a lot of benefits if you decide to use stateless functional components here; they are easy to write, understand, and test, and you can avoid the this keyword altogether.

**Source:** _github.com/sudheerj_

#### Q20: What are portals in ReactJS? ⭐⭐
**Answer:**
Portal is a recommended way to render children into a DOM node that exists outside the DOM hierarchy of the parent component.

```js
ReactDOM.createPortal(child, container);
```

The first argument (child) is any renderable React child, such as an element, string, or fragment. The second argument (container) is a DOM element.

**Source:** _github.com/sudheerj_

#### Q21: What are fragments? ⭐⭐
**Answer:**
It's common pattern in React which is used for a component to return multiple elements. Fragments let you group a list of children without adding extra nodes to the DOM.

```js
render() {
  return (
    <React.Fragment>
      <ChildA />
      <ChildB />
      <ChildC />
    </React.Fragment>
  );
}
```

There is also a shorter syntax which is not supported in many tools

```js
render() {
    return (
      <>
         <ChildA />
         <ChildB />
         <ChildC />
      </>
    );
  }
```

**Source:** _github.com/sudheerj_

#### Q22: Why is it necessary to capitalize the components? ⭐⭐
**Answer:**
It is necessary because components are not the DOM element but they are constructors. If they are not capitalized, they can cause various issues and can confuse developers with several elements.

**Source:** _github.com/sudheerj_

#### Q23: What is reconciliation? ⭐⭐
**Answer:**
When a component’s props or state change, React decides whether an actual DOM update is necessary by comparing the newly returned element with the previously rendered one. When they are not equal, React will update the DOM. This process is called **reconciliation**.

**Source:** _github.com/sudheerj_

#### Q24: What is the purpose of using super constructor with props argument? ⭐⭐
**Answer:**
A child class constructor cannot make use of **this** reference until `super()` method has been called. The same applies for ES6 sub-classes as well. The main reason of passing props parameter to super() call is to access this.props in your child constructors.

**Passing props:**
```js
class MyComponent extends React.Component {
    constructor(props) {
        super(props);
        console.log(this.props);  // Prints { name: 'sudheer',age: 30 }
    }
}
```
**Not passing props:**
```js
class MyComponent extends React.Component {
    constructor(props) {
        super();
        console.log(this.props); // Prints undefined
        // But Props parameter is still available
        console.log(props); // Prints { name: 'sudheer',age: 30 }
    }

    render() {
        // No difference outside constructor
        console.log(this.props) // Prints { name: 'sudheer',age: 30 }
    }
}
```

The above code snippets reveals that this.props behavior is different only with in the constructor. It would be same outside the constructor.

**Source:** _github.com/sudheerj_

#### Q25: When to use a Class Component over a Functional Component? ⭐⭐
**Answer:**
If the component need state or lifecycle methods then use class component otherwise use functional component.

**Source:** _https://github.com/sudheerj_

#### Q26: What are the advantages of using React? ⭐⭐
**Answer:**
- It is easy to know how a component is rendered, you just need to look at the render function.
- JSX makes it easy to read the code of your components. It is also really easy to see the layout, or how components are plugged/combined with each other.
- You can render React on the server-side. This enables improves SEO and performance.
- It is easy to test.
- You can use React with any framework (Backbone.js, Angular.js) as it is only a view layer.

**Source:** _github.com/Pau1fitz_

#### Q27: What are Higher-Order components? ⭐⭐
**Answer:**
A higher-order component **(HOC)** is a function that takes a component and returns a new component. Basically, it’s a pattern that is derived from React’s compositional nature
We call them as **“pure’ components”**  because they can accept any dynamically provided child component but they won’t modify or copy any behavior from their input components.
```js
const EnhancedComponent = higherOrderComponent(WrappedComponent);
```
HOC can be used for many use cases as below,

1. Code reuse, logic and bootstrap abstraction
2. Render High jacking
3. State abstraction and manipulation
4. Props manipulation

**Source:** _github.com/sudheerj_

#### Q28: What are controlled components? ⭐⭐
**Answer:**
A ReactJS component that controls the input elements within the forms on subsequent user input is called **“Controlled component”**. i.e, every state mutation will have an associated handler function.

For example, to write all the names in uppercase letters, we use handleChange as below,

```js
handleChange(event) {
    this.setState({
        value: event.target.value.toUpperCase()
    });
}
```

**Source:** _github.com/sudheerj_

#### Q29: What is the difference between a Presentational component and a Container component? ⭐⭐
**Answer:**
* **Presentational components** are concerned with _how things look_. They generally receive data and callbacks exclusively via props. These components rarely have their own state, but when they do it generally concerns UI state, as opposed to data state.

* **Container components** are more concerned with _how things work_. These components provide the data and behavior to presentational or other container components. They call Flux actions and provide these as callbacks to the presentational components. They are also often stateful as they serve as data sources. 

**Source:** _github.com/Pau1fitz_

#### Q30: What do you like about React? ⭐⭐
**Answer:**


**Source:** _github.com/Pau1fitz_

#### Q31: How to create refs? ⭐⭐
**Answer:**
**Refs** are created using `React.createRef()` method and attached to React elements via the ref attribute. In order to use refs throughout the component, just assign the ref to the instance property with in constructor.
```js
class MyComponent extends React.Component {
  constructor(props) {
    super(props);
    this.myRef = React.createRef();
  }
  render() {
    return <div ref={this.myRef} />;
  }
}
```
And:
```js
class UserForm extends Component {
  handleSubmit = () => {
    console.log("Input Value is: ", this.input.value)
  }
  render () {
    return (
      <form onSubmit={this.handleSubmit}>
        <input
          type='text'
          ref={(input) => this.input = input} /> // Access DOM input in handle submit
        <button type='submit'>Submit</button>
      </form>
    )
  }
}
```
We can also use it in functional components with the help of closures.

**Source:** _github.com/sudheerj_

#### Q32: What are the differences between a class component and functional component? ⭐⭐
**Answer:**
- **Class components** allows you to use additional features such as local state and lifecycle hooks. Also, to enable your component to have direct access to your store and thus holds state.

- When your component just receives props and renders them to the page, this is a **stateless component**, for which a pure function can be used. These are also called dumb components or presentational components.

**Source:** _github.com/Pau1fitz_

#### Q33: How is React different from AngularJS (1.x)? ⭐⭐
**Answer:**
For example, AngularJS (1.x) approaches building an application by extending HTML markup and injecting various constructs (e.g. Directives, Controllers, Services) at runtime. As a result, AngularJS is very opinionated about the greater architecture of your application — these abstractions are certainly useful in some cases, but they come at the cost of flexibility.

By contrast, React focuses exclusively on the creation of components, and has few (if any) opinions about an application’s architecture. This allows a developer an incredible amount of flexibility in choosing the architecture they deem “best” — though it also places the responsibility of choosing (or building) those parts on the developer.

**Source:** _codementor.io_

#### Q34: What happens during the lifecycle of a React component? ⭐⭐
**Answer:**
At the highest level, React components have lifecycle events that fall into three general categories:

1.  Initialization
2.  State/Property Updates
3.  Destruction

<img class="img-fluid" src="https://s3.amazonaws.com/codementor_content/2016-Jul/reactjs-qs1.png">

**Source:** _codementor.io_

#### Q35: What is the difference between state and props? ⭐⭐
**Answer:**
The *state* is a data structure that starts with a default value when a Component mounts. It may be mutated across time, mostly as a result of user events.

*Props* (short for properties) are a Component's configuration. They are received from above and immutable as far as the Component receiving them is concerned. A Component cannot change its props, but it is responsible for putting together the props of its child Components. Props do not have to just be data - callback functions may be passed in as props.

**Source:** _github.com/Pau1fitz_

#### Q36: What is inline conditional expressions? ⭐⭐
**Answer:**
You can use either if statements or ternary expressions which are available from JS to conditionally render expressions. Apart from these approaches, you can also embed any expressions in JSX by wrapping them in curly braces and then followed by JS logical operator(&&).
```js
<h1>Hello!</h1>
   {messages.length > 0 &&
<h2>
    You have {messages.length} unread messages.
</h2>
```

**Source:** _github.com/sudheerj_

#### Q37: How to pass a parameter to an event handler or callback? ⭐⭐
**Answer:**
You can use an arrow function to wrap around an event handler and pass parameters:

```js
<button onClick={() => this.handleClick(id)} />
```
This is equivalent to calling .bind as below,
```js
<button onClick={this.handleClick.bind(this, id)} />
```

**Source:** _github.com/sudheerj_

#### Q38: What is the purpose of callback function as an argument of setState? ⭐⭐
**Answer:**
The callback function is invoked when `setState` finished and the component gets rendered. Since `setState` is **asynchronous** the callback function is used for any post action.

**Note:** It is recommended to use lifecycle method rather this callback function.
```js
setState({name: 'sudheer'}, () => console.log('The name has updated and component re-rendered'));
```

**Source:** _https://github.com/sudheerj_

#### Q39: What happens when you call "setState"? ⭐⭐
**Answer:**
The first thing React will do when setState is called is merge the object you passed into setState into the current state of the component. This will kick off a process called reconciliation. The end goal of reconciliation is to, in the most efficient way possible, update the UI based on this new state.

To do this, React will construct a new tree of React elements (which you can think of as an object representation of your UI). Once it has this tree, in order to figure out how the UI should change in response to the new state, React will diff this new tree against the previous element tree.

By doing this, React will then know the exact changes which occurred, and by knowing exactly what changes occurred, will able to minimize its footprint on the UI by only making updates where absolutely necessary.

**Source:** _medium.freecodecamp.org/_

#### Q40: What is the difference between state and props? ⭐⭐
**Answer:**
Both **props** and **state** are plain JavaScript objects. While both of them hold information that influences the output of render, they are different in their functionality with respect to component. i.e, 
* Props get passed to the component similar to function parameters 
* state is managed within the component similar to variables declared within a function.

**Source:** _https://github.com/sudheerj_

#### Q41: What is state in ReactJS? ⭐⭐
**Answer:**
**State** of a component is an object that holds some information that may change over the lifetime of the component. We should always try to make our state as simple as possible and minimize the number of stateful components.

 Let's create user component with message state,

 ```js
 class User extends React.Component {
    constructor(props) {
       super(props);

       this.state = {
          message: "Welcome to React world",
       }
    }
    render() {
       return (
          <div>
             <h1>{this.state.message}</h1>
          </div>
       );
    }
 }
 ```

**Source:** _https://github.com/sudheerj_

#### Q42: What are refs used for in React? ⭐⭐
**Answer:**
*Refs* are an escape hatch which allow you to get direct access to a DOM element or an instance of a component. In order to use them you add a ref attribute to your component whose value is a callback function which will receive the underlying DOM element or the mounted instance of the component as its first argument.

```js
class UnControlledForm extends Component {
  handleSubmit = () => {
    console.log("Input Value: ", this.input.value)
  }
  render () {
    return (
      <form onSubmit={this.handleSubmit}>
        <input
          type='text'
          ref={(input) => this.input = input} />
        <button type='submit'>Submit</button>
      </form>
    )
  }
}
```
Above notice that our input field has a ref attribute whose value is a function. That function receives the actual DOM element of input which we then put on the instance in order to have access to it inside of the handleSubmit function.

It’s often misconstrued that you need to use a class component in order to use refs, but refs can also be used with functional components by leveraging closures in JavaScript.

```js
function CustomForm ({handleSubmit}) {
  let inputElement
  return (
    <form onSubmit={() => handleSubmit(inputElement.value)}>
      <input
        type='text'
        ref={(input) => inputElement = input} />
      <button type='submit'>Submit</button>
    </form>
  )
}
```

**Source:** _github.com/Pau1fitz_

#### Q43: When rendering a list what is a key and what is it's purpose? ⭐⭐
**Answer:**
*Keys* help React identify which items have changed, are added, or are removed. Keys should be given to the elements inside the array to give the elements a stable identity. The best way to pick a key is to use a string that uniquely identifies a list item among its siblings. 

```js
render () {
  return (
    <ul>
      {this.state.todoItems.map(({task, uid}) => {
        return <li key={uid}>{task}</li>
      })}
    </ul>
  )
}
```

Most often you would use IDs from your data as keys. When you don't have stable IDs for rendered items, you may use the item index as a key as a last resort. It is not recommend to use indexes for keys if the items can reorder, as that would be slow. 

**Source:** _github.com/Pau1fitz_

#### Q44: How to create components in ReactJS? ⭐⭐
**Answer:**
There are two possible ways to create ReactJS Components.

1. **Functional components:** This is the simplest way to create ReactJS components. It accepts props as an Object and returns ReactJS elements. We call it as “functional” because those are pure JavaScript functions.
```js
	function Greeting(props) {
   	   return <h1> Hello, {props.message}</h1> 
	}
```

2. **Class components:** You can also use Es6 class to define component. The above functional component can be written as below,
```js
      class Greeting extends React.Component {
  	    render() {
    		    return <h1>Hello, {this.props.message}</h1>;
  	        }
	    }
```


**Source:** _https://github.com/sudheerj_

#### Q45: What is the difference between Element and Component? ⭐⭐
**Answer:**
An **element** is a plain object describing what you want to appear on the screen in terms of the DOM nodes or other components. Elements can contain other elements in their props. Creating a React element is cheap. Once an element is created, it is never mutated.
The object representation of React element would be as follows,
```js
const element = React.createElement(
  'div',
  {id: 'login-btn'},
  'Login'
)
```
The above createElement returns as object as below,
```js
{
  type: 'div',
  props: {
    children: 'Login',
    id: 'login-btn'
  }
}
```
And finally it renders to the DOM using ReactDOM.render as below,
```js
<div id='login-btn'>Login</div>
```
Whereas a **component** can be declared in several different ways. It can be a class with a render() method. Alternatively, in simple cases, it can be defined as a function. In either case, it takes props as an input, and returns an element tree as the output. JSX transpiled as createElement at the end.
```js
function Button ({ onLogin }) {
  return React.createElement(
    'div',
    {id: 'login-btn', onClick: onLogin},
    'Login'
  )
}
```

**Source:** _https://github.com/sudheerj_

#### Q46: What is JSX? ⭐⭐
**Answer:**
JSX is a syntax notation for **JavaScript XML**(XML-like syntax extension to ECMAScript). It stands for JavaScript XML. It provides expressiveness of JavaScript along with HTML like template syntax. For example, the below text inside h1 tag return as javascript function to the render function,

```js
   render(){
    	return(
         <div>
            <h1> Welcome to React world!!</h1>
         </div>
    	);
     }
```

**Source:** _https://github.com/sudheerj_

#### Q47: Describe how events are handled in React. ⭐⭐
**Answer:**
In order to solve cross browser compatibility issues, your event handlers in React will be passed instances of SyntheticEvent, which is React’s cross-browser wrapper around the browser’s native event. These synthetic events have the same interface as native events you’re used to, except they work identically across all browsers.

What’s mildly interesting is that React doesn’t actually attach events to the child nodes themselves. React will listen to all events at the top level using a single event listener. This is good for performance and it also means that React doesn’t need to worry about keeping track of event listeners when updating the DOM.

**Source:** _tylermcginnis.com_

#### Q48: Where in a React component should you make an AJAX request? ⭐⭐
**Answer:**
`componentDidMount` is where an AJAX request should be made in a React component. 

This method will be executed when the component “mounts” (is added to the DOM) for the first time. This method is only executed once during the component’s life. Importantly, you can’t guarantee the AJAX request will have resolved before the component mounts. If it doesn't, that would mean that you’d be trying to setState on an unmounted component, which would not work. Making your AJAX request in `componentDidMount` will guarantee that there’s a component to update.

**Source:** _github.com/Pau1fitz_

#### Q49: What is the difference between component and container in react Redux? ⭐⭐
**Answer:**
**Component** is part of the React API. A Component is a class or function that describes part of a React UI.
**Container** is an informal term for a React component that is connected to a redux store. Containers receive Redux state updates and dispatch actions, and they usually don't render DOM elements; they delegate rendering to presentational child components.

**Source:** _github.com/sudheerj_

#### Q50: Where is the state kept in a React + Redux application? ⭐⭐
**Answer:**
In the store.

**Source:** _github.com/WebPredict_

#### Q51: What is the difference between React Native and React? ⭐⭐
**Answer:**
* **ReactJS** is a JavaScript library, supporting both front end web and being run on the server, for building user interfaces and web applications.

* **React Native** is a mobile framework that compiles to native app components, allowing you to build native mobile applications (iOS, Android, and Windows) in JavaScript that allows you to use ReactJS to build your components, and implements ReactJS under the hood.

**Source:** _github.com/sudheerj_

#### Q52: How do we pass a property from a parent component props to a child component? ⭐⭐
**Answer:**
For example: 
```html
<ChildComponent someProp={props.someProperty} />
```

**Source:** _github.com/WebPredict_

#### Q53: What is the point of Redux? ⭐⭐
**Answer:**
Application state management that is easy to reason about, maintain and manage in an asynchronous web application environment.

**Source:** _github.com/WebPredict_

#### Q54: What does it mean for a component to be mounted in React? ⭐⭐
**Answer:**
It has a corresponding element created in the DOM and is connected to that.

**Source:** _github.com/WebPredict_

#### Q55: What is Flow? ⭐⭐
**Answer:**
**Flow** is a static type checker, designed to find type errors in JavaScript programs, created by Facebook. Flow types can express much more fine-grained distinctions than traditional type systems. For example, Flow helps you catch errors involving null, unlike most type systems.

**Source:** _github.com/sudheerj_

#### Q56: What happens when you call setState? ⭐⭐
**Answer:**
The state property is updated in a React component with the object passed into setState, and this is done asynchronously. It tells React that this component and its children need to be re-rendered, but React may not do this immediately (it may batch these state update requests for better performance).

**Source:** _github.com/WebPredict_

#### Q57: What's the difference between a controlled component and an uncontrolled one in React? ⭐⭐
**Answer:**
* A controlled component has its state completely driven by React,
* Uncontrolled components can maintain their own internal state. E.g., a textarea's value.

**Source:** _github.com/WebPredict_

#### Q58: How would you prevent a component from rendering in React? ⭐⭐
**Answer:**
 Return `null` from the render method.

**Source:** _github.com/WebPredict_

#### Q59: How do you prevent the default behavior in an event callback in React? ⭐⭐
**Answer:**
You call `e.preventDefault();` on the event e passed into the callback.

**Source:** _github.com/WebPredict_

#### Q60: What is the difference between createElement and cloneElement? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q61: What's an alternative way to avoid having to bind to this in event callback methods? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q62: What are some limitations of things you shouldn't do in the component's render method? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q63: What is the point of using keys in React? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q64: What's the typical pattern for rendering a list of components from an array of data? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q65: What is the render method for? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q66: Why do class methods need to be bound to a class instance? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q67: What is reconciliation in React? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q68: What's the difference between an Element and a Component in React? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q69: What is StrictMode in React? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q70: What is useState() in React? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q71: What is the point of shouldComponentUpdate() method? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q72: What are PropTypes in React? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q73: What's the difference between `useRef` and `createRef`? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q74: What are React Hooks? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q75: What is ReactDOM? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q76: What are advantages of using React Hooks? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q77: What do these three dots (...) in React do? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q78: What are typical middleware choices for handling asynchronous calls in Redux? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q79: What's the difference between a "smart" component and a "dumb" component? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q80: Name the different lifecycle methods. ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q81: What's the typical flow of data like in a React + Redux app? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q82: What are controlled components? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q83:  What is state in react? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q84: How do you tell React to build in Production mode and what will that do? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q85: What is a higher order component? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q86: What is the difference between createElement and cloneElement? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q87: What are the advantages of React over VueJS? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q88: What advantages are using arrow functions? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q89: What are error boundaries in ReactJS (16)? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q90: What are Pure Components? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q91: Given the code defined above, can you identify two problems? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q92: What are stateless components? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q93: Name some popular Flux Libraries ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q94: Why should not we update the state directly? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q95: Why is it advised to pass a callback function to setState as opposed to an object? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q96: What is the difference between HTML and React event handling? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q97: How to bind methods or event handlers in JSX callbacks? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q98: What is the alternative of binding `this` in the constructor? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q99: What are synthetic events in ReactJS? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q100: How would you prevent a component from rendering? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q101: What is Key and benefit of using it in lists? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q102: What can you tell me about JSX? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q103: What don't you like about React? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q104: What are forward refs? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q105: What does "shouldComponentUpdate" do and why is it important? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q106: Why fragments are better than container divs? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q107: What is JSX? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q108: What is the difference between ShadowDOM and VirtualDOM? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q109: Why ReactJS uses className over class attribute? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q110: What is equivalent of the following using React.createElement? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q111: What are uncontrolled components? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q112: What would be the common mistake of function being called every time the component renders? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q113: What is Lifting State Up in ReactJS? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q114: What are the different phases of ReactJS component lifecycle? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q115: What are the lifecycle methods of ReactJS? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q116: How to set state with a dynamic key name? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q117: What is a store in redux? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q118: What is an action? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q119: What is children prop? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q120: What is prop drilling and how can you avoid it? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q121: How to create props proxy for HOC component? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q122: What is "Children"? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q123: What is a reducer? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q124: Why would you need to bind event handlers to "this"? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q125: What are some recent changes in the React library (e.g. in version 14, 15)? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q126: What is React Fiber? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q127: When would you use StrictMode component in React? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q128: Why are String Refs legacy? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q129: What is the purpose of super(props)? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q130: Which is preferred option with in callback refs and findDOMNode()? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q131: Why does React use SyntheticEvents? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q132: How to apply validation on Props in ReactJS? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q133: Are you familiar with Flux? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q134: Describe Flux vs MVC? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q135: If you created a React element like Twitter below, what would the component definition of Twitter look like? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q136: What is the difference between a controlled component and an uncontrolled component? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q137:  What are the recommended ways for static type checking? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q138: What is the difference between ReactJS and Angular? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q139: Why would you use React.Children.map(props.children, () => ) instead of props.children.map(() => )? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q140: How would you go about investigating slow React application rendering? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q141: Why would you use forceUpdate in a React component? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q142: Why would you eject from create-react-app? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q143: What is the difference between Flow and PropTypes? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q144: Explain the Virtual DOM concept in React. ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q145: What is mapStateToProps and mapDispatchToProps? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q146: What is the second argument that can optionally be passed to setState and what is its purpose? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q147: What is the React context? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q148: What is the difference between using constructor vs getInitialState in React? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q149: When is it important to pass props to super(), and why? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q150: Does React re-render all components and sub components every time setState is called? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q151: How to conditionally add attributes to React components? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q152: Do Hooks replace render props and higher-order components? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q153: If you need to access the underlying DOM node for a React component, what's the typical way to do this in React? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q154: What's a pure functional component in React? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q155: What is wrong with this code? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q156: How does React renderer work exactly when we call setState?  ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q157: What is React Fiber? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q158: What is reselect and how it works? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q159: How to use Polymer in ReactJS? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q160: What is the key architectural difference between a JavaScript library such as React and a JavaScript framework such as Angular? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q161: Explain some difference between Flux and AngularJS (1.x) approach ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q162: What is a pure function? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q163: What is Redux Thunk used for? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q164: How to avoid the need for binding in React? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

## [[⬆]](#toc) <a name=ReactNative>React Native</a> Interview Questions
#### Q1: Why do we use curly brace while importing some library? ⭐
**Details:**
Consider:
```
import { Text, StyleSheet } from "react-native";
```

**Answer:**
Curly braces are used to import **small** pieces of library. 
In above example we just want to make use of `Text` and `StyleSheet` component from react-native, so they are put in curly braces.

**Source:** _github.com_

#### Q2: What is React Native? ⭐
**Answer:**
- `React Native` is a mobile app development framework that enables the development of multi-platform **Android** and **iOS** apps using native UI elements. 
- It is based on the *JavaScriptCore* runtime and *Babel* transformers. With this setup react native supports new `JavaScript` (ES6+) features, e.g. arrow functions, async/await etc.
- This famous framework for **mobile app development** started in the summer of 2013 as Facebook’s internal hackathon project. 
- Its first public preview was released in January of 2015 at `Reactjs` Conference and in March of 2015, Facebook made React Native open and available on GitHub.

**Source:** _brainhub.eu_

#### Q3: List some benefits of using React Native for building mobile apps? ⭐
**Answer:**
Some benefits of React Native are:

- Known for Optimal Performance
- Can Reuse the Codes and Pre-Developed Components
- Large Community of Developers
- Advantage of Live and Hot Reloading
- Cost Effective Solution
- Offers Simple User Interface
- Support for Third-Party Plugins
- Modular Architecture
- Providing Handy Solutions and Libraries

**Source:** _brainhub.eu_

#### Q4: What are hybrid apps? ⭐
**Answer:**
- Hybrid mobile apps are applications that are installed on a device, just like any other app.
- Hybrid apps are deployed in a native container that uses a mobile `WebView` object. When the app is used, this object displays web content thanks to the use of web technologies (`CSS`, `JavaScript`, `HTML`).

**Source:** _brainhub.eu_

#### Q5: What are native apps? ⭐
**Answer:**
- Native mobile apps are the most common type of app. 
- They are built for specific platforms and are written in languages that the platform accepts. For example, `Swift` and *Objective-C* for native **iOS** apps and `Java` or `Kotlin` for native **Android** apps. 
- Native apps are also built using the specific *Integrated Development Environment* (IDE) for the selected operating systems

**Source:** _clearbridgemobile.com_

#### Q6: What are the advantages of hybrid apps over native apps? ⭐
**Answer:**
- Works across multiple platforms.
- Unified development.
- Faster build and lower cost of development.
- Easier to make changes and update.

#### Q7: How is React Native different from ReactJs? ⭐⭐
**Answer:**
**ReactJS**
React has as its main focus **Web Development.**
- **React’s virtual DOM is faster than the conventional full refresh model**, since the virtual DOM refreshes only parts of the page. 
- We use div, p, span, etc. HTML tags to build the UI of the web application.
- You can **reuse code components** in React, saving you a lot of time. (You can in React Native too.)
- As a business: The rendering of your pages completely, from the server to the browser will **improve the SEO of your web app**.
- It **improves the debugging speed** making your developer’s life easier.
- You can use hybrid mobile app development, like Cordova or Ionic, to build mobile apps with React, but is more efficiently building mobile apps with React Native from many points.

**React Native**
***An extension of React***, niched on **Mobile Development.**

- Its main focus is all about **Mobile User Interfaces**.
- **iOS & Android** are covered.
- **Reusable** React Native UI **components & modules** allow hybrid apps to render natively.
- We use `View`, `Text` imported from React Native library.
- No need to overhaul your old app. All you have to do is **add React Native UI components into your existing app’s code**, without having to rewrite.
- **Doesn't use HTML to render the app**. Provides alternative components that work in a similar way, so it wouldn't be hard to understand them.
- Because your code doesn’t get rendered in an HTML page, this also means you **won’t be able to reuse any libraries you previously used with React** that renders any kind of HTML, SVG or Canvas.
- React Native is not made from web elements and can’t be styled in the same way.

**Source:** _stackoverflow.com_

#### Q8: What are Refs used for in React Native? ⭐⭐
**Answer:**
**Refs** provide you direct access to a DOM element or a components instance.

**Source:** _github.com_

#### Q9: Tell us some options of storing persisting data in a react native app? ⭐⭐
**Answer:**
Some popular options are:
- Async Storage  ("built-in" to React Native)
- SQLite
- Realm
- Firebase
- MongoDB

**Source:** _stackoverflow.com_

#### Q10: How do you check if the react native app is in debug or release build? ⭐⭐
**Answer:**
You can use this command
```jsx
if (__DEV__) {
    console.log('I am in debug');
}
```

**Source:** _stackoverflow.com_

#### Q11: What are the advantages of native apps over hybrid apps? ⭐⭐
**Answer:**
-   They work efficiently as they are built for that specific platforms
-   Native apps are responsive on all the platform-specific devices
-   They are very fast and the best in the app performance
-   Native apps better integrate with mobile hardware
-   They have interactive and intuitive User Interface (UI) and User Experience (UX) as per the user expectations based on specific platforms
-   Some of the Native mobile apps work even without the Internet connection
-   Native apps are secured and reliable
-   They can easily access or utilize the other device-specific capabilities like GPS, Camera, Contacts, etc.

**Source:** _www.quora.com_

#### Q12: What does the Gesture Responder System do? ⭐⭐
**Answer:**
The **gesture responder system** manages the lifecycle of gestures in an app.

**Source:** _facebook.github.io_

#### Q13: What are components? ⭐⭐
**Answer:**
- **Components** are the building blocks of any `React` application.
- Components let you split the UI into **independent**, **reusable** pieces, and think about each piece in **isolation**.
- *React Native* provides a number of built-in components. Some are:-
	- Basic Components
	- User Interface
	- List Views
	- iOS-specific
	- Android-specific

**Source:** _facebook.github.io_

#### Q14: What are the types of data that control a component? ⭐⭐
**Answer:**
- There are two types of data that control a component: `props` and `state`.
- `props` are set by the parent and they are fixed throughout the lifetime of a component. For data that is going to change, we have to use `state`.

**Source:** _facebook.github.io_

#### Q15: What are props in React Native? ⭐⭐
**Answer:**
- The properties of React Native components are simply pronounced as  **props**. 
- In React Native, most of the components can be customized at the time of their creation with different parameters. These parameters are known as  **props**. 
- They are **immutable**, and they cannot be changed.

```jsx
import React, { Component } from 'react';  
import {  
  Platform,  
  StyleSheet,  
  Image,  
  Text,  
  View  
} from 'react-native';  
  
export default class App extends Component<{}> {  
  render() {  
    let imagePath = { uri: 'https://facebook.github.io/react-native/img/header_logo.png'};  
    return (  
        <View style={styles.container}>  
          <Text style={styles.welcome}>Welcome to React Native!</Text>  
          <Image source={imagePath} style={{width: 250, height: 250}} />  
        </View>  
    );  
  }  
}  
  
const styles = StyleSheet.create({  
  container: {  
    flex: 1,  
    justifyContent: 'center',  
    alignItems: 'center',  
    backgroundColor: '#a7a6a9',  
  },  
  welcome: {  
    fontSize: 30,  
    textAlign: 'center',  
    margin: 20,  
  }  
});  
```

Output

![React Native Props](https://static.javatpoint.com/tutorial/react-native/images/react-native-props-output.png)


**Source:** _facebook.github.io_

#### Q16: What determines the size of a component and what are the ways? ⭐⭐
**Answer:**
- The **height** and **width** determine the size of component on the screen.
- Two different ways to set height and width.
	- Fixed Dimensions
	- Flex Dimensions

**Source:** _facebook.github.io_

#### Q17: What are some ways of styling a react native component? ⭐⭐
**Answer:**
We can use: 
- Inline styling
- StyleSheet
- Styled Components

**Source:** _facebook.github.io_

#### Q18: When would you use ScrollView over FlatList or vice-versa? ⭐⭐
**Answer:**
- Do you need to render a list of similar items from an array or the data is very big? Use  `FlatList`
- Do you need to render generic content in a scrollable container and the data is small? Use  `ScrollView`

**Source:** _stackoverflow.com_

#### Q19: What is JSX? ⭐⭐
**Answer:**
- **JSX** is an *XML/HTML*-like syntax used by `React` that extends *ECMAScript* so that XML/HTML-like text can co-exist with `JavaScript/React` code. 
- The syntax is intended to be used by **preprocessors** (i.e., transpilers like Babel) to transform HTML-like text found in `JavaScript` files into standard JavaScript objects that a JavaScript engine will parse.
```js
const nav = (
    <ul id="nav">
      <li><a href="#">Home</a></li>
      <li><a href="#">About</a></li>
      <li><a href="#">Clients</a></li>
      <li><a href="#">Contact Us</a></li>
    </ul>
);
```

**Source:** _www.reactenlightenment.com_

#### Q20: How do you dismiss the keyboard in react native? ⭐⭐
**Answer:**
Using `Keyboard.dismiss()`

```jsx
import { Keyboard } from 'react-native'

// Hiding the keyboard
Keyboard.dismiss()
```

**Source:** _stackoverflow.com_

#### Q21: What will be the output of following snippet? ⭐⭐
**Details:**
```jsx
const ComponentScreen = () => {
const someArray = ['1', '2', '3']
  return (
    <View>
      <Text>{someArray}</Text>
    </View>
  )
 }
 export default ComponentScreen;
 ```

**Answer:**
`123`

**Source:** _github.com_

#### Q22: Will this piece of code work? ⭐⭐
**Details:**
```jsx
<View>
  <Text>Hey there!</Text>
  <Text style={{ fontsize: 40 }} >Example of inline style</Text>;
</View>
```

**Answer:**
**No**.  An error will be thrown as `Text` strings **must** be rendered within `Text` component. Because here semi-colon in third line will be treated as text, and in React native all texts needs to be rendered inside `Text` tag.

**Source:** _github.com_

#### Q23: Explain the use of Flexbox in React Native? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q24: What is View and how important is it? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q25: How is flexbox different in React Native and browser? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q26: What is the use of ScrollView component? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q27: What is the use of FlatList? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q28: What is State in react native? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q29: What is "autolinking" in react-native? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q30: How are props and state different? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q31: How do you perform logging in React native? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q32: How are Hot Reloading and Live Reloading in React Native different? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q33: How to fetch data from local JSON file on React Native? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q34: What are Touchable Interactions in React Native? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q35: What does TouchableHighlight do and when do you use it? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q36: How do you re-render a FlatList? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q37: How do you style a component in react native? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q38: What are some best practices to consider for an action? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q39: What is "Fast Refresh"? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q40: What happens if you edit a module that only exports React components in Fast Refresh? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q41: What happens if you edit modules with *exports* that aren't React components in Fast Refresh? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q42: In Fast Refresh, what will happen if you edit files imported by modules outside of the React Tree? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q43: What are some features of Fast Refresh? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q44: What does StyleSheet.create do and why is it useful? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q45: What is AppRegistry? Why is it required early in "require" sequence? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q46:  What is flex dimension and how is it different from fixed dimension? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q47: What is Lifting State Up? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q48: What are Presentational/Dumb Components? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q49: What are features of  presentational/dumb components? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q50: Are libraries such as TypeScript that compile to JavaScript compatible with React Naive? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q51: State the lifecycle of Gesture Responder System? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q52: What is Component Driven Development (CDD)? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q53: What are some advantages of Component Driven Development? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q54: Differentiate ScrollView and FlatList? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q55: What is Higher Order Component or HOC? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q56: What are some limitations of using react-native-cli for instantiating a project? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q57: How would you implement animations on events? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q58:  Does React Native compile JavaScript into Java for Android? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q59: What is AsyncStorage and how do you use it? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q60: What JavaScript engine does React native use? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q61: What does React Native Packager do in the React Native?   ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q62: How many threads run in a React Native app?  ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q63: What are Container/Smart components? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q64: What are the features of Container/Smart components? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q65: What are some benefits of Container-Presentational pattern? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q66: How does the Fabric architecture work? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q67: What is Fabric in React Native? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q68: How is InteractionManager important? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q69: What is wrong with this code for querying a native API? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q70: What is InteractionManager and how is it used? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q71: What are the disadvantages of StyleSheet.create? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q72:  Does React Native have a Virtual DOM? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

## [[⬆]](#toc) <a name=ReactiveProgramming>Reactive Programming</a> Interview Questions
#### Q1: What Are Some Advantages of Reactive Programming? ⭐⭐
**Answer:**
Here’s a short list of advantages :

*   avoid “callback hell”
*   a lot simpler to do async / threaded work
*   a lot of operators that simplify work
*   very simple to compose streams of data
*   complex threading becomes very easy
*   you end up with a more cleaner, readable code base
*   easy to implement back-pressure

**Source:** _medium.com_

#### Q2: What is Scalability of the Reactive System? ⭐⭐
**Answer:**
**Scalability** is the ability of a system to make use of more computing resources in order to increase its performance is measured by the ratio of throughput gain to resource increase. A perfectly scalable system is characterized by both numbers being proportional: a twofold allocation of resources will double the throughput. Scalability is typically limited by the introduction of bottlenecks or synchronization points within the system, leading to constrained scalability, see Amdahl’s Law and Gunther’s Universal Scalability Model.

**Source:** _reactivemanifesto.org_

#### Q3: What is the Reactive Manifesto?  ⭐⭐
**Answer:**
The **Reactive Manifesto** is a document that defines the core principles of reactive programming. It was first released in 2013 by a group of developers led by a man called Jonas Boner. The Reactive Manifesto underpins the principles of reactive programming.

**Source:** _reactivemanifesto.org_

#### Q4: What is Reactive Programming? ⭐⭐
**Answer:**
**Reactive programming is programming with asynchronous data streams.** Event buses or your typical click events are really an asynchronous event stream, on which you can observe and do some side effects. Reactive is that idea on steroids. You are able to create data streams of anything, not just from click and hover events. Streams are cheap and ubiquitous, anything can be a stream: variables, user inputs, properties, caches, data structures, etc. For example, imagine your Twitter feed would be a data stream in the same fashion that click events are. You can listen to that stream and react accordingly.

**Source:** _github.com_

#### Q5: What is Stream? ⭐⭐
**Answer:**
A **stream** is a sequence of ongoing events ordered in time. It can emit three different things: a value (of some type), an error, or a "completed" signal. 

<div class="text-center"/>
<img src="https://camo.githubusercontent.com/36c0a9ffd8ed22236bd6237d44a1d3eecbaec336/687474703a2f2f692e696d6775722e636f6d2f634c344d4f73532e706e67" class="img-fluid" style="max-width: 500px" />
</div>


**Source:** _github.com_

#### Q6: Name building blocks of Reactive Programming ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q7: What is Elasticity (in contrast to Scalability)? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q8: What Does It Mean to be Responsive for a Reactive System? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q9: What are some benefits of Reactive Systems? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q10: Explain the Term Non-Blocking ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q11: Name Some Characteristic of Reactive Systems ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q12: What is Reactive Programming? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q13: What Does Asynchrony Mean in the Context of Reactive Systems? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q14: What is Back-Pressure? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q15: What is Actor Model? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q16: What is the difference between Promises and Observables? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q17: Describe Difference Between Reactive Programming vs Imperative Programming ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q18: Imperative vs Functional vs Reactive Programming. Explain. ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q19: What Does It Mean to be Resilient for a Reactive System? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q20: Provide Definition Of Location Transparency ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q21: Explain Failure in Contrast to Error ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q22: What Does It Mean to be Elastic for a Reactive System? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q23: What is Difference Between Observer Pattern and Reactive Programming? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q24: What is the difference between Reactive and Functional-Reactive programming? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q25: What does Amdahl's Law mean? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q26: What Does It Mean to be Message Driven for a Reactive System? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q27: Explain Message-Driven vs Event-Driven Approaches ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

## [[⬆]](#toc) <a name=Redux>Redux</a> Interview Questions
#### Q1: What is Flux? ⭐
**Answer:**
**Flux** is an application design paradigm used as a replacement for the more traditional mvc pattern. It is not a framework or a library but a new kind of architecture that complements React and the concept of Unidirectional Data Flow. Facebook used this pattern internally when working with React The workflow between dispatcher, stores and views components with distinct inputs and outputs as follows:

<div class="text-center"/>
<img src="https://github.com/sudheerj/reactjs-interview-questions/raw/master/images/flux.png" class="img-fluid"/>
</div>


**Source:** _github.com/sudheerj_

#### Q2: What is Redux DevTools? ⭐
**Answer:**
**Redux DevTools** is a live-editing time travel environment for redux with hot reloading, action replay, and customizable UI. If you don’t want to bother with installing Redux DevTools and integrating it into your project, consider using Redux DevTools Extension for Chrome and Firefox.

**Source:** _github.com/sudheerj_

#### Q3: What is Redux? ⭐
**Answer:**
**Redux** is a predictable state container for JavaScript apps based on the Flux design pattern. Redux can be used together with ReactJS, or with any other view library. It is tiny (about 2kB) and has no dependencies.

**Source:** _github.com/sudheerj_

#### Q4: Do you need to keepIs all component states in Redux store? ⭐
**Answer:**
You need to keep your application state as small as possible. You don't have to push everything in there. Only do it makes a lot of sense to keep something there Or if it makes your life easier when using Dev Tools. But we shouldn't overload its importance too much.

**Source:** _github.com/sudheerj_

#### Q5: How to add multiple middlewares to Redux? ⭐⭐
**Answer:**
You can use `applyMiddleware` where you can pass each piece of middleware as a new argument. So you just need to pass each piece of middleware you'd like. For example, you can add Redux Thunk and logger middlewares as an argument as below,
```js
import { createStore, applyMiddleware } from 'redux'
const createStoreWithMiddleware = applyMiddleware(ReduxThunk, logger)(createStore);

```

**Source:** _github.com/sudheerj_

#### Q6: What are Redux selectors and Why to use them? ⭐⭐
**Answer:**
Selectors are functions that take Redux state as an argument and return some data to pass to the component.
For example, to get user details from the state:
```js
const getUserData = state => state.user.data;
```

**Source:** _github.com/sudheerj_

#### Q7: What are the features of Redux DevTools? ⭐⭐
**Answer:**
Below are the major features of Redux devTools
1. Lets you inspect every state and action payload
2. Lets you go back in time by “cancelling” actions
3. If you change the reducer code, each “staged” action will be re-evaluated
4. If the reducers throw, you will see during which action this happened, and what the error was
5. With `persistState()` store enhancer, you can persist debug sessions across page reloads

**Source:** _github.com/sudheerj_

#### Q8: What are reducers in redux? ⭐⭐
**Answer:**
The **reducer** is a _pure function_ that takes the previous state and an action, and returns the next state.

```js
(previousState, action) => newState
```

It's called a reducer because it's the type of function you would pass to `Array.prototype.reduce(reducer, ?initialValue)`. It's very important that the reducer stays _pure_. Things you should never do inside a reducer:

* Mutate its arguments;
* Perform side effects like API calls and routing transitions;
* Call non-pure functions, e.g. `Date.now()` or `Math.random()`.

**Source:** _redux.js.org_

#### Q9: What is Redux Thunk? ⭐⭐
**Answer:**
**Redux Thunk** middleware allows you to write action creators that return a function instead of an action. The thunk can be used to delay the dispatch of an action, or to dispatch only if a certain condition is met. The inner function receives the store methods dispatch and `getState()` as parameters.

**Source:** _github.com/sudheerj_

#### Q10: What is the difference between React context and React redux? ⭐⭐
**Answer:**
You can use **Context** in your application directly and is going to be great for passing down data to deeply nested components which what it was designed for. Whereas **Redux** is much more powerful and provides a large number of features that the Context Api doesn't provide. 

Also, React Redux uses context internally but it doesn’t expose this fact in the public API. So you should feel much safer using context via React Redux than directly because if it changes, the burden of updating the code will be on React Redux instead developer responsibility.

**Source:** _github.com/sudheerj_

#### Q11: What is redux-saga? ⭐⭐
**Answer:**
**redux-saga** is a library that aims to make side effects (i.e. asynchronous things like data fetching and impure things like accessing the browser cache) in React/Redux applications easier and better.
It is available in NPM as

```sh
npm install --save redux-saga
```

**Source:** _github.com/sudheerj_

#### Q12: What are the core principles of Redux? ⭐⭐
**Answer:**
Redux follows three fundamental principles:
1. **Single source of truth:** The state of your whole application is stored in an object tree within a single store. The single state tree makes it easier to keep track of changes over time and debug or inspect the application.
2. **State is ready only:** The only way to change the state is to emit an action, an object describing what happened. This ensures that neither the views nor the network callbacks will ever write directly to the state.
3. **Changes are made with pure functions:** To specify how the state tree is transformed by actions, you write pure reducers(Reducers are just pure functions that take the previous state and an action, and return the next state).

**Source:** _github.com/sudheerj_

#### Q13: How to set initial state in Redux? ⭐⭐
**Answer:**
You need to pass initial state as second argument to `createStore`
```js
const rootReducer = combineReducers({
  todos: todos,
  visibilityFilter: visibilityFilter
});

const initialState = {
  todos: [{id:123, name:'sudheer', completed: false}]
};

const store = createStore(
  rootReducer,
  initialState
);
```

**Source:** _github.com/sudheerj_

#### Q14: How to structure Redux top level directories? ⭐⭐
**Answer:**
Most of the applications has several top-level directories as below
1. **Components** Used for “dumb” React components unaware of Redux
2. **Containers** Used for “smart” React components connected to Redux
3. **Actions** Used for all action creators, where file name corresponds to part of the app
4. **Reducers** Used for all reducers, where file name corresponds to state key
5. **Store** Used for store initialization
This structure works well for small and mid-level size apps.

**Source:** _github.com/sudheerj_

#### Q15: What are the downsides of Redux over Flux? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q16: What are the differences between redux-saga and redux-thunk? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q17: What is the purpose of the constants in Redux? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q18: How to use connect from react redux? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q19: Are there any similarities between Redux and RxJS? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q20: What is Redux form? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q21: What are the main features of Redux Form? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q22: How to access redux store outside a react component? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q23: What is the proper way to access Redux store? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q24: What are the differences between call and put in redux-saga? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q25: Whats the purpose of at (@) symbol in the redux connect decorator? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q26: How to make Ajax request in Redux? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q27: Why are Redux state functions called as reducers? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q28: How to reset state in redux? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q29: What is the mental model of redux-saga? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q30: How Relay is different from Redux? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

## [[⬆]](#toc) <a name=Ruby>Ruby</a> Interview Questions
#### Q1: What is the highest level in the object model? ⭐
**Answer:**
`BasicObject`

**Source:** _githubusercontent.com_

#### Q2: Is there an equivalent of “continue” in Ruby? ⭐
**Answer:**
Yes, it's called `next`.

```js
for i in 0..5
   if i < 2
     next
   end
   puts "Value of local variable is #{i}"
end
```

**Source:** _stackoverflow.com_

#### Q3: Which core object includes the "Kernel" module?   ⭐
**Answer:**
`Object`

**Source:** _githubusercontent.com_

#### Q4: What can you say about an identifier that begins with a capital letter?   ⭐
**Answer:**
It is a constant.

**Source:** _githubusercontent.com_

#### Q5: Why Ruby is known as a language of flexibility? ⭐
**Answer:**
Ruby is known as a language of flexibility because it facilitates its author to alter the programming elements. Some specific parts of the language can be removed or redefined. Ruby does not restrict the user. For example, to add two numbers, Ruby allows to use `+` sign or the word `plus`. This alteration can be done with Ruby's built-in class Numeric.

**Source:** _javatpoint.com_

#### Q6: What is an object? ⭐
**Answer:**
An instance of a class. To some, it's also the root class in ruby (Object). Classes themselves descend from the Object root class.

**Source:** _stackoverflow.com_

#### Q7: What is a class? ⭐
**Answer:**
Classes hold **data**, have **methods** that interact with that data, and are used to **instantiate objects**.

```ruby
class WhatAreClasses
  def initialize
    @data = "I'm instance data of this object. Hello."
  end

  def method
    puts @data.gsub("instance", "altered")
  end
end

object = WhatAreClasses.new
object.method
 #=> I'm altered data of this object. Hello.
```

**Source:** _stackoverflow.com_

#### Q8: What are rubygems? ⭐
**Answer:**
**rubygems** is package manager software for ruby libraries (i.e. gems). The package manager has basic CRUD operations, dependency trees, and supports asynchronous communication between multiple gem servers.

**Source:** _stackoverflow.com_

#### Q9: Is everything in Ruby an object?   ⭐
**Answer:**
Methods are not objects. Blocks are not objects. Keywords are not objects. However, there exist Method objects and Proc objects, and some keywords refer to objects.

**Source:** _githubusercontent.com_

#### Q10: Are class variables inherited?   ⭐⭐
**Answer:**
No. The behavior is different than inheritance. Any alteration of a class variable by a subclass affects that class variable in the superclass and all other subclasses of the superclass.

**Source:** _githubusercontent.com_

#### Q11: What is the difference between a class variable and a class instance variable?   ⭐⭐
**Answer:**
Class instance variables are instance variables of a class. Class instance variables cannot be used within instance methods.

**Source:** _githubusercontent.com_

#### Q12: What are two uses of the splat operator?   ⭐⭐
**Answer:**
* Explode or expand the elements of an array. 
* Collect arguments of a parameter list into an array.

**Source:** _githubusercontent.com_

#### Q13:  What is the difference between `#==` and `#===`?   ⭐⭐
**Answer:**
`#==` performs the generic comparison while `#===` performs case equality comparison and is useful for providing meaningful semantics in case statements.


**Source:** _githubusercontent.com_

#### Q14: Why might you use `Hash#fetch` over `Hash#[]` when querying values in a hash?   ⭐⭐
**Answer:**
`Hash#fetch` provides options for handling the case where a key does not exist in the hash.

**Source:** _githubusercontent.com_

#### Q15: Why might you use `#each` instead of `for/in`?   ⭐⭐
**Answer:**
It's the "Ruby way" - an example of how Ruby defines methods that mimic natural language concepts. Iterator methods such as `#each` read more naturally. `#each` is a block so it defines a new variable scope. `for/in` depends on the existence of `#each` which implies that `#each` is a more fundamental aspect of the language.

**Source:** _githubusercontent.com_

#### Q16: Explain redo statement in Ruby ⭐⭐
**Answer:**
Ruby `redo` statement is used to repeat the current iteration of the loop. The redo statement is executed without evaluating loop's condition.

**Source:** _javatpoint.com_

#### Q17: What is the difference between nil and false in Ruby? ⭐⭐
**Answer:**
**nil**:
* nil cannot be a value
* nil is returned where there is no predicate
* nil is not a boolean data type
* nil is an object of nilclass

**false**:
* false can be a value
* in case of a predicate, true or false is returned by a method
* false is a boolean data type
* false is an object of falseclass


**Source:** _javatpoint.com_

#### Q18: Are instance methods public or private?   ⭐⭐
**Answer:**
They are public by default. You can change their visibility using `Module#private`, `Module#protected`, or back again using `Module#public`.

**Source:** _githubusercontent.com_

#### Q19: What is a predicate in the context of Ruby method naming conventions?  ⭐⭐
**Answer:**
A method that answers a question posed by the method invocation or method name. Predicates typically return a boolean.

```js
$ irb
> 5.odd?
=> true

> 5.even?
=> false

> 5.between?(1, 10)
=> true

> 5.between?(11, 20)
=> false
```

**Source:** _githubusercontent.com_

#### Q20: What is the difference between private and protected methods?   ⭐⭐
**Answer:**
A private method can only be called by any instance methods of the defining class or any subclasses and must be invoked in a functional style and not explicitly on `self` such as with `self.my_method`. A protected method may be explicitly invoked by any instance of the defining class, and is not restricted to implicit invocation on `self`.

**Source:** _githubusercontent.com_

#### Q21: Explain some differences between Ruby and Python ⭐⭐
**Answer:**
Similarities:

* High level language
* Support multiple platforms
* Use interactive prompt called irb
* Server side scripting language

Differences:

* Ruby is fully object oriented while Python is not.
* Ruby supports EclipseIDE while Python supports multiple IDEs.
* Ruby use Mixins while Python doesn't.
* Ruby supports blocks, procs and lambdas while Python doesn't.

**Source:** _javatpoint.com_

#### Q22: What is a DSL and how does it pertain to Ruby?   ⭐⭐
**Answer:**
A **Domain Specific Language** is an API that allows a developer to solve a problem or represent data more naturally than they might otherwise. The flexible nature of Ruby's syntax and the ability to alias and alter existing methods and classes makes it conducive to creating rich DSL's.

**Source:** _githubusercontent.com_

#### Q23: What is the difference between an instance variable and a class variable?   ⭐⭐
**Answer:**
A class variable is evaluated in reference to the class object created by the enclosing class definition while an instance variable is evaluated in reference to `self`. Instance variables cannot be referenced outside of instance methods.

**Source:** _githubusercontent.com_

#### Q24: What does it mean to coerce an object? Why would you do it?   ⭐⭐
**Answer:**
To *coerce an object* means to force it into an expected type. One might do this in order to try and force an unknown object type into the expected type or format required by the operation. This is a common practice involved in *duck typing*.

**Source:** _githubusercontent.com_

#### Q25: How might you specify a default value for a hash?  ⭐⭐
**Answer:**
Pass the default values as arguments to `::new` on initialization or change the default directly with the method `Hash#default`. You may also provide a default at the time of query with `Hash#fetch`.

**Source:** _githubusercontent.com_

#### Q26: Why are symbols typically used as hash keys instead of strings? ⭐⭐
**Answer:**
Strings are *mutable* while symbols are *immutable*. Though Ruby internally makes an immutable copy of a string when used as a hash key, comparing two symbols is faster than comparing two `String` objects. This is also a convention.

**Source:** _githubusercontent.com_

#### Q27: Check if a value exists in an array in Ruby ⭐⭐
**Details:**
I have a value `Dog` and an array `['Cat', 'Dog', 'Bird']`.

How do I check if it exists in the array without looping through it? Is there a simple way of checking if the value exists, nothing more?

**Answer:**
You're looking for include?:
```js
>> ['Cat', 'Dog', 'Bird'].include? 'Dog'
=> true
```

**Source:** _githubusercontent.com_

#### Q28: Is Ruby a strongly typed or a weakly typed language?   ⭐⭐
**Answer:**
Strongly typed since an object's type is checked before an operation is performed on it.

**Source:** _githubusercontent.com_

#### Q29: Is Ruby a statically typed or a dynamically typed language?   ⭐⭐
**Answer:**
Dynamically typed since type checking is done at runtime.

**Source:** _githubusercontent.com_

#### Q30: What is duck typing and how does it pertain to Ruby?   ⭐⭐
**Answer:**
That an object may be acted upon even if it isn't the expected type as long as it looks and behaves like the expected object. This is a characteristic of Ruby because the lack of type checking of parameters makes this an effective programming technique.

**Source:** _githubusercontent.com_

#### Q31: What is a module?  Can you tell me the difference between classes and modules? ⭐⭐
**Answer:**
Modules serve as a mechanism for **namespaces**.

```ruby
module ANamespace
  class AClass
    def initialize
      puts "Another object, coming right up!"
    end
  end
end

ANamespace::AClass.new
 #=> Another object, coming right up!
```

Also, modules provide as a mechanism for multiple inheritance via **mix-ins** and **cannot be instantiated** like classes can.

```ruby
module AMixIn
  def who_am_i?
    puts "An existentialist, that's who."
  end
end

# String is already the parent class
class DeepString < String
  # extend adds instance methods from AMixIn as class methods
  extend AMixIn
end

DeepString.who_am_i?
 #=> An existentialist, that's who.

AMixIn.new
 #=> NoMethodError: undefined method ‘new’ for AMixIn:Module
```

**Source:** _gist.github.com_

#### Q32: There are three ways to invoke a method in ruby.  Can you give me at least two? ⭐⭐
**Answer:**
We are looking for the **dot operator** (or period operator), the **Object#send** method, or **method(:foo).call**

```ruby
object = Object.new
puts object.object_id
 #=> 282660

puts object.send(:object_id)
 #=> 282660

puts object.method(:object_id).call # (Kudos to Ezra)
 #=> 282660
```

**Source:** _gist.github.com_

#### Q33: What is the return value for ... ⭐⭐
**Details:**
For the class `ABC` the given as:

```ruby
class ABC
  def xyz
    puts "xyz in ABC"
  end
end
```

What is the return value for:

*   `ABC::new::xyz`
*   `ABC::new.xyz`
*   `ABC.new::xyz`
*   `ABC.new.xyz`

**Answer:**
All the statements for the invocation of the xyz method through the object are valid.

When run through `IRB`:

```ruby
irb(main):001:0> ABC::new::xyz
xyz in ABC
=> nil
irb(main):002:0> ABC::new.xyz
xyz in ABC
=> nil
irb(main):003:0> ABC.new::xyz
xyz in ABC
=> nil
irb(main):004:0> ABC.new.xyz
xyz in ABC
=> nil
```

**Source:** _toptal.com_

#### Q34: Which of the expressions listed below will result in "false"? ⭐⭐
**Details:**
```ruby
true    ? "true" : "false"
false   ? "true" : "false"
nil     ? "true" : "false"
1       ? "true" : "false"
0       ? "true" : "false"
"false" ? "true" : "false"
""      ? "true" : "false"
[]      ? "true" : "false"
```

**Answer:**
In Ruby, the _only_ values that evaluate to false are `false` and `nil`. _Everything else_ – even zero (0) and an empty array (\[\]) – evaluates to true.

This comes as a real surprise to programmers who have previously been working in other languages like JavaScript.

**Source:** _toptal.com_

#### Q35: Write a function that sorts the keys in a hash by the length of the key as a string. ⭐⭐
**Details:**
For instance, the hash:
```ruby
{ abc: 'hello', 'another_key' => 123, 4567 => 'third' }
```
should result in:
```ruby
["abc", "4567", "another_key"]
```

**Answer:**
As is always true in programming, there are in fact multiple ways to accomplish this.
The most straightforward answer would be of the form:
```ruby
hsh.keys.map(&:to_s).sort_by(&:length)
```    
or:
```ruby
hsh.keys.collect(&:to_s).sort_by { |key| key.length }
```

Alternatively, Ruby’s [`Enumerable` mixin](http://ruby-doc.org/core-2.1.2/Enumerable.html) provides many methods to operate on collections. The key here is to turn the hash keys into a collection, convert them all to strings, then sort the array.

```ruby
def key_sort hsh
   hsh.keys.collect(&:to_s).sort { |a, b| a.length <=> b.length }
end
```

An equivalent call of the [`collect` method](http://www.tutorialspoint.com/ruby/ruby_iterators.htm) is done with the usual block syntax of:

```ruby
collect { |x| x.to_s }
```

**Source:** _toptal.com_

#### Q36: How do you remove `nil` values in array using ruby? ⭐⭐
**Answer:**
`Array#compact` removes `nil` values.

```ruby
>> [nil,123,nil,"test"].compact
=> [123, "test"]
```

**Source:** _toptal.com_

#### Q37: Explain each of the following operators and how and when they should be used ⭐⭐
**Details:**
* `==`
* `===`
* `eql?`
* `equal?`

**Answer:**
* `==` – Checks if the _value_ of two operands are equal (often overridden to provide a class-specific definition of equality).

* `===` – Specifically used to test equality within the `when` clause of a `case` statement (also often overridden to provide meaningful class-specific semantics in case statements).

* `eql?` – Checks if the _value_ and _type_ of two operands are the same (as opposed to the `==` operator which compares values but ignores types). For example, `1 == 1.0` evaluates to `true`, whereas `1.eql?(1.0)` evaluates to `false`.

* `equal?` – Compares the `identity` of two objects; i.e., returns `true` iff both operands have the same object id (i.e., if they both refer to the _same object_). Note that this will return `false` when comparing two identical _copies_ of the same object.


**Source:** _toptal.com_

#### Q38: Can you call a private method outside a Ruby class using its object? ⭐⭐
**Answer:**
Yes, with the help of the `send` method.

Given the class `Test`:
```ruby
class Test
   private
       def method
         p "I am a private method"
      end
end
```
    
We can execute the private method using `send`:

```ruby
>> Test.new.send(:method)
"I am a private method"
```

**Source:** _toptal.com_

#### Q39: What will be the values of ... ⭐⭐
**Details:**
Consider the following code:
```ruby
class A
  def self.a(b)
    if b > 0
      b * b
    end
  end
end
```
What will be the values of:

*   `var1 = A.a(0)`
*   `var2 = A.a(2)`

**Answer:**
*   var1 will be equal to `nil`
*   var2 will be equal to `4`

A conditional statement in Ruby is an expression that returns `nil` if the conditional is `false`.  Ruby methods return the last expression in the method body.

**Source:** _toptal.com_

#### Q40: Describe a closure in Ruby ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q41: When might you use the `do`/`end` syntax versus using the curly bracket syntax for a block?   ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q42: What is an iterator?  ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q43: What are two uses of ranges?   ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q44: What will be the value of ... ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q45: What is the value of the variable "upcased" in the below piece of code? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q46: Why might you want to avoid using string literals within loops?   ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q47: Explain redo vs. retry usage ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q48: What is the difference between `Kernel#require` and `Kernel#load`?   ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q49: How does block invocation differ from method invocation? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q50: Which operator must be defined in order to implement the `Comparable` module?   ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q51: What does a bang `!` at the end of a method signify?   ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q52: What is the difference between `#==` and `#equal?`?  ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q53: Why can you safely use a string as a hash key, even though a string is mutable?  ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q54: Can you tell me the three levels of method access control for classes and modules?  What do they imply about the method? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q55: What is the difference between `#==` and `#eql?`?   ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q56: Explain this ruby idiom: a ||= b ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q57: What does self mean? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q58: What is a Proc? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q59: Why might you want to alias a method?   ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q60: What will val1 and val2 equal after the code below is executed? Explain your answer. ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q61: How is the invocation of a private method different than the invocation of a public method from within its defining class?  ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q62: What is the difference between `throw/catch` and `raise/rescue`?   ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q63: What is the difference between `Module#remove_method` and `Module#undef_method`?   ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q64: What is the difference between `Array#map` and `Array#each`? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q65: What is the difference between calling "super" and calling "super()" ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q66:  What is the main difference between procs and lambdas? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q67: Explain the difference between ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q68: What is the difference between Proc invocation and lambda invocation?   ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q69: What are some disadvantages of a case statement versus repeated `elsif` statements? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q70: What is an eigenclass? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q71: Write a single line of Ruby code that prints the Fibonacci sequence of any length as an array. ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q72: Is a block an object?  ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q73: Is the line of code below valid Ruby code? If so, what does it do? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q74: What will be the result of each of the following lines of code ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q75: What is the primary difference in these two code snippets? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q76: What is the difference between `Object#dup` and `#clone`?   ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q77: How exactly does it work? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q78: What happens to a constant which is not assigned? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q79: When might you encounter a `LocalJumpError`?   ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q80: Is a method an object?   ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q81: Why doesn't Ruby support method overloading? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q82: What happens if a block is passed two arguments but only accepts one argument?   ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q83: What is the difference between `BasicObject#instance_eval` and `BasicObject#instance_exec`? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q84: What is the differnece between `extend` and `include` in ruby? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

## [[⬆]](#toc) <a name=RubyonRails>Ruby on Rails</a> Interview Questions
#### Q1: Explain what is ORM (Object-Relationship-Model) in Rails? ⭐
**Answer:**
ORM or Object Relationship Model in Rails indicate that your classes are mapped to the table in the database, and objects are directly mapped to the rows in the table.

**Source:** _career.guru99.com_

#### Q2: Mention what is Rails Migration? ⭐
**Answer:**
Rails Migration enables Ruby to make changes to the database schema, making it possible to use a version control system to leave things synchronized with the actual code.

**Source:** _career.guru99.com_

#### Q3: Explain what is rake in Rails? ⭐
**Answer:**
**Rake** is a Ruby Make; it is a Ruby utility that substitutes the Unix utility ‘make’, and uses a ‘Rakefile’ and ‘.rake files’ to build up a list of tasks. In Rails, Rake is used for normal administration tasks like migrating the database through scripts, loading a schema into the database, etc.

**Source:** _career.guru99.com_

#### Q4: What Is ORM In Rails? ⭐
**Answer:**
**ORM** tends for Object-Relationship-Model, where Classes are mapped to table in the database, and Objects are directly mapped to the rows in the table.

**Source:** _wisdomjobs.com/_

#### Q5: Explain what is Ruby on Rails? ⭐
**Answer:**
* Ruby: It is an object-oriented programming language inspired by PERL and Python
* Rails: It is a framework used for building web applications

#### Q6: What is the purpose of the resources method in the code snippet below? ⭐⭐
**Details:**
Consider:
```js
resources :posts do
  member do
      get ‘messages’
  end
  collection do
      post ‘bulk_upload'
  end
end
```

**Answer:**
Defining routes with the `resources` method automatically generates routes for the seven standard RESTful actions:

* GET /messages
* POST /messages
* GET /messages/new
* GET /messages/:id/edit
* GET /messages/:id
* PATCH/PUT /messages/:id
* DELETE /messages/:id

**Source:** _upwork.com_

#### Q7: What is the use of load and require in Ruby? ⭐⭐
**Answer:**
* You use `load()` to execute code 
* use `require()` to import libraries.

**Source:** _anilpunjabi.tumblr.com_

#### Q8: List out what can Rails Migration do? ⭐⭐
**Answer:**
Rails Migration can do following things

* Create table
* Drop table
* Rename table
* Add column
* Rename column
* Change column
* Remove column and so on

**Source:** _career.guru99.com_

#### Q9: Mention what is the role of Rails Controller? ⭐⭐
**Answer:**
The Rails **controller** is the logical center of the application. It facilitates the interaction between the users, views, and the model. It also performs other activities like

* It is capable of routing external requests to internal actions. It handles URL extremely well
* It regulates helper modules, which extend the capabilities of the view templates without bulking of their code
* It regulates sessions; that gives users the impression of an ongoing interaction with our applications

**Source:** _career.guru99.com_

#### Q10: Explain how you define Instance Variable, Global Variable and Class Variable in Ruby? ⭐⭐
**Answer:**
* Ruby Instance variable begins with — **@**
* Ruby Class variables begin with — **@@**
* Ruby Global variables begin with — **$**

**Source:** _career.guru99.com_

#### Q11: How Is Visibility Of Methods Changed In Ruby (encapsulation)? ⭐⭐
**Answer:**
By applying the access modifier: 
* Public, 
* Private and 
* Protected

**Source:** _wisdomjobs.com/_

#### Q12: Mention what are the positive aspects of Rails? ⭐⭐
**Answer:**
Rails provides many features like:

* **Meta-programming**: Rails uses code generation but for heavy lifting it relies on meta-programming. Ruby is considered as one of the best language for Meta-programming.
* **Active Record**: It saves object to the database through Active Record Framework. The Rails version of Active Record identifies the column in a schema and automatically binds them to your domain objects using metaprogramming
* **Scaffolding**: Rails have an ability to create scaffolding or temporary code automatically
* **Convention over configuration**: Unlike other development framework, Rails does not require much configuration, if you follow the naming convention carefully
* **Three environments**: Rails comes with three default environment testing, development, and production.
* **Built-in-testing**: It supports code called harness and fixtures that make test cases to write and execute.

**Source:** _career.guru99.com_

#### Q13: What Is The Difference Between Nil And False In Ruby? ⭐⭐
**Answer:**
False is a boolean datatype, Nil is not a data type it have object_id 4.

**Source:** _wisdomjobs.com/_

#### Q14: What Is MVC? And How It Works? ⭐⭐
**Answer:**
**MVC** tends for Model-View-Controller, used by many languages like PHP, Perl, Python etc. The flow goes like this:

Request first comes to the controller, controller finds and appropriate view and interacts with model, model interacts with your database and send the response to controller then controller based on the response give the output parameter to view.

**Source:** _wisdomjobs.com/_

#### Q15: What Are Helpers And How To Use Helpers In ROR? ⭐⭐
**Answer:**
**Helpers** are modules that provide methods which are automatically usable in your view. They provide shortcuts to commonly used display code and a way for you to keep the programming out of your views. The purpose of a helper is to simplify the view.

**Source:** _wisdomjobs.com/_

#### Q16: Mention what are the limits of Ruby on Rails? ⭐⭐
**Answer:**
Ruby on Rails has been designed for creating a CRUD web application using MVC. Some of the features that Rails does not support include:

* Foreign key in databases
* Linking to multiple database at once
* Soap web services
* Connection to multiple database servers at once

**Source:** _career.guru99.com_

#### Q17: How Many Types Of Associations Relationships Does A Model Have? ⭐⭐
**Answer:**
When you have more than one model in your rails application, you would need to create connection between those models. You can do this via associations. Active Record supports three types of associations:

* **one-to-one**: A one-to-one relationship exists when one item has exactly one of another item. For example, a person has exactly one birthday or a dog has exactly one owner.

* **one-to-many**: A one-to-many relationship exists when a single object can be a member of many other objects. For instance, one subject can have many books.

* **many-to-many**: A many-to-many relationship exists when the first object is related to one or more of a second object, and the second object is related to one or many of the first object.

You indicate these associations by adding declarations to your models: 
* has_one, 
* has_many, 
* belongs_to
* has_and_belongs_to_many

**Source:** _wisdomjobs.com/_

#### Q18: Explain what is a class library in Ruby? ⭐⭐
**Answer:**
**Ruby class** libraries consist of a variety of domains, such as thread programming, data types, various domains, etc. These classes give flexible capabilities at a high level of abstraction, giving you the ability to create powerful Ruby scripts useful in a variety of problem domains. The following domains which have relevant class libraries are,

* GUI programming
* Network programming
* CGI Programming
* Text processing

**Source:** _career.guru99.com_

#### Q19: Mention what is the difference in scope for these two variables: @@name and @name? ⭐⭐
**Answer:**
The difference in scope for these two variables is that:

* **@@name** is a class variable
* **@name** is an instance variable

**Source:** _career.guru99.com_

#### Q20: Explain what is the role of sub-directory app/controllers and app/helpers? ⭐⭐
**Answer:**
* App/controllers: A web request from the user is handled by the Controller. The controller sub-directory is where Rails looks to find controller classes
* App/helpers: The helper’s sub-directory holds any helper classes used to assist the view, model and controller classes.

**Source:** _career.guru99.com_

#### Q21: Mention what is the difference between a gem and a plugin in Ruby? ⭐⭐
**Answer:**
* **Gem**: A gem is a just ruby code. It is installed on a machine, and it’s available for all ruby applications running on that machine.
* **Plugin**: Plugin is also ruby code, but it is installed in the application folder and only available for that specific application.

**Source:** _career.guru99.com_

#### Q22: What Do You Mean By Render And Redirect_to? ⭐⭐
**Answer:**
* _render_ causes rails to generate a response whose content is provided by rendering one of your templates. Means, it will direct goes to view page.

* *redirect_to* generates a response that, instead of delivering content to the browser, just tells it to request another url. Means it first checks actions in controller and then goes to view page.

**Source:** _wisdomjobs.com/_

#### Q23: What Are The Various Components Of Rail? ⭐⭐
**Answer:**
1. **Action Pack**: Action Pack is a single gem that contains Action Controller, Action View and Action Dispatch. The "VC" part of "MVC".

 * Action Controller: Action Controller is the component that manages the controllers in a Rails application. The Action Controller framework processes incoming requests to a Rails application, extracts parameters, and dispatches them to the intended action.

 * Action View: Action View manages the views of your Rails application. It can create both HTML and XML output by default. Action View manages rendering templates, including nested and partial templates, and includes built-in AJAX support.

 * Action Dispatch: Action Dispatch handles routing of web requests and dispatches them as you want, either to your application or any other Rack application. Rack applications are a more advanced topic and are covered in a separate guide called Rails on Rack.

2. **Action Mailer**: Action Mailer is a framework for building e-mail services. You can use Action Mailer to receive and process incoming email and send simple plain text or complex multipart emails based on flexible templates.

3. **Active Model**: Active Model provides a defined interface between the Action Pack gem services and Object Relationship Mapping gems such as Active Record. Active Model allows Rails to utilize other ORM frameworks in place of Active Record if your application needs this.

4. **Active Record**: Active Record are like Object Relational Mapping (ORM), where classes are mapped to table, objects are mapped to columns and object attributes are mapped to data in the table.

5. **Active Resource**: Active Resource provides a framework for managing the connection between business objects and RESTful web services. It implements a way to map web-based resources to local objects with CRUD semantics.

6. **Active Support**: Active Support is an extensive collection of utility classes and standard Ruby library extensions that are used in Rails, both by the core code and by your applications.

**Source:** _wisdomjobs.com/_

#### Q24:  Explain what is Rails Active Record in Ruby on Rails? ⭐⭐
**Answer:**
Rails active record is the Object/Relational Mapping (ORM) layer supplied with Rails. It follows the standard ORM model as

* Table map to classes
* Rows map to objects
* Columns map to object attributes

**Source:** _career.guru99.com_

#### Q25: How Many Types Of Relationships Does A Model Has? ⭐⭐
**Answer:**
1. has_one
2. belongs_to
3. has_many
4. has_many :through

**Source:** _wisdomjobs.com/_

#### Q26: What do you mean by the term Scaffolding and what sort of advantages the Ruby can offer when it comes to same? ⭐⭐
**Answer:**
While developing the projects, the users often have to write codes in the early stage of development. These codes help building the application in a very reliable manner and quickly and also, a close eye can be kept on the working of some major components with this approach. In Ruby, the scaffolding is done automatically and the users are free to concentrate on the core development only from the first day of development. 

**Source:** _mindmajix.com_

#### Q27: Practical test: Genres of music ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q28: What is the difference between symbol and string? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q29: What is the use of Destructive Method? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q30: Explain Ruby on Rails Exception Handling ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q31: How should you use nested layouts? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q32: Can you explain the difference between ActiveSupport’s “HashWithIndifferentAccess” and Ruby’s “Hash”? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q33: How does Ruby on Rails use the Model View Controller (MVC) framework? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q34: What is the purpose of the rakefile available in the demo directory in Ruby? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q35: Explain what is Interpolation in Ruby? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q36: What is the difference between &&, || operators and "and, or"? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q37: Explain what is Polymorphic Association in Ruby on Rails? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q38: What Are Filters? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q39: Mention what is the purpose of RJs in Rails? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q40: What Things We Can Define In The Model? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q41: What Is The Difference Between Delete And Destroy? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q42: What Is A Proc? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q43: Mention what is the function of garbage collection in Ruby on Rails? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q44: Mention what is the difference between the Observers and Callbacks in Ruby on Rails? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q45: What exactly are Harnesses and Fixtures in the Ruby? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q46: Mention what is the difference between calling super() and super call? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q47: What are Strong Parameters? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q48: What Do You Mean By Naming Convention In Rails? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q49: Does Ruby Support Single Inheritance/multiple Inheritance Or Both? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q50: Hw would you choose between Belongs_to And Has_one? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q51: What Is The Difference Between "Save" And "Save!"? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q52: What is the difference between content_for and yield? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q53: What Are Filters? And How Many Types Of Filters Are There In Ruby? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q54: What Is The Flash? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q55: How to rollback a specific migration? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q56: How to check if a specific key is present in a hash or not? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q57: Is Rails Scalable? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q58: Explain the difference between Page, Action, Fragment, Low-Level, SQL caching types. ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q59: What is the Difference Between Gem And Plugin? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q60: What is ActiveJob? When should we use it? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q61: How To Find Second Max Element From Database? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q62: What is the difference between string and text in Rails? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q63: How Many Types Of Callbacks Available In Ror? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q64: What is Rack? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q65: What is the best thing which you find about the Ruby on Rail so far? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q66: What sort of problems you have faced with Ruby on Rails and how do you think the same can affect the projects? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q67: What is a Rails engine? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q68: What is Asset Pipeline? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q69: How Do I Find Only Duplicate Entries In A Database Table? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q70: What is Dynamic Finders? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q71: How To Use Two Databases Into A Single Application? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q72: Node.js vs Ruby on Rails. Which would you choose? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

## [[⬆]](#toc) <a name=SOA&RESTAPI>SOA & REST API</a> Interview Questions
#### Q1: What is RESTful Web Services? ⭐
**Answer:**
*Web Services* work on client-server model where client applications can access web services over the network. Web services provide endpoint URLs and expose methods that can be accessed over network through client programs written in java, shell script or any other different technologies. Web services are stateless and doesn’t maintain user session like web applications.

**Source:** _What is a Web Service?_

#### Q2: What is caching? ⭐
**Answer:**
*Caching* refers to storing server response in client itself so that a client needs not to make server request for same resource again and again. A server response should have information about how a caching is to be done so that a client caches response for a period of time or never caches the server response.


**Source:** _tutorialspoint.com_

#### Q3: Which protocol is used by RESTful webservices? ⭐
**Answer:**
RESTful web services make use of HTTP protocol as a medium of communication between client and server.

**Source:** _tutorialspoint.com_

#### Q4: What REST stands for? ⭐
**Answer:**
*REST* stands for *REpresentational State Transfer*. REST is web standards based architecture and uses HTTP Protocol for data communication. It revolves around resource where every component is a resource and a resource is accessed by a common interface using HTTP standard methods. REST was first introduced by Roy Fielding in 2000.

In REST architecture, a REST Server simply provides access to resources and REST client accesses and presents the resources. Here each resource is identified by URIs/ global IDs. REST uses various representations to represent a resource like text, JSON and XML. Now a days JSON is the most popular format being used in web services.

**Source:** _tutorialspoint.com_

#### Q5: What is REST Web Services? ⭐
**Answer:**
*REST* is the acronym for *REpresentational State Transfer.* REST is an architectural style for developing applications that can be accessed over the network. REST architectural style was brought in light by Roy Fielding in his doctoral thesis in 2000.

REST is a stateless client-server architecture where web services are resources and can be identified by their URIs. Client applications can use HTTP GET/POST methods to invoke Restful web services. REST doesn’t specify any specific protocol to use, but in almost all cases it’s used over HTTP/HTTPS. 

When compared to SOAP web services, these are lightweight and doesn’t follow any standard. We can use XML, JSON, text or any other type of data for request and response.

**Source:** _journaldev.com_

#### Q6: Mention what is the difference between AJAX and REST? ⭐⭐
**Answer:**
**Ajax**

* In Ajax, the request are sent to the server by using `XMLHttpRequest` objects. The response is used by the JavaScript code to dynamically alter the current page
* Ajax is a set of technology; it is a technique of dynamically updating parts of UI without having to reload the page
* Ajax eliminates the interaction between the customer and server asynchronously

**REST**

* REST requires the interaction between the customer and server
* REST have a URL structure and a request/response pattern the revolve around the use of resources
* REST is a type of software architecture and a method for users to request data or information from servers
* REST requires the interaction between the customer and server

**Source:** _career.guru99.com_

#### Q7: What are advantages of REST web services? ⭐⭐
**Answer:**
Some of the advantages of REST web services are:

* Learning curve is easy since it works on HTTP protocol
* Supports multiple technologies for data transfer such as text, xml, json, image etc.
* No contract defined between server and client, so loosely coupled implementation.
* REST is a lightweight protocol
* REST methods can be tested easily over browser.

**Source:** _journaldev.com_

#### Q8: What are different HTTP Methods supported in Restful Web Services? ⭐⭐
**Answer:**
Restful web services supported HTTP methods are:
* GET, 
* POST, 
* PUT, 
* DELETE and 
* HEAD.

**Source:** _journaldev.com_

#### Q9: What is WSDL? ⭐⭐
**Answer:**
*WSDL* stands for Web Service Description Language. WSDL is an XML based document that provides technical details about the web service. Some of the useful information in WSDL document are: 
* method name, 
* port types, 
* service end point, 
* binding, 
* method parameters etc.

**Source:** _journaldev.com_

#### Q10: What are different types of Web Services? ⭐⭐
**Answer:**
There are two types of web services:

* **SOAP Web Services**: Runs on SOAP protocol and uses XML technology for sending data.
* **Restful Web Services**: It’s an architectural style and runs on HTTP/HTTPS protocol almost all the time. REST is a stateless client-server architecture where web services are resources and can be identified by their URIs. Client applications can use HTTP GET/POST methods to invoke Restful web services.

**Source:** _journaldev.com_

#### Q11: Mention whether you can use GET request instead of PUT to create a resource? ⭐⭐
**Answer:**
No, you are not supposed to use POST or GET.  GET operations should only have view rights

**Source:** _career.guru99.com_

#### Q12: Mention what are resources in a REST architecture? ⭐⭐
**Answer:**
Resources are identified by logical URLs; it is the key element of a RESTful design.  Unlike, SOAP web services in REST, you view the product data as a resource and this resource should contain all the required information.

**Source:** _career.guru99.com_

#### Q13: What is a Resource in Restful web services? ⭐⭐
**Answer:**
*Resource* is the fundamental concept of Restful architecture. A resource is an object with:
*  a type, 
* relationship with other resources and 
* methods that operate on it. 

Resources are identified with:
* their URI, 
* HTTP methods they support and 
* request/response data type and format of data.

**Source:** _journaldev.com_

#### Q14: Mention some key characteristics of REST? ⭐⭐
**Answer:**
Some key characteristics of REST includes

* REST is stateless, therefore the SERVER has no state (or session data)
* With a well-applied REST API, the server could be restarted between two calls as every data is passed to the server
* Web service mostly uses POST method to make operations, whereas REST uses GET to access resources

**Source:** _career.guru99.com_

#### Q15: What is SOAP? ⭐⭐
**Answer:**
*SOAP* stands for Simple Object Access Protocol. SOAP is an XML based industry standard protocol for designing and developing web services. Since it’s XML based, it’s platform and language independent. So our server can be based on JAVA and client can be on .NET, PHP etc. and vice versa.

**Source:** _journaldev.com_

#### Q16: What are the core components of a HTTP Request? ⭐⭐
**Answer:**
A HTTP Request has five major parts −

*   **Verb** − Indicate HTTP methods such as GET, POST, DELETE, PUT etc.
*   **URI** − Uniform Resource Identifier (URI) to identify the resource on server.
*   **HTTP Version** − Indicate HTTP version, for example HTTP v1.1 .
*   **Request Header** − Contains metadata for the HTTP Request message as key-value pairs. For example, client ( or browser) type, format supported by client, format of message body, cache settings etc.
*   **Request Body** − Message content or Resource representation.

**Source:** _tutorialspoint.com_

#### Q17: What are the advantages of Web Services? ⭐⭐
**Answer:**
Some of the advantages of web services are:

* **Interoperability**: Web services are accessible over network and runs on HTTP/SOAP protocol and uses XML/JSON to transport data, hence it can be developed in any programming language. Web service can be written in java programming and client can be PHP and vice versa.
* **Reusability**: One web service can be used by many client applications at the same time.
* **Loose Coupling**: Web services client code is totally independent with server code, so we have achieved loose coupling in our application.
* **Easy to deploy and integrate**, just like web applications.
* **Multiple service versions** can be running at same time.

**Source:** _journaldev.com_

#### Q18: What is purpose of a URI in REST based webservices? ⭐⭐
**Answer:**
*URI* stands for *Uniform Resource Identifier*. Each resource in REST architecture is identified by its URI. Purpose of an URI is to locate a resource(s) on the server hosting the web service.

A URI is of following format:
```sh
<protocol>://<service-name>/<ResourceType>/<ResourceID>
```

**Source:** _tutorialspoint.com_

#### Q19: Explain the architectural style for creating web API? ⭐⭐
**Answer:**
The architectural style for creating web api are

* HTTP for client server communication
* XML/JSON as formatting language
* Simple URI as the address for the services
* Stateless communication

**Source:** _career.guru99.com_

#### Q20: Mention what are the HTTP methods supported by REST? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q21: What is UDDI? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q22: Define SOA? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q23: What are advantages of SOAP Web Services? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q24: What are disadvantages of SOAP Web Services? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q25: What are disadvantages of REST web services? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q26: What are the best practices to design a resource representation? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q27: Mention what are the different application integration styles? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q28: Mention what is the difference between PUT and POST? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q29: Mention what is the difference between RPC or document style web services? How you determine to which one to choose? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q30: What are the various approaches available for developing SOAP based web services? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q31: What is messaging in RESTful webservices? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q32: What are different ways to test web services? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q33: What are the core components of a HTTP response? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q34: What are the primary security issues of web service? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q35: What is the use of Accept and Content-Type Headers in HTTP Request? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q36: What are the best practices to create a standard URI for a web service? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q37: What is statelessness in RESTful Webservices? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q38: Explain WSDL? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q39: What are the disadvantages of statelessness in RESTful Webservices? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q40:  What is Payload? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q41: What is the purpose of HTTP Status Code? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q42: What are the best practices for caching? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q43: How would you choose between SOAP and REST web services? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q44: What is addressing in RESTful webservices? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q45: Enlist the operation types response used in WSDL? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q46: What should be the purpose of OPTIONS method of RESTful web services? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q47: What are different components of WSDL? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q48: Which type of Webservices methods are to be idempotent? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q49: What do you mean by idempotent operation? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q50: Explain Cache-control header ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q51: What are the important characteristics of SOAP envelope element? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q52: What are the two attributes of <Port> element in WSDL? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q53: Explain <definition> element? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q54: What are the elements of a SOAP message? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q55: Which header of HTTP response provides control over caching? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q56: Explain the message element in WSDL? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q57: What are the different elements of WSDL documents? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q58: What are the advantages of statelessness in RESTful Webservices? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q59: What is difference between SOA and Web Services? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q60: What is difference between Top Down and Bottom Up approach in SOAP Web Services? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q61: Is binding between SOAP and WSDL possible? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q62:  Enlist some important constraints for RESTful web services. ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q63: What are the best practices to be followed while designing a secure RESTful web service? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q64: What is Open API Initiative? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q65: Name some best practices for better RESTful API design ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q66: What should be the purpose of HEAD method of RESTful web services? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

## [[⬆]](#toc) <a name=SQL>SQL</a> Interview Questions
#### Q1: What is PRIMARY KEY? ⭐
**Answer:**
A **PRIMARY KEY** constraint is a unique identifier for a row within a database table. Every table should have a primary key constraint to uniquely identify each row and only one primary key constraint can be created for each table. The primary key constraints are used to enforce entity integrity.

**Source:** _github.com/dhaval1406_

#### Q2: Define a temp table  ⭐
**Answer:**
In a nutshell, a temp table is a temporary storage structure. What does that mean? Basically, you can use a temp table to store data temporarily so you can manipulate and change it before it reaches its destination format.

**Source:** _github.com/dhaval1406_

#### Q3: What is a view? ⭐
**Answer:**
A **view** is simply a virtual table that is made up of elements of multiple physical or “real” tables. Views are most commonly used to join multiple tables together, or control access to any tables existing in background server processes.	

**Source:** _github.com/dhaval1406_

#### Q4: What’s the difference between a local  temp table and a global temp table?  ⭐⭐
**Answer:**
* **Local tables** are accessible to a current user connected to the server. These tables disappear once the user has disconnected from the server. 
* **Global temp** tables, on the other hand, are available to all users regardless of the connection. These tables stay active until all the global connections are closed.

**Source:** _github.com/dhaval1406_

#### Q5: What is blocking? ⭐⭐
**Answer:**
SQL Server blocking occurs when one connection holds a lock on a record and other connection tries to fetch the record or update the record.

**Source:** _github.com/chetansomani_

#### Q6: What is the difference between WHERE clause and HAVING clause? ⭐⭐
**Answer:**
- WHERE clause can only be applied on a static non-aggregated column 
- we will need to use HAVING for aggregated columns.

**Source:** _github.com/dhaval1406_

#### Q7: What is FOREIGN KEY? ⭐⭐
**Answer:**
A **FOREIGN KEY** constraint prevents any actions that would destroy links between tables with the corresponding data values. A foreign key in one table points to a primary key in another table. Foreign keys prevent actions that would leave rows with foreign key values when there are no primary keys with that value. The foreign key constraints are used to enforce referential integrity.

**Source:** _github.com/dhaval1406_

#### Q8: What is Normalization? ⭐⭐
**Answer:**
It is the process of eliminating redundant data and maintaining data dependencies.

**Source:** _github.com/dhaval1406_

#### Q9: How can a column with a default value be added to an existing table? ⭐⭐
**Answer:**
Consider:
```sql
ALTER TABLE SomeTable
        ADD SomeCol Bit NULL --Or NOT NULL.
 CONSTRAINT D_SomeTable_SomeCol --When Omitted a Default-Constraint Name is autogenerated.
    DEFAULT (0)--Optional Default-Constraint.
WITH VALUES --Add if Column is Nullable and you want the Default Value for Existing Records.
```
Keep in mind that if the column is nullable, then null will be the value used for existing rows. 

**Source:** _github.com/chetansomani_

#### Q10: What is DEFAULT? ⭐⭐
**Answer:**
**Default** allows to add values to the column if the value of that column is not set. Default can be defined on number and datetime fields. They cannot be defined on timestamp and IDENTITY columns.

**Source:** _github.com/chetansomani_

#### Q11: What is the difference between inner and outer join? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q12: Discuss INNER JOIN ON vs WHERE clause ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q13: What are the difference between clustered and a non-clustered index? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q14: How do I perform an IF…THEN in an SQL SELECT? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q15: Finding duplicate values in a SQL table ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q16: How does a hash table index work? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q17: What are the advantages of using Stored Procedures? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q18: What is Denormalization? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q19: How to select first 5 records from a table? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q20: Define ACID Properties ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q21: How a database index can help performance? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q22: What is the difference between UNION and UNION ALL?	 ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q23: What is a cursor how does it work? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q24: How do I UPDATE from a SELECT in SQL Server? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q25: What is the difference between “INNER JOIN” and “OUTER JOIN”? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q26: Is table size reduced, when you delete data from the table? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q27: Explain Function vs. Stored Procedure in SQL Server ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q28: What are row constructors? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q29: What is the difference between JOIN and UNION? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q30: What is collation? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q31: Describe the difference between truncate and delete  ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q32: How does B-trees index work? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q33: What are statistics? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q34: How deadlock is resolved? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q35: What is the difference among UNION, MINUS and INTERSECT? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q36: What is a filegroup? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q37: How can I do an UPDATE statement with JOIN in SQL? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q38: How does truncate and delete operation effect Identity? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q39: Explain a usage difference between user defined functions and stored procedures ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q40: What is a linked server? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q41: How can we transpose a table using SQL (changing rows to column or vice-versa) ? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q42: What would happen without an index? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q43: Name types of Triggers ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q44: What are DMV's and DMF's? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q45: What's the difference between a primary key and a unique key? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q46: Delete duplicate values in a SQL table ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q47: What is the cost of having a database index? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q48: How to generate row number in SQL Without ROWNUM ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q49: Explain the difference between exclusive lock and update lock ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q50: Insert results of a stored procedure into a temporary table ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q51: What are some other types of indexes? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q52: Name some disadvantages of a hash index ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q53: How does database indexing work? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q54: How does primary key constraint and unique key constraint effect null? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q55: Select first row in each GROUP BY group (greatest-n-per-group problem)? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q56: What is Optimistic Locking and Pessimistic locking? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

## [[⬆]](#toc) <a name=SoftwareArchitecture>Software Architecture</a> Interview Questions
#### Q1: What defines a software architect? ⭐⭐
**Answer:**
An **architect** is the captain of the ship, making the decisions that cross multiple areas of concern (navigation, engineering, and so on), taking final responsibility for the overall health of the ship and its crew (project and its members), able to step into any station to perform those duties as the need arises (write code for any part of the project should they lose a member). He has to be familiar with the problem domain, the technology involved, and keep an eye out on new technologies that might make the project easier or answer new customers' feature requests.

**Source:** _stackoverflow.com_

#### Q2: Why Do You Need Clustering? ⭐⭐
**Answer:**
*Clustering* is needed for achieving high availability for a server software. The main purpose of clustering is to achieve 100% availability or a zero down time in service. A typical server software can be running on one computer machine and it can serve as long as there is no hardware failure or some other failure. By creating a cluster of more than one machine, we can reduce the chances of our service going un-available in case one of the machine fails.  
  
Doing clustering does not always guarantee that service will be 100% available since there can still be a chance that all the machine in a cluster fail at the same time. However it in not very likely in case you have many machines and they are located at different location or supported by their own resources.  
  

**Source:** _fromdev.com_

#### Q3: Why is it a good idea for “lower” application layers not to be aware of “higher” ones? ⭐⭐
**Answer:**
The fundamental motivation is this: 

_You want to be able to rip an entire layer out and substitute a completely different (rewritten) one, and NOBODY SHOULD (BE ABLE TO) NOTICE THE DIFFERENCE._ 

The most obvious example is ripping the bottom layer out and substituting a different one. This is what you do when you develop the upper layer(s) against a simulation of the hardware, and then substitute in the real hardware.

Also layers, modules, indeed architecture itself, are means of making computer programs easier to understand by humans. 

**Source:** _stackoverflow.com_

#### Q4: What Is A Cluster? ⭐⭐
**Answer:**
A cluster is group of computer machines that can individually run a software. Clusters are typically utilized to achieve high availability for a server software. Clustering is used in many types of servers for high availability.  

*   **App Server Cluster**  
    An app server cluster is group of machines that can run a application server that can be reliably utilized with a minimum of down-time.
*   **Database Server Cluster**  
    An database server cluster is group of machines that can run a database server that can be reliably utilized with a minimum of down-time.

**Source:** _fromdev.com_

#### Q5: What Is Scalability? ⭐⭐
**Answer:**
Scalability is the ability of a system, network, or process to handle a growing amount of load by adding more resources. The adding of resource can be done in two ways  
  

*   **Scaling Up**  
    This involves adding more resources to the existing nodes. For example, adding more RAM, Storage or processing power.
*   **Scaling Out**  
    This involves adding more nodes to support more users.

Any of the approaches can be used for scaling up/out a application, however the cost of adding resources (per user) may change as the volume increases. If we add resources to the system It should increase the ability of application to take more load in a proportional manner of added resources.  
  
An ideal application should be able to serve high level of load in less resources. However, in practical, linearly scalable system may be the best option achievable. Poorly designed applications may have really high cost on scaling up/out since it will require more resources/user as the load increases.  
  

**Source:** _fromdev.com_

#### Q6: What is meant by the KISS principle? ⭐⭐
**Answer:**
**KISS**, a backronym for "keep it simple, stupid", is a design principle noted by the U.S. Navy in 1960. The KISS principle states that most systems work best if they are kept simple rather than made complicated; therefore simplicity should be a key goal in design, and that unnecessary complexity should be avoided.

**Source:** _stackoverflow.com_

#### Q7: What Is Fail Over? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q8: What Is Session Replication? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q9: What Do You Mean By High Availability? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q10: What Is ACID Property Of A System? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q11: What Is Middle Tier Clustering? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q12: How Do You Update A Live Heavy Traffic Site With Minimum Or Zero Down Time? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q13: What does SOLID stand for? What are its principles? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q14: What Is Load Balancing? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q15: How can you keep one copy of your utility code and let multiple consumer components use and deploy it? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q16: Explain the Single Responsibility Principle?  ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q17: "People who like this also like... ". How would you implement this feature in an e-commerce shop? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q18: What Is Sticky Session Load Balancing? What Do You Mean By "Session Affinity"? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q19: What are the DRY and DIE principles? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q20: Is it better to return NULL or empty values from functions/methods where the return value is not present? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q21: Why should you structure your solution by components? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q22: Why layering your application is important? Provide some bad layering example. ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q23: What is actor model in context of a programming language? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q24: Could you provide an example of the Single Responsibility Principle? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q25: Defend the monolithic architecture. ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q26: What Is Sharding? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q27: Explain threads to your grandparents ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q28: How to handle exceptions in a layered application? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q29: What's the difference between principles YAGNI and KISS? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q30: What is GOD class and why should we avoid it? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q31: What Is IP Address Affinity Technique For Load Balancing? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q32: What Is BASE Property Of A System? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q33: Why is writing software difficult? What makes maintaining software hard? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q34: What are heuristic exceptions? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q35: What Is Shared Nothing Architecture? How Does It Scale? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q36: What Does Eventually Consistent Mean? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q37: What Is CAP Theorem? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q38: Are you familiar with The Twelve-Factor App principles? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

## [[⬆]](#toc) <a name=SoftwareTesting>Software Testing</a> Interview Questions
#### Q1: What is profiling? ⭐⭐
**Answer:**
**Profiling **measures how long various parts of the code take to run. Profilers are implemented a lot like debuggers too, except that rather than allowing you to stop the program and poke around, they simply let it run and keep track of how much time gets spent in every part of the program. 

This is particularly useful if you have some code that is running slower than you need it to run, as you can figure out exactly where all the time is going, and concentrate your efforts on fixing just that bottleneck.

**Source:** _stackoverflow.com_

#### Q2: What is the difference between load and stress testing? ⭐⭐
**Answer:**
A **load test** is usually conducted to understand the behaviour of the system under a specific expected load. This load can be the *expected concurrent number of users* on the application performing a specific number of transactions within the set duration. This test will give out the response times of all the important business critical transactions.

A **stress testing** instead is performed to understand the upper limits of capacity within the system. This kind of test is done to determine the system's robustness in terms of *extreme load* and helps application administrators to determine if the system will perform sufficiently if the current load goes well above the expected maximum.

**Source:** _en.wikipedia.org_

#### Q3: What is Load Testing? ⭐⭐
**Answer:**
**Load testing** measures system performance as the workload increases. That workload could mean concurrent users or transactions.The system is monitored to measure response time and system staying power as workload increases. That workload falls within the parameters of normal working conditions.

**Source:** _stackify.com_

#### Q4: Difference between acceptance test and functional test? ⭐⭐
**Answer:**
* **Functional testing**: This is a _verification_ activity; did we build a correctly working product? Does the software meet the business requirements? A functional test verifies that the product actually works as you (the developer) think it does.

* **Acceptance testing**: This is a _validation_ activity; did we build the right thing? Is this what the customer really needs? Acceptance tests verify the product actually solves the problem it was made to solve. This can best be done by the user (customer), for instance performing his/her tasks that the software assists with.

**Source:** _stackoverflow.com_

#### Q5: What is the difference between unit tests and functional tests? ⭐⭐
**Answer:**
* **Unit Test** - testing an individual unit, such as a method (function) in a class, with all dependencies mocked up.

* **Functional Test** - AKA Integration Test, testing a slice of functionality in a system. This will test many methods and may interact with dependencies like Databases or Web Services.

**Source:** _stackoverflow.com_

#### Q6: Name some performance testing steps ⭐⭐
**Answer:**
Some of the performance testing steps are:

* Identify the testing environment
* Identify performance metrics
* Plan and design performance tests
* Configure the test environment
* Implement your test design
* Execute tests
* Analyze, report, retest

**Source:** _stackify.com_

#### Q7: What is Mocking? ⭐⭐
**Answer:**
**Mocking** is primarily used in unit testing. An object under test may have dependencies on other (complex) objects. To isolate the behavior of the object you want to replace the other objects by mocks that simulate the behavior of the real objects. This is useful if the real objects are impractical to incorporate into the unit test.

In short, **mocking **is creating objects that simulate the behavior of real objects.

**Source:** _stackoverflow.com_

#### Q8: What is Endurance Testing? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q9: Explain the purpose of Scalability testing ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q10: Name some performance testing mistakes ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q11: Name most common problems observed in performance testing ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q12: What is Stress Testing? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q13: Name some Performance Testing metrics to measure ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q14: Name some types of performance testing for software ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q15: How would you unit test private methods? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q16: Name some Performance Testing best practices ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q17: What is a reasonable code coverage % for unit tests (and why)? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q18: What's the difference between faking, mocking, and stubbing? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q19: What is Unit test, Integration Test, Smoke test, Regression Test and what are the differences between them?  ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q20: Explain some load testing metrics ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q21: What is Spike Testing? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q22: How to interpret load/stress test metrics? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q23: How do I test a private function or a class that has private methods, fields or inner classes? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q24: Is Unit Testing worth the effort? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q25: Could you name some common Performance Testing fallacies? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q26: Why would you conduct Volume Testing? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

## [[⬆]](#toc) <a name=Spring>Spring</a> Interview Questions
#### Q1: What is Spring? ⭐
**Answer:**
**Spring** is an open source development framework for enterprise Java. The core features of the Spring Framework can be used in developing any Java application, but there are extensions for building web applications on top of the Java EE platform. Spring framework targets to make J2EE development easier to use and promote good programming practice by enabling a POJO-based (Plain Old Java Object) programming model.

**Source:** _tutorialspoint.com_

#### Q2: What is the DispatcherServlet and what is it used for? ⭐⭐
**Answer:**
The `DispatcherServlet` is an implementation of the Front Controller design pattern that handles all incoming web request to a Spring MVC application. A Front Controller pattern (see Enterprise application design pattern) is a common pattern in web applications whose job is to receive all request and route it to different components of the application for actual processing.

In Spring MVC, `DispatcherServlet` is used for finding the correct Controller to process a request, which it does with the help of handler mapping, e.g. the `@RequestMapping` annotation.

**Source:** _stackoverflow.com_

#### Q3: What are benefits of using Spring? ⭐⭐
**Answer:**
Following is the list of few of the great benefits of using Spring Framework:
*   **Lightweight** − Spring is lightweight when it comes to size and transparency. The basic version of spring framework is around 2MB.
*   **Inversion of control (IOC)** − Loose coupling is achieved in spring using the technique Inversion of Control. The objects give their dependencies instead of creating or looking for dependent objects.
*   **Aspect oriented (AOP)** − Spring supports Aspect oriented programming and enables cohesive development by separating application business logic from system services.
*   **Container** − Spring contains and manages the life cycle and configuration of application objects.
*   **MVC Framework** − Spring's web framework is a well-designed web MVC framework, which provides a great alternative to web frameworks such as Struts or other over-engineered or less popular web frameworks.
*   **Transaction Management** − Spring provides a consistent transaction management interface that can scale down to a local transaction (using a single database, for example) and scale up to global transactions (using JTA, for example).
*   **Exception Handling** − Spring provides a convenient API to translate technology-specific exceptions (thrown by JDBC, Hibernate, or JDO, for example) into consistent, unchecked exceptions.

**Source:** _tutorialspoint.com_

#### Q4: What are the different modules in Spring framework? ⭐⭐
**Answer:**
Following are the modules of the Spring framework:

*   Core module
*   Bean module
*   Context module
*   Expression Language module
*   JDBC module
*   ORM module
*   OXM module
*   Java Messaging Service(JMS) module
*   Transaction module
*   Web module
*   Web-Servlet module
*   Web-Struts module
*   Web-Portlet module

**Source:** _tutorialspoint.com_

#### Q5: What are Spring beans? ⭐⭐
**Answer:**
The objects that form the backbone of your application and that are managed by the Spring IoC container are called **beans**. A bean is an object that is instantiated, assembled, and otherwise managed by a Spring IoC container. These beans are created with the configuration metadata that you supply to the container, for example, in the form of XML `<bean/>` definitions.

**Source:** _tutorialspoint.com_

#### Q6: What does a bean definition contain? ⭐⭐
**Answer:**
The bean definition contains the information called configuration metadata which is needed for the container to know the followings −

*   How to create a bean
*   Bean's lifecycle details
*   Bean's dependencies

**Source:** _tutorialspoint.com_

#### Q7: How do you provide configuration metadata to the Spring Container? ⭐⭐
**Answer:**
There are following three important methods to provide configuration metadata to the Spring Container −

*   XML based configuration file.
*   Annotation-based configuration
*   Java-based configuration

**Source:** _tutorialspoint.com_

#### Q8: What is a View and what's the idea behind supporting different types of View? ⭐⭐
**Answer:**
A `View` is an interface in Spring MVC application whose implementations are responsible for rendering context and exposing the _model_. A single view exposes multiple model attributes. Views in Spring MVC can be beans.

They are likely to be instantiated as beans by a `ViewResolver`. As this interface is stateless, view implementations should be thread-safe. By using `ViewResolver`, a logical name of view can be resolved into different types of View implementation, e.g. JstlView for displaying JSP or other view implementations for FreeMarker and Velocity.

**Source:** _dzone.com_

#### Q9: What is the Model?  ⭐⭐
**Answer:**
**Model** is a reference to encapsulate the data or output for rendering. Model is always created and passed to the view in Spring MVC. If a mapped controller method has Model as a method parameter, then a model instance is automatically injected by Spring framework to that method.

**Source:** _dzone.com_

#### Q10: What are ORM's Spring supports? ⭐⭐
**Answer:**
Spring supports the following ORM's:

*   Hibernate
*   iBatis
*   JPA (Java Persistence API)
*   TopLink
*   JDO (Java Data Objects)
*   OJB

**Source:** _tutorialspoint.com_

#### Q11: Explain the _@Controller_ annotation. ⭐⭐
**Answer:**
The _@Controller_ annotation indicates that a particular class serves the role of a controller. Spring does not require you to extend any controller base class or reference the Servlet API.

**Source:** _tutorialspoint.com_

#### Q12: What is Spring MVC framework? ⭐⭐
**Answer:**
The **Spring web MVC framework** provides _model-view-controller_ architecture and ready components that can be used to develop flexible and loosely coupled web applications. The MVC pattern results in separating the different aspects of the application (input logic, business logic, and UI logic), while providing a loose coupling between these elements.

**Source:** _tutorialspoint.com_

#### Q13: What is default scope of bean in Spring framework? ⭐⭐
**Answer:**
The default scope of bean is **Singleton** for Spring framework.

**Source:** _tutorialspoint.com_

#### Q14: How is event handling done in Spring? ⭐⭐
**Answer:**
Event handling in the _ApplicationContext_ is provided through the _ApplicationEvent_ class and _ApplicationListener_ interface. So if a bean implements the _ApplicationListener_, then every time an _ApplicationEvent_ gets published to the ApplicationContext, that bean is notified.

**Source:** _tutorialspoint.com_

#### Q15: What is the purpose of the Core Container module? ⭐⭐
**Answer:**
The core container provides the essential functionality of the Spring framework. A primary component of the core container is the `BeanFactory`, an implementation of the Factory pattern. The `BeanFactory` applies the _Inversion of Control_ (IOC) pattern to separate an application's configuration and dependency specification from the actual application code.

**Source:** _developersbook.com_

#### Q16: What is Application Context? ⭐⭐
**Answer:**
On the surface, an application context is the same as a bean factory. Both load bean definitions, wire beans together, and dispense beans upon request. But it also provides:

*   A means for resolving text messages, including support for internationalization
*   A generic way to load file resources
*   Events to beans that are registered as listeners

**Source:** _developersbook.com_

#### Q17: What do you mean by Bean wiring ? ⭐⭐
**Answer:**
The act of creating associations between application components (beans) within the Spring container is referred to as **Bean wiring**.

**Source:** _developersbook.com_

#### Q18: Do you need spring-mvc.jar in your classpath or is it part of spring-core?  ⭐⭐
**Answer:**
The `spring-mvc.jar` is not part of spring-core, which means that if you want to use Spring MVC framework in your Java project, you must include `spring-mvc.jar` in your application's classpath. In a Java web application, `spring-mvc.jar` is usually placed inside the `/WEB-INF/lib` folder.

**Source:** _stackoverflow.com_

#### Q19: How to integrate  Java Server Faces (JSF) with Spring? ⭐⭐
**Answer:**
JSF and Spring do share some of the same features, most noticeably in the area of IOC services. By declaring JSF managed-beans in the faces-config.xml configuration file, you allow the FacesServlet to instantiate that bean at startup. Your JSF pages have access to these beans and all of their properties.We can integrate JSF and Spring in two ways:

*   **DelegatingVariableResolver:** Spring comes with a JSF variable resolver that lets you use JSF and Spring together. The DelegatingVariableResolver will first delegate value lookups to the default resolver of the underlying JSF implementation, and then to Spring's 'business context' WebApplicationContext. This allows one to easily inject dependencies into one's JSF-managed beans.


<div class="text-center"/>
<img src="http://www.developersbook.com/spring/images/Jsf-Spring.jpg" class="img-fluid" style="max-width: 500px" />
</div>


*   **FacesContextUtils**: custom VariableResolver works well when mapping one's properties to beans in faces-config.xml, but at times one may need to grab a bean explicitly. The FacesContextUtils class makes this easy. It is similar to WebApplicationContextUtils, except that it takes a FacesContext parameter rather than a ServletContext parameter.

```java
ApplicationContext ctx = FacesContextUtils.getWebApplicationContext(FacesContext.getCurrentInstance());
```

**Source:** _developersbook.com_

#### Q20: What is Spring Security? ⭐⭐
**Answer:**
**Spring Security** is a separate module of the Spring framework that focuses on providing authentication and authorization methods in Java applications. It also takes care of most of the common security vulnerabilities such as CSRF attacks.

To use Spring Security in web applications, you can get started with a simple annotation: _@EnableWebSecurity_.

**Source:** _developersbook.com_

#### Q21: What is Spring Boot? ⭐⭐
**Answer:**
**Spring Boot** is a project that provides a pre-configured set of frameworks to reduce boilerplate configuration so that you can have a Spring application up and running with the smallest amount of code.

**Source:** _developersbook.com_

#### Q22: How does the scope _Prototype_ work?** ⭐⭐
**Answer:**
Scope _prototype_ means that every time you call for an instance of the Bean, Spring will create a new instance and return it. This differs from the default _singleton_ scope, where a single object instance is instantiated once per Spring IoC container.

**Source:** _developersbook.com_

#### Q23: Explain _@RequestMapping_ annotation. ⭐⭐
**Answer:**
_@RequestMapping_ annotation is used to map a URL to either an entire class or a particular handler method.

**Source:** _tutorialspoint.com_

#### Q24: What in the world are Spring beans? ⭐⭐
**Answer:**
Spring beans are just object instances that are managed by the Spring container, namely, they are created and wired by the framework and put into a "bag of objects" (the container) from where you can get them later.

The "wiring" part there is what dependency injection is all about, what it means is that you can just say "I will need this thing" and the framework will follow some rules to get you the proper instance.

**Source:** _stackoverflow.com_

#### Q25: What are the types of the transaction management Spring supports? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q26: Why are controllers testable artifacts?  ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q27: What is Aspect? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q28: Is the DispatcherServlet instantiated via an application context? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q29: What are the differences between @RequestParam and @PathVariable? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q30: Describe some of the standard Spring events ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q31: Explain Bean lifecycle in Spring framework ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q32: What is the difference between Bean Factory and ApplicationContext? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q33: What is Bean Factory? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q34: How can you inject Java Collection in Spring? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q35: What is the difference between Bean Factory and Application Context?  ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q36: What is the typical Bean life cycle in Spring Bean Factory Container? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q37: What is bean auto wiring? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q38: How is the right View chosen when it comes to the rendering phase?  ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q39: What is Spring JDBCTemplate class and how to use it? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q40: What is AOP? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q41: What is Controller in Spring MVC framework? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q42: Name some of the Design Patterns used in the Spring Framework? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q43: What is Spring IoC container? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q44: What is the purpose of the session scope? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q45: Explain the difference between spring @Controller and @RestController annotation ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q46: How do you define a bean scope? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q47: What is Spring IoC Container? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q48: Does Spring Bean provide thread safety? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q49: How to handle exceptions in Spring MVC Framework? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q50: How would you relate Spring MVC Framework to MVC architecture? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q51: What is the use of WebClient and WebTestClient? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q52: Can we send an Object as the response of Controller handler method? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q53: How to validate form data in Spring Web MVC Framework? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q54: What do you mean by Auto Wiring?  ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q55: Compare @Component (v2.5) versus @Bean (v 3.0) ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q56: How is an incoming request mapped to a controller and mapped to a method? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q57: Is Spring 5 compatible with older versions of Java? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q58: What are the disadvantages of using Reactive Streams? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q59: What are some of the important Spring annotations you have used? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q60: What is Spring WebFlux? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q61: What’s the difference between @Component, @Controller, @Repository & @Service annotations in Spring? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q62: What is reactive programming? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q63: What are Aspect, Advice, Pointcut, and JoinPoint in AOP? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q64: What are the different types of Advices? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q65: What is Aspect-Oriented Programming? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q66: How does Spring 5 integrate with JDK 9 modularity? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q67: What are some benefits of using Spring Transactions? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q68: What is Spring MVC Interceptor and how to use it? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q69: What is Join point? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q70: What is the difference between concern and cross-cutting concern in Spring AOP? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q71: What is Weaving? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q72: What is the default scope in the web context? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q73: What are the advantages of Spring MVC over Struts MVC ? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q74: What are the limitations with autowiring? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q75: What are different Modes of auto wiring? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q76: What are inner beans in Spring? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q77: What bean scopes does Spring support? Explain them. ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q78: Where does the @Transactional annotation belong? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q79: Can we use both Web MVC and WebFlux in the same application? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q80: What are the Mono and Flux types? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q81: What are some of the best practices for Spring Framework? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q82: What's the difference between @Component, @Repository & @Service annotations in Spring? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q83: I want to know what actually happens when you annotate a method with @Transactional? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q84: Explain the difference between <context:annotation-config> vs <context:component-scan> ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q85: What are some of the valid return types of a controller method?  ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q86: What is the difference between @Inject and @Autowired in Spring Framework? Which one to use under what condition? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q87: How does autowiring work in Spring? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

## [[⬆]](#toc) <a name=Statistics>Statistics</a> Interview Questions
#### Q1: Name three most common ‘averages’ in statistics ⭐
**Answer:**
In the study of statistics, the three most common ‘averages’ in statistics are Mean, Median and Mode.

**Source:** _www.educba.com_

#### Q2: What is Covariance? ⭐
**Answer:**
In covariance two items vary together and it’s a measure that indicates the extent to which two random variables change in cycle. It is a statistical term; it explains the systematic relation between a pair of random variables, wherein changes in one variable reciprocal by a corresponding change in another variable.

**Source:** _www.educba.com_

#### Q3: What is Median? ⭐
**Answer:**
Median is also a way of finding the average of a group of data points. It’s the middle number of a set of numbers. There are two possibilities, the data points can be an odd number group or it can be en even number group.
If the group is odd, arrange the numbers in the group from smallest to largest. The median will be the one which is exactly sitting in the middle, with an equal number on either side of it. If the group is even, arrange the numbers in order and pick the two middle numbers and add them then divide by 2. It will be the median number of that set.

**Source:** _www.educba.com_

#### Q4: What is Mode? ⭐
**Answer:**
The mode is also one of the types for finding the average. A mode is a number, which occurs most frequently in a group of numbers. Some series might not have any mode; some might have two modes which is called bimodal series.

In the study of statistics, the three most common ‘averages’ in statistics are Mean, Median and Mode.

**Source:** _www.educba.com_

#### Q5: What is Standard Deviation (Sigma)? ⭐
**Answer:**
Standard Deviation is a measure of how much your data is spread out in statistics.

**Source:** _www.educba.com_

#### Q6: What is Arithmetic Mean? ⭐
**Answer:**
It is the important technique in statistics. Arithmetic Mean can also be called an average. It is the number or the quantity obtained by summing two or more numbers/variables and then dividing the sum by the number of numbers/variables.

**Source:** _www.educba.com_

#### Q7: Explain about statistics branches? ⭐
**Answer:**
The two main branches of statistics are descriptive statistics and inferential statistics.

**Descriptive statistics** summarises the data from a sample using indexes such as mean or standard deviation. Descriptive Statistics methods include displaying, organising and describing the data.

**Inferential Statistics** draws the conclusions from data that are subject to random variation such as observation errors and sample variation.

**Source:** _www.educba.com_

#### Q8: What is a linear regression in statistics? ⭐
**Answer:**
Linear regression is one of the statistical techniques used in a predictive analysis, this technique will identify the strength of the impact that the independent variables show on dependent variables.

**Source:** _www.educba.com_

#### Q9: What is a Sample in Statistics and list the sampling methods? ⭐
**Answer:**
In a Statistical study, a Sample is a set of or a portion of collected or processed data from a statistical population by a structured and defined procedure, and the elements within the sample are known as a sample point.

Below are the 4 sampling methods:

**Cluster Sampling:** In cluster sampling method the population will be divided into groups or clusters.

**Simple Random:** This sampling method simply follows the pure random division.

**Stratified:** In stratified sampling, the data will be divided into groups or strata.

**Systematical:** Systematical sampling method picks every kth member of the population.

**Source:** _www.educba.com_

#### Q10: What is Correlation? ⭐
**Answer:**
Correlation is considered or described as the best technique for measuring and also for estimating the quantitative relationship between two variables. Correlation measures how strongly two variables are related.

**Source:** _www.educba.com_

#### Q11: What is Regression? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

## [[⬆]](#toc) <a name=T-SQL>T-SQL</a> Interview Questions
#### Q1: Is it possible to rename a database?  If so, how would you rename the database? ⭐
**Answer:**
 *   Yes - Databases can be renamed in similar manners as other relational database objects.
    *   It is possible to rename a database by one of these options:
        *   Issue the sp\_renamedb system stored procedure.
        *   Issue the sp\_rename system stored procedure and specify 'database' as the parameter.
        *   Use Management Studio by right clicking on the database and selecting the 'Rename' option.

**Source:** _mssqltips.com_

#### Q2: Mention what is TOP in TSQL? ⭐
**Answer:**
`TOP` limits the rows returned in a query result set to a specified number of rows or percentage of rows in SQL Server. When TOP is used in combination with the ORDER BY clause, the result set is limited to the first N number of ordered rows. Otherwise, it retrieves the first N number of rows in an undefined order.

**Source:** _educba.com_

#### Q3: What is TSQL Window functions? ⭐⭐
**Answer:**
A window function is a function that's applied to a set of rows defined by a window descriptor and returns a single value for each row from the underlying query. The purpose of the window descriptor is to define the set of rows that the function should apply to. You provide the window specification using a clause called OVER.

```sql
SELECT empid, ordermonth, qty,
  SUM(qty) OVER(PARTITION BY empid
        ORDER BY ordermonth
        ROWS BETWEEN UNBOUNDED PRECEDING
             AND CURRENT ROW) AS runqty
FROM Sales.EmpOrders;
```

**Source:** _docs.microsoft.com_

#### Q4: Name 5 commands that can be used to manipulate text in T-SQL code ⭐⭐
**Answer:**
*   CHARINDEX( findTextData, textData, \[startingPosition\] ) - Returns the starting position of the specified expression in a character string. The starting position is optional.
*   LEFT( character\_expression , integer\_expression ) - Returns the left part of a character string with the specified number of characters.
*   LEN( textData ) - Returns integer value of the length of the string, excluding trailing blanks.
*   LOWER ( character\_expression ) - Returns a character expression after converting uppercase character data to lowercase.
*   LTRIM( textData) - Removes leading blanks. PATINDEX( findTextData, textData ) - Returns integer value of the starting position of text found in the string.
*   REPLACE( textData, findTextData, replaceWithTextData ) - Replaces occurrences of text found in the string with a new value.
*   REPLICATE( character\_expression , integer\_expression ) - Repeats a character expression for a specified number of times.
*   REVERSE( character\_expression ) - Returns the reverse of a character expression.
*   RTRIM( textData) - Removes trailing blanks. SPACE( numberOfSpaces ) - Repeats space value specified number of times.
*   STUFF( textData, start , length , insertTextData ) - Deletes a specified length of characters and inserts another set of characters at a specified starting point.
*   SUBSTRING( textData, startPosition, length ) - Returns portion of the string.
*   UPPER( character\_expression ) - Returns a character expression with lowercase character data converted to uppercase.

**Source:** _mssqltips.com_

#### Q5: Mention what is OFFSET-FETCH filter in tsql? ⭐⭐
**Answer:**
In TSQL `OFFSET-FETCH` filter is designed similar to `TOP` but with an extra element.  It helps to define how many rows you want to skip before specifying how many rows you want to filter.

**Source:** _career.guru99.com_

#### Q6: What are the two commands to remove all of the data from a table?  Are there any implications with the specific commands? ⭐⭐
**Answer:**
* **TRUNCATE** removes all rows from a table. The operation cannot be rolled back and no triggers will be fired. As such, TRUCATE is faster and doesn't use as much undo space as a DELETE.
* The **DELETE** command is used to remove rows from a table. A WHERE clause can be used to only remove some rows. If no WHERE condition is specified, all rows will be removed. After performing a DELETE operation you need to COMMIT or ROLLBACK the transaction to make the change permanent or to undo it. Note that this operation will cause all DELETE triggers on the table to fire.

**Source:** _mssqltips.com_

#### Q7: What are the three ways that Dynamic SQL can be issued? ⭐⭐
**Answer:**
 *   Writing a query with parameters.
 *   Using EXEC.
 *   Using sp\_executesql.

**Source:** _stackoverflow.com_

#### Q8: What are the new error handling commands introduced with SQL Server 2005 and beyond?  ⭐⭐
**Answer:**
*   The new commands are TRY and CATCH.
*   Although they do not directly replace any specific command, in many respects the TRY and CATCH has been used over the RAISERROR command.
*   The TRY block is for the business logic and the CATCH logic is for capturing the error.

**Source:** _mssqltips.com_

#### Q9: Could you explain the difference between Primary Key and Unique Index? ⭐⭐
**Answer:**
The differences between the two are:

* Column(s) that make the Primary Key of a table cannot be NULL since by definition, the Primary Key cannot be NULL since it helps uniquely identify the record in the table. The column(s) that make up the unique index can be nullable. A note worth mentioning over here is that different RDBMS treat this differently –> while SQL Server and DB2 do not allow more than one NULL value in a unique index column, Oracle allows multiple NULL values. That is one of the things to look out for when designing/developing/porting applications across RDBMS.
* There can be only one Primary Key defined on the table where as you can have many unique indexes defined on the table (if needed).
* Also, in the case of SQL Server, if you go with the default options then a Primary Key is created as a clustered index while the unique index (constraint) is created as a non-clustered index. This is just the default behavior though and can be changed at creation time, if needed.

**Source:** _stackoverflow.com_

#### Q10: When should I use primary key or index? ⭐⭐
**Answer:**
Basically, a primary key is (at the implementation level) a special kind of index. Specifically:

* A table can have only one primary key, and with very few exceptions, every table should have one.
* A primary key is implicitly `UNIQUE` - you cannot have more than one row with the same primary key, since its purpose is to uniquely identify rows.
* A primary key can never be `NULL`, so the row(s) it consists of must be NOT NULL

A table can have multiple indexes, and indexes are not necessarily `UNIQUE`. Indexes exist for two reasons:

 - To enforce a uniquness constraint (these can be created implicitly when you declare a column UNIQUE)
 - To improve performance. Comparisons for equality or "greater/smaller than" in WHERE clauses, as well as JOINs, are much faster on columns that have an index. But note that each index decreases update/insert/delete performance, so you should only have them where they're actually needed.

**Source:** _stackoverflow.com_

#### Q11: Explain what are the differences between SQL and T-SQL? ⭐⭐
**Answer:**
* SQL is a query language to operate on sets.
* TSQL is a proprietary procedural language used by Microsoft in SQL Server.

T-SQL adds a number of features that are not available in SQL.

This includes procedural programming elements and a local variable to provide more flexible control of how the application flows. A number of functions were also added to T-SQL to make it more powerful; functions for mathematical operations, string operations, date and time processing, and the like. These additions make T-SQL comply with the Turing completeness test, a test that determines the universality of a computing language. SQL is not Turing complete and is very limited in the scope of what it can do.

Another significant difference between T-SQL and SQL is the changes done to the DELETE and UPDATE commands that are already available in SQL. With T-SQL, the DELETE and UPDATE commands both allow the inclusion of a FROM clause which allows the use of JOINs. This simplifies the filtering of records to easily pick out the entries that match a certain criteria unlike with SQL where it can be a bit more complicated.


**Source:** _educba.com_

#### Q12: Mention what are the limitations of IDENTITY column? ⭐⭐
**Answer:**
The limitations of the IDENTITY column is that column values cannot be updated once generated. Also, it may require to specify this column as a PRIMARY KEY, as such, there is a possibility of duplication of values within a table.  Identity property is applicable for integer based column only.

**Source:** _career.guru99.com_

#### Q13: Mention what is subquery? ⭐⭐
**Answer:**
A subquery is a query that is nested inside a SELECT, INSERT, UPDATE, or DELETE statement, or inside another subquery.

Consider:
```sql
SELECT Ord.SalesOrderID, Ord.OrderDate,
    (SELECT MAX(OrdDet.UnitPrice)
     FROM Sales.SalesOrderDetail AS OrdDet
     WHERE Ord.SalesOrderID = OrdDet.SalesOrderID) AS MaxUnitPrice
FROM Sales.SalesOrderHeader AS Ord;
```

**Source:** _docs.microsoft.com_

#### Q14: In what version of SQL Server were synonyms released, what do synonyms do and when could you make the case for using them? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q15: What are the practical differences between COALESCE() and ISNULL(,'')? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q16: Provide an example of Left Outer Join with Exclusions ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q17: Mention what are the Join Types in TSQL? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q18: Mention what is uncommittable transactions? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q19: What's the difference between TRUNCATE and DELETE in SQL? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q20: What are bitwise operators and what is the value from a database design perspective? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q21: What two commands were released in SQL Server 2005 related to comparing data sets from two or more separate SELECT statements?  ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q22: Mention what are ROLLUP and CUBE in T-SQL? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q23: Is there a difference between T-SQL linked server and a synonym? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q24: How can you delete duplicate records in a table with no primary key? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q25: What are types of XML indexes in SQL Server? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q26: Mention what does the T-SQL command IDENT_CURRENT does? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q27: How can you capture the length of a column when it is a Text, NText and/or Image data type? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q28: What is the difference between EXEC vs sp_executesql? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q29: What do Clustered and Non clustered index actually mean? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q30: What is the use of GO in Transact SQL? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q31: What is the difference between PARTITION BY and GROUP BY ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q32: Is it possible to import data directly from T-SQL commands without using SQL Server Integration Services?  If so, what are the commands? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q33: Is it correct/best practice to have the TRY/CATCH block inside the transaction or should the transaction be inside the TRY block? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q34: From a T-SQL perspective, how would you prevent T-SQL code from running on a production SQL Server? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q35: What are the best practices for using a GUID as a primary key, specifically regarding performance? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q36: What is the native system stored procedure to issue a command against all databases? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

## [[⬆]](#toc) <a name=TypeScript>TypeScript</a> Interview Questions
#### Q1: What is TypeScript and why do we need it? ⭐
**Answer:**
JavaScript is the only client side language universally supported by all browsers. But JavaScript is not the best designed language. It’s not a class-based object-oriented language, doesn’t support class based inheritance, unreliable dynamic typing and lacks in compile time error checking. And TypeScript addresses all these problems. In other words, TypeScript is an attempt to “fix” JavaScript problems.

TypeScript is a free and open source programming language developed and maintained by Microsoft. It is a strict superset of JavaScript, and adds **optional static typing** and **class-based object-oriented programming** to the language. TypeScript is quite easy to learn and use for developers familiar with C#, Java and all strong typed languages. At the end of day “TypeScript is a language that generates plain JavaScript files.”

As stated on [Typescript official website](http://www.typescriptlang.org/), “TypeScript lets you write JavaScript the way you really want to. TypeScript is a typed superset of JavaScript that compiles to plain JavaScript. Any browser. Any host. Any OS. Open Source.” Where “**typed**” means that it considers the types of variables, parameters and functions.

**Source:** _talkingdotnet.com_

#### Q2: What are Modules in Typescript? ⭐
**Answer:**
Modules in Typescript helps in organizing the code. There are 2 types of Modules — Internal and External

* **Internal Modules** are now replaceable by using Typescript’s namespace.

* **External Modules** used to specify and load dependencies between multiple external js files. If there is only one js file used, then external modules are not relevant.

#### Q3:  What is Typescript and why one should use it? ⭐
**Answer:**
TypeScript is a free and open-source programming language developed and maintained by Microsoft. It is a strict syntactical superset of JavaScript, and adds optional static typing and class-based object-oriented programming to the language.

#### Q4: Explain generics in TypeScript ⭐
**Answer:**
Generics are able to create a component or function to work over a variety of types rather than a single one.

```js
/** A class definition with a generic parameter */
class Queue<T> {
  private data = [];
  push = (item: T) => this.data.push(item);
  pop = (): T => this.data.shift();
}

const queue = new Queue<number>();
queue.push(0);
queue.push("1"); // ERROR : cannot push a string. Only numbers allowed

```


**Source:** _basarat.gitbooks.io_

#### Q5: What is TypeScript and why would I use it in place of JavaScript? ⭐
**Details:**



**Answer:**
**TypeScript** is a superset of JavaScript which primarily provides optional static typing, classes and interfaces. One of the big benefits is to enable IDEs to provide a richer environment for spotting common errors as *you type the code*. For a large JavaScript project, adopting TypeScript might result in more robust software, while still being deployable where a regular JavaScript application would run.

In details:
* TypeScript supports new ECMAScript standards and compiles them to (older) ECMAScript targets of your choosing. This means that you can use features of ES2015 and beyond, like modules, lambda functions, classes, the spread operator, destructuring, today. 
* JavaScript code is valid TypeScript code; TypeScript is a superset of JavaScript. 
* TypeScript adds type support to JavaScript. The type system of TypeScript is relatively rich and includes: interfaces, enums, hybrid types, generics, union and intersection types, access modifiers and much more. TypeScript makes typing a bit easier and a lot less explicit by the usage of type inference.
* The development experience with TypeScript is a great improvement over JavaScript. The IDE is informed in real-time by the TypeScript compiler on its rich type information. 
* With strict null checks enabled (`--strictNullChecks` compiler flag) the TypeScript compiler will not allow undefined to be assigned to a variable unless you explicitly declare it to be of nullable type. 
* To use TypeScript you need a build process to compile to JavaScript code. The TypeScript compiler can inline source map information in the generated .js files or create separate .map files. This makes it possible for you to set breakpoints and inspect variables during runtime directly on your TypeScript code. 
* TypeScript is open source (Apache 2 licensed, see github) and backed by Microsoft. *Anders Hejlsberg*, the lead architect of C# is spearheading the project.

**Source:** _stackoverflow.com_

#### Q6: How to call base class constructor from child class in TypeScript? ⭐
**Answer:**
We can call base class constructor using `super()`.

**Source:** _http://www.talkingdotnet.com_

#### Q7: Do we need to compile TypeScript files and why? ⭐
**Answer:**
Yes we do. Typescript is just a language Extension browsers can't interpret it. Converting from TypeScript to JavaScript is called compiling. Compiling doesn't mean binary code is created in this case. For this kind of translation, also the term transpilation is used instead of compilation.

**Source:** _stackoverflow.com_

#### Q8: List the built-in types in Typescript ⭐
**Answer:**
These are also called the primitive types in TypeScript:
* **Number** type: it is used to represent number type values and represents double precision floating point values.
```js
var variable_name: number;
```
* **String** type: it represents a sequence of characters stored as Unicode UTF-16 code. It is the same as JavaScript primitive type.
```js
var variable_name: string;
```
* **Boolean** type: in Typescript, it is used to represent a logical value. When we use the Boolean type, we get output only in true or false. It is also the same as JavaScript primitive type.
```js
var variable_name: bool;
```
* **Null** type: it represents a null literal and it is not possible to directly reference the null type value itself.
```js
var variable_name:number = null;
```
* **Undefined** type: it is the type of undefined literal. This type of built-in type is the sub-type of all the types.
```js
var variable_name:number = undefined;
```


#### Q9: What are the benefits of TypeScript? ⭐
**Answer:**
TypeScript has following benefits.

*   It helps in code structuring.
*   Use class based object oriented programming.
*   Impose coding guidelines.
*   Offers type checking.
*   Compile time error checking.
*   Intellisense.

**Source:** _talkingdotnet.com_

#### Q10: What are the difference beetween Typescript and JavaScript? ⭐⭐
**Answer:**
* It is an object oriented programming language (not pure).
* Here it is static typing (We can declare a variable in multiple ways). ex: var num : number.
* It has interfaces.
* It has optional parameter feature.
* It has Rest Parameter feature.
* Supports generics.
* Supports Modules
* Number, string etc. are the interfaces.


#### Q11: What is Interface in TypeScript? ⭐⭐
**Answer:**
One of TypeScript’s core principles is that type-checking focuses on the *shape* that values have.

An `interface` is a virtual structure that only exists within the context of TypeScript. The TypeScript compiler uses interfaces solely for type-checking purposes.

When you define your interface you’re saying that any object (not an instance of a class) given this contract must be an object containing interfaces properties.

**Source:** _medium.com_

#### Q12: When to use interfaces and when to use classes in TypeScript? ⭐⭐
**Answer:**
If you need/wish to create an instance of perhaps a custom object, whilst getting the benefits of type-checking things such as arguments, return types or generics - a class makes sense. 

If you’re not creating instances - we have interfaces at our disposal, and their benefit comes from not generating any source code, yet allowing us to somewhat “virtually” type-check our code.

**Source:** _toddmotto.com_

#### Q13: Which object oriented terms are supported by TypeScript? ⭐⭐
**Answer:**
TypeScript supports following object oriented terms:

*   Modules
*   Classes
*   Interfaces
*   Data Types
*   Member functions

**Source:** _http://www.talkingdotnet.com_

#### Q14: What is getters/setters in TypeScript? ⭐⭐
**Answer:**
TypeScript supports **getters/setters** as a way of intercepting accesses to a member of an object. This gives you a way of having finer-grained control over how a member is accessed on each object.

```js
class foo {
  private _bar:boolean = false;

  get bar():boolean {
    return this._bar;
  }
  set bar(theBar:boolean) {
    this._bar = theBar;
  }
}

var myBar = myFoo.bar;  // correct (get)
myFoo.bar = true;  // correct (set)
```

**Source:** _typescriptlang.org_

#### Q15: Does TypeScript support all object oriented principles? ⭐⭐
**Answer:**
The answer is **YES**. There are 4 main principles to Object Oriented Programming: 

* Encapsulation, 
* Inheritance, 
* Abstraction, and 
* Polymorphism. 

TypeScript can implement all four of them with its smaller and cleaner syntax.

**Source:** _jonathanmh.com_

#### Q16: How could you check null and undefined in TypeScript? ⭐⭐
**Answer:**
Just use:
```js
if (value) {
}
```
It will evaluate to `true` if `value` is not:

* `null`
* `undefined`
* `NaN`
* empty string `''`
* `0`
* `false`

TypesScript includes JavaScript rules.


**Source:** _stackoverflow.com_

#### Q17: How to implement class constants in TypeScript? ⭐⭐
**Answer:**
In TypeScript, the `const` keyword cannot be used to declare class properties. Doing so causes the compiler to an error with "A class member cannot have the 'const' keyword." TypeScript 2.0 has the `readonly` modifier:

```js
class MyClass {
    readonly myReadonlyProperty = 1;

    myMethod() {
        console.log(this.myReadonlyProperty);
    }
}

new MyClass().myReadonlyProperty = 5; // error, readonly
```

**Source:** _stackoverflow.com_

#### Q18: Could we use TypeScript on backend and how? ⭐⭐
**Answer:**
Typescript doesn’t only work for browser or frontend code, you can also choose to write your backend applications. For example you could choose Node.js and have some additional type safety and the other abstraction that the language brings.

1. Install the default Typescript compiler  

```sh
npm i -g typescript
```
2. The TypeScript compiler takes options in the shape of a tsconfig.json file that determines where to put built files and in general is pretty similar to a babel or webpack config.

```sh
{
  "compilerOptions": {
    "target": "es5",
    "module": "commonjs",
    "declaration": true,
    "outDir": "build"
  }
}
```
3. Compile ts files

```sh
tsc
```
4. Run

```js
node build/index.js
```

**Source:** _jonathanmh.com_

#### Q19: What is the difference between Classes and Interfaces in Typescript? ⭐⭐
**Answer:**
We use classes as object factories. A class defines a blueprint of what an object should look like and act like and then implements that blueprint by initialising class properties and defining methods. Classes are present throughout all the phases of our code.

Unlike classes, an interface is a virtual structure that only exists within the context of TypeScript. The TypeScript compiler uses interfaces solely for type-checking purposes. Once code is transpiled to its target language, it will be stripped from interfaces.

A class may define a factory or a singleton by providing initialisation to its properties and implementation to its methods, an interface is simply a structural contract that defines what the properties of an object should have as a name and as a type.

**Source:** _toddmotto.com_

#### Q20: What is "Decorators" in TypeScript? ⭐⭐
**Answer:**
A *Decorator* is a special kind of declaration that can be attached to a class declaration, method, accessor, property, or parameter. Decorators are functions that take their target as the argument. With decorators we can run arbitrary code around the target execution or even entirely replace the target with a new definition.

There are 4 things we can decorate in ECMAScript2016 (and Typescript): constructors, methods, properties and parameters. 

**Source:** _www.sparkbit.pl_

#### Q21: What is a TypeScript Map file? ⭐⭐
**Answer:**
`.map` files are source map files that let tools map between the emitted JavaScript code and the TypeScript source files that created it. Many debuggers (e.g. Visual Studio or Chrome's dev tools) can consume these files so you can debug the TypeScript file instead of the JavaScript file.

**Source:** _stackoverflow.com_

#### Q22: What's wrong with that code? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q23: What are different components of TypeScript? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q24: Is that TypeScript code valid? Explain why. ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q25: What is Typings in Typescript? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q26: How To Use external plain JavaScript Libraries in TypeScript? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q27: How TypeScript is optionally statically typed language? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q28: Are strongly-typed functions as parameters possible in TypeScript? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q29: What is the default access modifier for members of a class in TypeScript? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q30: How can you allow classes defined in a module to accessible outside of the module? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q31: Explain how and why we could use property decorators in TS? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q32: Does TypeScript supports function overloading? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q33: Explain why that code is marked as WRONG? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q34: What is the difference between "interface vs type" statements? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q35: How would you overload a class constructor in TypeScript? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q36: What is one thing you would change about TypeScript? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q37: Explain when to use "declare" keyword in TypeScript ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q38: What are Ambients in TypeScripts and when to use them? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q39: Is it possible to generate TypeScript declaration files from JS library? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

## [[⬆]](#toc) <a name=UXDesign>UX Design</a> Interview Questions
#### Q1: Name some basic design elements ⭐
**Answer:**
The elements of design are:

* **LINE** – The linear marks made with a pen or brush or the edge created when two shapes meet.
* **SHAPE** – A shape is a self contained defined area of geometric (squares and circles), or organic (free formed shapes or natural shapes). A positive shape automatically creates a negative shape.
* **DIRECTION** – All lines have direction – Horizontal, Vertical or Oblique. Horizontal suggests calmness, stability and tranquillity. Vertical gives a feeling of balance, formality and alertness. Oblique suggests movement and action
* **SIZE** – Size is simply the relationship of the area occupied by one shape to that of another.
* **TEXTURE** – Texture is the surface quality of a shape – rough, smooth, soft hard glossy etc.
* **COLOUR** – Colour is light reflected off objects. Color has three main characteristics: hue or its name (red, green, blue, etc.), value (how light or dark it is), and intensity (how bright or dull it is).

<div class="text-center">
<img src="http://www.j6design.com.au/wp-content/uploads/2014/02/designelements-1024x640.jpg" class="img-fluid" style="max-width: 500px;"/>
</div>

**Source:** _j6design.com.au_

#### Q2: What is User Centered Design? ⭐⭐
**Answer:**
**User-centered design** is an iterative design process in which designers focus on the users and their needs in each phase of the design process. UCD calls for involving users throughout the design process via a variety of research and design techniques so as to create highly usable and accessible products for them.

User-centered design demands that designers employ a mixture of *investigative* (e.g., surveys and interviews) and *generative* (e.g., brainstorming) methods and tools to develop an understanding of user needs.

**Source:** _interaction-design.org_

#### Q3: What is User Research? ⭐⭐
**Answer:**
User research is conducted so as to understand users’ characteristics, aims, and behaviors towards achieving these aims. Its purpose is to produce designs that improve their working practices and lives. User research also involves the continuous evaluation of the impact of designs on the users, not only during the design and development phase but after long-term use, too.

**Source:** _interaction-design.org_

#### Q4: Name some UX Design tools you prefer to work with ⭐⭐
**Answer:**
Just to name a few: 

* Adobe XD, 
* Figma,
* Invision studio
* Sketch
* Balsamiq

**Source:** _uxplanet.org_

#### Q5: Is UX design UI design? What’s the difference? ⭐⭐
**Answer:**
User interface (UI) design is not the same as UX design. A seasoned UX design pro understands the vital difference and is able to articulate it clearly. Designing for the user interface often plays an important role in the work of a UX designer, but it is not the only function.

Whereas UI design is concerned with the effective layout of visual elements on a user interface, UX design is ‘people first.’ It’s about what motivates them—how they think and behave.

A great UX designer should be able to demonstrate knowledge describing the differences, in particular how UI design is only one slice of the UX design process ‘pie’, and only one of many different disciplines that reside under the UX banner. These include, but are not limited to: a user-centered design strategy, core user demographic definition, persona creation, user research, information architecture, content strategy, interaction design, visual design and usability testing.

**Source:** _toptal.com_

#### Q6: What is Graphic Design? ⭐⭐
**Answer:**
**Graphic designers** work with graphical images, whether they be illustrations, typography, or images, and on a variety of media including print and web. Graphic design is typically rendered in 2D — printed on a physical surface or displayed on a screen but not limited to 2D.

As a graphic designer, you can specialize in the following

* Logo design
* Brand design
* Print Designer

**Source:** _uxplanet.org_

#### Q7: What is Interaction Design? ⭐⭐
**Answer:**
Interaction designers, focus on digital products and interactive software design. **Interaction design** helps humans experience or manipulate software or interface with screen-based hardware in order to achieve specific goals — checking email, withdrawing money from an ATM, or “Liking” a webpage.

Interaction design is heavily focused on satisfying the needs and desires 
of the people who will use the product.

Interaction design can be broken down into two parts or the same whole

* **UI Design** — User interface design
* **UX Design** — User experience design

**Source:** _uxplanet.org_

#### Q8: Describe what User Interface (UI) Design does mean for you? ⭐⭐
**Answer:**
**User Interface (UI) design** is the design of software or websites with the focus on the user’s experience and interaction. The goal of user interface design is to make the user’s interaction as simple and efficient as possible. Good user interface design puts emphasis on *goals* and *completing tasks*, and good UI design never draws more attention to itself than enforcing user goals.

**Source:** _uxplanet.org_

#### Q9: What does the term "design-thinking" mean to you? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q10: What is Industrial Design? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q11: Name some goals of UX Design ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q12: Name fundamental principles of design ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q13: Name a main difference Between UX And UI Design ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

## [[⬆]](#toc) <a name=Vue.js>Vue.js</a> Interview Questions
#### Q1: How to create an instance of Vue.js? ⭐
**Answer:**
Every Vue application starts by creating a new Vue instance with the Vue function:

```js
var vm = new Vue({
  // options
})
```

**Source:** _onlineinterviewquestions.com_

#### Q2: What is Vue.js? ⭐
**Answer:**
The **Vue.js** is a progressive JavaScript framework and used to building the interactive user interfaces and also it’s focused on the view layer only (front end). The  **Vue.js**  was developed by “**Evan You**”, an Ex Google software engineer. The latest version is Vue.js 2. The Vue.js 2 is very similar to Angular because Evan You was inspired by Angular.

#### Q3: What is Vue.js? ⭐
**Answer:**
**Vue js** is progressive javascript script used to create dynamic user interfaces.Vue js is very easy to learn.In order to work with Vue js you just need to add few dynamic features to a website.You don’t need to install any thing to use Vue js just need add Vue js library in your project.

**Source:** _onlineinterviewquestions.com_

#### Q4: How to use local storage with Vue.js? ⭐⭐
**Answer:**
You can just do following:

```js
localStorage.setItem('YourItem', response.data)
localStorage.getItem('YourItem')
localStorage.removeItem('YourItem')
```

**Source:** _stackoverflow.com_

#### Q5: How to create Two-Way Bindings in Vue.js? ⭐⭐
**Answer:**
`v-model` directive is used to create Two-Way Bindings in Vue js.In Two-Way Bindings data or model is bind with DOM and Dom is binded back to model.

In below example you can see how Two-Way Bindings is implemented.

```html
<div id="app">
  {{message}}
  <input v-model="message">
</div>
<script type="text/javascript">
  var message = 'Vue.js is rad';
  new Vue({ el: '#app', data: { message } });
</script>
```

**Source:** _onlineinterviewquestions.com_

#### Q6: What are filters in Vue.js? ⭐⭐
**Answer:**
In Vue js filters are used to transform the output that are going to rendered on browser.

A Vue.js filter is essentially a function that takes a value, processes it, and then returns the processed value. In the markup it is denoted by a single pipe (|) and can be followed by one or more arguments:

```html
<element directive="expression | filterId \[args...\]"></element>
```

**Source:** _onlineinterviewquestions.com_

#### Q7: What are components props? ⭐⭐
**Answer:**
Every component instance has its own isolated scope. This means you cannot (and should not) directly reference parent data in a child component’s template. Data can be passed down to child components using **props**. Props are custom attributes you can register on a component. When a value is passed to a prop attribute, it becomes a property on that component instance.

```js
Vue.component('blog-post', {
  // camelCase in JavaScript
  props: ['postTitle'],
  template: '<h3>{{ postTitle }}</h3>'
})
```

**Source:** _stackoverflow.com_

#### Q8: How to deploy Vue.js app? ⭐⭐
**Answer:**
If you've created your project like this:
```sh
vue init webpack myproject
```
Now you can run
```sh
npm run build
```
Then copy index.html and /dist/ folder into your website root directory. Done.

**Source:** _stackoverflow.com_

#### Q9: What are Components in Vue.js? ⭐⭐
**Answer:**
*Components* are one of most powerful features of Vue js.In Vue components are custom elements that help extend basic HTML elements to encapsulate reusable code.

Following is the way to register a Vue component inside another component:
```js
export default {
  el: '#your-element'
  components: {
      'your-component'
  }
}
```

**Source:** _onlineinterviewquestions.com_

#### Q10: What are Directives in Vue.js, List some of them you used? ⭐⭐
**Answer:**
The concept of directive in Vue js is drastically simpler than that in Angular. Vue.js directives provides a way to extend HTML with new attributes and tags. Vue.js has a set of built-in directives which offers extended functionality to your applications.You can also write your custom directives in Vue.js .

Below are list of commonly used directives in Vue.js

*   v-show
*   v-if
*   v-model
*   v-else
*   v-on

**Source:** _onlineinterviewquestions.com_

#### Q11: What is filters in Vue.js? ⭐⭐
**Answer:**
Vue.js allows you to define **filters** that can be used to apply common text formatting. Filters are usable in two places: mustache interpolations and v-bind expressions (the latter supported in 2.1.0+). Filters should be appended to the end of the JavaScript expression, denoted by the “pipe” symbol:

```html
<!-- in mustaches -->
{{ message | capitalize }}

<!-- in v-bind -->
<div v-bind:id="rawId | formatId"></div>
```

**Source:** _stackoverflow.com_

#### Q12: List some features of Vue.js ⭐⭐
**Answer:**
Vue js comes with following features

*   Templates
*   Reactivity
*   Components
*   Transitions
*   Routing

**Source:** _onlineinterviewquestions.com_

#### Q13: How can you redirect to another page in Vue.js? ⭐⭐
**Answer:**
If you are using  `vue-router`, you should use  `router.go(path)`  to navigate to any particular route. The router can be accessed from within a component using  `this.$router`.  `router.go()`  changed in VueJS 2.0. You can use  `router.push({ name: "yourroutename"})`or just  `router.push("yourroutename")`  now to redirect. 


#### Q14: Can I pass parameters in computer properties in Vue.js? ⭐⭐
**Answer:**
You can use a _method_ or _computed function_.

The method way:

```js
<span>{{ fullName('Hi') }}</span>

methods: {
  fullName(salut) {
      return `${salut} ${this.firstName} ${this.lastName}`
  }
}
```
Computed property with a parameter way:

```js
computed: { 
	fullName() {
		return salut => `${salut} ${this.firstName} 		
		 ${this.lastName}`
    }
}
```

#### Q15: Explain the basic logical Vue.js app organisation ⭐⭐
**Answer:**
A **Vue.js application** consists of a root Vue instance created with new Vue, optionally organized into a tree of nested, reusable components. For example, a todo app’s component tree might look like this:

```sh
Root Instance
└─ TodoList
   ├─ TodoItem
   │  ├─ DeleteTodoButton
   │  └─ EditTodoButton
   └─ TodoListFooter
      ├─ ClearTodosButton
      └─ TodoListStatistics
```
All Vue components are also Vue instances.

**Source:** _vuejs.org_

#### Q16: What are the Advantages/Disadvantages of Vuejs? ⭐⭐
**Answer:**
**Vue.js Advantages**
- Easy for applications and interfaces development
- Support Two-way communication as like AngularJs
- Ability to control the states
- Natural thought process

**Vue.js** **Disadvantages**
- Limited scope
- Single creator
- Small developer community

#### Q17: Explain the differences between one-way data flow and two-way data binding? ⭐⭐
**Answer:**
In one-way data flow the view(UI) part of application does not updates automatically when data Model is change  we need to write some custom code to make it updated every time a data model is changed. In Vue js **v-bind** is used for one-way data flow or binding.

In two-way data binding the view(UI) part of application automatically updates when data Model is changed.  In Vue.js **v-model** directive is used for two way data binding.

**Source:** _onlineinterviewquestions.com_

#### Q18: How can I fetch query parameters in Vue.js? ⭐⭐
**Answer:**
You have access to a `$route` object from your components, that expose what we need.

```js    
//from your component
console.log(this.$route.query.test)
```

**Source:** _stackoverflow.com_

#### Q19: List type of Directive are available in Vue.js. ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q20: How to loop in Vue.js? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q21: What is the difference v-bind and v-model? Provide some code example. ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q22: How to call function on child component on parent events? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q23: List some benefits of Vue.js ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q24: How to pass an argument to Vue.js filters? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q25: How can you prevent layout jumps in Vue.js? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q26: How to use Gulp with Vue.js? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q27: Can you force Vue.js to reload/rerender? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q28: Are there any drawback of Vue.js you know? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q29: How can you bind styles in Vue.js? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q30: Could you listen for components props changes? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q31: What's the equivalent of Angular Service in Vue.js? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q32: What is Vuex? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q33: How to save new value to data variables in Vue.js whenever the user types? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q34: How to implement simple routing in Vue.js (without external library)? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q35: List some types of components communication channels in Vue.js app ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q36: How can I watch an array length using Vue.js? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q37: Why we need Vue.js mixins? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q38: What is the best way to create a constant, that can be accessible from entire application in VueJs ? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q39: What is the main difference between a method and a computed value in Vue.js? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q40: What is a proper way to communicate between sibling components in vuejs 2.0? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q41: How do you toggle a class in Vue.js? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

## [[⬆]](#toc) <a name=WCF>WCF</a> Interview Questions
#### Q1: What is WCF? ⭐
**Answer:**
**Windows Communication Foundation (WCF)** is a framework for building service-oriented applications. Using WCF, you can send data as asynchronous messages from one service endpoint to another. A service endpoint can be part of a continuously available service hosted by IIS, or it can be a service hosted in an application. An endpoint can be a client of a service that requests data from a service endpoint. The messages can be as simple as a single character or word sent as XML, or as complex as a stream of binary data.

**Source:** _docs.microsoft.com_

#### Q2: Could you name basic WCF service components? ⭐⭐
**Answer:**
Have a look at this mindmap to navigate yourself through WCF service components:
<div class="text-center">
<img src="http://1.bp.blogspot.com/_ilf9yT58u-k/R5dVNShe9nI/AAAAAAAAACM/jvIaKFVrU8g/s1600/Windows+Communication+Foundation+Mindmap.png" class="img-fluid"/>
</div>


**Source:** _codeproject.com_

#### Q3: What are WCF Service Endpoints? ⭐⭐
**Answer:**
All communication with a Windows Communication Foundation (WCF) service occurs through the **endpoints** of the service. Endpoints provide clients access to the functionality offered by a WCF service.

A **WCF service** endpoint has three basic elements, i.e. `Address`, `Binding` and `Contract` (ABC).

*   **Address**: It defines "WHERE". `Address` is the URL that identifies the location of the service.
*   **Binding**: It defines "HOW". `Binding` defines how the service can be accessed.
*   **Contract**: It defines "WHAT". `Contract` identifies what is exposed by the service.

**Source:** _codeproject.com_

#### Q4: What is a service contract in WCF? ⭐⭐
**Answer:**
A **service contract** defines the operations which are exposed by the service to the outside world. A service contract is the interface of the WCF service and it tells the outside world what the service can do. It may have service-level settings, such as the name of the service and namespace for the service.

```csharp
[ServiceContract]
interface IMyContract { 
    [OperationContract]
	string MyMethod();
}

class MyService: IMyContract {
	public string MyMethod() {
		return "Hello World";
	}
}
```

**Source:** _dotnettricks.com_

#### Q5: Explain what is SOA? ⭐⭐
**Answer:**
**SOA** stands for **service-oriented architecture. Service Oriented Architecture is an architectural approach in software development where the application is organized as "Services". Services are a group of methods that contain the business logic to connect a DB or other services. For instance you go to a hotel and order food. Your order first goes to the counter and then it goes to the kitchen where the food is prepared and finally the waiter serves the food. 

**Some important characteristics of Service Oriented Architecture**

*   SOA services should be **independent** of other services.  Altering a service should not affect the client calling the service.  
*   Services should be **self-contained. **  Services should be able to **define themselves** (in the Web Service Description Language (WSDL)).  It should be able to tell the client what all of the operations it does, what are all the data types it uses and what kind of value it will return.

**Source:** _c-sharpcorner.com_

#### Q6: What are the features and advantage of WCF? ⭐⭐
**Answer:**
Features of WCF**  
  
Windows Communication Foundation (WCF) is a secure, reliable, and scalable messaging platform for the .NET Framework 3.0,

*   Service Orientation
*   Interoperability
*   Multiple Message Patterns
*   Service Metadata
*   Data Contracts
*   Security
*   Multiple Transports and Encodings
*   Reliable and Queued Messages
*   Durable Messages
*   Transactions
*   AJAX and REST Support
*   Extensibility

**Advantages of WCF**:

1.  Service Oriented
2.  Location Independent
3.  Language Independent
4.  Platform Independent
5.  Support Multiple operation
6.  WCF can maintain transaction like COM+ Does
7.  It can maintain state
8.  It can control concurrency
9.  It can be hosted on IIS, WAS, Self hosting, Windows services.

**Source:** _docs.microsoft.com_

#### Q7: Provide some scenarios when we could use WCF services ⭐⭐
**Answer:**
A few sample scenarios include:

* A secure service to process business transactions.
* A service that supplies current data to others, such as a traffic report or other monitoring service.
* A chat service that allows two people to communicate or exchange data in real time.
* A dashboard application that polls one or more services for data and presents it in a logical presentation.
* Exposing a workflow implemented using Windows Workflow Foundation as a WCF service.
* A Silverlight application to poll a service for the latest data feeds.

While creating such applications was possible prior to the existence of WCF, WCF makes the development of endpoints easier than ever. In summary, WCF is designed to offer a manageable approach to creating Web services and Web service clients.

**Source:** _docs.microsoft.com_

#### Q8: What is an Operation Contract in WCF? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q9: What is WCF Data Contract? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q10: Why we need Fault Contracts in WCF? Why not just use error codes? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q11: What is meant by WS-*? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q12: What is transport in WCF? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q13: Name some different types of contracts in WCF ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q14: When DataContract and ServiceContract should be used in an application ? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q15: What is WCF Binding and how many of them do you know? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q16: Explain the difference between WCF vs ASP.NET Web API? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q17: What are the differences between WCF and ASMX Web Services? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q18: What are the Possible Ways of Hosting a WCF Service?  ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q19: Explain WCF Message exchange Pattern ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q20: What is Message Contract in WCF? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q21: Why we need Streaming? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q22: When would we use binary encoder? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q23: When would you use Duplex WCF service? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q24: Can I use MessageContract instead of DataContract or in complement to DataContract? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q25: Will it make any difference if I change the operation contract of methods having no return value by [OperationContract (IsOneWay=true)]? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q26: What is interoperability and how is it achieved with WCF services? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q27: Explain Message Encoding in WCF and when to use one? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q28: Could we use WSHttpBinding with Request-CallBack (also called Duplex) exchange pattern? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q29: Explain Binary vs MTOM vs Streaming in WCF? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q30: What is the difference between hosting WCF service on IIS, Windows Service and self-hosted app? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q31: What is the main difference between Request-Response and Duplex in WCF Message Exchange Pattern? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q32: Should I use WCF or raw sockets? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q33: What replaces WCF in .Net Core? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

## [[⬆]](#toc) <a name=WPF>WPF</a> Interview Questions
#### Q1: What is XAML in WPF and why do we need it? ⭐
**Answer:**
XAML is a XML file which represents your WPF UI. The whole point of creating the UI representation in XML was write once and run it anywhere. So the same XAML UI can be rendered as windows application with WPF and the same UI can be displayed on the browser using WPF browser or Silverlight application.

**Source:** _c-sharpcorner.com_

#### Q2: What is WPF? ⭐
**Answer:**
**WPF** stands for Windows Presentation Foundation. It's a re-invention of a UI for Desktop applications using WPF. Apart from dropping controls on "**Windows Forms**" just as developers have been doing for years, WPF provides an extra rapid boost to the application development including Rich User Interface, Animation and much more.

In a nutshell the following things can be done using WPF:

*   Draw normal controls and graphics.
*   Can easily load/play audio and video files.
*   Can provide smooth graphical effects such as drop shadows and color gradients.
*   Can use shared styles which can be used across the same controls to provide the same theme, skin and design.
*   Transforming objects including shapes, controls and video.
*   Can create and animate 3D graphics.
*   Can easily draw vector graphics that scale without jagged aliasing.

**Advantages**

*   Tight multimedia integration
*   Resolution independence
*   Hardware acceleration

**Source:** _c-sharpcorner.com_

#### Q3: What are differences between Visibility.Collapsed and Visibility.Hidden in WPF? ⭐⭐
**Answer:**
* `Visibility.Hidden` hides the control, but reserves the space it occupies in the layout. So it renders whitespace instead of the control.
* `Visibilty.Collapsed` does not render the control *and* does not reserve the whitespace. The space the control would take is 'collapsed', hence the name.

**Source:** _stackoverflow.com_

#### Q4: What are static and dynamic resources? ⭐⭐
**Answer:**
There are two types of resource, namely,

*   Static Resource - The value of StaticResource is determined at the time of loading.
*   Dynamic Resource - Dynamic Resource we use in a situation where we want to change the value of property at run time.

**Source:** _c-sharpcorner.com_

#### Q5: Explain WPF styles ⭐⭐
**Answer:**
WPF styles work just like CSS style, In the CSS we define styles for a control and we reuse the same where ever we need in the application, same way the styles in WPF allows to define the properties and can be reused in the application.

**Source:** _c-sharpcorner.com_

#### Q6: What is Command Design Pattern in WPF? ⭐⭐
**Answer:**
Command Design Pattern is one of the most powerful design patterns in object oriented design patterns. This pattern allows you to decouple the request of an action from the object that actually performs an action, in other words a command pattern represents an action as an object. A Command object does not contain the functionality that is to be executed. This removes the direct link between the command definitions and the functionality and it’s promoting a loose coupling. When you want to implement operations based on the user request then the command pattern is the best pattern to handle your object.

The following are the members of the Command Design Pattern:

*   Client
*   Invoker
*   Command
*   Concrete Command
*   Receiver

**Source:** _c-sharpcorner.com_

#### Q7: What is the need of WPF when we had windows forms? ⭐⭐
**Answer:**
Remember: - ABCDEFG

* A - Anywhere execution ( Windows or Web)
* B - Bindings ( less coding)
* C - Common look and feel ( resource and styles)
* D - Declarative programming (XAML)
* E - Expression blend animation ( Animation ease)
* F - Fast execution ( Hardware acceleration)
* G - Graphic hardware independent ( resolution independent)

**Source:** _c-sharpcorner.com_

#### Q8: What are Resources in WPF? ⭐⭐
**Answer:**
Windows Presentation Foundation (WPF) resources provide a simple way to reuse commonly defined objects and values. Resources in WPF allow you to set the properties of multiple controls at a time. For example, you can set the background property on several elements in a WPF application using a single resource.

The best way of defining the resources is on a Window or Page element level. Any resource that you define for an element also applies to their child elements of that element. 

**Source:** _c-sharpcorner.com_

#### Q9: What is value convertor in WPF? ⭐⭐
**Answer:**
A **Value Converter** functions as a bridge between a target and a source and it is necessary when a target is bound with one source, for instance you have a text box and a button control. You want to enable or disable the button control when the text of the text box is filled or null.

In this case you need to convert the string data to Boolean. This is possible using a Value Converter. To implement Value Converters, there is the requirement to inherit from **I Value Converter** in the **System.Windows.Data** namespace and implement the two methods **Convert** and **Convert Back.**

**Source:** _c-sharpcorner.com_

#### Q10: What is xmlns in XAML file? ⭐⭐
**Answer:**
“xmlns” stands for XML namespaces. It helps us to avoid name conflicts and confusion in XML documents.

**Source:** _c-sharpcorner.com_

#### Q11: Is XAML meant only for WPF ? ⭐⭐
**Answer:**
No, XAML is not meant only for WPF. XAML is a XML-based language and it had various variants.

* **WPF XAML** is used to describe WPF content, such as WPF objects, controls and documents. In WPF XAML we also have XPS XAML which defines an XML representation of electronic documents.
* **Silverlight XAML** is a subset of WPF XAML meant for Silverlight applications. Silverlight is a cross-platform browser plug-in which helps us to create rich web content with 2-dimensional graphics, animation, and audio and video.
* **WWF XAML** helps us to describe Windows Workflow Foundation content. WWF engine then uses this XAML and invokes workflow accordingly.

**Source:** _c-sharpcorner.com_

#### Q12: What are the different kinds of controls in WPF? ⭐⭐
**Answer:**
WPF controls can be categorized into four categories:

*   **Control: -** This is the basic control with which you will work most of time. For example textbox, buttons etc. Now controls which are standalone control like a button , text box , labels etc are termed as content control. Now there are other controls which can hold other controls, for instance itemscontrols. Itemscontrol can have multiple textbox controls, label controls etc.
*   **Shape: -** These controls help us to create simple graphic controls like Ellipse, line, rectangle etc.
*   **Panel: -** These controls help to align and position the controls. For instance, grid helps us to align in a table manner, stack panel helps for horizontal and vertical alignment.
*   **Content presenter: -** This control helps to place any XAML content inside it. Used when we want to add dynamic controls on a WPF screen.

**Source:** _c-sharpcorner.com_

#### Q13: When should we use “x:name” vs “name” ? ⭐⭐
**Answer:**
There is no difference between “x:name” and “name” , “name” is short hand of “x:name”. But in classes where you do not find “name” property (this is a rare situations) we need to use “x:name” property.


**Source:** _c-sharpcorner.com_

#### Q14: What is the difference between xmlns and xmlns:x in WPF? ⭐⭐
**Answer:**
Both the namespaces helps to define/resolved XAML UI elements.
* The first namespace is the default namespace and helps to resolve overall WPF elements.
* The second namespace is prefixed by “x:” and helps to resolve XAML language definition.

For instance for the below XAML snippet , we have two things one is the “StackPanel” and the other is “x:name”. “StackPanel” is resolved by the default namespace and the “x:name” is resolved by using “xmlns:x” namespace.

```xml
<StackPanel x:Name="myStack" />
```

**Source:** _c-sharpcorner.com_

#### Q15: What is the difference between XML and XAML? ⭐⭐
**Answer:**
Following are the differences between XML and XAML:

1. All XAML docs are also authentic XML documents. However, the reverse cannot be true.
2. XAML is a declarative application language while XML is a markup language.
3. XML is primarily used in web applications. In contrast, the XAML is used to design controls of Windows and other web applications.
4. XAML focuses on object properties, definition and the relationship among them.
5. XML is a markup language produced by W3C and is used to describe other markup languages.

**Source:** _quora.com_

#### Q16: What is Command Design Pattern and ICommand in WPF? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q17: What is the difference between a Page and a Window in WPF when you are adding a new file in the Solution Explorer? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q18: What is the difference between style and resource in WPF? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q19: What is the difference between Visual and Logical Tree in WPF? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q20: What is MVVM? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q21: How to globally catch exceptions in a WPF application? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q22: Does WPF build on top of Windows Forms or are they totally different? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q23: ListBox vs. ListView - what and when to choose for data binding? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q24: Name some advantages of using Windows Forms instead of WPF ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q25: In WPF, what are the differences between the x:Name and Name attributes? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q26: Can you explain the overall architecture of WPF? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q27: How can you explain view and view model in MVVM? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q28: What's the difference between StaticResource and DynamicResource in WPF? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q29: Does that mean WPF has replaced DirectX? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q30: Can you explain the complete WPF object hierarchy? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q31: What is the use of a Dispatcher Object in WPF? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q32: What is Freezable Object? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q33: Could you tell me what is the main differences between Style and ControlTemplate? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q34: Name some advantages of using WPF instead of Windows forms ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q35: Why do we need dependency properties? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q36: Explain the difference between SelectedItem, SelectedValue and SelectedValuePath? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q37: What is difference between a ControlTemplate and a DataTemplate in WPF? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q38: What is the difference between ObservableCollection and BindingList? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q39: What's the difference between ContentControl and ContentPresenter? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q40: What is the relationship between Threads and Dispatchers? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q41: What is the difference between Freezable.Clone() & Freezable.CloneCurrentValue() methods? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q42: What is the exact difference between Bubbling Events and Tunneling events?  ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q43: When should I use dependency properties in WPF? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q44: What is the difference between Property and Dependency Property? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q45: In what scenarios does freezing WPF objects benefit performance greatly? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q46: What framework for MVVM should I use? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

## [[⬆]](#toc) <a name=WebSecurity>Web Security</a> Interview Questions
#### Q1: What is a DDOS attack? ⭐
**Answer:**
**A denial-of-service attack (DoS attack)** is an attempt to make a computer resource unavailable to its intended users.

Denial of service is typically accomplished by flooding the targeted machine or resource with superfluous requests in an attempt to overload systems and prevent some or all legitimate requests from being fulfilled.

In a **distributed denial-of-service attack (DDoS attack)**, the incoming traffic flooding the victim originates from many different sources. This effectively makes it impossible to stop the attack simply by blocking a single source.


**Source:** _en.wikipedia.org_

#### Q2: What is a botnet? ⭐
**Answer:**
A **botnet** is a number of Internet-connected devices, each of which is running one or more bots. Botnets can be used to perform distributed denial-of-service attack (DDoS attack), steal data, send spam, and allows the attacker to access the device and its connection. 

**Source:** _en.wikipedia.org_

#### Q3: What is Security Testing? ⭐
**Answer:**
Security testing can be considered most important in all type of software testing. Its main objective is to find vulnerabilities in any software (web or networking) based application and protect their data from possible attacks or intruders.

As many applications contains confidential data and needs to be protected being leaked. Software testing needs to be done periodically on such applications to identify threats and to take immediate action on them.

**Source:** _softwaretestinghelp.com_

#### Q4: What is “Vulnerability”? ⭐
**Answer:**
The **Vulnerability** can be defined as weakness of any system through which intruders or bugs can attack on the system.

If security testing has not been performed rigorously on the system then chances of vulnerabilities get increase. Time to time patches or fixes requires preventing a system from the vulnerabilities

**Source:** _softwaretestinghelp.com_

#### Q5:  List the various methodologies in Security testing? ⭐
**Answer:**
Methodologies in Security testing are:
* **White Box** - All the information are provided to the testers.
* **Black Box** - No information is provided to the testers and they can test the system in real world scenario.
* **Grey Box** - Partial information is with the testers and rest they have to rest on their own.

**Source:** _softwaretestinghelp.com_

#### Q6: What is the difference between Authentication vs Authorization? ⭐
**Answer:**
* **Authentication** is the process of ascertaining that somebody really is who he claims to be.
* **Authorization** refers to rules that determine who is allowed to do what. E.g. Adam may be authorized to create and delete databases, while Usama is only authorised to read.

Or in short:
* **Authentication** = login + password (who you are)
* **Authorization** = permissions (what you are allowed to do)

Also:
* Authentication = **Verification** 
* Authorization = **Permissions** 

#### Q7: What is OWASP? ⭐
**Answer:**
**OWASP** stands for *Open Web Application Security Project*.  It is an organization which supports secure software development.

**Source:** _career.guru99.com_

#### Q8: What is SQL injection? ⭐
**Answer:**
Injection attacks stem from a lack of strict separation between program instructions (i.e., code) and user-provided (or external) input. This allows an attacker to inject malicious code into a data snippet. 

*SQL injection* is one of the most common types of injection attack. To carry it out, an attacker provides malicious SQL statements through the application. 

How to prevent:
* **Prepared statements with parameterized queries**
* **Stored procedures**
* **Input validation** - blacklist validation and whitelist validation
* **Principle of least privilege** - Application accounts shouldn’t assign DBA or admin type access onto the database server. This ensures that if an application is compromised, an attacker won’t have the rights to the database through the compromised application.

**Source:** _https://www.synopsys.com_

#### Q9: Provide some "robots.txt" anti-pattern usage ⭐⭐
**Answer:**
`robots.txt` is a text file placed within the root directory of a site that tells robots (such as indexers employed by search engines) how to behave, by instructing them not to index certain paths on the website.

It should not be used as a way to prevent the disclosure of private information or to hide portions of a website. Although this does prevent these sites from appearing in search engines, it does not prevent its discovery from attackers, as robots.txt is frequently used for reconnaisance.

```sh
# Using robots.txt to hide certain directories is a terrible idea
User-agent: *
Disallow: /secret/admin-interface
```

**Source:** _infosec.mozilla.org_

#### Q10: What is Cross-Site Scripting (XSS)? ⭐⭐
**Answer:**
Cross-Site Scripting (XSS) is an attack that occurs when an attacker uses a web application to send malicious code, generally in the form of a browser side script, to a different end user. 

The page provided by the server when someone requests it is unaltered. Instead, an XSS attack exploits a weakness in a page that include a variable submitted in a request to show up in raw form in the response. The page is only reflecting back what was submitted in that request. 

**Source:** _synopsys.com_

#### Q11: How to mitigate the SQL Injection risks? ⭐⭐
**Answer:**
To mitigate SQL injection:

*   **Prepared Statements with Parameterized Queries:** Always ensure that your SQL interpreter always able to differentiate between code and data. Never use dynamic queries which fail to find the difference between code and data. Instead, use static SQL query and then pass in the external input as a parameter to query.  Use of Prepared Statements (with Parameterized Queries) force developer to first define all the SQL code, and then pass in each parameter to the query later.
*   **Use of Stored Procedures:** Stored Procedure is like a function in C where database administrator call it whenever he/she need it. It is not completely mitigated SQL injection but definitely helps in reducing risks of SQL injection by avoiding dynamic SQL generation inside.
*   **White List Input Validation:** Always use white list input validation and allow only preapproved input by the developer. Never use blacklist approach as it is less secure than whitelist approach.
*   **Escaping All User Supplied Input**
*   **Enforcing Least Privilege**

**Source:** _career.guru99.com_

#### Q12: How can I prevent XSS? ⭐⭐
**Answer:**
XSS can be prevented by sanitizing user input to the application. Always allowed those elements as input which is absolutely essential for that field.

**Source:** _allabouttesting.org_

#### Q13: What is DOM-based XSS? ⭐⭐
**Answer:**
**DOM-based XSS** is a type of cross-site scripting which appears in DOM(Document Object Model), instead of HTML.

**Source:** _allabouttesting.org_

#### Q14: What is Intrusion Detection System (IDS)? ⭐⭐
**Answer:**
An **intrusion detection system (IDS)** is a device or software application that monitors a network or systems for malicious activity or policy violations. 

Intrusion detection check following:

* Possible attacks
* Any abnormal activity
* Auditing the system data
* Analysis of different collected data etc.

**Source:** _en.wikipedia.org_

#### Q15: Mention what flaw arises from session tokens having poor randomness across a range of values? ⭐⭐
**Answer:**
*Session hijacking*, is the issue related to A2: 2017 – Broken Authentication. It is also called cookie hijacking. In this type of attack, there is the possibility of exploitation of a valid computer session—sometimes also called a session key—to gain unauthorized access to information or services in a system. This flaw comes when there is a poor randomness in session key.

**Source:** _career.guru99.com_

#### Q16: Explain what threat arises from not flagging HTTP cookies with tokens as secure? ⭐⭐
**Answer:**
*Access Control Violation* threat arises from not flagging HTTP cookies with tokens as secure.

**Source:** _career.guru99.com_

#### Q17: What is Cross Site Scripting (XSS)? ⭐⭐
**Answer:**
By using **Cross Site Scripting (XSS)** technique, users executed malicious scripts (also called payloads) unintentionally by clicking on untrusted links and hence, these scripts pass cookies information to attackers.

**Source:** _allabouttesting.org_

#### Q18: What is Session Hijacking? ⭐⭐
**Answer:**
**Session Hijacking** involves the exploitation of the web session control mechanism. The attacker basically exploits vulnerable connections and steals HTTP cookies to gain unauthorized access to sensitive information/data stored in web servers.

The most effective countermeasure network-level session hijacking is to pick encrypted transport protocols that enable secure connections.

**Source:** _checkmarx.com_

#### Q19: Why is the Root Certificate important? ⭐⭐
**Answer:**
A **Root SSL certificate** is a certificate issued by a trusted certificate authority (CA).

In the SSL ecosystem, anyone can generate a signing key and sign a new certificate with that signature. However, that certificate is not considered valid unless it has been directly or indirectly signed by a trusted CA.

A **trusted certificate authority** is an entity that has been entitled to verify that someone is effectively who it declares to be. In order for this model to work, all the participants on the game must agree on a set of CA which they trust. All operating systems and most of web browsers ship with a set of trusted CAs.

**Source:** _https://support.dnsimple.com/articles/what-is-ssl-root-certificate/_

#### Q20: What is Content Security Policy? ⭐⭐
**Answer:**
**Content Security Policy (CSP)** is an HTTP header that allows site operators fine-grained control over where resources on their site can be loaded from. The use of this header is the best method to prevent cross-site scripting (XSS) vulnerabilities. Due to the difficulty in retrofitting CSP into existing websites, CSP is mandatory for all new websites and is strongly recommended for all existing high-risk sites.

The primary benefit of CSP comes from disabling the use of unsafe inline JavaScript. Inline JavaScript – either reflected or stored – means that improperly escaped user-inputs can generate code that is interpreted by the web browser as JavaScript. By using CSP to disable inline JavaScript, you can effectively eliminate almost all XSS attacks against your site.

**Source:** _infosec.mozilla.org_

#### Q21: What is CORS and how to enable one? ⭐⭐
**Answer:**
A request for a resource (like an image or a font) outside of the origin is known as a *cross-origin request*. CORS (cross-origin resource sharing) manages cross-origin requests. CORS allows servers to specify who (i.e., which origins) can access the assets on the server, among many other things.

**Access-Control-Allow-Origin** is an HTTP header that defines which foreign origins are allowed to access the content of pages on your domain via scripts using methods such as XMLHttpRequest. 

For example, if your server provides both a website and an API intended for XMLHttpRequest access on a remote websites, only the API resources should return the Access-Control-Allow-Origin header. Failure to do so will allow foreign origins to read the contents of any page on your origin.

```sh
# Allow any site to read the contents of this JavaScript library, so that subresource integrity works
Access-Control-Allow-Origin: *
```

**Source:** _infosec.mozilla.org_

#### Q22: How can we Protect Web Applications From Forced Browsing? ⭐⭐
**Answer:**
To protect web applications from forced browsing, strictly monitor access-control settings are accurate and up to date on every page and application on the site.

**Source:** _allabouttesting.org_

#### Q23: What is impersonation? ⭐⭐
**Answer:**
Impersonation is an act of pretending to be another person. For IT Systems impersonation means that some specific users (usually Admins) could get an access to other user's data. 

#### Q24: What is an SSL Certificate? ⭐⭐
**Answer:**
**SSL Certificates** are small data files that digitally bind a *cryptographic key* to an organization’s details. When installed on a web server, it activates the padlock and the https protocol (over port 443) and allows secure connections from a web server to a browser.

**Source:** _globalsign.com_

#### Q25: What is Cross-site request forgery and how to mitigate it? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q26: What is the difference between encryption, encoding, and hashing? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q27: Mention what happens when an application takes user inserted data and sends it to a web browser without proper validation and escaping? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q28: Mention what threat can be avoided by having unique usernames produced with a high degree of entropy? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q29: List Top 10 OWASP Vulnerabilities ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q30: List the attributes of Security Testing ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q31: What is the difference between IDS and firewalls? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q32: What is a Honeypot? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q33: How to mitigate the risk of Weak authentication and session management? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q34: What is HTTP Public Key Pinning and when to use it? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q35:  What Is Failure to Restrict URL Access? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q36: What is PKI? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q37: Name the elements of PKI ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q38: What is Cross-Site Request Forgery? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q39: What information can an attacker steal using XSS? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q40: Apart from mailing links of error pages, are there other methods of exploiting XSS? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q41:  theCould you explain the difference between penetration testing and other forms of security testing? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q42: What is ClickJacking? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q43: Can XSS be prevented without modifying the source code? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q44: How to mitigate the risk of Sensitive Data Exposure? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q45: How to check if HSTS is enabled? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q46: How does SSL/TLS work ? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q47: What is a Bug Bounty? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q48: What is Stored XSS? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q49: What is Reflected XSS? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q50: What are X-Frame-Options? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q51: How to Prevent Breaches Due to Failure to Restrict URL Access? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q52: How come that hash values are not reversible? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q53: What is Cross Site Tracing (XST)? How can it be prevented? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q54: What is HSTS? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q55: What are the types of XSS? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q56: Mention what is the basic design of OWASP ESAPI? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q57: How to use Content Security Policy (CSP) against clickjacking? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q58: What is Content Security Policy (CSP)? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

## [[⬆]](#toc) <a name=Webpack>Webpack</a> Interview Questions
#### Q1: What is webpack? ⭐
**Answer:**
**Webpack** is a build tool that puts all of your assets, including Javascript, images, fonts, and CSS, in a dependency graph. Webpack lets you use `require()` in your source code to point to local files, like images, and decide how they're processed in your final Javascript bundle, like replacing the path with a URL pointing to a CDN.



**Source:** _blog.andrewray.me_

#### Q2: Why and when should I Use Webpack? ⭐
**Answer:**
If you're building a complex Front End application with many **non-code static assets** such as CSS, images, fonts, etc, then yes, Webpack will give you great benefits.

If your application is fairly small, and you don't have many static assets and you only need to build one Javascript file to serve to the client, then Webpack might be more overhead than you need.

**Source:** _blog.andrewray.me_

#### Q3: What is a bundle in webpack? ⭐
**Answer:**
Bundle is the output file generated by webpack. It contains all of the modules which are used in application. Bundles generation process is regulated by webpack config file.

**Source:** _github.com/styopdev_

#### Q4: What is the advantage of CompressionPlugin? ⭐⭐
**Answer:**
*CompressionPlugin* builds gzip-ed version of bundles. Its possible to simply add server side compression e.g using nginx or expres compression plugin. Server-side compression is not recommended because it addes load on CPU and increases response time.

**Source:** _webpack.js.org_

#### Q5: Describe a plugin in webpack ⭐⭐
**Answer:**
**Plugins** used to customize webpack’s build process in a variety of ways. A webpack plugin is a JavaScript object that has an apply property. This apply property is called by the webpack compiler, giving access to the entire compilation lifecycle. Webpack comes with a multiple built-in plugins available under `webpack.[plugin-name]`.

**Source:** _webpack.js.org_

#### Q6: Do loaders work in a synchronous or an asynchronous way? ⭐⭐
**Answer:**
webpack enables use of loaders to preprocess files. This allows you to bundle any static resource way beyond JavaScript. Loaders can work synchronous or asynchronous.

**Source:** _github.com/styopdev_

#### Q7: What is the main difference between Webpack and other build tools like Gulp or Grunt? ⭐⭐
**Answer:**
Webpack is a **module bundler**, though it is quite often used instead of Gulp or Grunt **task runners**. This advanced tool provides developers with control of spliting the modules, allowing them to adjust builds to particular situations and workaround solutions that don’t function properly out of the box.

Comparing Webpack vs Grunt, the first of those offers more flexibility and advanced functionality for modern front-end projects. It comes with a functional core and can be extended using particular loaders and plugins. Essentially it is used for bundling JavaScript modules with dependencies into files, but for complex JavaScript applications with lots of non-code assets (images, fonts, CSS, etc.) it can provide great benefits.

Talking about Webpack vs Gulp vs Grunt performance, the two latter look into a defined path for files that match your configuration, while the Webpack analyzes the whole project. It looks through all the dependencies, processes them with loaders and produces a bundled JS file. 

**Source:** _github.com/styopdev_

#### Q8: How would you remove unused selectors from css using webpack? ⭐⭐
**Answer:**
Using [purifycss-webpack](https://github.com/webpack-contrib/purifycss-webpack) plugin

**Source:** _webpack.js.org_

#### Q9: What is an "entry" point? ⭐⭐
**Answer:**
The entry object is where webpack looks to start building the bundle, at this point the application starts executing.

**Source:** _github.com/styopdev_

#### Q10: What is a dependency graph and how does webpack build it? ⭐⭐
**Answer:**
Any time one file depends on another, webpack treats this as a dependency. Starting from entry point(s), webpack recursively builds a dependency graph that includes every module your application needs, using `import` and `require` statements, then packages all of those modules into bundle(s).

**Source:** _github.com/styopdev_

#### Q11: What is a loader in webpack? ⭐⭐
**Answer:**
**Loaders** are transformations that are applied on the source code of a module. Webpack supports modules written in a variety of languages and preprocessors, via loaders. Loaders describe to webpack how to process non-JavaScript modules and include these dependencies into your bundles.

**Source:** _github.com/styopdev_

#### Q12: Which modules design patterns webpack supports out of the box? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q13: Name some loaders features ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q14: Name some benefits of using webpack ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q15: Name some plugins you think are very important and helpful ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q16: What are some advantages of using webpack-dev-server over simple "http" server or "nginx"? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q17: Explain this code ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q18: Why is OccurenceOrderPlugin the part of webpack optimization? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q19: What is difference between "hash" and "chunkhash"? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q20: Webpack gives us a dependency graph. What does that mean? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q21: List some pitfalls of Webpack ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q22: Explain me the difference between NPM vs. Bower vs. Browserify vs. Gulp vs. Grunt vs. Webpack? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q23: What's the difference between webpack loaders and plugins? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q24: Briefly describe long-term caching and how to achieve it using webpack? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q25: How to move some data (e.g css code) from a bundle to a separate file in webpack? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q26: Explain this code ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q27: Explain this code ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q28: Describe the webpack runtime and manifest ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q29: What is Hot-Modules-Replacement? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q30: What is parallel-webpack and how does it affect webpack's build process? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q31: Is it possible to use other languages (except javascript) for the webpack config file? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q32: Describe tree shaking mechanism in webpack ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

## [[⬆]](#toc) <a name=XML&XSLT>XML & XSLT</a> Interview Questions
#### Q1: Is XML case-sensitive? ⭐
**Answer:**
Yes - **XML is case sensitive**.  There's nothing to stop you writing an XML application which is case insensitive. But it wouldn't be expected or usual. 

**Source:** _stackoverflow.com_

#### Q2: How do I comment out a block of tags in XML? ⭐
**Answer:**
You can use that style of comment across multiple lines (which exists also in HTML):

```xml
<detail>
    <band height="20">
    <!--
      Hello,
         I am a multi-line XML comment
         <staticText>
            <reportElement x="180" y="0" width="200" height="20"/>
            <text><![CDATA[Hello World!]]></text>
          </staticText>
      -->
     </band>
</detail>
```

**Source:** _stackoverflow.com_

#### Q3: When would I use XML instead of SQL? ⭐
**Answer:**
XML **is not a database**. It was never meant to be a database. It is never going to be a database. Relational databases are proven technology with more than 20 years of implementation experience. They are solid, stable, useful products. They are not going away. XML is a very useful technology for moving data between different databases or between databases and other programs. However, it is not itself a database. Don't use it like one.

You can build a DBMS with a DOM/XPath interface but to get **ACID** properties or scale to large data sets you need to implement a DBMS engine and a data format with indexes, logging and other artifacts of a DBMS - which (by definition) makes it something other than XML.

**Source:** _stackoverflow.com_

#### Q4: Why is Everyone Choosing JSON Over XML? ⭐⭐
**Answer:**
Basically because JSON is recognized natively by JavaScript, it's really lightweight, minimalistic and highly portable because it relies only on two fundamental structures:

* A collection of name/value pairs. In various languages, this is realized as an object, record, struct, dictionary, hash table, keyed list, or associative array.
* An ordered list of values. In most languages, this is realized as an array, vector, list, or sequence.

**Source:** _stackoverflow.com_

#### Q5: What is the purpose of XSD files? ⭐⭐
**Answer:**
**XSD** files are used to validate that XML files conform to a certain format. In that respect they are similar to DTDs that existed before them. The main difference between XSD and DTD is that XSD is written in XML and is considered easier to read and understand.

Without XML Schema (XSD file) an XML file is a relatively free set of elements and attributes. The XSD file defines which elements and attributes are permitted and in which order.

In general XML is a metalanguage. XSD files define specific languages within that metalanguage. For example, if your XSD file contains the definition of XHTML 1.0, then your XML file is required to fit XHTML 1.0 rather than some other format.

**Source:** _stackoverflow.com_

#### Q6: What characters do I need to escape in XML documents? ⭐⭐
**Answer:**
If you use an appropriate class or library, they will do the escaping for you. Many XML issues are caused by string concatenation.
 
1. **Always**
     - Escape `<` as `&lt;` unless `<` is starting a `<tag/>`
     - Escape `&` as `&amp;` unless `&` is starting an `&entity;`


 2. **Attribute Values**
     - `attr="` `'`Single quotes`'` are ok within double quotes.`"`
     - `attr='` `"`Double quotes`"` are ok within single quotes.`'`
     - Escape `"` as `&quot;` and `'` as `&apos;` otherwise.


 3. **Comments, CDATA, and Processing Instructions**
     - `<!--` Within comments `-->` nothing has to be escaped but no `--` strings are allowed. 
     - `<![CDATA[` Within CDATA `]]>` nothing has to be escaped, but no `]]>` strings are allowed.
     - `<?PITarget` Within PIs `?>` nothing has to be escaped, but no `?>` strings are allowed.


 4. **Esoterica**
     - Escape `]]>` as `]]&gt;` unless `]]>` is ending a CDATA section. This rule applies to character data in general &ndash; even outside a CDATA section.

**Source:** _stackoverflow.com_

#### Q7: What is the difference between XML and XSD? ⭐⭐
**Answer:**
XSD (XML Schema Definition) specifies how to formally describe the elements in an Extensible Markup Language (XML) document. XML was designed to describe data.

Actually the XSD is XML itself. Its purpose is to validate the structure of another XML document. The XSD is not mandatory for any XML, but it assures that the XML could be used for some particular purposes. The XML is only containing data in suitable format and structure.

Differences:

* XSD is based and written on XML.
* XSD defines elements and structures that can appear in the document, while XML does not.
* XSD ensures that the data is properly interpreted, while XML does not.
* An XSD document is validated as XML, but the opposite may not always be true.
* XSD is better at catching errors than XML.

**Source:** _stackoverflow.com_

#### Q8: What is XSLT? ⭐⭐
**Answer:**
Before XSLT, first we should learn about XSL. XSL stands for EXtensible Stylesheet Language. It is a styling language for XML just like CSS is a styling language for HTML. **XSLT** stands for XSL Transformation. It is used to transform XML documents into other formats (like transforming XML into HTML).

In HTML documents, tags are predefined but in XML documents, tags are not predefined. World Wide Web Consortium (W3C) developed XSL to understand and style an XML document, which can act as XML based Stylesheet Language. An XSL document specifies how a browser should render an XML document.

The XSLT stylesheet is written in XML format. It is used to define the transformation rules to be applied on the target XML document. The XSLT processor takes the XSLT stylesheet and applies the transformation rules on the target XML document and then it generates a formatted document in the form of XML, HTML, or text format. At the end it is used by XSLT formatter to generate the actual output and displayed on the end-user.

<div class="text-center"/>
<img src="https://static.javatpoint.com/xslt/images/what-is-xsltl1.png" class="img-fluid" />
</div>


**Source:** _www.javatpoint.com_

#### Q9: What is XPath? ⭐⭐
**Answer:**
**XPath** is an important and core component of XSLT standard. It is used to traverse the elements and attributes in an XML document.

XPath is a W3C recommendation. XPath provides different types of expressions to retrieve relevant information from the XML document. It is syntax for defining parts of an XML document.

**Source:** _www.javatpoint.com_

#### Q10: XPath: How to check if an attribute exists? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q11: What's the difference between an element and a node in XML? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q12: What is difference between XHTML and HTML? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q13: Create XML based on DTD ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q14: Create XPath to select Element by attribute value ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q15: What does “xmlns” in XML mean? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q16: What are some features of XPath ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q17: How can I build XML in C#? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q18: What are some advantages of XSLT? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q19: Transform this XML into HTML document ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q20: What is the correct XPath for choosing attributes that contain “foo”? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q21: What does [CDATA[]] in XML mean? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q22: When to prefer JSON over XML? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q23: Is there any difference between 'valid xml' and 'well formed xml'? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q24: When to prefer XML over JSON? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q25: What are some advantages and disadvantages of XSLT? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q26: Compare XML to JSON ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q27: What is Processing Instructions in XML? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q28: What is meaning of <?xml version=“1.0” encoding=“utf-8”?> ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q29: What are some ways to represent null XML elements? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q30: Name some good reasons why one should use XML? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q31: How do I comment out a block of tags in XML? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q32: Does a valid XML file require an XML declaration? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q33: What's the difference between <el/> and <el xsi:nil=“true” />? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q34: XML best practices: attributes vs additional elements? Wha tis best practice? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q35: What is difference between XML Schema and DTD? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q36: How to implement if-else statement in XSLT? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q37: Create DTD based on XML ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q38: What XPath will give you all nodes that have attributes containing 'Foo' regardless of node name or attribute name? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q39: What's the need for XHTML? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q40: Why is XSLT so rarely used on the web? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q41: When would you use PIs in XML? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

## [[⬆]](#toc) <a name=Xamarin>Xamarin</a> Interview Questions
#### Q1: What is Xamarin? ⭐
**Answer:**
**Xamarin** is a Cross Platform Mobile Development technology by Microsoft where we can develop the native app using the same code base across all platforms (iOS, Android, UWP) using the C# language. Xamarin uses two approaches for the app development:
* Xamarin.Forms and 
* Xamarin Native. 

Xamarin.Forms uses MVVM & XAML while Xamarin Native uses native UI technology and MVC or MVVMCross Architecture.

**Source:** _codeproject.com_

#### Q2: What is App.cs class? ⭐⭐
**Answer:**
_App.cs_ is the main class of the app which offers features like:

*   **MainPage**: It helps to set the initial page for the app.
*   **Properties Dictionary**: It helps us store simple values across lifecycle states.
*   **Static Current Property**: It gives the instance of the current application object.

**Source:** _codeproject.com_

#### Q3: What are Pages in Xamarin.Forms? ⭐⭐
**Answer:**
**Pages** are Xamarin Forms generic representation of Cross Mobil Application Screens. A Page occupies most or all of a screen and contains a single child.

On IOS, the Page is mapped to ViewController, on Android, it is mapped to somewhat like Activity and on Universal Windows Platform, it is mapped to  Page. Pages can be of several types, viz. Master /Detail Page, navigational Page, Carousel Page, Tabbed Page, Template Page, etc.

**Source:** _knowledgehut.com_

#### Q4: What are the various flavors of Xamarin Applications that can be made? ⭐⭐
**Answer:**
Xamarin allows two different ways of creating applications, based on the amount of code reusability and customization:

* The first approach is the **Traditional Native Approach** wherein platform-specific apps using Xamarin.iOSiOS and Xamarin.Android can be made. This way of creating apps is generally used when there is a lot of customization specific to the platform is required as it allows direct access to platform-specific APIs. Xamarin.iOS is used for iOS applications and Xamarin.Android is used to create Android applications.

* The second approach is creating apps through **Xamarin.Forms approach**. Xamarin.Forms are used when there is a possibility of reuse of a lot of platform-independent code and the focus is less on custom UI. The platform-independent code is separated and kept in Shared Project or PCL or .NET Standard Library and Platform Specific projects consume this common code by including it.

**Source:** _knowledgehut.com_

#### Q5: How to display static HTML string in Xamarin.Forms? ⭐⭐
**Answer:**
We can use WebView control to display `static` HTML `string`. `WebView` can be used to display Websites, HTML string, Documents, Local Files depending on the platform support.

**Source:** _codeproject.com_

#### Q6: How to store simple Key-Value data? ⭐⭐
**Answer:**
Xamarin.Forms's `Application` class exposes the `Application.Current.Properties` `Dictionary` which is used to store the simple Key-Value pair data. The `Properties` dictionary uses a `string` key and stores an object value.

**Source:** _codeproject.com_

#### Q7: What is the difference between Xamarin.Forms & Xamarin Native? ⭐⭐
**Answer:**
Xamarin.Forms is used when:

*   Less platform-specific code is required
*   Code sharing is more important than custom UI
*   UI is not complex

Xamarin Native is used when:

*   Lot of platform specific code is required
*   Custom UI is more important then code sharing
*   Many platform-specific APIs are used

**Source:** _codeproject.com_

#### Q8: What is is the difference between ListView & TableView? ⭐⭐
**Answer:**
The ListView and TableView controls are so similar, you can think of them as a single control. The major difference between the two is the manner in which they lay out their items, and it’s easy to change the layout so each control emulates the other.

* The ListView control displays its data stacked vertically, much like a standard listbox. Use this control to display an ordered list of data, especially long lists that require scrolling like a list of email messages, a list of contacts, or search results.

* The TableView control displays its data stacked horizontally in rows (although you can alter this behavior and have it displayed in columns first, as well). You use this control when you need more space for rich visualization of each item to be displayed.

One of the big differences is ListView provides you a ItemsSource and a Itemtemplate and TableView does not. So items must be added as children manually.

**Source:** _greenstechnologys.com_

#### Q9: What is the difference between Margin and Padding properties? ⭐⭐
**Answer:**
* `Margin` property represents the distance between the element and its adjacent elements and is used to control the element's rendering position, and the rendering position of its neighbors. Margin can be specified on `Layout` and `View` classes.

* `Padding` property represents the distance between an `Element` and the child elements of it and thus it is used to separate the control from its own content. `Padding` values can be specified on `Layout` classes.

Suppose, two adjacent elements have a margin of value 20 pixels assigned, what will be the distance between these two elements? Why?

The distance between two elements will be 40 pixels in this case, because, `Margin` property values are `Additive`. In addition to this, if `Margin` and `Padding` both are applied, then the distance between element and its content will be `Margin + Padding`.

**Source:** _codeproject.com_

#### Q10: What is Xamarin.Forms and what are the benefits of using it? ⭐⭐
**Answer:**
**Xamarin.Forms** is a Cross-Platform Toolkit which helps share Business Logic as well as UI using XAML across all supported platforms.

It uses MVVM pattern along with Binding into the XAML UI to accomplish this. It produces pure native controls for each individual platforms. Using Xamarin.Forms, we can share the whole business logic as well as UI among all supporting platforms like iOS, Android and UWP. It also provides a way for platform specific customization of any native controls using Renderers. Thus, we can almost share about 80-90% of code across platforms. We can say Xamarin is the King of Cross Platforms.


**Source:** _codeproject.com_

#### Q11: Name few widely used Layout Controls ⭐⭐
**Answer:**
*   `Frame`: It contains a single element as a child having a default padding of 20.
*   `Grid`: It is used when UI components are to be arranged into Rows & Columns.
*   `StackLayout`: It is used when UI components are to be arranged either horizontally or vertically.
*   `ScrollView`: It enables the scrolling for a child element if required. It has one child only.

There are other Layout Controls too like `AbsoluteLayout`, `RelativeLayout`, `ContentView`, `ContentPresenter`, etc.

**Source:** _codeproject.com_

#### Q12: How will you navigate from one page to another? ⭐⭐
**Answer:**
On some button click event of First Page, we can call the following method, which will navigate to the second page:

```csharp
await Navigation.PushAsync (new MySecondPageXaml (), true);
```

We have to use the "`Navigation`" property which is available under `ContentPage` class (XAML Page's code behind). So this navigation can be written in the Page's code behind file.

**Source:** _codeproject.com_

#### Q13: Which Languages are supported for Xamarin development? ⭐⭐
**Answer:**
C# & F#

**Source:** _codeproject.com_

#### Q14: Explain Lifecycle methods of Xamarin.Forms app ⭐⭐
**Answer:**
Lifecycle methods are set of methods which get executed when application enters into a specific state. Following are such methods:

*   `OnStart`: Executes when application starts from the beginning
*   `OnSleep`: Executes each time when application goes into the background
*   `OnResume`: Executes when application comes into the foreground from the Sleeping state

**Source:** _codeproject.com_

#### Q15: What is the basic architecture of Xamarin.Forms project? ⭐⭐
**Answer:**
Xamarin.Forms can consists of four (this varies based on requirements) projects under one solution.

*   .NET Standard, PCL or Shared Project
*   iOS Project
*   Android Project
*   UWP Project

Here, .NET Standard, PCL or Shared Project contains all UI & Business logic inside it.

iOS, Android, UWP contains platform specific code containing Renderers or Dependency Services Implementations.


**Source:** _codeproject.com_

#### Q16: Explain .NET Standard Libraries For Sharing Code on Xamarin? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q17: How To Share Code Between Cross-Platform Applications on Xamarin? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q18: What are Triggers? How many types of Triggers are available? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q19: What are the advantages and disadvantages of using XAML in Xamarin.Forms? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q20: What is the purpose of INotifyPropertyChanged? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q21: How To Share Code Between Cross-Platform Applications on Xamarin? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q22: What is difference between ControlTemplate & DataTemplate? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q23: How to do Xamarin.Android applications work? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q24: What is Custom Renderers and what is its purpose? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q25: What is Behaviors and give some examples where we should use Behaviors? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q26: What is Fresh MVVM? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q27: What is TestFlight? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q28: What is the difference between Xamarin.Forms and Xamarin Native? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q29: What is info.plist in Xamarin.iOS ? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q30: What is the special meaning with "AndExpand" Suffix with each LayoutOptions? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q31: What is ViewCell and How many types of built-in Cells are available? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q32: What are Effects and when should they be used? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q33: What are Custom renderers in Xamarin.Forms? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q34: What is the purpose of InitializeComponent() method in Page? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q35: What is Dependency Service and how it functions on Xamarin.Forms? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q36: When would you use the NavigationPage as a MainPage? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q37: How to perform Binding in Code Behind? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q38: What is ResourceDictionary? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q39: What is XAML Markup Extensions? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q40: What is the purpose of XAML Compiler (XAMLC)? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q41: What is View-to-View Binding? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q42: What is the difference between Xaml & Axml in Xamarin Technology? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q43: What is the difference between PCL & Shared Project? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q44: How many ways can we share the code? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q45: Explain how to use shared projects in Xamarin? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q46: How many types of Pages are available in Xamarin.Forms? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q47: What is MVVM Light ? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q48: How many types of different XAML Markup Extensions do you know? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q49: How to render different types of ViewCell in the same ListView during runtime? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q50: Which best practices to follow while designing the XAML Page? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q51: What is Xamarin.Essentials? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q52: What is Effects and When should we use it over Custom Renderers? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q53: What is DependencyService? Describe steps for the implementation. ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q54: What are the disadvantages of Xamarin for Android development? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q55: How to design separate layouts or functionality between Phone & Tablets? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q56: How do we provide Platform specific styling or values in XAML? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q57: How many ways we can Bind data? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q58: How many ways you can Bind a ViewModel with XAML? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q59: Is there any benefit in binding a ViewModel in backend .cs file? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q60: How does compilation work for Xamarin? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q61: What the Xamarin platform consists of? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q62: What is MessagingCenter? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q63: What are some features of Fresh MVVM? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q64: What is MVVM Cross? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q65: Why do we need to create a Custom ViewCell? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q66: How to call a specific method for some specific Platform only? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q67: Name some types of Behaviors in Xamarin? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q68: What is the difference between Entry and Editor in Xamarin.Forms? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q69: What are Services in Xamarin.Android? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q70: Name some types of keys defined in info.plist files ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q71: How to make iOS native libraries accessible in Xamarin apps? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q72: What are Android Callable Wrappers (ACWs)? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q73: What is the disadvantage of Xamarin to using for example Objective-C or Java for iOS and Android separately? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q74: So, what is the difference between MessagingCenter and Events? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q75: Can we really declare Parametrized ViewModel instance as BindingContext in XAML? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q76: Explain what is linking process on Xamarin ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q77: Name some limitation of Xamarin.iOS ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q78: What are provisioning profiles on Xamarin.iOS? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q79: How to increase the ListView performance? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q80: Explain what happens when the Xamarin.Android application compiles? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q81: Why AOT is used for Xamarin.iOS? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q82: What is Selector in Xamarin.iOS? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q83: What is Registrar in Xamarin.iOS? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

## [[⬆]](#toc) <a name=iOS&Swift>iOS & Swift</a> Interview Questions
## [[⬆]](#toc) <a name=jQuery>jQuery</a> Interview Questions
#### Q1: What is jQuery? ⭐
**Answer:**
**jQuery** is **fast, lightweight and feature-rich** client side JavaScript Library/Framework which helps in to traverse HTML DOM, make animations, add Ajax interaction, manipulate the page content, change the style and provide cool UI effect. It is one of the most popular client side library and as per a survey it runs on every second website.  

**Source:** _codeproject.com_

#### Q2: What is event.PreventDefault? ⭐⭐
**Answer:**
The `event.preventDefault()` method stops the default action of an element from happening. For example, Prevents a link from following the URL.  

**Source:** _codeproject.com_

#### Q3: Is jQuery replacement of Java Script? ⭐⭐
**Answer:**
**No.** jQuery is not a replacement of JavaScript. jQuery is a different library which is written on top of JavaScript. jQuery is a lightweight JavaScript library that emphasizes interaction between JavaScript and HTML.  

**Source:** _codeproject.com_

#### Q4: Is jQuery a library for client scripting or server scripting? ⭐⭐
**Answer:**
Client side scripting.  

**Source:** _codeproject.com_

#### Q5: Is jQuery a W3C standard? ⭐⭐
**Answer:**
No. jQuery is not a W3C standard.  

**Source:** _codeproject.com_

#### Q6: Which is the starting point of code execution in jQuery? ⭐⭐
**Answer:**
The starting point of jQuery code execution is `$(document).ready()` function which is executed when DOM is loaded. 

**Source:** _codeproject.com_

#### Q7: What does dollar sign ($) means in jQuery? ⭐⭐
**Answer:**
Dollar Sign is nothing but it's an alias for JQuery. Take a look at below jQuery code.

```js
$(document).ready(function(){
});
```

Over here $ sign can be replaced with "jQuery" keyword.

```js
jQuery(document).ready(function(){
});
```

**Source:** _codeproject.com_

#### Q8: Can we have multiple document.ready() function on the same page? ⭐⭐
**Answer:**
**YES**. We can have any number of document.ready() function on the same page.  

**Source:** _codeproject.com_

#### Q9: What is jQuery.noConflict? ⭐⭐
**Answer:**
As other client side libraries like MooTools, Prototype can be used with jQuery and they also use `$()` as their global function and to define variables. This situation creates conflict as `$()` is used by jQuery and other library as their global function. To overcome from such situations, jQuery has introduced `jQuery.noConflict()`.

```js
jQuery.noConflict();
// Use jQuery via jQuery(...)
jQuery(document).ready(function(){
   jQuery("div").hide();
});  
```

You can also use your own specific character in the place of `$` sign in jQuery.

```js
var $j = jQuery.noConflict();
// Use jQuery via jQuery(...)
$j(document).ready(function(){
   $j("div").hide();
});  
```

**Source:** _codeproject.com_

#### Q10: How JavaScript and jQuery are different? ⭐⭐
**Answer:**
JavaScript is a language While jQuery is a library built in the JavaScript language that helps to use the JavaScript language.  

**Source:** _codeproject.com_

#### Q11: What is a CDN? ⭐⭐
**Answer:**
A content delivery network or content distribution network (CDN) is a large distributed system of servers deployed in multiple data centers across the Internet. The goal of a CDN is to serve content to end-users with high availability and high performance.  

There are 3 popular jQuery CDNs:

1.  1\. Google.
2.  2\. Microsoft
3.  3\. jQuery.

Advantages of using CDN:

*   It reduces the load from your server.
*   It saves bandwidth. jQuery framework will load faster from these CDN.
*   The most important benefit is it will be cached, if the user has visited any site which is using jQuery framework from any of these CDN

**Source:** _codeproject.com_

#### Q12: How do you select element by ID in jQuery? ⭐⭐
**Answer:**
To select element use ID selector. We need to prefix the id with "#" (hash symbol). For example, to select element with ID "txtName", then syntax would be,

```js
$('#txtName')
```

**Source:** _codeproject.com_

#### Q13: What does $("div") will select? ⭐⭐
**Answer:**
This will select all the div elements on page.  

**Source:** _codeproject.com_

#### Q14: How to select element having a particular class (".selected")? ⭐⭐
**Answer:**
`$('.selected')`. This selector is known as class selector. We need to prefix the class name with "." (dot). 

**Source:** _codeproject.com_

#### Q15: What does $("div.parent") will select? ⭐⭐
**Answer:**
All the div element with parent class.  

**Source:** _codeproject.com_

#### Q16: What is the use of jquery .each() function? ⭐⭐
**Answer:**
The `$.each()` function is used to iterate over a jQuery object. The `$.each()` function can be used to iterate over any collection, whether it is an object or an array.  

**Source:** _codeproject.com_

#### Q17: Why do we use jQuery? ⭐⭐
**Answer:**
Due to following advantages.

*   Easy to use and learn.
*   Easily expandable.
*   Cross-browser support (IE 6.0+, FF 1.5+, Safari 2.0+, Opera 9.0+)
*   Easy to use for DOM manipulation and traversal.
*   Large pool of built in methods.
*   AJAX Capabilities.
*   Methods for changing or applying CSS, creating animations.
*   Event detection and handling.
*   Tons of plug-ins for all kind of needs.

**Source:** _codeproject.com_

#### Q18: What is the difference between .js and .min.js? ⭐⭐
**Answer:**
jQuery library comes in 2 different versions Development and Production/Deployment. The deployment version is also known as _minified_ version. So .min.js is basically the minified version of jQuery library file. Both the files are same as far as functionality is concerned. but .min.js is quite small in size so it loads quickly and saves bandwidth.  

**Source:** _codeproject.com_

#### Q19: What are the fastest/slowest selectors in jQuery? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q20: How jQuery selectors are executed? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q21: Which is fast document.getElementByID('txtName') or $('#txtName').? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q22: Difference between $(this) and 'this' in jQuery? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q23: Is there any difference between body onload() and document.ready() function? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q24: What is the difference between jquery.size() and jquery.length? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q25: What are various methods to make ajax request in jQuery? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q26: What are selectors in jQuery and how many types of selectors are there? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q27: What is the difference between eq() and get() methods in jQuery? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q28: What is chaining in jQuery? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q29: What is wrong with this code line "$('#myid\\.3').text('blah blah!!!');" ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q30: When would you use AngularJS vs jQuery? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q31: How to create clone of any object using jQuery? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q32: What is difference between prop and attr? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q33: What is the difference between event.PreventDefault and event.stopPropagation? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q34: What is the difference between parent() and parents() methods in jQuery? ⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q35: What is the difference between event.PreventDefault and "return false"? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q36: How do you attach a event to element which should be executed only once? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q37: In what situation you would use multiple version of jQuery and how would you include them? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q38: Is there any significant difference between event.preventDefault() vs. return false to stop event propagation? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q39: Explain .bind() vs .live() vs .delegate() vs .on() ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q40: How does caching helps and how to use caching in jQuery?  ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q41: What is the difference between $('div') and $('<div/>') in jQuery? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q42: Is there any advantage of using $.ajax() for ajax call against $.get() or $.post()? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q43: What are the differences between JavaScript's window.onload and jQuery's $(document).ready() method? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q44: How can I get jQuery to perform a synchronous, rather than asynchronous, Ajax request? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q45: What are deferred and promise object in jQuery? ⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q46: Can we execute/run multiple Ajax request simultaneously in jQuery? If yes, then how? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q47: Is it possible to get value of multiple CSS properties in single statement? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q48: What is the difference between event.stopPropagation and event.stopImmediatePropagation? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q49: How can I implement my own $(document).ready functionality without using jQuery? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q50: Is it possible to hold or delay document.ready execution for sometime? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

#### Q51: What is the advantage of using protocol less URL while referencing jQuery from CDNs? ⭐⭐⭐⭐⭐
Read answer on 👉 <a href='https://www.fullstack.cafe'>FullStack.Cafe</a>

