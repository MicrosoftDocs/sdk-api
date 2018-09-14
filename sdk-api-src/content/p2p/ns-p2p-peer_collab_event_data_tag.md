---
UID: NS:p2p.peer_collab_event_data_tag
title: peer_collab_event_data_tag
author: windows-sdk-content
description: Contains variant data for each possible peer collaboration network event raised on a peer.
old-location: p2p\peer_collab_event_data.htm
tech.root: p2psdk
ms.assetid: 4ddf200d-0b7a-4e99-b7db-19b4e0412711
ms.author: windowssdkdev
ms.date: 08/31/2018
ms.keywords: "*PPEER_COLLAB_EVENT_DATA, PEER_COLLAB_EVENT_DATA, PEER_COLLAB_EVENT_DATA structure [Peer Networking], PPEER_COLLAB_EVENT_DATA, PPEER_COLLAB_EVENT_DATA structure pointer [Peer Networking], p2p.peer_collab_event_data, p2p/PEER_COLLAB_EVENT_DATA, p2p/PPEER_COLLAB_EVENT_DATA, peer_collab_event_data_tag"
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
 - PEER_COLLAB_EVENT_DATA
product: Windows
targetos: Windows
req.typenames: PEER_COLLAB_EVENT_DATA, *PPEER_COLLAB_EVENT_DATA
req.redist: 
---

# peer_collab_event_data_tag structure


## -description


The <b>PEER_COLLAB_EVENT_DATA</b> union contains variant data for each possible peer collaboration network event raised on a peer.


## -struct-fields




### -field eventType


<a href="p2p.peer_collab_event_type">PEER_COLLAB_EVENT_TYPE</a> enumeration value that contains the type of the event whose corresponding data structure appears in the subsequent union arm.


### -field watchListChangedData

 


### -field watchListChangedData.case

 


### -field watchListChangedData.case.PEER_EVENT_WATCHLIST_CHANGED

 


### -field presenceChangedData

A <a href="https://msdn.microsoft.com/31b64adf-f015-404a-aed7-0b9a21d83c9a">PEER_EVENT_PRESENCE_CHANGED_DATA</a> structure. This data structure is present when <b>eventType</b> is set to PEER_EVENT_ENDPOINT_PRESENCE_CHANGED or PEER_EVENT_MY_PRESENCE_CHANGED.


### -field presenceChangedData.case

 


### -field presenceChangedData.case.PEER_EVENT_ENDPOINT_PRESENCE_CHANGED

 


### -field presenceChangedData.case.PEER_EVENT_MY_PRESENCE_CHANGED

 


### -field applicationChangedData

A <a href="https://msdn.microsoft.com/f06e9fbd-7655-4d00-8d84-78852a34f016">PEER_EVENT_APPLICATION_CHANGED_DATA</a> structure. This data structure is present when <b>eventType</b> is set to PEER_EVENT_ENDPOINT_APPLICATION_CHANGED or PEER_EVENT_MY_APPLICATION_CHANGED.


### -field applicationChangedData.case

 


### -field applicationChangedData.case.PEER_EVENT_ENDPOINT_APPLICATION_CHANGED

 


### -field applicationChangedData.case.PEER_EVENT_MY_APPLICATION_CHANGED

 


### -field objectChangedData

A <a href="https://msdn.microsoft.com/bba6a282-7ccd-45b2-a74c-3258449b990e">PEER_EVENT_OBJECT_CHANGED_DATA</a> structure. This data structure is present when <b>eventType</b> is set to PEER_EVENT_ENDPOINT_OBJECT_CHANGED or PEER_EVENT_MY_OBJECT_CHANGED.


### -field objectChangedData.case

 


### -field objectChangedData.case.PEER_EVENT_ENDPOINT_OBJECT_CHANGED

 


### -field objectChangedData.case.PEER_EVENT_MY_OBJECT_CHANGED

 


### -field endpointChangedData

A <a href="https://msdn.microsoft.com/e2ce28c6-6dc0-4ceb-aa3f-7b86a2581425">PEER_EVENT_ENDPOINT_CHANGED_DATA</a> structure. This data structure is present when <b>eventType</b> is set to PEER_EVENT_ENDPOINT_CHANGED or PEER_EVENT_MY_ENDPOINT_CHANGED.


### -field endpointChangedData.case

 


### -field endpointChangedData.case.PEER_EVENT_ENDPOINT_CHANGED

 


### -field endpointChangedData.case.PEER_EVENT_MY_ENDPOINT_CHANGED

 


### -field peopleNearMeChangedData

A <a href="https://msdn.microsoft.com/d983a399-17b1-43ea-a8fb-05b5d75e179a">PEER_EVENT_PEOPLE_NEAR_ME_CHANGED_DATA</a> structure. This data structure is present when <b>eventType</b> is set to PEER_EVENT_PEOPLE_NEAR_ME_CHANGED.


### -field peopleNearMeChangedData.case

 


### -field peopleNearMeChangedData.case.PEER_EVENT_PEOPLE_NEAR_ME_CHANGED

 


### -field requestStatusChangedData

A <a href="https://msdn.microsoft.com/88bcf892-5591-49a0-bb00-090f4d5f2f79">PEER_EVENT_REQUEST_STATUS_CHANGED_DATA</a> structure. This data structure is present when <b>eventType</b> is set to PEER_EVENT_REQUEST_STATUS_CHANGED.


### -field requestStatusChangedData.case

 


### -field requestStatusChangedData.case.PEER_EVENT_REQUEST_STATUS_CHANGED

 


### -field switch_is

 


### -field switch_is.eventType

 




#### - watchlistChangedData

A <a href="https://msdn.microsoft.com/9d4af44c-c03f-4d9f-9b36-c04513a18133">PEER_EVENT_WATCHLIST_CHANGED_DATA</a> structure. This data structure is present when <b>eventType</b> is set to PEER_EVENT_WATCHLIST_CHANGED.


## -see-also




<a href="https://msdn.microsoft.com/2634899c-3263-45ce-9fac-407e11e42cd4">Peer Collaboration API Structures</a>
 

 

