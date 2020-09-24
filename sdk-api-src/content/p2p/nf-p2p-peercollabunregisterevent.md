---
UID: NF:p2p.PeerCollabUnregisterEvent
title: PeerCollabUnregisterEvent function (p2p.h)
description: Deregisters an application from notification about specific peer collaboration events.
helpviewer_keywords: ["PeerCollabUnregisterEvent","PeerCollabUnregisterEvent function [Peer Networking]","p2p.peercollabunregisterevent","p2p/PeerCollabUnregisterEvent"]
old-location: p2p\peercollabunregisterevent.htm
tech.root: p2p
ms.assetid: dc1bcdaa-e58e-4567-9fd2-e1fa9071880f
ms.date: 12/05/2018
ms.keywords: PeerCollabUnregisterEvent, PeerCollabUnregisterEvent function [Peer Networking], p2p.peercollabunregisterevent, p2p/PeerCollabUnregisterEvent
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
req.lib: P2P.lib
req.dll: P2P.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - PeerCollabUnregisterEvent
 - p2p/PeerCollabUnregisterEvent
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - P2P.dll
api_name:
 - PeerCollabUnregisterEvent
---

# PeerCollabUnregisterEvent function


## -description

The <b>PeerCollabUnregisterEvent</b> function deregisters an application from notification about specific peer collaboration events.

## -parameters

### -param hPeerEvent [in]

Handle to the peer collaboration event the peer application will deregister. This handle is obtained with a previous call to <a href="/windows/desktop/api/p2p/nf-p2p-peercollabregisterevent">PeerCollabRegisterEvent</a>.

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

<a href="/windows/desktop/P2PSdk/collaboration-api-functions">Peer Collaboration API Functions</a>