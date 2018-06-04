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

# _EC_SUBSCRIPTION_CONTENT_FORMAT enumeration


## -description


The <b>EC_SUBSCRIPTION_CONTENT_FORMAT</b> enumeration specifies how events will be rendered on the computer that sends the events before the events are sent to the event collector computer.


## -enum-fields




### -field EcContentFormatEvents

When an event is received, the Event Collector service sends an event as the received event to an event log. The service sends the raw event data only, and not any localized event data.


### -field EcContentFormatRenderedText

When an event is received, the Event Collector service sends an event as rendered text to an event log. The service sends raw event data and localized event information.

