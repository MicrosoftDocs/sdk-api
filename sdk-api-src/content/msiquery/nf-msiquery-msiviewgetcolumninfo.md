---
UID: NF:msiquery.MsiViewGetColumnInfo
title: MsiViewGetColumnInfo function
author: windows-sdk-content
description: The MsiViewGetColumnInfo function returns a record containing column names or definitions. This function returns a handle that should be closed using MsiCloseHandle.
old-location: setup\msiviewgetcolumninfo.htm
tech.root: msi
ms.assetid: f1b8e24c-ac90-4a25-a1d1-c005c403dffc
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: MSICOLINFO_NAMES, MSICOLINFO_TYPES, MsiViewGetColumnInfo, MsiViewGetColumnInfo function, _msi_msiviewgetcolumninfo, msiquery/MsiViewGetColumnInfo, setup.msiviewgetcolumninfo
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
 - MsiViewGetColumnInfo
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- MsiViewGetColumnInfo
: 
---

# MsiViewGetColumnInfo function


## -description


The 
<b>MsiViewGetColumnInfo</b> function returns a record containing column names or definitions. This function returns a handle that should be closed using 
<a href="https://msdn.microsoft.com/b9e90ed4-fda8-4628-a713-67c651e1b572">MsiCloseHandle</a>.


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
<a href="https://msdn.microsoft.com/77379664-26f2-4c1d-8c44-d9be2376efa9">Column Definition Format</a>. Each column is described by a string in the corresponding record field. The definition string consists of a single letter representing the data type followed by the width of the column (in characters when applicable, bytes otherwise). A width of zero designates an unbounded width (for example, long text fields and streams). An uppercase letter indicates that null values are allowed in the column.

Note that it is recommended to use variables of type PMSIHANDLE because the installer closes PMSIHANDLE objects as they go out of scope, whereas you must close MSIHANDLE objects by calling 
<a href="https://msdn.microsoft.com/b9e90ed4-fda8-4628-a713-67c651e1b572">MsiCloseHandle</a>. For more information see <a href="windows_installer_best_practices.htm">Use PMSIHANDLE instead of HANDLE</a> section in the <a href="https://msdn.microsoft.com/ff48d995-fe6f-4d1b-898d-67574ed3c5b7">Windows Installer Best Practices</a>.



