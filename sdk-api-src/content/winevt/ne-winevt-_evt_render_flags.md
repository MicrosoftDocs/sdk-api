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

# _EVT_RENDER_FLAGS enumeration


## -description


Defines the values that specify what to render.


## -enum-fields




### -field EvtRenderEventValues

Render the event properties specified in the rendering context.


### -field EvtRenderEventXml

Render the event as an XML string. For details on the contents of the XML string, see the <a href="https://msdn.microsoft.com/36037697-b777-4e5c-99af-77964200a3e4">Event</a> schema.


### -field EvtRenderBookmark

Render the bookmark as an XML string, so that you can easily persist the bookmark for use later.

