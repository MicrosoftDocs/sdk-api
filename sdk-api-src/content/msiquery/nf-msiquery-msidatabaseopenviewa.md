---
UID: NF:msiquery.MsiDatabaseOpenViewA
title: MsiDatabaseOpenViewA function (msiquery.h)
description: The MsiDatabaseOpenView function prepares a database query and creates a view object. This function returns a handle that should be closed using MsiCloseHandle. (ANSI)
helpviewer_keywords: ["MsiDatabaseOpenViewA", "msiquery/MsiDatabaseOpenViewA"]
old-location: setup\msidatabaseopenview.htm
tech.root: setup
ms.assetid: 1ef23f9a-7d79-4d07-9349-8e9c132f1b94
ms.date: 12/05/2018
ms.keywords: MsiDatabaseOpenView, MsiDatabaseOpenView function, MsiDatabaseOpenViewA, MsiDatabaseOpenViewW, _msi_msidatabaseopenview, msiquery/MsiDatabaseOpenView, msiquery/MsiDatabaseOpenViewA, msiquery/MsiDatabaseOpenViewW, setup.msidatabaseopenview
req.header: msiquery.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7. Windows Installer 4.0 or Windows Installer 4.5 on   Windows Server 2008 or Windows Vista. Windows Installer on Windows Server 2003 or Windows XP
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: MsiDatabaseOpenViewW (Unicode) and MsiDatabaseOpenViewA (ANSI)
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
 - MsiDatabaseOpenViewA
 - msiquery/MsiDatabaseOpenViewA
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
 - MsiDatabaseOpenView
 - MsiDatabaseOpenViewA
 - MsiDatabaseOpenViewW
---

# MsiDatabaseOpenViewA function


## -description

The 
<b>MsiDatabaseOpenView</b> function prepares a database query and creates a view object. This function returns a handle that should be closed using 
<a href="/windows/desktop/api/msi/nf-msi-msiclosehandle">MsiCloseHandle</a>.

## -parameters

### -param hDatabase [in]

Handle to the database to which you want to open a view object. You can get the handle as described in <a href="/windows/desktop/Msi/obtaining-a-database-handle">Obtaining a Database Handle</a>.

### -param szQuery [in]

Specifies a SQL query string for querying the database. For correct syntax, see 
<a href="/windows/desktop/Msi/sql-syntax">SQL Syntax</a>.

### -param phView [out]

Pointer to a handle for the returned view.

## -returns

The 
<b>MsiDatabaseOpenView</b> function returns one of the following values:

ERROR_SUCCESS if successful, and the view handle which the phView [out] parameter points to is set.

ERROR_INVALID_HANDLE, ERROR_INVALID_HANDLE_STATE, ERROR_BAD_QUERY_SYNTAX or ERROR_GEN_FAILURE if failure, and sets the error record, accessible via MsiGetLastErrorRecord.

## -remarks

The 
<b>MsiDatabaseOpenView</b> function opens a view object for a database. You must open a view object for a database before performing any execution or fetching.

If an error occurs, you can call 
<a href="/windows/desktop/api/msiquery/nf-msiquery-msigetlasterrorrecord">MsiGetLastErrorRecord</a> for more information.

Note that it is recommended to use variables of type PMSIHANDLE because the installer closes PMSIHANDLE objects as they go out of scope, whereas you must close MSIHANDLE objects by calling 
<a href="/windows/desktop/api/msi/nf-msi-msiclosehandle">MsiCloseHandle</a>. For more information see <a href="/windows/desktop/Msi/windows-installer-best-practices">Use PMSIHANDLE instead of HANDLE</a> section in the <a href="/windows/desktop/Msi/windows-installer-best-practices">Windows Installer Best Practices</a>.

If the function fails, you can obtain extended error information by using <a href="/windows/desktop/api/msiquery/nf-msiquery-msigetlasterrorrecord">MsiGetLastErrorRecord</a>.





> [!NOTE]
> The msiquery.h header defines MsiDatabaseOpenView as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/Msi/database-functions">General Database Access Functions</a>
