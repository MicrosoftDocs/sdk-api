---
UID: NF:msiquery.MsiOpenDatabaseA
title: MsiOpenDatabaseA function
author: windows-sdk-content
description: The MsiOpenDatabase function opens a database file for data access. This function returns a handle that should be closed using MsiCloseHandle.
old-location: setup\msiopendatabase.htm
old-project: Msi
ms.assetid: 984996e3-aa2c-49ff-9067-ebefd3afdecb
ms.author: windowssdkdev
ms.date: 07/24/2018
ms.keywords: MSIDBOPEN_CREATE, MSIDBOPEN_CREATEDIRECT, MSIDBOPEN_DIRECT, MSIDBOPEN_PATCHFILE, MSIDBOPEN_READONLY, MSIDBOPEN_TRANSACT, MsiOpenDatabase, MsiOpenDatabase function, MsiOpenDatabaseA, MsiOpenDatabaseW, _msi_msiopendatabase, msiquery/MsiOpenDatabase, msiquery/MsiOpenDatabaseA, msiquery/MsiOpenDatabaseW, setup.msiopendatabase
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: msiquery.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7. Windows Installer 4.0 or Windows Installer 4.5 on   Windows Server 2008 or Windows Vista. Windows Installer on Windows Server 2003 or Windows XP
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: MsiOpenDatabaseW (Unicode) and MsiOpenDatabaseA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: InkRecoGuide
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Msi.dll
 - Ext-MS-Win-MSI-Misc-l1-1-0.dll
api_name:
 - MsiOpenDatabase
 - MsiOpenDatabaseA
 - MsiOpenDatabaseW
product: Windows
targetos: Windows
req.lib: Msi.lib
req.dll: Msi.dll
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# MsiOpenDatabaseA function


## -description


The 
<b>MsiOpenDatabase</b> function opens a database file for data access. This function returns a handle that should be closed using 
<a href="https://msdn.microsoft.com/b9e90ed4-fda8-4628-a713-67c651e1b572">MsiCloseHandle</a>.


## -parameters




### -param szDatabasePath [in]

Specifies the full path or relative path to the database file.


### -param szPersist [in]

Receives the full path to the file or the persistence mode. You can use the <i>szPersist</i> parameter to direct the persistent output to a new file or to specify one of the following predefined persistence modes.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="MSIDBOPEN_CREATEDIRECT"></a><a id="msidbopen_createdirect"></a><dl>
<dt><b>MSIDBOPEN_CREATEDIRECT</b></dt>
</dl>
</td>
<td width="60%">
Create a new database, direct mode read/write.

</td>
</tr>
<tr>
<td width="40%"><a id="MSIDBOPEN_CREATE"></a><a id="msidbopen_create"></a><dl>
<dt><b>MSIDBOPEN_CREATE</b></dt>
</dl>
</td>
<td width="60%">
Create a new database, transact mode read/write.

</td>
</tr>
<tr>
<td width="40%"><a id="MSIDBOPEN_DIRECT"></a><a id="msidbopen_direct"></a><dl>
<dt><b>MSIDBOPEN_DIRECT</b></dt>
</dl>
</td>
<td width="60%">
Open a database direct read/write without transaction.

</td>
</tr>
<tr>
<td width="40%"><a id="MSIDBOPEN_READONLY"></a><a id="msidbopen_readonly"></a><dl>
<dt><b>MSIDBOPEN_READONLY</b></dt>
</dl>
</td>
<td width="60%">
Open a database read-only, no persistent changes.

</td>
</tr>
<tr>
<td width="40%"><a id="MSIDBOPEN_TRANSACT"></a><a id="msidbopen_transact"></a><dl>
<dt><b>MSIDBOPEN_TRANSACT</b></dt>
</dl>
</td>
<td width="60%">
Open a database read/write in transaction mode.

</td>
</tr>
<tr>
<td width="40%"><a id="MSIDBOPEN_PATCHFILE"></a><a id="msidbopen_patchfile"></a><dl>
<dt><b>MSIDBOPEN_PATCHFILE</b></dt>
</dl>
</td>
<td width="60%">
Add this flag to indicate a patch file.

</td>
</tr>
</table>
 


### -param phDatabase [out]

Pointer to the location of the returned database handle.


## -returns




					The 
<b>MsiOpenDatabase</b> function returns the following values:




## -remarks



To make and save changes to a database first open the database in transaction (MSIDBOPEN_TRANSACT), create (MSIDBOPEN_CREATE or MSIDBOPEN_CREATEDIRECT), or direct (MSIDBOPEN_DIRECT) mode. After making the changes, always call 
<a href="https://msdn.microsoft.com/bc42b90b-51db-4e13-af2f-4942923badf6">MsiDatabaseCommit</a> before closing the database handle. 
<b>MsiDatabaseCommit</b> flushes all buffers.

Always call 
<a href="https://msdn.microsoft.com/bc42b90b-51db-4e13-af2f-4942923badf6">MsiDatabaseCommit</a> on a database that has been opened in direct mode (MSIDBOPEN_DIRECT or MSIDBOPEN_CREATEDIRECT) before closing the database's handle. Failure to do this may corrupt the database.

Because 
<b>MsiOpenDatabase</b> initiates database access, it cannot be used with a running installation.

Note that it is recommended to use variables of type PMSIHANDLE because the installer closes PMSIHANDLE objects as they go out of scope, whereas you must close MSIHANDLE objects by calling 
<a href="https://msdn.microsoft.com/b9e90ed4-fda8-4628-a713-67c651e1b572">MsiCloseHandle</a>. For more information see <a href="windows_installer_best_practices.htm">Use PMSIHANDLE instead of HANDLE</a> section in the <a href="https://msdn.microsoft.com/ff48d995-fe6f-4d1b-898d-67574ed3c5b7">Windows Installer Best Practices</a>.

<div class="alert"><b>Note</b>  When a database is opened as the output of another database, the summary information stream of the output database is actually a read-only mirror of the original database, and, thus, cannot be changed. Additionally, it is not persisted with the database. To create or modify the summary information for the output database, it must be closed and reopened.</div>
<div> </div>
If the function fails, you can obtain extended error information by using <a href="https://msdn.microsoft.com/0d6f4506-367b-43d7-ba1c-2a93c1d0cc51">MsiGetLastErrorRecord</a>.




## -see-also




<a href="https://msdn.microsoft.com/54a8d571-ebc3-42d5-bc34-8f29b245b4d8">A Database and Patch Example</a>



<a href="database_functions.htm">General Database Access Functions</a>
 

 

