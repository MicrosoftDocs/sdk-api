---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
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

The p2phost.exe service must running to receive this event. P2phost.exe is launched when an application calls <a href="https://msdn.microsoft.com/db7daf08-8d79-493f-8df5-172dae498df0">PeerCollabRegisterEvent</a> on this event.




## -see-also




<a href="https://msdn.microsoft.com/ef8f1cc7-e1db-4d6d-9ff6-141746d0787a">PEER_CHANGE_TYPE</a>



<a href="https://msdn.microsoft.com/b84a17fc-35d6-4098-9bb3-18e708541a80">PEER_CONTACT</a>



<a href="https://msdn.microsoft.com/2634899c-3263-45ce-9fac-407e11e42cd4">Peer Collaboration API Structures</a>
 

 

