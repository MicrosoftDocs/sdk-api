---
UID: NS:p2p.peer_event_watchlist_changed_data_tag
title: PEER_EVENT_WATCHLIST_CHANGED_DATA (p2p.h)
description: The PEER_EVENT_WATCHLIST_CHANGED_DATA structure contains information returned when a PEER_EVENT_WATCHLIST_CHANGED event is raised on a peer participating in a peer collaboration network.
helpviewer_keywords: ["*PPEER_EVENT_WATCHLIST_CHANGED_DATA","PEER_EVENT_WATCHLIST_CHANGED_DATA","PEER_EVENT_WATCHLIST_CHANGED_DATA structure [Peer Networking]","PPEER_EVENT_WATCHLIST_CHANGED_DATA","PPEER_EVENT_WATCHLIST_CHANGED_DATA structure pointer [Peer Networking]","p2p.peer_event_watchlist_changed_data","p2p/PEER_EVENT_WATCHLIST_CHANGED_DATA","p2p/PPEER_EVENT_WATCHLIST_CHANGED_DATA"]
old-location: p2p\peer_event_watchlist_changed_data.htm
tech.root: p2p
ms.assetid: 9d4af44c-c03f-4d9f-9b36-c04513a18133
ms.date: 12/05/2018
ms.keywords: '*PPEER_EVENT_WATCHLIST_CHANGED_DATA, PEER_EVENT_WATCHLIST_CHANGED_DATA, PEER_EVENT_WATCHLIST_CHANGED_DATA structure [Peer Networking], PPEER_EVENT_WATCHLIST_CHANGED_DATA, PPEER_EVENT_WATCHLIST_CHANGED_DATA structure pointer [Peer Networking], p2p.peer_event_watchlist_changed_data, p2p/PEER_EVENT_WATCHLIST_CHANGED_DATA, p2p/PPEER_EVENT_WATCHLIST_CHANGED_DATA'
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: PEER_EVENT_WATCHLIST_CHANGED_DATA, *PPEER_EVENT_WATCHLIST_CHANGED_DATA
req.redist: 
ms.custom: 19H1
f1_keywords:
 - peer_event_watchlist_changed_data_tag
 - p2p/peer_event_watchlist_changed_data_tag
 - PPEER_EVENT_WATCHLIST_CHANGED_DATA
 - p2p/PPEER_EVENT_WATCHLIST_CHANGED_DATA
 - PEER_EVENT_WATCHLIST_CHANGED_DATA
 - p2p/PEER_EVENT_WATCHLIST_CHANGED_DATA
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - P2P.h
api_name:
 - PEER_EVENT_WATCHLIST_CHANGED_DATA
---

# PEER_EVENT_WATCHLIST_CHANGED_DATA structure


## -description

The <b>PEER_EVENT_WATCHLIST_CHANGED_DATA</b> structure contains information returned when a PEER_EVENT_WATCHLIST_CHANGED event is raised on a peer participating in a peer collaboration network.

## -struct-fields

### -field pContact

Pointer to a <a href="/windows/desktop/api/p2p/ns-p2p-peer_contact">PEER_CONTACT</a> structure that contains information about the peer contact in the watchlist whose change raised the event.

### -field changeType

<a href="/windows/desktop/api/p2p/ne-p2p-peer_change_type">PEER_CHANGE_TYPE</a> enumeration value that specifies the type of change that occurred in the peer's watchlist.

## -remarks

The PEER_EVENT_WATCHLIST_CHANGED event is raised when the watch list is changed. The watch list is composed of the contacts that have <b>fWatch</b> set to true. If a new contact is added with <b>fWatch</b> set to true, or if an existing contact's <b>fWatch</b> is changed to true, the <b>changeType</b> member is set to PEER_CHANGE_ADDED. If <b>fWatch</b> is changed to false or if a contact is deleted, <b>changeType</b> is set to PEER_CHANGE_DELETED. 

The p2phost.exe service must running to receive this event. P2phost.exe is launched when an application calls <a href="/windows/desktop/api/p2p/nf-p2p-peercollabregisterevent">PeerCollabRegisterEvent</a> on this event.

## -see-also

<a href="/windows/desktop/api/p2p/ne-p2p-peer_change_type">PEER_CHANGE_TYPE</a>



<a href="/windows/desktop/api/p2p/ns-p2p-peer_contact">PEER_CONTACT</a>



<a href="/windows/desktop/P2PSdk/collaboration-api-structures">Peer Collaboration API Structures</a>