---
UID: NF:msports.ComDBResizeDatabase
title: ComDBResizeDatabase function (msports.h)
description: ComDBResizeDatabase resizes the COM port database.
helpviewer_keywords: ["ComDBResizeDatabase","ComDBResizeDatabase function [Serial Ports]","comdb_b0a32b8b-517e-45af-970a-7f192e5434fb.xml","msports/ComDBResizeDatabase","serports.comdbresizedatabase"]
old-location: serports\comdbresizedatabase.htm
tech.root: serports
ms.assetid: fef761be-57c5-4188-8de9-dbca31d91870
ms.date: 12/05/2018
ms.keywords: ComDBResizeDatabase, ComDBResizeDatabase function [Serial Ports], comdb_b0a32b8b-517e-45af-970a-7f192e5434fb.xml, msports/ComDBResizeDatabase, serports.comdbresizedatabase
req.header: msports.h
req.include-header: Msports.h
req.target-type: Desktop
req.target-min-winverclnt: 
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
req.lib: Msports.lib
req.dll: Msports.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ComDBResizeDatabase
 - msports/ComDBResizeDatabase
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Msports.dll
api_name:
 - ComDBResizeDatabase
---

# ComDBResizeDatabase function


## -description

<b>ComDBResizeDatabase</b> resizes the COM port database.

## -parameters

### -param HComDB [in]

Handle to the COM port database that was returned by <a href="/windows/desktop/api/msports/nf-msports-comdbopen">ComDBOpen</a>.

### -param NewSize [in]

Specifies a new size for the COM port database, where the database size is the number of port numbers currently arbitrated in the database. This value must be an integer multiple of 1024, must be greater than the current size, and must be less than or equal to COMDB_MAX_PORTS_ARBITRATED.

## -returns

<b>ComDBResizeDatabase</b> returns one of the following status values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_SUCCESS</b></dt>
</dl>
</td>
<td width="60%">
The database was successfully resized.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_BAD_LENGTH</b></dt>
</dl>
</td>
<td width="60%">
<i>NewSize</i> is less than or equal to the current database size, or it is greater than COMDB_MAX_PORTS_ARBITRATED.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_CANTWRITE</b></dt>
</dl>
</td>
<td width="60%">
The routine could not write to the database.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
One of the following is true: The specified handle to the COM port database is not valid. <i>NewSize</i> is not a multiple of 1024.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NOT_CONNECTED</b></dt>
</dl>
</td>
<td width="60%">
The routine could not access the database. To get extended error information, call <b>GetLastError</b>.

</td>
</tr>
</table>

## -remarks

Use <a href="/windows/desktop/api/msports/nf-msports-comdbgetcurrentportusage">ComDBGetCurrentPortUsage</a> to obtain the current database size.

<b>ComDBResizeDatabase</b> runs in user mode.

For more information, see <a href="/previous-versions/ff546481(v=vs.85)">Resizing the COM Port Database</a>.

## -see-also

<a href="/windows/desktop/api/msports/nf-msports-comdbgetcurrentportusage">ComDBGetCurrentPortUsage</a>