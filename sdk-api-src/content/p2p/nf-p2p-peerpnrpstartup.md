---
UID: NF:p2p.PeerPnrpStartup
title: PeerPnrpStartup function
author: windows-sdk-content
description: Starts the Peer Name Resolution Protocol (PNRP) service for the calling peer.
old-location: p2p\peerpnrpstartup.htm
old-project: P2PSdk
ms.assetid: 27d8d6ab-679d-4b7b-bf90-7b0859e7e048
ms.author: windowssdkdev
ms.date: 05/29/2018
ms.keywords: PeerPnrpStartup, PeerPnrpStartup function [Peer Networking], p2p.peerpnrpstartup, p2p/PeerPnrpStartup
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
req.typenames: PEER_WATCH_PERMISSION
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	P2P.dll
api_name:
-	PeerPnrpStartup
product: Windows
targetos: Windows
req.lib: P2P.lib
req.dll: P2P.dll
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# PeerPnrpStartup function


## -description


The <b>PeerPnrpStartup</b> function starts the Peer Name Resolution Protocol (PNRP) service for the calling peer.


## -parameters




### -param wVersionRequested

The version of PNRP to use for this service instance. The default value is PNRP_VERSION (2).


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
<dt><b>PEER_E_UNSUPPORTED_VERSION</b></dt>
</dl>
</td>
<td width="60%">
The provided version is unsupported.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>PEER_E_SERVICE_NOT_AVAILABLE </b></dt>
</dl>
</td>
<td width="60%">
The Peer Collaboration infrastructure, which includes People Near Me, is not available. This code will also be returned whenever an attempt is made to utilize the Collaboration infrastructure from an elevated process.

</td>
</tr>
</table>
 




## -remarks



To shutdown the PNRP service for the calling peer and release all resources associated with it, call <a href="https://msdn.microsoft.com/e617fb5b-ace2-46b4-b165-4cd9cf891ac7">PeerPnrpShutdown</a>.




## -see-also




<a href="https://msdn.microsoft.com/e617fb5b-ace2-46b4-b165-4cd9cf891ac7">PeerPnrpShutdown</a>
 

 

