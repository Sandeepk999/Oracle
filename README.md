# Oracle SQL 2.0

***ARGOS LABS plugin module Oracle***

> This function is one of Plugins Operation.You can find the movie in [ARGOS RPA+ video tutorial](https://www.argos-labs.com/video-tutorial/).

## Name of the plugin
| Item         |        Value         |
|--------------|:--------------------:|
| Icon         | ![oracle](icon.png)  | 
| Display Name |  **Oracle SQL 2.0**  |

## Name of the author (Contact info of the author)

Arun Kumar 
* [email](mailto:arunk@argos-labs.com)
  
Sandeep Kumar 
* [email](mailto:sandeepsharma@argos-labs.com)



## Notification

### Dependent modules
| Module   | Source Page                                             |
|----------|---------------------------------------------------------|
| [oracledb](https://github.com/oracle/python-oracledb) | [oracledb](https://github.com/oracle/python-oracledb)   |


## Warning 
![warning](warning.png) **IMPORTANT NOTE**<br>
The ORACLE SQL 2.0 plugin requires the ORACLE DLL to be downloaded in the ARGOS Virtual Environment if the python version is above 3.9 . (V-Env) The DLL file size is nearly 100 MB. Depending on your network speed, it might take a few minutes to set up the V-Env.

## Primary Features
* The Oracle SQL 2.0 plugin enables your bot to directly connect and manipulate the ORACLE database.
## Limitations
The plugin today supports ORACLE on Windows. Other environments such as Linux and Mac are under testing now and will be released soon.

## Version Control 
* 7.804.1737
* Release Date: Aug 05, 2025

## Input (Required) 
| Display Name | Input Method    | Default Value | Description                                                      |
|--------------|-----------------|---------------|------------------------------------------------------------------|
| DB Host      | IP Address      | -             | Specify IP address of the host.                                  |
| DB Port      | Port No.        | -             | Specify the port no of the database.                             |
| DB User      | User ID(String) | -             | Determine the specified user ID of the data base.                |
| DB Password  | Password        | -             | Determine the specified password of the data base.               |
| DB Name      | String          | -             | Specify the Database SID (e.g. XE) or Service Name (e.g. orcl).  |

## Input (Optional)
| Display Name     | Input Method | Default Value | Description                                                                                                   |
|------------------|--------------|---------------|---------------------------------------------------------------------------------------------------------------|
| SQL string       | String       | -             | SQL can be sent either as char String or from a text file                                                     |
| SQL file         | fileread     | -             | SQL from file. (Note, either one of `SQL string` or `SQL file`)                                               |
| CSV bulk input   | fileread     | -             | Data input can be made from a CSV file in case of `INSERT` sql.                                               |
| Exc N Headers    | int          | -             | If there is(are) header(s), you can use the Exclusion count option here.                                      |
| Character Set    | String       | -             | The database also uses this character set for metadata such as table names, column names, and SQL statements. |
| Encoding         | -            | utf-8         | By checking this the target strings will be encoded.                                                          |
| As SYSDBA        | -            | -             | Check this option to enable SYSDBA mode for User.                                                             |

## Return Value

### For `SELECT` SQL
Result will be the output records with CSV output

### for otherwise SQL
Reuslt will the `affected_row_count` and integer value

![Text_from_Image](README_02.png)


## Parameter setting examples
Example SQL file

--- insert static records

INSERT INTO foo (name, age)

values

('nobody me', 100),

(‘foobar', 200)



![Text_from_Image](README_01.png)



## Return Code
| Code | Meaning               |
|------|-----------------------|
| 0    | Execution Successful  |
| 9    | Execution Failed      |
    
