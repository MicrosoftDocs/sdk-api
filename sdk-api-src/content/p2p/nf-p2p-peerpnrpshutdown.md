---
UID: NF:p2p.PeerPnrpShutdown
title: PeerPnrpShutdown function
author: windows-sdk-content
description: Shuts down a running instance of the Peer Name Resolution Protocol (PNRP) service and releases all resources associated with it.
old-location: p2p\peerpnrpshutdown.htm
old-project: P2PSdk
ms.assetid: e617fb5b-ace2-46b4-b165-4cd9cf891ac7
ms.author: windowssdkdev
ms.date: 05/29/2018
ms.keywords: PeerPnrpShutdown, PeerPnrpShutdown function [Peer Networking], p2p.peerpnrpshutdown, p2p/PeerPnrpShutdown
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: p2p.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP with SP2 [desktop apps only],Windows XP with SP1 with the Advanced Networking Pack for Windows XP
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	P2P.dll
api_name:
-	PeerPnrpShutdown
product: Windows
targetos: Windows
req.lib: P2P.lib
req.dll: P2P.dll
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# PeerPnrpShutdown function


## -description


The <b>PeerPnrpShutdown</b> function shuts down a running instance of the Peer Name Resolution Protocol (PNRP) service and releases all resources associated with it.


## -parameters






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
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
There is not enough memory to perform the specified operation.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/27d8d6ab-679d-4b7b-bf90-7b0859e7e048">PeerPnrpStartup</a>
 

 

