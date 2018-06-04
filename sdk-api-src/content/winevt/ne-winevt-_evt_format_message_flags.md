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

# _EVT_FORMAT_MESSAGE_FLAGS enumeration


## -description


Defines the values that specify the message string from the event to format.


## -enum-fields




### -field EvtFormatMessageEvent

Format the event's message string.


### -field EvtFormatMessageLevel

Format the message string of the level specified in the event.


### -field EvtFormatMessageTask

Format the message string of the task specified in the event.


### -field EvtFormatMessageOpcode

Format the message string of the opcode specified in the event.


### -field EvtFormatMessageKeyword

Format the message string of the keywords specified in the event. If the event specifies multiple keywords, the formatted string is a list of null-terminated strings. Increment through the strings until your pointer points past the end of the used buffer.


### -field EvtFormatMessageChannel

Format the message string of the channel specified in the event.


### -field EvtFormatMessageProvider

Format the provider's message string.


### -field EvtFormatMessageId

Format the message string associated with a resource identifier. The provider's metadata contains the resource identifiers; the message compiler assigns a resource identifier to each string when it compiles the manifest.   


### -field EvtFormatMessageXml

Format all the message strings in the event. The formatted message is an XML string that contains the event details and the message strings. The message strings are included in the <a href="https://msdn.microsoft.com/85a4cfc6-6277-4af8-af4e-cae3bd3aac13">RenderingInfo</a> section of the event details.


## -see-also




<a href="https://msdn.microsoft.com/744fe166-b12c-49d4-ab13-b2ef6a6f9625">EvtFormatMessage</a>
 

 

