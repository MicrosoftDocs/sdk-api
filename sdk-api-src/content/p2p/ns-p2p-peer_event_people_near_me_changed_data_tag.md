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
 

 

