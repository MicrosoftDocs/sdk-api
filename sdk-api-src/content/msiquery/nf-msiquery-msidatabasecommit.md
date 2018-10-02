---
UID: NF:msiquery.MsiDatabaseCommit
title: MsiDatabaseCommit function
author: windows-sdk-content
description: The MsiDatabaseCommit function commits changes to a database.
old-location: setup\msidatabasecommit.htm
tech.root: MSI
ms.assetid: bc42b90b-51db-4e13-af2f-4942923badf6
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: MsiDatabaseCommit, MsiDatabaseCommit function, _msi_msidatabasecommit, msiquery/MsiDatabaseCommit, setup.msidatabasecommit
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: msiquery.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7. Windows Installer 4.0 or Windows Installer 4.5 on   Windows Server 2008 or Windows Vista. Windows Installer on Windows Server 2003 or Windows XP
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
 - MsiDatabaseCommit
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# MsiDatabaseCommit function


## -description


The 
<b>MsiDatabaseCommit</b> function commits changes to a database.


## -parameters




### -param hDatabase [in]

Handle to the database obtained from <a href="https://msdn.microsoft.com/984996e3-aa2c-49ff-9067-ebefd3afdecb">MsiOpenDatabase</a>.


## -returns



The 
<b>MsiDatabaseCommit</b> function returns one of the following values:




## -remarks



The 
<b>MsiDatabaseCommit</b> function finalizes the persistent form of the database. All persistent data is then written to the writable database. No temporary columns or rows are written. The 
<b>MsiDatabaseCommit</b> function has no effect on a database that is opened as read-only. You can call this function multiple times to save the current state of tables loaded into memory. When the database is finally closed, any changes made after the database is committed are rolled back. This function is normally called prior to shutdown when all database changes have been finalized.

If the function fails, you can obtain extended error information by using <a href="https://msdn.microsoft.com/0d6f4506-367b-43d7-ba1c-2a93c1d0cc51">MsiGetLastErrorRecord</a>.




## -see-also




<a href="database_functions.htm">General Database Access Functions</a>
 

 

