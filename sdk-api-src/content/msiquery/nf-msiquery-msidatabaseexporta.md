---
UID: NF:msiquery.MsiDatabaseExportA
title: MsiDatabaseExportA function (msiquery.h)
author: windows-sdk-content
description: The MsiDatabaseExport function exports a Microsoft Installer table from an open database to a Text Archive File.
old-location: setup\msidatabaseexport.htm
tech.root: Msi
ms.assetid: c20c168d-900e-496a-894c-5678f308cdbe
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: MsiDatabaseExport, MsiDatabaseExport function, MsiDatabaseExportA, MsiDatabaseExportW, _msi_msidatabaseexport, msiquery/MsiDatabaseExport, msiquery/MsiDatabaseExportA, msiquery/MsiDatabaseExportW, setup.msidatabaseexport
ms.topic: function
req.header: msiquery.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7. Windows Installer 4.0 or Windows Installer 4.5 on   Windows Server 2008 or Windows Vista. Windows Installer on Windows Server 2003 or Windows XP
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: MsiDatabaseExportW (Unicode) and MsiDatabaseExportA (ANSI)
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
 - MsiDatabaseExport
 - MsiDatabaseExportA
 - MsiDatabaseExportW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# MsiDatabaseExportA function


## -description


The 
<b>MsiDatabaseExport</b> function exports a Microsoft Installer table from an open database to a <a href="https://docs.microsoft.com/windows/desktop/Msi/text-archive-files">Text Archive File</a>.


## -parameters




### -param hDatabase [in]

The handle to a database  from <a href="https://docs.microsoft.com/windows/desktop/api/msiquery/nf-msiquery-msiopendatabasea">MsiOpenDatabase</a>.


### -param szTableName [in]

The name of the table to export.


### -param szFolderPath [in]

The name of the folder that contains archive files.


### -param szFileName [in]

The name of the exported table archive file.


## -returns



The 
<b>MsiDatabaseExport</b> function returns one of the following values:

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_BAD_PATHNAME</b></dt>
</dl>
</td>
<td width="60%">
An invalid path is passed to the function.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_FUNCTION_FAILED</b></dt>
</dl>
</td>
<td width="60%">
The function fails.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_HANDLE</b></dt>
</dl>
</td>
<td width="60%">
An invalid or inactive handle is supplied.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
An invalid parameter is passed to the function.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_SUCCESS</b></dt>
</dl>
</td>
<td width="60%">
The function succeeds.

</td>
</tr>
</table>
 




## -remarks



If a table contains streams, 
<b>MsiDatabaseExport</b> exports each stream to a separate file.

For more information, see 
<a href="https://docs.microsoft.com/windows/desktop/api/msiquery/nf-msiquery-msidatabaseimporta">MsiDatabaseImport</a>.

This function cannot be called from custom actions. A call to this function from a custom action causes the function to fail.

If the function fails, you can get extended error information by using <a href="https://docs.microsoft.com/windows/desktop/api/msiquery/nf-msiquery-msigetlasterrorrecord">MsiGetLastErrorRecord</a>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/Msi/database-functions">Database Management Functions</a>



<a href="https://docs.microsoft.com/windows/desktop/Msi/text-archive-files">Text Archive Files</a>
 

 

