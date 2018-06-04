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

# PeerCollabCloseHandle function


## -description


The <b>PeerCollabCloseHandle</b> function closes the handle to a Peer Collaboration activity invitation.


## -parameters




### -param hInvitation

TBD




#### - handle [in]

Handle obtained by a previous call to <a href="https://msdn.microsoft.com/2101e16e-ee05-417f-835b-c00cba7f6576">PeerCollabAsyncInviteContact</a> or <a href="https://msdn.microsoft.com/2606d2ef-26d3-4c52-b481-3ea38350295a">PeerCollabAsyncInviteEndpoint</a>.


## -returns



Returns S_OK if the function succeeds. Otherwise, the function returns one of the following values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
There is not enough memory to support this operation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_HANDLE</b></dt>
</dl>
</td>
<td width="60%">
The handle specified is invalid.

</td>
</tr>
</table>
 




## -remarks



You must call this API after the handle has been signaled for an event and any data associated with the event has been obtained.




## -see-also




<a href="https://msdn.microsoft.com/00c3c1f1-c36c-469a-a644-0ec60f02d25e">Peer Collaboration API Functions</a>



<a href="https://msdn.microsoft.com/2101e16e-ee05-417f-835b-c00cba7f6576">PeerCollabAsyncInviteContact</a>



<a href="https://msdn.microsoft.com/2606d2ef-26d3-4c52-b481-3ea38350295a">PeerCollabAsyncInviteEndpoint</a>
 

 

