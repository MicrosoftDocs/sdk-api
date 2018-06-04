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

# _RTM_EVENT_TYPE enumeration


## -description


The <b>RTM_EVENT_TYPE</b> enumeration enumerates the events that the routing table manager can notify the client about using the 
<a href="https://msdn.microsoft.com/57179cea-d92b-4199-bb61-b34d980532cf">RTM_EVENT_CALLBACK</a> callback.


## -enum-fields




### -field RTM_ENTITY_REGISTERED

A client has just registered with the routing table manager.


### -field RTM_ENTITY_DEREGISTERED

A client has just unregistered.


### -field RTM_ROUTE_EXPIRED

A route has timed out.


### -field RTM_CHANGE_NOTIFICATION

A change notification has been made.


## -see-also




<a href="https://msdn.microsoft.com/57179cea-d92b-4199-bb61-b34d980532cf">RTM_EVENT_CALLBACK</a>
 

 

