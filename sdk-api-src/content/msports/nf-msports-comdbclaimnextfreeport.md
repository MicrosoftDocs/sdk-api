---
UID: NF:msports.ComDBClaimNextFreePort
title: ComDBClaimNextFreePort function
author: windows-sdk-content
description: ComDBClaimNextFreePort returns the lowest COM port number that is not already in use.
old-location: serports\comdbclaimnextfreeport.htm
old-project: serports
ms.assetid: b32b42e8-d38c-4bb5-bf8a-96538a03cb5b
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: ComDBClaimNextFreePort, ComDBClaimNextFreePort function [Serial Ports], comdb_ed1e04f0-bebb-4d9f-8603-20e7d15b7644.xml, msports/ComDBClaimNextFreePort, serports.comdbclaimnextfreeport
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: msports.h
req.include-header: Msports.h
req.redist: 
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
tech.root: 
req.typenames: MSPEVENTITEM, *PMSPEVENTITEM
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Msports.dll
api_name:
 - ComDBClaimNextFreePort
product: Windows
targetos: Windows
req.lib: Msports.lib
req.dll: Msports.dll
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# ComDBClaimNextFreePort function


## -description


<b>ComDBClaimNextFreePort</b> returns the lowest COM port number that is not already in use.


## -parameters




### -param HComDB [in]

Handle to the COM port database that is returned by <a href="https://msdn.microsoft.com/6ae22de0-b71e-441d-af12-8518a3f474e3">ComDBOpen</a>.


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

For more information, see <a href="https://msdn.microsoft.com/c9baf147-6e33-4ed2-b682-c141938eb0da">Obtaining and Releasing a COM Port Number</a>.




## -see-also




<a href="https://msdn.microsoft.com/d0baa783-1039-41a4-8bb1-78c977ed62b6">ComDBClaimPort</a>



<a href="https://msdn.microsoft.com/bece99c5-75de-4ab4-be26-14dc8cc1819c">ComDBReleasePort</a>
 

 

