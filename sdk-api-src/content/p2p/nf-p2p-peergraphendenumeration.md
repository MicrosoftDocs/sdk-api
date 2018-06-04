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
 

 

