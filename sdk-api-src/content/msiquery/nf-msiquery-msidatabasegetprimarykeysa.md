---
UID: NF:msiquery.MsiDatabaseGetPrimaryKeysA
title: MsiDatabaseGetPrimaryKeysA function (msiquery.h)
author: windows-sdk-content
description: The MsiDatabaseGetPrimaryKeys function returns a record containing the names of all the primary key columns for a specified table. This function returns a handle that should be closed using MsiCloseHandle.
old-location: setup\msidatabasegetprimarykeys.htm
tech.root: Msi
ms.assetid: 08ceaf05-a64b-41ac-964b-ae4648e42bae
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: MsiDatabaseGetPrimaryKeys, MsiDatabaseGetPrimaryKeys function, MsiDatabaseGetPrimaryKeysA, MsiDatabaseGetPrimaryKeysW, _msi_msidatabasegetprimarykeys, msiquery/MsiDatabaseGetPrimaryKeys, msiquery/MsiDatabaseGetPrimaryKeysA, msiquery/MsiDatabaseGetPrimaryKeysW, setup.msidatabasegetprimarykeys
ms.topic: function
f1_keywords: 
 - "msiquery/MsiDatabaseGetPrimaryKeys"
req.header: msiquery.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7. Windows Installer 4.0 or Windows Installer 4.5 on   Windows Server 2008 or Windows Vista. Windows Installer on Windows Server 2003 or Windows XP
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: MsiDatabaseGetPrimaryKeysW (Unicode) and MsiDatabaseGetPrimaryKeysA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Msi.lib
req.dll: Msi.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Msi.dll
api_name:
 - MsiDatabaseGetPrimaryKeys
 - MsiDatabaseGetPrimaryKeysA
 - MsiDatabaseGetPrimaryKeysW
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# MsiDatabaseGetPrimaryKeysA function


## -description


The 
<b>MsiDatabaseGetPrimaryKeys</b> function returns a record containing the names of all the primary key columns for a specified table. This function returns a handle that should be closed using 
<a href="https://docs.microsoft.com/windows/desktop/api/msi/nf-msi-msiclosehandle">MsiCloseHandle</a>.


## -parameters




### -param hDatabase [in]

Handle to the database. See 
<a href="https://docs.microsoft.com/windows/desktop/Msi/obtaining-a-database-handle">Obtaining a Database Handle</a>.


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
<a href="https://docs.microsoft.com/windows/desktop/Msi/-tables-table">_Tables table</a> or the 
<a href="https://docs.microsoft.com/windows/desktop/Msi/-columns-table">_Columns table</a>.

Note that it is recommended to use variables of type PMSIHANDLE because the installer closes PMSIHANDLE objects as they go out of scope, whereas you must close MSIHANDLE objects by calling 
<a href="https://docs.microsoft.com/windows/desktop/api/msi/nf-msi-msiclosehandle">MsiCloseHandle</a>. For more information see <a href="https://docs.microsoft.com/windows/desktop/Msi/windows-installer-best-practices">Use PMSIHANDLE instead of HANDLE</a> section in the <a href="https://docs.microsoft.com/windows/desktop/Msi/windows-installer-best-practices">Windows Installer Best Practices</a>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/Msi/database-functions">General Database Access Functions</a>
 

 

