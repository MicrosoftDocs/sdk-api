---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# MsiDatabaseGetPrimaryKeysA function


## -description


The 
<b>MsiDatabaseGetPrimaryKeys</b> function returns a record containing the names of all the primary key columns for a specified table. This function returns a handle that should be closed using 
<a href="https://msdn.microsoft.com/b9e90ed4-fda8-4628-a713-67c651e1b572">MsiCloseHandle</a>.


## -parameters




### -param hDatabase [in]

Handle to the database. See 
<a href="https://msdn.microsoft.com/53cf73bc-4d52-471c-8384-46d106a36e38">Obtaining a Database Handle</a>.


### -param szTableName [in]

Specifies the name of the table from which to obtain primary key names.


### -param phRecord [out]

Pointer to the handle of the record that holds the primary key names.


## -returns



This function returns UINT.




## -remarks



The field count of the returned record is the count of primary key columns returned by the 
<b>MsiDatabaseGetPrimaryKeys</b> function. The returned record contains the table name in Field (0) and the column names that make up the primary key names in succeeding fields. These primary key names correspond to the column numbers for the fields.

This function cannot be used with the 
<a href="https://msdn.microsoft.com/d064855b-8c10-476e-9570-cc3ab48ae998">_Tables table</a> or the 
<a href="https://msdn.microsoft.com/1ddde4e2-90a9-4dd8-a4f9-b6802d0b11cf">_Columns table</a>.

Note that it is recommended to use variables of type PMSIHANDLE because the installer closes PMSIHANDLE objects as they go out of scope, whereas you must close MSIHANDLE objects by calling 
<a href="https://msdn.microsoft.com/b9e90ed4-fda8-4628-a713-67c651e1b572">MsiCloseHandle</a>. For more information see <a href="windows_installer_best_practices.htm">Use PMSIHANDLE instead of HANDLE</a> section in the <a href="https://msdn.microsoft.com/ff48d995-fe6f-4d1b-898d-67574ed3c5b7">Windows Installer Best Practices</a>.




## -see-also




<a href="database_functions.htm">General Database Access Functions</a>
 

 

