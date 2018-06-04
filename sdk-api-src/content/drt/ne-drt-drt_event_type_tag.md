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

# drt_event_type_tag enumeration


## -description


The <b>DRT_EVENT_TYPE</b> enumeration defines the set of events that can be raised by the Distributed Routing Table.


## -enum-fields




### -field DRT_EVENT_STATUS_CHANGED

The status of the local DRT instance has changed.


### -field DRT_EVENT_LEAFSET_KEY_CHANGED

A key or node was changed from the DRT leaf set of the local node.


### -field DRT_EVENT_REGISTRATION_STATE_CHANGED

A locally published key is no longer resolvable by other nodes.


## -remarks



The event handle passed to <a href="https://msdn.microsoft.com/67320767-f622-478a-a886-bbea1650ac1a">DrtOpen</a> is signaled with an event  specified by the <b>DRT_EVENT_TYPE</b> enumeration.




## -see-also




<a href="https://msdn.microsoft.com/67320767-f622-478a-a886-bbea1650ac1a">DrtOpen</a>
 

 

