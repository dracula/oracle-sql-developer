### [Oracle SQL Developer](https://www.oracle.com/database/technologies/appdev/sql-developer.html)

#### Installation

Unfortunately Oracle doesn't make it easy to import a new colour scheme into SQL Developer, thus a little bit of hacking is required.

- Close SQL Developer. This is important. If you modify the scheme file while SQL Developer is open, your changes won't be saved.

- Locate file `dtcache.xml` in the [SQL Developer's settings directory](https://docs.oracle.com/en/database/oracle/sql-developer/19.1/rptig/installing-sql-developer.html#GUID-16F0A7C3-6EC1-4176-9B15-FE4AA8D70D5F).

Windows:

```%APPDATA%\SQL Developer\systemn.n.n.n.n.n\o.ide.n.n.n.n.n.n.n```

Example:

```C:\Users\dracula\AppData\Roaming\SQL Developer\system3.2.20.09.87\o.ide.11.1.1.4.37.59.48```

Linux or Mac OS X:

```~/.sqldeveloper/systemn.n.n.n.n.n/o.ide.n.n.n.n.n.n.n```

Example:

```~/.sqldeveloper/system19.1.0.094.2042/o.ide.13.0.0.1.42.170225.201```

- Locate `<schemeMap>` tag inside dtcache.xml file. Insert the content of the color scheme xml file inside `<schemeMap>` alongside the other colour schemes. Be careful not to break the XML.

![Insert the contents of color scheme xml file after opening schemeMap tag](https://raw.githubusercontent.com/dracula/oracle-sql-developer/master/images/theme_insert_here.png)

- Launch SQL Developer. Navigate to menu Tools->Preferences, then select item Code Editor -> PL/SQL Syntax Colors in the left pane.

- Select theme in the "Scheme" drop down list on the top.

![](https://raw.githubusercontent.com/dracula/oracle-sql-developer/master/images/dracula_select.png)

__See original instructions providing by [Ozmoroz](https://github.com/ozmoroz/ozbsidian-sqldeveloper/blob/master/README.md)__