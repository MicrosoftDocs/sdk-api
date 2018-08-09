---
UID: NF:p2p.PeerGraphSearchRecords
title: PeerGraphSearchRecords function
author: windows-sdk-content
description: The PeerGraphSearchRecords function searches the peer graph for specific records.
old-location: p2p\peergraphsearchrecords.htm
old-project: p2psdk
ms.assetid: 0f20c738-ae56-4352-a1fb-5aa469a58bc8
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: PeerGraphSearchRecords, PeerGraphSearchRecords function [Peer Networking], p2p.peergraphsearchrecords, p2p/PeerGraphSearchRecords
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
 - PeerGraphSearchRecords
product: Windows
targetos: Windows
req.lib: P2PGraph.lib
req.dll: P2PGraph.dll
req.irql: 
req.product: ADAM
---

# PeerGraphSearchRecords function


## -description


The <b>PeerGraphSearchRecords</b> function searches the peer graph for specific records.


## -parameters




### -param hGraph [in]

Handle to the peer graph.


### -param pwzCriteria [in]

Pointer to an XML string that specifies the records to search for. For information on formulating an XML query string to search the peer graphing records, see <a href="https://msdn.microsoft.com/2c5ab425-6959-418a-8d9a-c8155257fc7e">Record Search Query Format</a>.


### -param phPeerEnum [out]

Handle to the enumeration.


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
<tr>
<td width="40%">
<dl>
<dt><b>PEER_E_INVALID_GRAPH</b></dt>
</dl>
</td>
<td width="60%">
The handle to the peer graph is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>PEER_E_INVALID_SEARCH</b></dt>
</dl>
</td>
<td width="60%">
The specified query does not adhere to the search schema.  See <a href="https://msdn.microsoft.com/2c5ab425-6959-418a-8d9a-c8155257fc7e">Record Search Query Format</a> for further information.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>PEER_E_NOT_INITIALIZED</b></dt>
</dl>
</td>
<td width="60%">
The peer graph must be  initialized with a call to <a href="https://msdn.microsoft.com/00ffdec7-f084-4170-a4a1-e6112bab4d61">PeerGraphStartup</a> before using this function.

</td>
</tr>
</table>
 




## -remarks



The <a href="https://msdn.microsoft.com/528c7172-56ed-4e14-991a-69e9fde7b227">PeerGraphEnumRecords</a> function is more efficient than the  <b>PeerGraphSearchRecords</b> function.

When <a href="https://msdn.microsoft.com/f595e66d-570f-4642-bef8-ff5cf070649c">PeerGraphGetNextItem</a> is called with the handle returned by  <b>PeerGraphSearchRecords</b>, <b>PeerGraphGetNextItem</b>  returns the data in the  <a href="https://msdn.microsoft.com/4e0a1c44-e5a4-42d6-bb56-9bdcf7f9e6f1">PEER_RECORD</a> structure.




## -see-also




<a href="https://msdn.microsoft.com/4e0a1c44-e5a4-42d6-bb56-9bdcf7f9e6f1">PEER_RECORD</a>



<a href="https://msdn.microsoft.com/31a18705-b8bf-461c-98e0-c03c6d269b51">PeerGraphEndEnumeration</a>



<a href="https://msdn.microsoft.com/528c7172-56ed-4e14-991a-69e9fde7b227">PeerGraphEnumRecords</a>



<a href="https://msdn.microsoft.com/db97b7e0-6f85-4b61-843f-efb4bc93149b">PeerGraphGetItemCount</a>



<a href="https://msdn.microsoft.com/f595e66d-570f-4642-bef8-ff5cf070649c">PeerGraphGetNextItem</a>
 

 

