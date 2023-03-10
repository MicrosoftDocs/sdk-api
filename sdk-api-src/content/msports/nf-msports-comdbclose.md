---
UID: NF:msports.ComDBClose
title: ComDBClose function (msports.h)
description: ComDBClose closes a handle to the COM port database.
helpviewer_keywords: ["ComDBClose","ComDBClose function [Serial Ports]","comdb_0274a1cb-0128-48c8-b536-3a10792582f4.xml","msports/ComDBClose","serports.comdbclose"]
old-location: serports\comdbclose.htm
tech.root: serports
ms.assetid: 3ea720ba-6cc9-4862-83d2-4f87e5c13da4
ms.date: 12/05/2018
ms.keywords: ComDBClose, ComDBClose function [Serial Ports], comdb_0274a1cb-0128-48c8-b536-3a10792582f4.xml, msports/ComDBClose, serports.comdbclose
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
 - ComDBClose
 - msports/ComDBClose
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
 - ComDBClose
---

# ComDBClose function


## -description

<b>ComDBClose</b> closes a handle to the COM port database.

## -parameters

### -param HComDB [in]

Handle to the COM port database that was returned by <a href="/windows/desktop/api/msports/nf-msports-comdbopen">ComDBOpen</a>.

## -returns

<b>ComDBClose</b> returns one of the following status values.

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
The COM port database was closed.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
The specified COM port database handle is not valid.

</td>
</tr>
</table>

## -remarks

To open the COM port database, call <b>ComDBOpen</b>.

<b>ComDBOpen</b> is called from user mode.

For more information, see <a href="/previous-versions/ff546481(v=vs.85)">Opening and Closing the COM Port Database</a>.

## -see-also

<a href="/windows/desktop/api/msports/nf-msports-comdbopen">ComDBOpen</a>