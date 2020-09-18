---
UID: NF:p2p.PeerCollabRegisterEvent
title: PeerCollabRegisterEvent function (p2p.h)
description: Registers an application with the peer collaboration infrastructure to receive callbacks for specific peer collaboration events.
helpviewer_keywords: ["PeerCollabRegisterEvent","PeerCollabRegisterEvent function [Peer Networking]","p2p.peercollabregisterevent","p2p/PeerCollabRegisterEvent"]
old-location: p2p\peercollabregisterevent.htm
tech.root: p2p
ms.assetid: db7daf08-8d79-493f-8df5-172dae498df0
ms.date: 12/05/2018
ms.keywords: PeerCollabRegisterEvent, PeerCollabRegisterEvent function [Peer Networking], p2p.peercollabregisterevent, p2p/PeerCollabRegisterEvent
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
 - PeerCollabRegisterEvent
 - p2p/PeerCollabRegisterEvent
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
 - PeerCollabRegisterEvent
---

# PeerCollabRegisterEvent function


## -description

The <b>PeerCollabRegisterEvent</b> function registers an application with the peer collaboration infrastructure to receive callbacks for specific peer collaboration events.

## -parameters

### -param hEvent [in]

Handle created by CreateEvent that the application is signaled on  when an event is triggered.  When an application is signaled, it must call <a href="/windows/desktop/api/p2p/nf-p2p-peercollabgeteventdata">PeerCollabGetEventData</a> to retrieve events until PEER_S_NO_EVENT_DATA is returned.

### -param cEventRegistration [in]

The number of <a href="/windows/desktop/api/p2p/ns-p2p-peer_collab_event_registration">PEER_COLLAB_EVENT_REGISTRATION</a> structures in <i>pEventRegistrations</i>.

### -param pEventRegistrations [in]

An array of <a href="/windows/desktop/api/p2p/ns-p2p-peer_collab_event_registration">PEER_COLLAB_EVENT_REGISTRATION</a> structures that specify the peer collaboration events for which the application requests notification.

### -param phPeerEvent [out]

The peer event handle returned by this function. This handle is passed to <a href="/windows/desktop/api/p2p/nf-p2p-peercollabgeteventdata">PeerCollabGetEventData</a> when a peer collaboration network event is raised on the peer.

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
<tr>
<td width="40%">
<dl>
<dt><b>PEER_E_SERVICE_NOT_AVAILABLE</b></dt>
</dl>
</td>
<td width="60%">
An attempt was made to call <a href="/windows/desktop/api/p2p/nf-p2p-peercollabregisterevent">PeerCollabRegisterEvent</a> from an elevated process.

</td>
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
</table>

## -remarks

If the p2phost.exe service is not running, this function will attempt to launch it for registrations that require p2phost. 

If attempt is made to launch p2phost.exe from an elevated process, an error is returned. As a result, security cannot be compromised by an application mistakenly granting administrative privileges   to p2phost.exe. It is not possible to launch p2phost.exe in a non-interactive mode, as it needs to display Windows dialog boxes for incoming invites.

When <b>PeerCollabRegisterEvent</b> is called on machines under heavy stress, the function may return  the PEER_E_SERVICE_NOT_AVAILABLE error code.

An application can call <b>PeerCollabRegisterEvent</b> multiple times, where each call is   considered to be a separate registration. When an event is registered multiple times, each registration  receives a  copy of the event.

## -see-also

<a href="/windows/desktop/api/p2p/ns-p2p-peer_collab_event_registration">PEER_COLLAB_EVENT_REGISTRATION</a>



<a href="/windows/desktop/P2PSdk/collaboration-api-functions">Peer Collaboration API Functions</a>



<a href="/windows/desktop/api/p2p/nf-p2p-peercollabgeteventdata">PeerCollabGetEventData</a>