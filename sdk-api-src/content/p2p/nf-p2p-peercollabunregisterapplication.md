---
UID: NF:p2p.PeerCollabUnregisterApplication
title: PeerCollabUnregisterApplication function
author: windows-sdk-content
description: Unregisters the specific applications of a peer from the local computer.
old-location: p2p\peercollabunregisterapplication.htm
old-project: p2psdk
ms.assetid: 2479b726-20f1-4370-9fcf-f29cec44c3ec
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: PeerCollabUnregisterApplication, PeerCollabUnregisterApplication function [Peer Networking], p2p.peercollabunregisterapplication, p2p/PeerCollabUnregisterApplication
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: p2p.h
req.include-header: 
req.redist: 
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
 - PeerCollabUnregisterApplication
product: Windows
targetos: Windows
req.lib: P2P.lib
req.dll: P2P.dll
req.irql: 
req.product: ADAM
---

# PeerCollabUnregisterApplication function


## -description


The <b>PeerCollabUnregisterApplication</b> function unregisters the specific applications of a peer from the local computer.


## -parameters




### -param pApplicationId [in]

Pointer to the GUID value that represents a particular peer's application.


### -param registrationType [in]

A <a href="https://msdn.microsoft.com/58f14e46-377e-494b-93ef-fc19e8d87fcc">PEER_APPLICATION_REGISTRATION_TYPE</a> value that describes whether the peer's application is deregistered for the current user or all users of the peer's machine.


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
The application  requested to unregister was not registered for the given <i>registrationType.</i>

</td>
</tr>
</table>
 




## -remarks



An <i>application</i> is a set of software or software  features available on the peer's endpoint. Commonly, this refers to software packages that support peer networking activities, like games or other collaborative applications.

The collaboration infrastructure can receive application invites from trusted contacts or from "People Near Me", which are based on what scope the collaboration infrastructure is signed in with using PeerCollabSignin.

A peer's application has a GUID representing a single specific application. When application is registered for a peer, this GUID and the corresponding application can be made available to all trusted contacts of the peer, indicating the activities the peer can participate in. To unregister a peer's application, call <b>PeerCollabUnregisterApplication</b> with this GUID.

To unregister the application for all users, the caller of this API must be elevated.




## -see-also




<a href="https://msdn.microsoft.com/58f14e46-377e-494b-93ef-fc19e8d87fcc">PEER_APPLICATION_REGISTRATION_TYPE</a>



<a href="https://msdn.microsoft.com/00c3c1f1-c36c-469a-a644-0ec60f02d25e">Peer Collaboration API Functions</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa371076(v=VS.85).aspx">PeerCollabRegisterApplication</a>
 

 

