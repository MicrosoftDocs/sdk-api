---
UID: NF:p2p.PeerGraphEnumRecords
title: PeerGraphEnumRecords function
author: windows-sdk-content
description: The PeerGraphEnumRecords function creates and returns an enumeration handle used to enumerate records of a specific type of record, user, or both. An enumeration provides a snapshot of records at the time an enumeration is performed.
old-location: p2p\peergraphenumrecords.htm
old-project: P2PSdk
ms.assetid: 528c7172-56ed-4e14-991a-69e9fde7b227
ms.author: windowssdkdev
ms.date: 07/16/2018
ms.keywords: PeerGraphEnumRecords, PeerGraphEnumRecords function [Peer Networking], p2p.peergraphenumrecords, p2p/PeerGraphEnumRecords
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
tech.root: 
req.typenames: PEER_WATCH_PERMISSION
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - P2PGraph.dll
api_name:
 - PeerGraphEnumRecords
product: Windows
targetos: Windows
req.lib: P2PGraph.lib
req.dll: P2PGraph.dll
req.irql: 
req.product: ADAM
---

# PeerGraphEnumRecords function


## -description



      The <b>PeerGraphEnumRecords</b> function creates and returns an enumeration handle used to enumerate records of a specific type of record,   user, or both.  An enumeration provides  a snapshot of records at the time an enumeration is performed.


## -parameters




### -param hGraph [in]

Handle to a peer graph.


### -param pRecordType [in]

Pointer to the type of record to enumerate. Specify <b>NULL</b> to enumerate   all record types.


### -param pwzPeerId [in]

Pointer to a string that identifies the creator that an application is requesting an enumeration for. Specify <b>NULL</b> to enumerate   all records.


### -param phPeerEnum [out]

Receives a handle to an enumeration. Supply the handle to all calls to <a href="https://msdn.microsoft.com/f595e66d-570f-4642-bef8-ff5cf070649c">PeerGraphGetNextItem</a>. When a handle is not needed, free it by calling <a href="https://msdn.microsoft.com/31a18705-b8bf-461c-98e0-c03c6d269b51">PeerGraphEndEnumeration</a>.


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
One  parameter is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
There is not enough memory to perform a specified operation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>PEER_E_INVALID_GRAPH</b></dt>
</dl>
</td>
<td width="60%">
The handle to a peer graph is invalid.

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
 




## -remarks



<ul>
<li>If both the <i>pRecordType</i> and <i>pwzPeerId</i> parameters are  <b>NULL</b>, all records are returned.</li>
</ul>
<ul>
<li>For simple enumeration tasks, use the <b>PeerGraphEnumRecords</b> function, because it is more efficient than the  <a href="https://msdn.microsoft.com/0f20c738-ae56-4352-a1fb-5aa469a58bc8">PeerGraphSearchRecords</a> function. For complex enumeration and filtering tasks such as heuristic searches of the database,  use the <b>PeerGraphSearchRecords</b> function. </li>
</ul>
<ul>
<li>When <a href="https://msdn.microsoft.com/f595e66d-570f-4642-bef8-ff5cf070649c">PeerGraphGetNextItem</a> is called with the handle that   <b>PeerGraphEnumRecords</b>  returns, <b>PeerGraphGetNextItem</b>  returns the data in the  <a href="https://msdn.microsoft.com/4e0a1c44-e5a4-42d6-bb56-9bdcf7f9e6f1">PEER_RECORD</a> structure.</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/4e0a1c44-e5a4-42d6-bb56-9bdcf7f9e6f1">PEER_RECORD</a>



<a href="https://msdn.microsoft.com/31a18705-b8bf-461c-98e0-c03c6d269b51">PeerGraphEndEnumeration</a>



<a href="https://msdn.microsoft.com/db97b7e0-6f85-4b61-843f-efb4bc93149b">PeerGraphGetItemCount</a>



<a href="https://msdn.microsoft.com/f595e66d-570f-4642-bef8-ff5cf070649c">PeerGraphGetNextItem</a>



<a href="https://msdn.microsoft.com/0f20c738-ae56-4352-a1fb-5aa469a58bc8">PeerGraphSearchRecords</a>
 

 

