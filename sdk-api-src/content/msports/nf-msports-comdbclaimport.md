---
UID: NF:msports.ComDBClaimPort
title: ComDBClaimPort function (msports.h)
description: ComDBClaimPort logs an unused COM port number as &quot;in use&quot; in the COM port database.
helpviewer_keywords: ["ComDBClaimPort","ComDBClaimPort function [Serial Ports]","comdb_e636ae45-1105-4322-9429-f8bf24333432.xml","msports/ComDBClaimPort","serports.comdbclaimport"]
old-location: serports\comdbclaimport.htm
tech.root: serports
ms.assetid: d0baa783-1039-41a4-8bb1-78c977ed62b6
ms.date: 12/05/2018
ms.keywords: ComDBClaimPort, ComDBClaimPort function [Serial Ports], comdb_e636ae45-1105-4322-9429-f8bf24333432.xml, msports/ComDBClaimPort, serports.comdbclaimport
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
 - ComDBClaimPort
 - msports/ComDBClaimPort
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
 - ComDBClaimPort
---

# ComDBClaimPort function


## -description

<b>ComDBClaimPort</b> logs an unused COM port number as "in use" in the COM port database.

## -parameters

### -param HComDB [in]

Handle to the COM port database that is returned by <a href="/windows/desktop/api/msports/nf-msports-comdbopen">ComDBOpen</a>.

### -param ComNumber [in]

Specifies which COM port number the caller attempts to claim. A port number is an integer that can range from 1 to COMDB_MAX_PORTS_ARBITRATED.

### -param ForceClaim [in]

Reserved for internal use only.

### -param Forced [out, optional]

Reserved for internal use only.

## -returns

<b>ComDBClaimPort</b> returns one of the following status values.

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
The COM port number was not in use and is now logged as "in use".

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
One of the following is true: The specified handle to the COM port database is not valid. The specified port number is greater than COMDB_MAX_PORTS_ARBITRATED.

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
<dt><b>ERROR_SHARING_VIOLATION</b></dt>
</dl>
</td>
<td width="60%">
The specified port number is already in use.

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

<b>ComDBClaimPort</b> runs in user mode.

For more information, see <a href="/previous-versions/ff546481(v=vs.85)">Obtaining and Releasing a COM Port Number</a>.

## -see-also

<a href="/windows/desktop/api/msports/nf-msports-comdbclaimnextfreeport">ComDBClaimNextFreePort</a>



<a href="/windows/desktop/api/msports/nf-msports-comdbreleaseport">ComDBReleasePort</a>