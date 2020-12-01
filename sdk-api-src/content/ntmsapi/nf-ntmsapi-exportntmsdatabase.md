---
UID: NF:ntmsapi.ExportNtmsDatabase
title: ExportNtmsDatabase function (ntmsapi.h)
description: The ExportNtmsDatabase function creates a consistent set of database files in the RSM database directory.
helpviewer_keywords: ["ExportNtmsDatabase","ExportNtmsDatabase function [Files]","_zaw_exportntmsdatabase","base.exportntmsdatabase","fs.exportntmsdatabase","ntmsapi/ExportNtmsDatabase"]
old-location: fs\exportntmsdatabase.htm
tech.root: fs
ms.assetid: 0c6df5d3-c771-4749-8fbd-de5c02ffa5d9
ms.date: 12/05/2018
ms.keywords: ExportNtmsDatabase, ExportNtmsDatabase function [Files], _zaw_exportntmsdatabase, base.exportntmsdatabase, fs.exportntmsdatabase, ntmsapi/ExportNtmsDatabase
req.header: ntmsapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Ntmsapi.lib
req.dll: Ntmsapi.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ExportNtmsDatabase
 - ntmsapi/ExportNtmsDatabase
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Ntmsapi.dll
api_name:
 - ExportNtmsDatabase
---

# ExportNtmsDatabase function


## -description

<p class="CCE_Message">[<a href="/previous-versions/windows/desktop/bb540725(v=vs.85)">Removable Storage Manager</a> is no longer available as of Windows 7 and  Windows Server 2008 R2.]

The 
<b>ExportNtmsDatabase</b> function creates a consistent set of database files in the RSM database directory.

## -parameters

### -param hSession [in]

Handle to the session returned by the 
<a href="/windows/desktop/api/ntmsapi/nf-ntmsapi-openntmssessiona">OpenNtmsSession</a> function.

## -returns

This function returns one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_ACCESS_DENIED</b></dt>
</dl>
</td>
<td width="60%">
Access to one or more RSM objects is denied.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_DATABASE_FAILURE</b></dt>
</dl>
</td>
<td width="60%">
The database query or update failed.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_HANDLE</b></dt>
</dl>
</td>
<td width="60%">
The value specified in the <i>hSession</i> parameter is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NOT_CONNECTED</b></dt>
</dl>
</td>
<td width="60%">
Unable to connect to the RSM service.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_SHARING_VIOLATION</b></dt>
</dl>
</td>
<td width="60%">
One of the files that the function must write to is open.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_SUCCESS</b></dt>
</dl>
</td>
<td width="60%">
The function was successful.

</td>
</tr>
</table>

## -remarks

The 
<b>ExportNtmsDatabase</b> function is used by backup applications to create a copy of the RSM database. Any existing files in the Export directory are overwritten by this function.

The default location of the database is%SystemRoot%\System32\NtmsData, but this can be set by defining a registry value:

<b>HKLM</b>&#92;<b>System</b>&#92;<b>CurrentControlSet</b>&#92;<b>Control</b>&#92;<b>NTMS</b>&#92;<b>NtmsData</b>

This function creates a subdirectory called Export and places the consistent files there.

## -see-also

<a href="/previous-versions/windows/desktop/rsm/removable-storage-manager-functions">Database Backup and Recovery Functions</a>



<a href="/windows/desktop/api/ntmsapi/nf-ntmsapi-importntmsdatabase">ImportNtmsDatabase</a>