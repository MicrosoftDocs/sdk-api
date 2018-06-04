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

# PeerDistUnregisterForStatusChangeNotification function


## -description


The <b>PeerDistUnregisterForStatusChangeNotification</b> function unregisters the status change notification for the session associated with the specified handle.


## -parameters




### -param hPeerDist [in]

A <b>PEERDIST_INSTANCE_HANDLE</b> returned by <a href="https://msdn.microsoft.com/62d4f139-ab18-4d65-bda5-1cf09d7ddab9">PeerDistStartup</a>.


## -returns



If the function succeeds, the return value is <b>ERROR_SUCCESS</b>. Otherwise, the function may return one of the following values:

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
One or more parameters are invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_HANDLE</b></dt>
</dl>
</td>
<td width="60%">
The <i>hPeerDist</i> handle is invalid.

</td>
</tr>
</table>
 




## -remarks



This function cancels any registered notification  previously set by a <a href="https://msdn.microsoft.com/7b01a499-534b-4c0f-9c9c-bafa066ad742">PeerDistRegisterForStatusChangeNotification</a> function call.

To confirm successfully canceled operations, a call should be made to <a href="http://go.microsoft.com/fwlink/p/?linkid=131012">GetOverlappedResult</a> using the <b>OVERLAPPED</b> structure returned by <a href="http://go.microsoft.com/fwlink/p/?linkid=131008">GetQueuedCompletionStatus</a> with an expected return of <b>FALSE</b>.

Additionally, calling <a href="http://go.microsoft.com/fwlink/p/?linkid=131013">GetLastError</a> immediately after a successful <a href="https://msdn.microsoft.com/7b01a499-534b-4c0f-9c9c-bafa066ad742">PeerDistRegisterForStatusChangeNotification</a> will return the <b>ERROR_OPERATION_ABORTED</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/7b01a499-534b-4c0f-9c9c-bafa066ad742">PeerDistRegisterForStatusChangeNotification</a>
 

 

