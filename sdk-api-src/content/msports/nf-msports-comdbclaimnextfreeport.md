---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
---

# ComDBClaimNextFreePort function


## -description


<b>ComDBClaimNextFreePort</b> returns the lowest COM port number that is not already in use.


## -parameters




### -param HComDB [in]

Handle to the COM port database that is returned by <a href="https://msdn.microsoft.com/library/windows/hardware/ff546476">ComDBOpen</a>.


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




<a href="https://msdn.microsoft.com/library/windows/hardware/ff546472">ComDBClaimPort</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff546477">ComDBReleasePort</a>
 

 

