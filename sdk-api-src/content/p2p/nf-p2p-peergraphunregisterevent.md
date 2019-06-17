---
UID: NF:p2p.PeerGraphUnregisterEvent
title: PeerGraphUnregisterEvent function (p2p.h)
author: windows-sdk-content
description: The PeerGraphUnregisterEvent function requests that the application no longer be notified of changes associated with a peer graph and record type.
old-location: p2p\peergraphunregisterevent.htm
tech.root: P2PSdk
ms.assetid: de37bb9a-e1b2-4448-9610-566f77acf542
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: PeerGraphUnregisterEvent, PeerGraphUnregisterEvent function [Peer Networking], p2p.peergraphunregisterevent, p2p/PeerGraphUnregisterEvent
ms.topic: function
f1_keywords: ["p2p/PeerGraphUnregisterEvent"]
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
req.lib: P2PGraph.lib
req.dll: P2PGraph.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - P2PGraph.dll
api_name:
 - PeerGraphUnregisterEvent
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# PeerGraphUnregisterEvent function


## -description


The <b>PeerGraphUnregisterEvent</b> function requests that the application no longer be  notified of changes associated with a peer graph and  record type.


## -parameters




### -param hPeerEvent [in]

Peer event handle obtained from call to <a href="https://docs.microsoft.com/windows/desktop/api/p2p/nf-p2p-peergraphregisterevent">PeerGraphRegisterEvent</a>.


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
The parameter is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>PEER_E_NOT_INITIALIZED</b></dt>
</dl>
</td>
<td width="60%">
The peer graph must be  initialized with a call to <a href="https://docs.microsoft.com/windows/desktop/api/p2p/nf-p2p-peergraphstartup">PeerGraphStartup</a> before using this function.

</td>
</tr>
</table>
 




## -remarks



The peer event handle passed to <a href="https://docs.microsoft.com/windows/desktop/api/p2p/nf-p2p-peergraphregisterevent">PeerGraphRegisterEvent</a> must be closed only after <b>PeerGraphUnregisterEvent</b> has been called.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/p2p/nf-p2p-peergraphregisterevent">PeerRegisterEvent</a>
 

 

