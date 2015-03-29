Servlet sepcifications defines the default encoding as ISO-8859-1.
gwt-table-to excle uses this encoding as default.

But
**Some spoken languages needs extended encoding** There is variations in servers implementations

Since 0.0.2, you can define the encoding.

# Configuration #
## web.xml ##
```
<servlet>
	<servlet-name>gwtTableToExcelServlet</servlet-name>
	<servlet-class>com.googlecode.gwtTableToExcel.server.TableToExcelServlet</servlet-class>
	<init-param>
		<param-name>encoding</param-name>
		<param-value>UTF-8</param-value>
	</init-param>
</servlet>
```

## Page ##
You must configure your page in the same encoding, in the head section (and the html file itself)


&lt;meta http-equiv="content-type" content="text/html; charset=UTF-8"&gt;



# Servers #
|Server|Version|Encoding|
|:-----|:------|:-------|
|AppEngine||ISO-8859-1(default)|
|Jetty|6.1.10|ISO-8859-1|
|Tomcat|6.0.32|UTF-8|


http://www.oracle.com/technetwork/java/download-139443.html