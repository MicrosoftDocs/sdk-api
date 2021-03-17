---
UID: NF:ntmsapi.ImportNtmsDatabase
title: ImportNtmsDatabase function (ntmsapi.h)
description: The ImportNtmsDatabase function causes RSM to import the database files from the database Export directory at the next restart of the RSM.
helpviewer_keywords: ["ImportNtmsDatabase","ImportNtmsDatabase function [Files]","_zaw_importntmsdatabase","base.importntmsdatabase","fs.importntmsdatabase","ntmsapi/ImportNtmsDatabase"]
old-location: fs\importntmsdatabase.htm
tech.root: fs
ms.assetid: 9bb41109-6548-4d22-92c8-0d8ed960f119
ms.date: 12/05/2018
ms.keywords: ImportNtmsDatabase, ImportNtmsDatabase function [Files], _zaw_importntmsdatabase, base.importntmsdatabase, fs.importntmsdatabase, ntmsapi/ImportNtmsDatabase
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
 - ImportNtmsDatabase
 - ntmsapi/ImportNtmsDatabase
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
 - ImportNtmsDatabase
---

# ImportNtmsDatabase function


## -description

<p class="CCE_Message">[<a href="/previous-versions/windows/desktop/bb540725(v=vs.85)">Removable Storage Manager</a> is no longer available as of Windows 7 and  Windows Server 2008 R2.]

The 
<b>ImportNtmsDatabase</b> function causes RSM to import the database files from the database Export directory at the next restart of the RSM.

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
Access to at least one RSM object is denied.

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
Unable to connect to the RSM.

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
<b>ImportNtmsDatabase</b> function is used by backup applications during disaster recovery.

## -see-also

<a href="/previous-versions/windows/desktop/rsm/removable-storage-manager-functions">Database Backup and Recovery Functions</a>



<a href="/windows/desktop/api/ntmsapi/nf-ntmsapi-exportntmsdatabase">ExportNtmsDatabase</a>