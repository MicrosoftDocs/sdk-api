---
UID: NS:evntprov._EVENT_FILTER_EVENT_NAME
title: "_EVENT_FILTER_EVENT_NAME"
author: windows-sdk-content
description: Defines event IDs used in an EVENT_FILTER_DESCRIPTOR structure for an event name or stalk walk name filter.
old-location: etw\event_filter_event_name.htm
tech.root: etw
ms.assetid: 85E8C8F8-31D4-42F1-9267-15F74E473D57
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: "*PEVENT_FILTER_EVENT_NAME, EVENT_FILTER_EVENT_NAME, EVENT_FILTER_EVENT_NAME structure [ETW], _EVENT_FILTER_EVENT_NAME, etw.event_filter_event_name, evntprov/EVENT_FILTER_EVENT_NAME"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: evntprov.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10, version 1709 [desktop apps only]
req.target-min-winversvr: Windows Server 2016 [desktop apps only]
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
 - Evntprov.h
api_name:
 - EVENT_FILTER_EVENT_NAME
product: Windows
targetos: Windows
req.typenames: EVENT_FILTER_EVENT_NAME, *PEVENT_FILTER_EVENT_NAME
req.redist: 
---

# _EVENT_FILTER_EVENT_NAME structure


## -description


The <b>EVENT_FILTER_EVENT_NAME</b> structure defines event IDs used in an <a href="https://msdn.microsoft.com/9318868a-29d8-4a5e-9579-c06a7c0fd78f">EVENT_FILTER_DESCRIPTOR</a> structure for an  event name or stalk walk name filter. 

This filter will only be applied to events that are otherwise enabled
on the logging session, via level/keyword in the enable call.


## -struct-fields




### -field MatchAnyKeyword

Bitmask of keywords that determine the category of events to filter on.


### -field MatchAllKeyword

This bitmask is optional. This mask further restricts the category of events that you want to filter on. If the event's keyword meets the <b>MatchAnyKeyword</b> condition, the provider will filter the event only if all of the bits in this mask exist in the event's keyword. This mask is not used if <b>MatchAnyKeyword</b> is zero.


### -field Level

Defines the severity level of the event to filter on.


### -field FilterIn

<b>True</b> to filter the events matching the provided names in; <b>false</b> to filter them out.

When used for the <b>EVENT_FILTER_TYPE_STACKWALK_NAME</b>filter type, the filtered in events will have stacks collected for them.


### -field NameCount

The number of names in the <b>Names</b> member.


### -field Names

An <b>NameCount</b> long array of null-terminated, UTF-8
event names.


## -remarks







