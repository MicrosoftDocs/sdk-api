---
UID: NF:p2p.PeerGraphDeleteRecord
title: PeerGraphDeleteRecord function
author: windows-sdk-content
description: The PeerGraphDeleteRecord function marks a record as deleted within a peer graph. The record is not available on a local node to function calls, for example, calls to PeerGraphGetRecord and PeerGraphEnumRecords.
old-location: p2p\peergraphdeleterecord.htm
old-project: p2psdk
ms.assetid: d6ecc762-8702-4366-81fc-c2b168dc8cb3
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: PeerGraphDeleteRecord, PeerGraphDeleteRecord function [Peer Networking], p2p.peergraphdeleterecord, p2p/PeerGraphDeleteRecord
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
 - PeerGraphDeleteRecord
product: Windows
targetos: Windows
req.lib: P2PGraph.lib
req.dll: P2PGraph.dll
req.irql: 
req.product: ADAM
---

# PeerGraphDeleteRecord function


## -description


The <b>PeerGraphDeleteRecord</b> function marks a record as deleted within a peer graph.  The record is not  available on a local node to function calls, for example, calls   to <a href="https://msdn.microsoft.com/5e777c02-980c-42f9-add7-9568c86c2efe">PeerGraphGetRecord</a> and  <a href="https://msdn.microsoft.com/528c7172-56ed-4e14-991a-69e9fde7b227">PeerGraphEnumRecords</a>.


## -parameters




### -param hGraph [in]

Handle to a peer graph.


### -param pRecordId [in]

Pointer to a record ID to delete.


### -param fLocal [in]

Specify <b>TRUE</b> to remove a record from only  a local database without notifying the rest of  a peer graph about the change.  Specify FALSE to delete the record from an entire peer graph.

<div class="alert"><b>Note</b>   Specifying <b>TRUE</b> does not prevent  a record from being added again during the next graph synchronization with a neighbor. Specifying <b>TRUE</b> is only effective if PEER_SECURITY_INTERFACE is specified in a call to <a href="https://msdn.microsoft.com/a34656f1-3e29-4bcb-a8a7-0eed19368184">PeerGraphOpen</a> or <a href="https://msdn.microsoft.com/62e3ec57-378c-4322-9ad4-a40d98e03dab">PeerGraphCreate</a>, and only if  PEER_SECURITY_INTERFACE contains a <a href="https://msdn.microsoft.com/5d81f09b-e46b-43e6-b0a8-ed7c236f2968">PFNPEER_VALIDATE_RECORD</a> function that returns PEER_E_INVALID_RECORD when validating the record.</div>
<div> </div>

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
<dt><b>E_ACCESSDENIED</b></dt>
</dl>
</td>
<td width="60%">
Cannot access a  peer graph.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>PEER_E_GRAPH_NOT_READY</b></dt>
</dl>
</td>
<td width="60%">
The peer graph is not synchronized. Records cannot be deleted until the graph is synchronized.

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
The peer graph must be initialized with a call to <a href="https://msdn.microsoft.com/00ffdec7-f084-4170-a4a1-e6112bab4d61">PeerGraphStartup</a> before using this function.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>PEER_E_RECORD_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
The specified record cannot be found.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/5e777c02-980c-42f9-add7-9568c86c2efe">PeerGraphAddRecord</a>



<a href="https://msdn.microsoft.com/528c7172-56ed-4e14-991a-69e9fde7b227">PeerGraphEnumRecords</a>



<b>PeerGraphGetRecord</b>



<a href="https://msdn.microsoft.com/9007095f-4f2a-4e92-895b-9a4033f0f7b9">PeerGraphUpdateRecord</a>
 

 

