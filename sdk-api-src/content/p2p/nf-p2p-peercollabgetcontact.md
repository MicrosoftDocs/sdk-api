---
UID: NF:p2p.PeerCollabGetContact
title: PeerCollabGetContact function
author: windows-sdk-content
description: Obtains the information for a peer contact given the peer name of the contact.
old-location: p2p\peercollabgetcontact.htm
old-project: p2psdk
ms.assetid: b1233942-1bd5-4198-a00c-6d0516ab32dc
ms.author: windowssdkdev
ms.date: 07/17/2018
ms.keywords: PeerCollabGetContact, PeerCollabGetContact function [Peer Networking], p2p.peercollabgetcontact, p2p/PeerCollabGetContact
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
 - PeerCollabGetContact
product: Windows
targetos: Windows
req.lib: P2P.lib
req.dll: P2P.dll
req.irql: 
req.product: ADAM
---

# PeerCollabGetContact function


## -description


The <b>PeerCollabGetContact</b> function obtains the information for a peer contact given the peer name of the contact.


## -parameters




### -param pwzPeerName [in, optional]

Pointer to zero-terminated Unicode string that contains the name of the peer contact for which to obtain information. 

If this parameter is <b>NULL</b>, the 'Me' contact information for the calling peer is returned.


### -param ppContact [out, optional]

Pointer to a pointer to a <a href="https://msdn.microsoft.com/b84a17fc-35d6-4098-9bb3-18e708541a80">PEER_CONTACT</a> structure. It receives the address of a PEER_CONTACT structure containing peer contact information for the peer name supplied in <i>pwzPeerName</i>. When this parameter is <b>NULL</b>, this function returns E_INVALIDARG.

Call <a href="https://msdn.microsoft.com/54288829-c991-42d6-a7c4-874ed28dd106">PeerFreeData</a> on the address of the <a href="https://msdn.microsoft.com/b84a17fc-35d6-4098-9bb3-18e708541a80">PEER_CONTACT</a> structure to free this data.


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
 




## -see-also




<a href="https://msdn.microsoft.com/b84a17fc-35d6-4098-9bb3-18e708541a80">PEER_CONTACT</a>



<a href="https://msdn.microsoft.com/00c3c1f1-c36c-469a-a644-0ec60f02d25e">Peer Collaboration API Functions</a>
 

 

