---
UID: NF:p2p.PeerCollabSignout
title: PeerCollabSignout function
author: windows-sdk-content
description: Signs a peer out of a specific type of peer collaboration network presence provider.
old-location: p2p\peercollabsignout.htm
old-project: P2PSdk
ms.assetid: aa69a233-6104-47c6-a0b5-378794108623
ms.author: windowssdkdev
ms.date: 05/29/2018
ms.keywords: PeerCollabSignout, PeerCollabSignout function [Peer Networking], p2p.peercollabsignout, p2p/PeerCollabSignout
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: p2p.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: None supported
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
req.typenames: PEER_WATCH_PERMISSION
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - P2P.dll
api_name:
 - PeerCollabSignout
product: Windows
targetos: Windows
req.lib: P2P.lib
req.dll: P2P.dll
req.irql: 
req.product: Rights Management Services client 1.0 or later
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
 

 

