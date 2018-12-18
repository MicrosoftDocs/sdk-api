---
UID: NF:p2p.PeerCollabDeleteObject
title: PeerCollabDeleteObject function
author: windows-sdk-content
description: Deletes a peer object from the calling endpoint.
old-location: p2p\peercollabdeleteobject.htm
tech.root: P2PSdk
ms.assetid: 4849f8da-7f8a-4951-94eb-624ee186ec83
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: PeerCollabDeleteObject, PeerCollabDeleteObject function [Peer Networking], p2p.peercollabdeleteobject, p2p/PeerCollabDeleteObject
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
 - PeerCollabDeleteObject
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# PeerCollabDeleteObject function


## -description


The <b>PeerCollabDeleteObject</b> function deletes a peer object from the calling endpoint.


## -parameters




### -param pObjectId [in]

Pointer to a GUID value that uniquely identifies the peer object to delete from the calling endpoint.


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
<tr>
<td width="40%">
<dl>
<dt><b>PEER_E_NOT_SIGNED_IN</b></dt>
</dl>
</td>
<td width="60%">
The operation requires the user to be signed in.

</td>
</tr>
</table>
 




## -remarks



Peer objects are run-time data items associated with a particular application, such as a picture, an avatar, a certificate, or a specific description. Each peer object must be smaller than 3216K in size.

Trusted contacts watching this peer object and the subscriber of the "Me" contact will have a PEER_EVENT_OBJECT_CHANGED event raised, signaling this peer object's change in status. PEER_EVENT_MY_OBJECT_CHANGED will be raised locally.

Pre-defined objects, like Picture objects, cannot be deleted by calling this API.




## -see-also




<a href="https://msdn.microsoft.com/00c3c1f1-c36c-469a-a644-0ec60f02d25e">Peer Collaboration API Functions</a>
 

 

