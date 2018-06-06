---
UID: NF:p2p.PeerGraphAddRecord
title: PeerGraphAddRecord function
author: windows-sdk-content
description: The PeerGraphAddRecord function adds a new record to a peer graph. A record added with this function is sent to each node in a peer graph.
old-location: p2p\peergraphaddrecord.htm
old-project: P2PSdk
ms.assetid: 8256e379-e5d5-4aef-ab05-e220602edf12
ms.author: windowssdkdev
ms.date: 05/29/2018
ms.keywords: PeerGraphAddRecord, PeerGraphAddRecord function [Peer Networking], p2p.peergraphaddrecord, p2p/PeerGraphAddRecord
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
 - PeerGraphAddRecord
product: Windows
targetos: Windows
req.lib: P2PGraph.lib
req.dll: P2PGraph.dll
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# PeerGraphAddRecord function


## -description



      The <b>PeerGraphAddRecord</b> function adds a new record to a peer graph.  A record added with this function is  sent to each node in a peer graph.


## -parameters




### -param hGraph [in]

Handle to a peer graph.


### -param pRecord [in]

Pointer to a record to add.


### -param pRecordId [out]

Specifies   the record ID that uniquely identifies a  record in a peer graph.


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
Cannot access a peer graph.

</td>
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
There is not enough memory to perform a specified operation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>PEER_E_GRAPH_NOT_READY</b></dt>
</dl>
</td>
<td width="60%">
A graph is not synchronized. Records cannot be added until the peer graph is synchronized.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>PEER_E_GRAPH_SHUTTING_DOWN</b></dt>
</dl>
</td>
<td width="60%">

<a href="https://msdn.microsoft.com/7600da14-7641-4b5c-b5ba-e33ffc28097c">PeerGraphClose</a> has been called.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>PEER_E_INVALID_ATTRIBUTES</b></dt>
</dl>
</td>
<td width="60%">
The specified attributes do not match the schema.

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
<dt><b>PEER_E_MAX_RECORD_SIZE_EXCEEDED</b></dt>
</dl>
</td>
<td width="60%">
The record exceeds the maximum size allowed by a peer graph.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>PEER_E_NOT_INITIALIZED</b></dt>
</dl>
</td>
<td width="60%">
The graph must be initialized with a call to <a href="https://msdn.microsoft.com/00ffdec7-f084-4170-a4a1-e6112bab4d61">PeerGraphStartup</a>—before using this function.

</td>
</tr>
</table>
 




## -remarks



The following members of the <a href="https://msdn.microsoft.com/4e0a1c44-e5a4-42d6-bb56-9bdcf7f9e6f1">PEER_RECORD</a> structure must contain valid values:

<ul>
<li><b>dwSize</b>.</li>
<li><b>type</b>.</li>
<li><b>ftExpiration</b> - Must be later than the current graph time, and must be specified in peer time by using <a href="https://msdn.microsoft.com/4d2c8943-cef5-4df3-96fe-447bd5bf37e8">PeerGraphUniversalTimeToPeerTime</a>.</li>
</ul>

				The following members of the <b>PEER_RECORD</b> structure are optional. Set them to <b>NULL</b> if they are not used by your application:

<ul>
<li><b>data</b></li>
<li><b>pwzAttributes</b></li>
<li><b>securityData</b></li>
<li><b>dwVersion</b></li>
</ul>
If any of the following members are <b>NULL</b>, the Peer Graphing API performs the specified default behavior:

<ul>
<li><b>pwzCreatorId</b> - Uses the peer ID passed to either <a href="https://msdn.microsoft.com/62e3ec57-378c-4322-9ad4-a40d98e03dab">PeerGraphCreate</a> or <a href="https://msdn.microsoft.com/a34656f1-3e29-4bcb-a8a7-0eed19368184">PeerGraphOpen</a>.</li>
<li><b>pwzModifiedById</b> - Uses the  <b>pwzCreatorId</b>.</li>
</ul>
The following members cannot be specified; any value used is overwritten by the Peer Graphing infrastructure:

<ul>
<li><b>id</b>.</li>
<li><b>ftCreation</b> - Uses peer time.</li>
<li><b>ftLastModified</b> - Uses peer time.</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/4e0a1c44-e5a4-42d6-bb56-9bdcf7f9e6f1">
        PEER_RECORD</a>



<a href="https://msdn.microsoft.com/7962e425-ca74-4695-a394-5495e74bd460">PeerGraphDelete</a>



<a href="https://msdn.microsoft.com/b64bb920-3fbc-4927-a1b1-39c99850bdd5">PeerGraphGetEventData</a>



<a href="https://msdn.microsoft.com/a34656f1-3e29-4bcb-a8a7-0eed19368184">PeerGraphUpdate</a>
 

 

