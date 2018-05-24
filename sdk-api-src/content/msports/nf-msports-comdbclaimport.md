---
UID: NF:msports.ComDBClaimPort
title: ComDBClaimPort function
author: windows-driver-content
description: ComDBClaimPort logs an unused COM port number as &#0034;in use&#0034; in the COM port database.
old-location: serports\comdbclaimport.htm
old-project: serports
ms.assetid: d0baa783-1039-41a4-8bb1-78c977ed62b6
ms.author: windowsdriverdev
ms.date: 4/23/2018
ms.keywords: ComDBClaimPort, ComDBClaimPort function [Serial Ports], comdb_e636ae45-1105-4322-9429-f8bf24333432.xml, msports/ComDBClaimPort, serports.comdbclaimport
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
req.typenames: MSPEVENTITEM, *PMSPEVENTITEM
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Msports.dll
api_name:
-	ComDBClaimPort
product: Windows
targetos: Windows
req.lib: Msports.lib
req.dll: Msports.dll
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# ComDBClaimPort function


## -description


<b>ComDBClaimPort</b> logs an unused COM port number as "in use" in the COM port database.


## -parameters




### -param HComDB [in]

Handle to the COM port database that is returned by <a href="https://msdn.microsoft.com/library/windows/hardware/ff546476">ComDBOpen</a>.


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

For more information, see <a href="https://msdn.microsoft.com/c9baf147-6e33-4ed2-b682-c141938eb0da">Obtaining and Releasing a COM Port Number</a>.




## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff546469">ComDBClaimNextFreePort</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff546477">ComDBReleasePort</a>
 

 

