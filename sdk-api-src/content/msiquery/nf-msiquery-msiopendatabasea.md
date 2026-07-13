---
UID: NF:msiquery.MsiOpenDatabaseA
title: MsiOpenDatabaseA function (msiquery.h)
description: The MsiOpenDatabase function opens a database file for data access. This function returns a handle that should be closed using MsiCloseHandle. (ANSI)
helpviewer_keywords: ["MSIDBOPEN_CREATE", "MSIDBOPEN_CREATEDIRECT", "MSIDBOPEN_DIRECT", "MSIDBOPEN_PATCHFILE", "MSIDBOPEN_READONLY", "MSIDBOPEN_TRANSACT", "MsiOpenDatabaseA", "msiquery/MsiOpenDatabaseA"]
old-location: setup\msiopendatabase.htm
tech.root: setup
ms.assetid: 984996e3-aa2c-49ff-9067-ebefd3afdecb
ms.date: 12/05/2018
ms.keywords: MSIDBOPEN_CREATE, MSIDBOPEN_CREATEDIRECT, MSIDBOPEN_DIRECT, MSIDBOPEN_PATCHFILE, MSIDBOPEN_READONLY, MSIDBOPEN_TRANSACT, MsiOpenDatabase, MsiOpenDatabase function, MsiOpenDatabaseA, MsiOpenDatabaseW, _msi_msiopendatabase, msiquery/MsiOpenDatabase, msiquery/MsiOpenDatabaseA, msiquery/MsiOpenDatabaseW, setup.msiopendatabase
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
req.lib: Msi.lib
req.dll: Msi.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - MsiOpenDatabaseA
 - msiquery/MsiOpenDatabaseA
dev_langs:
 - c++
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
---

# MsiOpenDatabaseA function


## -description

The 
<b>MsiOpenDatabase</b> function opens a database file for data access. This function returns a handle that should be closed using 
<a href="/windows/desktop/api/msi/nf-msi-msiclosehandle">MsiCloseHandle</a>.

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
<a href="/windows/desktop/api/msiquery/nf-msiquery-msidatabasecommit">MsiDatabaseCommit</a> before closing the database handle. 
<b>MsiDatabaseCommit</b> flushes all buffers.

Always call 
<a href="/windows/desktop/api/msiquery/nf-msiquery-msidatabasecommit">MsiDatabaseCommit</a> on a database that has been opened in direct mode (MSIDBOPEN_DIRECT or MSIDBOPEN_CREATEDIRECT) before closing the database's handle. Failure to do this may corrupt the database.

Because 
<b>MsiOpenDatabase</b> initiates database access, it cannot be used with a running installation.

Note that it is recommended to use variables of type PMSIHANDLE because the installer closes PMSIHANDLE objects as they go out of scope, whereas you must close MSIHANDLE objects by calling 
<a href="/windows/desktop/api/msi/nf-msi-msiclosehandle">MsiCloseHandle</a>. For more information see <a href="/windows/desktop/Msi/windows-installer-best-practices">Use PMSIHANDLE instead of HANDLE</a> section in the <a href="/windows/desktop/Msi/windows-installer-best-practices">Windows Installer Best Practices</a>.

<div class="alert"><b>Note</b>  When a database is opened as the output of another database, the summary information stream of the output database is actually a read-only mirror of the original database, and, thus, cannot be changed. Additionally, it is not persisted with the database. To create or modify the summary information for the output database, it must be closed and reopened.</div>
<div> </div>
If the function fails, you can obtain extended error information by using <a href="/windows/desktop/api/msiquery/nf-msiquery-msigetlasterrorrecord">MsiGetLastErrorRecord</a>.





> [!NOTE]
> The msiquery.h header defines MsiOpenDatabase as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/Msi/a-database-and-patch-example">A Database and Patch Example</a>



<a href="/windows/desktop/Msi/database-functions">General Database Access Functions</a>
