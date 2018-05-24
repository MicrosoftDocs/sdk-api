---
UID: NF:p2p.PeerGraphEndEnumeration
title: PeerGraphEndEnumeration function
author: windows-driver-content
description: The PeerGraphEndEnumeration function releases an enumeration handle, and frees the resources associated with an enumeration.
old-location: p2p\peergraphendenumeration.htm
old-project: P2PSdk
ms.assetid: 31a18705-b8bf-461c-98e0-c03c6d269b51
ms.author: windowsdriverdev
ms.date: 5/8/2018
ms.keywords: PeerGraphEndEnumeration, PeerGraphEndEnumeration function [Peer Networking], p2p.peergraphendenumeration, p2p/PeerGraphEndEnumeration
ms.prod: windows-hardware
ms.technology: windows-devices
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
-	P2PGraph.dll
api_name:
-	PeerGraphEndEnumeration
product: Windows
targetos: Windows
req.lib: P2PGraph.lib
req.dll: P2PGraph.dll
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# PeerGraphEndEnumeration function


## -description



      The <b>PeerGraphEndEnumeration</b> function releases an enumeration handle,  and frees the resources associated with an enumeration.


## -parameters




### -param hPeerEnum [in]

Handle to an  enumeration to release. This handle is  returned by one of the following functions: <a href="https://msdn.microsoft.com/ef4ea3e2-fd71-48d8-a9a8-db38ef06df20">PeerGraphEnumConnections</a>, <a href="https://msdn.microsoft.com/68231b0a-6002-4974-84d7-08b0629f3622">PeerGraphEnumNodes</a>, <a href="https://msdn.microsoft.com/528c7172-56ed-4e14-991a-69e9fde7b227">PeerGraphEnumRecords</a>, or <a href="https://msdn.microsoft.com/0f20c738-ae56-4352-a1fb-5aa469a58bc8">PeerGraphSearchRecords</a>.


## -returns



If the function call succeeds, the return value is <b>S_OK</b>. Otherwise, it  returns one of the following values.

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
A parameter is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>PEER_E_NOT_INITIALIZED</b></dt>
</dl>
</td>
<td width="60%">
A graph must be  initialized with a call to <a href="https://msdn.microsoft.com/00ffdec7-f084-4170-a4a1-e6112bab4d61">PeerGraphStartup</a> before using this function.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/ef4ea3e2-fd71-48d8-a9a8-db38ef06df20">PeerGraphEnumConnections</a>



<a href="https://msdn.microsoft.com/68231b0a-6002-4974-84d7-08b0629f3622">PeerGraphEnumNodes</a>



<a href="https://msdn.microsoft.com/528c7172-56ed-4e14-991a-69e9fde7b227">PeerGraphEnumRecords</a>



<a href="https://msdn.microsoft.com/0f20c738-ae56-4352-a1fb-5aa469a58bc8">PeerGraphSearchRecords</a>
 

 

