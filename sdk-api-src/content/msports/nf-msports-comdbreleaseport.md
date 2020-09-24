---
UID: NF:msports.ComDBReleasePort
title: ComDBReleasePort function (msports.h)
description: ComDBReleasePort releases a COM port number in the COM port database.
helpviewer_keywords: ["ComDBReleasePort","ComDBReleasePort function [Serial Ports]","comdb_dd9f4f27-aea1-4bd8-aa59-ca5aaa05e210.xml","msports/ComDBReleasePort","serports.comdbreleaseport"]
old-location: serports\comdbreleaseport.htm
tech.root: serports
ms.assetid: bece99c5-75de-4ab4-be26-14dc8cc1819c
ms.date: 12/05/2018
ms.keywords: ComDBReleasePort, ComDBReleasePort function [Serial Ports], comdb_dd9f4f27-aea1-4bd8-aa59-ca5aaa05e210.xml, msports/ComDBReleasePort, serports.comdbreleaseport
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
 - ComDBReleasePort
 - msports/ComDBReleasePort
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
 - ComDBReleasePort
---

# ComDBReleasePort function


## -description

<b>ComDBReleasePort</b> releases a COM port number in the COM port database.

## -parameters

### -param HComDB [in]

Handle to the COM port database that was returned by <a href="/windows/desktop/api/msports/nf-msports-comdbopen">ComDBOpen</a>.

### -param ComNumber [in]

Specifies the COM port number to release. A port number is an integer that ranges from one to COMDB_MAX_PORTS_ARBITRATED.

## -returns

<b>ComDBReleasePort</b> returns one of the following status values.

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
The COM port number was released.

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
One of the following is true: The specified handle to the COM port database is not valid. The specified port number is not in the COM port database.

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

<i>Releasing</i> a COM port number means to log the port number as "not in use".

<b>ComDBReleasePort</b> runs in user mode.

For more information, see <a href="/previous-versions/ff546481(v=vs.85)">Obtaining and Releasing a COM Port Number</a>.

## -see-also

<a href="/windows/desktop/api/msports/nf-msports-comdbclaimnextfreeport">ComDBClaimNextFreePort</a>



<a href="/windows/desktop/api/msports/nf-msports-comdbclaimport">ComDBClaimPort</a>