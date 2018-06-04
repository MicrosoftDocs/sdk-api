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

# PeerEnumIdentities function


## -description



      The <b>PeerEnumIdentities</b> function creates and returns a peer enumeration handle used to enumerate all the peer identities that belong to a specific user.


## -parameters




### -param phPeerEnum [out]

 Receives a handle to the peer enumeration that contains the list of peer identities, with each item represented as a pointer to a <a href="https://msdn.microsoft.com/4c64664e-33c6-490e-b160-7bdb5fb428fa">PEER_NAME_PAIR</a> structure. Pass this handle to <a href="https://msdn.microsoft.com/015faeb3-82d9-49e5-a451-7394bf83240f">PeerGetNextItem</a> to retrieve the items; when finished, call <a href="https://msdn.microsoft.com/cc9484fb-57b9-4970-91b8-c74db6bf2248">PeerEndEnumeration</a>  to release the memory.


## -returns



If the function call succeeds, the return value is S_OK. Otherwise, it  returns one of the following values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
One of the parameters is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
There is not enough memory to perform the specified operation.

</td>
</tr>
</table>
 




## -remarks




        Once the application has obtained the peer enumeration handle, use <a href="https://msdn.microsoft.com/015faeb3-82d9-49e5-a451-7394bf83240f">PeerGetNextItem</a> and <a href="https://msdn.microsoft.com/8f6fec31-8867-4d65-b5b0-e6506be9c991">PeerGetItemCount</a> to enumerate the peer identities.

When enumerating peer identities, <a href="https://msdn.microsoft.com/015faeb3-82d9-49e5-a451-7394bf83240f">PeerGetNextItem</a>  returns an array of pointers to <a href="https://msdn.microsoft.com/4c64664e-33c6-490e-b160-7bdb5fb428fa">PEER_NAME_PAIR</a> structures.

Call <a href="https://msdn.microsoft.com/cc9484fb-57b9-4970-91b8-c74db6bf2248">PeerEndEnumeration</a> to free the enumeration handle when it is no longer required.




## -see-also




<a href="https://msdn.microsoft.com/4c64664e-33c6-490e-b160-7bdb5fb428fa">PEER_NAME_PAIR</a>



<a href="https://msdn.microsoft.com/cc9484fb-57b9-4970-91b8-c74db6bf2248">PeerEndEnumeration</a>



<a href="https://msdn.microsoft.com/8f6fec31-8867-4d65-b5b0-e6506be9c991">PeerGetItemCount</a>



<a href="https://msdn.microsoft.com/015faeb3-82d9-49e5-a451-7394bf83240f">PeerGetNextItem</a>
 

 

