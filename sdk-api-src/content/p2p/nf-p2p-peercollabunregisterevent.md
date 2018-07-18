---
UID: NF:p2p.PeerCollabUnregisterEvent
title: PeerCollabUnregisterEvent function
author: windows-sdk-content
description: Deregisters an application from notification about specific peer collaboration events.
old-location: p2p\peercollabunregisterevent.htm
old-project: P2PSdk
ms.assetid: dc1bcdaa-e58e-4567-9fd2-e1fa9071880f
ms.author: windowssdkdev
ms.date: 07/16/2018
ms.keywords: PeerCollabUnregisterEvent, PeerCollabUnregisterEvent function [Peer Networking], p2p.peercollabunregisterevent, p2p/PeerCollabUnregisterEvent
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: p2p.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
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
 - P2P.dll
api_name:
 - PeerCollabUnregisterEvent
product: Windows
targetos: Windows
req.lib: P2P.lib
req.dll: P2P.dll
req.irql: 
req.product: ADAM
---

# PeerCollabUnregisterEvent function


## -description


The <b>PeerCollabUnregisterEvent</b> function deregisters an application from notification about specific peer collaboration events.


## -parameters




### -param hPeerEvent [in]

Handle to the peer collaboration event the peer application will deregister. This handle is obtained with a previous call to <a href="https://msdn.microsoft.com/library/Aa371077(v=VS.85).aspx">PeerCollabRegisterEvent</a>.


## -returns



Returns S_OK if the function succeeds. Otherwise, the function returns one of the following values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
There is not enough memory to support this operation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
One of the arguments is invalid.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/00c3c1f1-c36c-469a-a644-0ec60f02d25e">Peer Collaboration API Functions</a>
 

 

