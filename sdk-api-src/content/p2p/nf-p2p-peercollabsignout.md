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

# PeerCollabSignout function


## -description


The <b>PeerCollabSignout</b> function signs a peer out of a specific type of peer collaboration network presence provider.


## -parameters




### -param dwSigninOptions

TBD




#### - dwSignoutOptions [in]


<a href="https://msdn.microsoft.com/00b7f57a-222d-4152-bded-93f1899692da">PEER_SIGNIN_FLAGS</a> enumeration value that contains the presence provider sign-in options for the calling peer. This value is obtained by calling <a href="https://msdn.microsoft.com/2b1452d3-2474-40c9-a913-de7e148e2d94">PeerCollabGetSigninOptions</a> from the peer application.


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
<dt><b>PEER_E_NOT_INITIALIZED</b></dt>
</dl>
</td>
<td width="60%">
The application did not make a previous call to <a href="https://msdn.microsoft.com/b3f4ac2a-c722-4609-b893-c4b9667ae559">PeerCollabStartup</a>.

</td>
</tr>
</table>
 




## -remarks



If the local peer's collaboration infrastructure is signed out of both Internet and People Near Me presence, all transient information like objects and the endpoint ID are deleted. Any application that uses this information must republish the information. A single event that indicates signout is raised, instead of sending multiple individual events for each object or application. 

 Multiple applications can  use the infrastructure at any given moment. It is not recommended for a single application to sign out, as other applications will not be able to use the infrastructure.
Applications must also be prepared to handle user sign in and sign out, or situations where a machine goes to sleep or into hibernation.




## -see-also




<a href="https://msdn.microsoft.com/00b7f57a-222d-4152-bded-93f1899692da">PEER_SIGNIN_FLAGS</a>



<a href="https://msdn.microsoft.com/00c3c1f1-c36c-469a-a644-0ec60f02d25e">Peer Collaboration API Functions</a>



<a href="https://msdn.microsoft.com/2b1452d3-2474-40c9-a913-de7e148e2d94">PeerCollabGetSigninOptions</a>
 

 

