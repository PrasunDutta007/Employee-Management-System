# Employee-Management-System

## Software
#### Eclipse

## Features

- Add Employee
- Delete Employee
- Update Employee
- Track Employee
- Admin Login
- Employee Login


  
## To Run The Project

```bash
  import the project into Eclipse
```
```bash
  install `Tomcat server` properly in your system using the documentation provided below in `Resoources Section`
```
```bash
  Check if your tomcat server is running by running the following in your Web Browser URL:
  `http://localhost:8080`
```
```bash
  Next install MySQL in your System by following the documentation provided below in `Resoources Section`
```
```bash
  Copy the given below code into your your JSP directory under /usr/local/etc/httpd/htdocs/html/LOGIN (where LOGIN is your login name). You will need to change the 'xxxxxx' of     "con=DriverManager.getConnection("jdbc:mysql://localhost/"+db,user,"xxxxxxx");" to reflect your MySQL password. Copy the HTML form (right click and view source) to the same     directory above or to your public_html directory and use it connect to your database via the JSP code. 
  
  `
  <%@ page import="java.sql.*"%>
<html>
<head>
<title>JDBC Connection example</title>
</head>

<body>
<h1>JDBC Connection example</h1>

<%
  String db = request.getParameter("db");
  String user = db; // assumes database name is the same as username
  try {
    java.sql.Connection con;
    Class.forName("org.gjt.mm.mysql.Driver");
    con = DriverManager.getConnection("jdbc:mysql://localhost/"+db, user, "xxxxxxx");
    out.println (db+ "database successfully opened.");
  }
  catch(SQLException e) {
    out.println("SQLException caught: " +e.getMessage());
  }
%>

</body>
</html>
  `
```
```bash
  Now setup Tomcat as the Server in your Eclipse Folder by doing the following steps:
  'IDE -> right click on blank area -> New -> Servers -> choose tomcat then its version -> next -> click on Browse button -> select the apache tomcat root folder previous to bin -> next -> addAll -> Finish'
```
```bash
  Finally run the file via the Tomcat server through Eclipse
  
  Done!!
```

## Resources
- https://dev.mysql.com/doc/mysql-installation-excerpt/8.0/en/windows-install-archive.html
- https://tomcat.apache.org/tomcat-8.5-doc/setup.html

## Credits
https://github.com/aritra108
