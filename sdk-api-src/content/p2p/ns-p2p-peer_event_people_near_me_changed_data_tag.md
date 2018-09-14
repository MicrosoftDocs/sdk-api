---
UID: NS:p2p.peer_event_people_near_me_changed_data_tag
title: peer_event_people_near_me_changed_data_tag
author: windows-sdk-content
description: The PEER_EVENT_PEOPLE_NEAR_ME_CHANGED_DATA structure contains information returned when a PEER_EVENT_PEOPLE_NEAR_ME_CHANGED event is raised on a peer participating in a subnet-specific peer collaboration network.
old-location: p2p\peer_event_people_near_me_changed_data.htm
tech.root: p2psdk
ms.assetid: d983a399-17b1-43ea-a8fb-05b5d75e179a
ms.author: windowssdkdev
ms.date: 08/31/2018
ms.keywords: "*PPEER_EVENT_PEOPLE_NEAR_ME_CHANGED_DATA, PEER_EVENT_PEOPLE_NEAR_ME_CHANGED_DATA, PEER_EVENT_PEOPLE_NEAR_ME_CHANGED_DATA structure [Peer Networking], PPEER_EVENT_PEOPLE_NEAR_ME_CHANGED_DATA, PPEER_EVENT_PEOPLE_NEAR_ME_CHANGED_DATA structure pointer [Peer Networking], p2p.peer_event_people_near_me_changed_data, p2p/PEER_EVENT_PEOPLE_NEAR_ME_CHANGED_DATA, p2p/PPEER_EVENT_PEOPLE_NEAR_ME_CHANGED_DATA, peer_event_people_near_me_changed_data_tag"
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - P2P.h
api_name:
 - PEER_EVENT_PEOPLE_NEAR_ME_CHANGED_DATA
product: Windows
targetos: Windows
req.typenames: PEER_EVENT_PEOPLE_NEAR_ME_CHANGED_DATA, *PPEER_EVENT_PEOPLE_NEAR_ME_CHANGED_DATA
req.redist: 
---

# peer_event_people_near_me_changed_data_tag structure


## -description


The <b>PEER_EVENT_PEOPLE_NEAR_ME_CHANGED_DATA</b> structure contains information returned when a PEER_EVENT_PEOPLE_NEAR_ME_CHANGED event is raised on a peer participating in a subnet-specific peer collaboration network. 


## -struct-fields




### -field changeType


<a href="https://msdn.microsoft.com/ef8f1cc7-e1db-4d6d-9ff6-141746d0787a">PEER_CHANGE_TYPE</a> enumeration value that describes the type of change that occurred for a contact available on the local subnet.


### -field pPeopleNearMe

Pointer to a <a href="https://msdn.microsoft.com/15dae06d-0f44-4e7d-b146-6fcd7cc6912e">PEER_PEOPLE_NEAR_ME</a> structure that contains the peer endpoint information for the contact on the subnet that raised the change event.


## -remarks



The information that can be changed in a peer contact include the endpoint's name or its associated IPv6 address. 

 If the <b>changeType</b> is set to PEER_CHANGE_ADDED and <b>pEndpoint</b> is set to <b>NULL</b>, then the local peer has signed in. Otherwise, if <b>changeType</b> is set to PEER_CHANGE_DELETEDimplies the local peer has signed out.




## -see-also




<a href="https://msdn.microsoft.com/ef8f1cc7-e1db-4d6d-9ff6-141746d0787a">PEER_CHANGE_TYPE</a>



<a href="https://msdn.microsoft.com/15dae06d-0f44-4e7d-b146-6fcd7cc6912e">PEER_PEOPLE_NEAR_ME</a>



<a href="https://msdn.microsoft.com/2634899c-3263-45ce-9fac-407e11e42cd4">Peer Collaboration API Structures</a>
 

 

