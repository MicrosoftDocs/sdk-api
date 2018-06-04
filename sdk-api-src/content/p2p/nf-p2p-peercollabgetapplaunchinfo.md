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

# PeerCollabGetAppLaunchInfo function


## -description


The <b>PeerCollabGetAppLaunchInfo</b> function obtains the peer application launch information, including the contact name, the peer endpoint, and the invitation request.


## -parameters




### -param ppLaunchInfo [out]

Pointer to a <a href="https://msdn.microsoft.com/98c7f7b8-438f-4ce3-86ab-0e824ff08dc4">PEER_APP_LAUNCH_INFO</a> structure that receives the peer application launch data.

Free the memory associated with this structure by passing it to <a href="https://msdn.microsoft.com/54288829-c991-42d6-a7c4-874ed28dd106">PeerFreeData</a>.


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
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
One of the arguments is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>PEER_E_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
The requested data does not exist.

</td>
</tr>
</table>
 




## -remarks



When an application invite is accepted, the application is launched with  the information sent as part of the application invite. This information can be obtained by calling <b>PeerCollabGetAppLaunchInfo</b>.




## -see-also




<a href="https://msdn.microsoft.com/98c7f7b8-438f-4ce3-86ab-0e824ff08dc4">PEER_APP_LAUNCH_INFO</a>



<a href="https://msdn.microsoft.com/00c3c1f1-c36c-469a-a644-0ec60f02d25e">Peer Collaboration API Functions</a>
 

 

