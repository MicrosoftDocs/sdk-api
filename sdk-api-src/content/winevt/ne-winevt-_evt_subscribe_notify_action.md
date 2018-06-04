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

# _EVT_SUBSCRIBE_NOTIFY_ACTION enumeration


## -description


Defines the possible types of data that the subscription service can deliver to your callback.


## -enum-fields




### -field EvtSubscribeActionError

Indicates that the <i>Event</i> parameter contains a Win32 error code.


### -field EvtSubscribeActionDeliver

Indicates that the <i>Event</i> parameter contains an event that matches the subscriber's query.


## -see-also




<a href="https://msdn.microsoft.com/935a787c-fd71-492d-a803-80cb2c9019ea">EVT_SUBSCRIBE_CALLBACK</a>
 

 

