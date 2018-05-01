---
UID: NF:p2p.PeerGraphDelete
title: PeerGraphDelete function
author: windows-driver-content
description: The PeerGraphDelete function deletes the data associated with a specified peer graph.
old-location: p2p\peergraphdelete.htm
old-project: P2PSdk
ms.assetid: 7962e425-ca74-4695-a394-5495e74bd460
ms.author: windowsdriverdev
ms.date: 4/23/2018
ms.keywords: PeerGraphDelete, PeerGraphDelete function [Peer Networking], p2p.peergraphdelete, p2p/PeerGraphDelete
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
-	PeerGraphDelete
product: Windows
targetos: Windows
req.lib: P2PGraph.lib
req.dll: P2PGraph.dll
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# PeerGraphDelete function


## -description



      The <b>PeerGraphDelete</b> function deletes the data  associated with a specified peer graph.


## -parameters




### -param pwzGraphId [in]

The name of a peer graph to delete data for.  Specify the same ID used in calls to <a href="https://msdn.microsoft.com/62e3ec57-378c-4322-9ad4-a40d98e03dab">PeerGraphCreate</a> or <a href="https://msdn.microsoft.com/a34656f1-3e29-4bcb-a8a7-0eed19368184">PeerGraphOpen</a>.


### -param pwzPeerId [in]

The peer ID to delete  data for. Specify the same ID used in calls to  <a href="https://msdn.microsoft.com/62e3ec57-378c-4322-9ad4-a40d98e03dab">PeerGraphCreate</a> or <a href="https://msdn.microsoft.com/a34656f1-3e29-4bcb-a8a7-0eed19368184">PeerGraphOpen</a>.


### -param pwzDatabaseName [in]

The name of  a database associated with a peer graph. Specify the same ID used in calls to  <a href="https://msdn.microsoft.com/62e3ec57-378c-4322-9ad4-a40d98e03dab">PeerGraphCreate</a> or <a href="https://msdn.microsoft.com/a34656f1-3e29-4bcb-a8a7-0eed19368184">PeerGraphOpen</a>.


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
Access to a  graph is denied.

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
<dt><b>PEER_E_NOT_INITIALIZED</b></dt>
</dl>
</td>
<td width="60%">
A graph must be initialized with a call to <a href="https://msdn.microsoft.com/00ffdec7-f084-4170-a4a1-e6112bab4d61">PeerGraphStartup</a> before using this function.

</td>
</tr>
</table>
 




## -remarks



A peer graph must be closed by using <a href="https://msdn.microsoft.com/7600da14-7641-4b5c-b5ba-e33ffc28097c">PeerGraphClose</a> before it can be deleted.

If  a delete operation fails, a Windows file error code is returned.




## -see-also




<a href="https://msdn.microsoft.com/7600da14-7641-4b5c-b5ba-e33ffc28097c">PeerGraphClose</a>



<a href="https://msdn.microsoft.com/62e3ec57-378c-4322-9ad4-a40d98e03dab">PeerGraphCreate</a>



<a href="https://msdn.microsoft.com/a34656f1-3e29-4bcb-a8a7-0eed19368184">PeerGraphOpen</a>



<a href="https://msdn.microsoft.com/00ffdec7-f084-4170-a4a1-e6112bab4d61">PeerGraphStartup</a>
 

 

