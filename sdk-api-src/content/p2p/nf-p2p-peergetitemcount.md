---
UID: NF:p2p.PeerGetItemCount
title: PeerGetItemCount function
author: windows-sdk-content
description: The PeerGetItemCount function returns a count of the items in a peer enumeration.
old-location: p2p\peergetitemcount.htm
old-project: P2PSdk
ms.assetid: 8f6fec31-8867-4d65-b5b0-e6506be9c991
ms.author: windowssdkdev
ms.date: 05/08/2018
ms.keywords: PeerGetItemCount, PeerGetItemCount function [Peer Networking], p2p.peergetitemcount, p2p/PeerGetItemCount
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: p2p.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2 [desktop apps only],Windows XP with SP1 with the Advanced Networking Pack forWindows XP
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
req.typenames: PEER_WATCH_PERMISSION
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	P2P.dll
api_name:
-	PeerGetItemCount
product: Windows
targetos: Windows
req.lib: P2P.lib
req.dll: P2P.dll
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# PeerGetItemCount function


## -description



      The <b>PeerGetItemCount</b> function returns a count of the items  in a peer enumeration.


## -parameters




### -param hPeerEnum [in]

Handle to the peer enumeration on which a count is performed. A peer enumeration function generates this handle.


### -param pCount [out]

Returns the total number of items in a peer enumeration. 


## -returns



Returns <b>S_OK</b> if the operation succeeds. Otherwise, the function returns one of the following values.

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
 




## -see-also




<a href="https://msdn.microsoft.com/cc9484fb-57b9-4970-91b8-c74db6bf2248">PeerEndEnumeration</a>



<a href="https://msdn.microsoft.com/debb3c57-b5d2-440b-acf2-b6d8e712849b">PeerEnumGroups</a>



<a href="https://msdn.microsoft.com/91f18185-0292-41a3-8aff-8b345cab5e82">PeerEnumIdentities</a>



<a href="https://msdn.microsoft.com/015faeb3-82d9-49e5-a451-7394bf83240f">PeerGetNextItem</a>



<a href="https://msdn.microsoft.com/84a26066-3d6a-44c8-86a1-b3f997c17739">PeerGroupEnumConnections</a>



<a href="https://msdn.microsoft.com/1201ce0b-961a-4848-9b9c-ad6491e3ff4a">PeerGroupEnumMembers</a>



<a href="https://msdn.microsoft.com/d9a0654a-850a-40bb-9112-03ec9bf47370">PeerGroupEnumRecords</a>
 

 

