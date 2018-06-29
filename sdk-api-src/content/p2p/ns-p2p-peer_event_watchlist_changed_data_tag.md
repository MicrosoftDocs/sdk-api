---
UID: NS:p2p.peer_event_watchlist_changed_data_tag
title: peer_event_watchlist_changed_data_tag
author: windows-sdk-content
description: The PEER_EVENT_WATCHLIST_CHANGED_DATA structure contains information returned when a PEER_EVENT_WATCHLIST_CHANGED event is raised on a peer participating in a peer collaboration network.
old-location: p2p\peer_event_watchlist_changed_data.htm
old-project: P2PSdk
ms.assetid: 9d4af44c-c03f-4d9f-9b36-c04513a18133
ms.author: windowssdkdev
ms.date: 05/29/2018
ms.keywords: "*PPEER_EVENT_WATCHLIST_CHANGED_DATA, PEER_EVENT_WATCHLIST_CHANGED_DATA, PEER_EVENT_WATCHLIST_CHANGED_DATA structure [Peer Networking], PPEER_EVENT_WATCHLIST_CHANGED_DATA, PPEER_EVENT_WATCHLIST_CHANGED_DATA structure pointer [Peer Networking], p2p.peer_event_watchlist_changed_data, p2p/PEER_EVENT_WATCHLIST_CHANGED_DATA, p2p/PPEER_EVENT_WATCHLIST_CHANGED_DATA, peer_event_watchlist_changed_data_tag"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
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
req.typenames: PEER_EVENT_WATCHLIST_CHANGED_DATA, *PPEER_EVENT_WATCHLIST_CHANGED_DATA
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - P2P.h
api_name:
 - PEER_EVENT_WATCHLIST_CHANGED_DATA
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: ADAM
---

# peer_event_watchlist_changed_data_tag structure


## -description


The <b>PEER_EVENT_WATCHLIST_CHANGED_DATA</b> structure contains information returned when a PEER_EVENT_WATCHLIST_CHANGED event is raised on a peer participating in a peer collaboration network.


## -struct-fields




### -field pContact

Pointer to a <a href="https://msdn.microsoft.com/b84a17fc-35d6-4098-9bb3-18e708541a80">PEER_CONTACT</a> structure that contains information about the peer contact in the watchlist whose change raised the event.


### -field changeType


<a href="https://msdn.microsoft.com/ef8f1cc7-e1db-4d6d-9ff6-141746d0787a">PEER_CHANGE_TYPE</a> enumeration value that specifies the type of change that occurred in the peer's watchlist.


## -remarks



The PEER_EVENT_WATCHLIST_CHANGED event is raised when the watch list is changed. The watch list is composed of the contacts that have <b>fWatch</b> set to true. If a new contact is added with <b>fWatch</b> set to true, or if an existing contact's <b>fWatch</b> is changed to true, the <b>changeType</b> member is set to PEER_CHANGE_ADDED. If <b>fWatch</b> is changed to false or if a contact is deleted, <b>changeType</b> is set to PEER_CHANGE_DELETED. 

The p2phost.exe service must running to receive this event. P2phost.exe is launched when an application calls <a href="https://msdn.microsoft.com/library/Aa371077(v=VS.85).aspx">PeerCollabRegisterEvent</a> on this event.




## -see-also




<a href="https://msdn.microsoft.com/ef8f1cc7-e1db-4d6d-9ff6-141746d0787a">PEER_CHANGE_TYPE</a>



<a href="https://msdn.microsoft.com/b84a17fc-35d6-4098-9bb3-18e708541a80">PEER_CONTACT</a>



<a href="https://msdn.microsoft.com/2634899c-3263-45ce-9fac-407e11e42cd4">Peer Collaboration API Structures</a>
 

 

