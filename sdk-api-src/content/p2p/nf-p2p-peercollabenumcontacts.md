---
UID: NF:p2p.PeerCollabEnumContacts
title: PeerCollabEnumContacts function
author: windows-sdk-content
description: Returns a handle to an enumerated set that contains all of the peer collaboration network contacts currently available on the calling peer.
old-location: p2p\peercollabenumcontacts.htm
tech.root: p2psdk
ms.assetid: e5a259e5-c5cb-4a7e-8f60-29e4d7cc6ede
ms.author: windowssdkdev
ms.date: 08/31/2018
ms.keywords: PeerCollabEnumContacts, PeerCollabEnumContacts function [Peer Networking], p2p.peercollabenumcontacts, p2p/PeerCollabEnumContacts
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.lib: P2P.lib
req.dll: P2P.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - P2P.dll
api_name:
 - PeerCollabEnumContacts
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# PeerCollabEnumContacts function


## -description


The <b>PeerCollabEnumContacts</b> function returns a handle to an enumerated set that contains all of the peer collaboration network contacts currently available on the calling peer.


## -parameters




### -param phPeerEnum [out]

Handle to an enumerated set that contains all of the peer collaboration network contacts currently available on the calling peer, excluding the "Me" contact. 


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
The Windows Peer infrastructure is not initialized. Calling the relevant initialization function  is required.

</td>
</tr>
</table>
 




## -remarks



To obtain the individual peer contacts, pass the returned handle to <a href="https://msdn.microsoft.com/015faeb3-82d9-49e5-a451-7394bf83240f">PeerGetNextItem</a>. An array of pointers to <a href="https://msdn.microsoft.com/b84a17fc-35d6-4098-9bb3-18e708541a80">PEER_CONTACT</a> structures will be returned. To close the enumeration and release the resources associated with it, pass this handle to <a href="https://msdn.microsoft.com/cc9484fb-57b9-4970-91b8-c74db6bf2248">PeerEndEnumeration</a>. Individual items returned by the enumeration must be released with <a href="https://msdn.microsoft.com/54288829-c991-42d6-a7c4-874ed28dd106">PeerFreeData</a>.




## -see-also




<a href="https://msdn.microsoft.com/00c3c1f1-c36c-469a-a644-0ec60f02d25e">Peer Collaboration API Functions</a>
 

 

