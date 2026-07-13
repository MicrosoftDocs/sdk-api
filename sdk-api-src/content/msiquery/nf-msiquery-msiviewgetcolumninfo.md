---
UID: NF:msiquery.MsiViewGetColumnInfo
title: MsiViewGetColumnInfo function (msiquery.h)
description: The MsiViewGetColumnInfo function returns a record containing column names or definitions. This function returns a handle that should be closed using MsiCloseHandle.
helpviewer_keywords: ["MSICOLINFO_NAMES","MSICOLINFO_TYPES","MsiViewGetColumnInfo","MsiViewGetColumnInfo function","_msi_msiviewgetcolumninfo","msiquery/MsiViewGetColumnInfo","setup.msiviewgetcolumninfo"]
old-location: setup\msiviewgetcolumninfo.htm
tech.root: setup
ms.assetid: f1b8e24c-ac90-4a25-a1d1-c005c403dffc
ms.date: 12/05/2018
ms.keywords: MSICOLINFO_NAMES, MSICOLINFO_TYPES, MsiViewGetColumnInfo, MsiViewGetColumnInfo function, _msi_msiviewgetcolumninfo, msiquery/MsiViewGetColumnInfo, setup.msiviewgetcolumninfo
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - MsiViewGetColumnInfo
 - msiquery/MsiViewGetColumnInfo
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ext-ms-win-msi-misc-l1-1-0.dll
 - Msi.dll
api_name:
 - MsiViewGetColumnInfo
---

# MsiViewGetColumnInfo function


## -description

The 
<b>MsiViewGetColumnInfo</b> function returns a record containing column names or definitions. This function returns a handle that should be closed using 
<a href="/windows/desktop/api/msi/nf-msi-msiclosehandle">MsiCloseHandle</a>.

## -parameters

### -param hView [in]

Handle to the view from which to obtain column information.

### -param eColumnInfo [in]

Specifies a flag indicating what type of information is needed. This parameter must be one of the following values. 



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="MSICOLINFO_NAMES"></a><a id="msicolinfo_names"></a><dl>
<dt><b>MSICOLINFO_NAMES</b></dt>
</dl>
</td>
<td width="60%">
Column names are returned.

</td>
</tr>
<tr>
<td width="40%"><a id="MSICOLINFO_TYPES"></a><a id="msicolinfo_types"></a><dl>
<dt><b>MSICOLINFO_TYPES</b></dt>
</dl>
</td>
<td width="60%">
Definitions are returned.

</td>
</tr>
</table>

### -param phRecord [out]

Pointer to a handle to receive the column information data record.

## -returns

Note that in low memory situations, this function can raise a STATUS_NO_MEMORY exception.

## -remarks

The column description returned by 
<b>MsiViewGetColumnInfo</b> is in the format described in the section: 
<a href="/windows/desktop/Msi/column-definition-format">Column Definition Format</a>. Each column is described by a string in the corresponding record field. The definition string consists of a single letter representing the data type followed by the width of the column (in characters when applicable, bytes otherwise). A width of zero designates an unbounded width (for example, long text fields and streams). An uppercase letter indicates that null values are allowed in the column.

Note that it is recommended to use variables of type PMSIHANDLE because the installer closes PMSIHANDLE objects as they go out of scope, whereas you must close MSIHANDLE objects by calling 
<a href="/windows/desktop/api/msi/nf-msi-msiclosehandle">MsiCloseHandle</a>. For more information see <a href="/windows/desktop/Msi/windows-installer-best-practices">Use PMSIHANDLE instead of HANDLE</a> section in the <a href="/windows/desktop/Msi/windows-installer-best-practices">Windows Installer Best Practices</a>.