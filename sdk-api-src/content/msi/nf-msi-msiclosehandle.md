---
UID: NF:msi.MsiCloseHandle
title: MsiCloseHandle function (msi.h)
description: The MsiCloseHandle function closes an open installation handle.
helpviewer_keywords: ["MsiCloseHandle","MsiCloseHandle function","_msi_msiclosehandle","msi/MsiCloseHandle","setup.msiclosehandle"]
old-location: setup\msiclosehandle.htm
tech.root: setup
ms.assetid: b9e90ed4-fda8-4628-a713-67c651e1b572
ms.date: 12/05/2018
ms.keywords: MsiCloseHandle, MsiCloseHandle function, _msi_msiclosehandle, msi/MsiCloseHandle, setup.msiclosehandle
req.header: msi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7. Windows Installer 4.0 or Windows Installer 4.5 on   Windows Server 2008 or Windows Vista. Windows Installer on Windows Server 2003 or Windows XP. See the Windows Installer Run-Time Requirements for information about the minimum Windows service pack that is required by a Windows Installer version.
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - MsiCloseHandle
 - msi/MsiCloseHandle
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
 - MsiCloseHandle
---

# MsiCloseHandle function


## -description

The 
<b>MsiCloseHandle</b> function closes an open installation handle.

## -parameters

### -param hAny [in]

Specifies any open installation handle.

## -returns

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_HANDLE</b></dt>
</dl>
</td>
<td width="60%">
An invalid handle was passed to the function.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_SUCCESS</b></dt>
</dl>
</td>
<td width="60%">
The function succeeded.

</td>
</tr>
</table>
 


<div> </div>

## -remarks

<b>MsiCloseHandle</b> must be called from the same thread that requested the creation of the handle.

The following functions supply handles that should be closed after use by calling 
<b>MsiCloseHandle</b>:

<a href="/windows/desktop/api/msiquery/nf-msiquery-msicreaterecord">MsiCreateRecord</a>
<a href="/windows/desktop/api/msiquery/nf-msiquery-msigetactivedatabase">MsiGetActiveDatabase</a>
<a href="/windows/desktop/api/msiquery/nf-msiquery-msigetlasterrorrecord">MsiGetLastErrorRecord</a>
<a href="/windows/desktop/api/msi/nf-msi-msiopenpackagea">MsiOpenPackage</a>
<a href="/windows/desktop/api/msi/nf-msi-msiopenproducta">MsiOpenProduct</a>
<a href="/windows/desktop/api/msiquery/nf-msiquery-msiopendatabasea">MsiOpenDatabase</a>
<a href="/windows/desktop/api/msiquery/nf-msiquery-msidatabaseopenviewa">MsiDatabaseOpenView</a>
<a href="/windows/desktop/api/msiquery/nf-msiquery-msiviewfetch">MsiViewFetch</a>
<a href="/windows/desktop/api/msiquery/nf-msiquery-msiviewgetcolumninfo">MsiViewGetColumnInfo</a>
<a href="/windows/desktop/api/msiquery/nf-msiquery-msidatabasegetprimarykeysa">MsiDatabaseGetPrimaryKeys</a>
<a href="/windows/desktop/api/msiquery/nf-msiquery-msigetsummaryinformationa">MsiGetSummaryInformation</a>
<a href="/windows/desktop/api/msiquery/nf-msiquery-msienableuipreview">MsiEnableUIPreview</a>
Note that when writing custom actions, it is recommended to use variables of type PMSIHANDLE because the installer closes PMSIHANDLE objects as they go out of scope, whereas you must close MSIHANDLE objects by calling 
<b>MsiCloseHandle</b>.

For example, if you use code like this:

MSIHANDLE hRec = MsiCreateRecord(3);

Change it to:

PMSIHANDLE hRec = MsiCreateRecord(3);

## -see-also

<a href="/windows/desktop/Msi/installer-function-reference">Handle Management Functions</a>