---
UID: NE:winevt._EVT_FORMAT_MESSAGE_FLAGS
title: "_EVT_FORMAT_MESSAGE_FLAGS"
author: windows-sdk-content
description: Defines the values that specify the message string from the event to format.
old-location: wes\evt_format_message_flags.htm
tech.root: wes
ms.assetid: 6a8ed14a-1952-4fcf-ac66-12c1fecd363f
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: EVT_FORMAT_MESSAGE_FLAGS, EVT_FORMAT_MESSAGE_FLAGS enumeration [EventLog], EvtFormatMessageChannel, EvtFormatMessageEvent, EvtFormatMessageId, EvtFormatMessageKeyword, EvtFormatMessageLevel, EvtFormatMessageOpcode, EvtFormatMessageProvider, EvtFormatMessageTask, EvtFormatMessageXml, _EVT_FORMAT_MESSAGE_FLAGS, wes.evt_format_message_flags, winevt/EVT_FORMAT_MESSAGE_FLAGS, winevt/EvtFormatMessageChannel, winevt/EvtFormatMessageEvent, winevt/EvtFormatMessageId, winevt/EvtFormatMessageKeyword, winevt/EvtFormatMessageLevel, winevt/EvtFormatMessageOpcode, winevt/EvtFormatMessageProvider, winevt/EvtFormatMessageTask, winevt/EvtFormatMessageXml
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
req.header: winevt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
 - WinEvt.h
api_name:
 - EVT_FORMAT_MESSAGE_FLAGS
product: Windows
targetos: Windows
req.typenames: EVT_FORMAT_MESSAGE_FLAGS
req.redist: 
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
 

 

