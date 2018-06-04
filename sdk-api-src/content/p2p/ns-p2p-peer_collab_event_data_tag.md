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

# peer_collab_event_data_tag structure


## -description


The <b>PEER_COLLAB_EVENT_DATA</b> union contains variant data for each possible peer collaboration network event raised on a peer.


## -struct-fields




### -field eventType


<a href="https://msdn.microsoft.com/2266c518-d383-4f37-9494-d57a3f780ced">PEER_COLLAB_EVENT_TYPE</a> enumeration value that contains the type of the event whose corresponding data structure appears in the subsequent union arm.


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
 

 

