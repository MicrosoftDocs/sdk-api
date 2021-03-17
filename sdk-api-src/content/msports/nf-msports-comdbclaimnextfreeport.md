---
UID: NF:msports.ComDBClaimNextFreePort
title: ComDBClaimNextFreePort function (msports.h)
description: ComDBClaimNextFreePort returns the lowest COM port number that is not already in use.
helpviewer_keywords: ["ComDBClaimNextFreePort","ComDBClaimNextFreePort function [Serial Ports]","comdb_ed1e04f0-bebb-4d9f-8603-20e7d15b7644.xml","msports/ComDBClaimNextFreePort","serports.comdbclaimnextfreeport"]
old-location: serports\comdbclaimnextfreeport.htm
tech.root: serports
ms.assetid: b32b42e8-d38c-4bb5-bf8a-96538a03cb5b
ms.date: 12/05/2018
ms.keywords: ComDBClaimNextFreePort, ComDBClaimNextFreePort function [Serial Ports], comdb_ed1e04f0-bebb-4d9f-8603-20e7d15b7644.xml, msports/ComDBClaimNextFreePort, serports.comdbclaimnextfreeport
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
 - ComDBClaimNextFreePort
 - msports/ComDBClaimNextFreePort
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
 - ComDBClaimNextFreePort
---

# ComDBClaimNextFreePort function


## -description

<b>ComDBClaimNextFreePort</b> returns the lowest COM port number that is not already in use.

## -parameters

### -param HComDB [in]

Handle to the COM port database that is returned by <a href="/windows/desktop/api/msports/nf-msports-comdbopen">ComDBOpen</a>.

### -param ComNumber [out]

Pointer to the COM port number that the routine returns to the caller. This pointer must be non-NULL. A port number is an integer that ranges from 1 to COMDB_MAX_PORTS_ARBITRATED.

## -returns

<b>ComDBClaimNextFreePort</b> returns one of the following status values.

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
The routine successfully returned a COM port number.

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
The specified COM port database handle is not valid. 

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NO_LOG_SPACE</b></dt>
</dl>
</td>
<td width="60%">
The database cannot arbitrate any more port numbers.

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
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_Xxx</b></dt>
</dl>
</td>
<td width="60%">
An internal error occurred; call <b>GetLastError</b> to get extended error information.

</td>
</tr>
</table>

## -remarks

<i>Claiming</i> a COM port number in the COM port database logs the port number as "in use". Note that the database does not contain information about the caller or device that claims a port number.

<b>ComDBClaimNextFreePort</b> runs in user mode.

For more information, see <a href="/previous-versions/ff546481(v=vs.85)">Obtaining and Releasing a COM Port Number</a>.

## -see-also

<a href="/windows/desktop/api/msports/nf-msports-comdbclaimport">ComDBClaimPort</a>



<a href="/windows/desktop/api/msports/nf-msports-comdbreleaseport">ComDBReleasePort</a>