---
UID: NS:evntprov._EVENT_FILTER_LEVEL_KW
title: EVENT_FILTER_LEVEL_KW (evntprov.h)
author: windows-sdk-content
description: Defines event IDs used in an EVENT_FILTER_DESCRIPTOR structure for a stack walk level-keyword filter.
old-location: etw\event_filter_level_kw.htm
tech.root: ETW
ms.assetid: 2FE25C55-8028-4894-9DD8-FC997B7D9ADB
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: "*PEVENT_FILTER_LEVEL_KW, EVENT_FILTER_LEVEL_KW, EVENT_FILTER_LEVEL_KW structure [ETW], PEVENT_FILTER_LEVEL_KW, PEVENT_FILTER_LEVEL_KW structure pointer [ETW], etw.event_filter_level_kw, evntprov/EVENT_FILTER_LEVEL_KW, evntprov/PEVENT_FILTER_LEVEL_KW"
ms.topic: struct
f1_keywords: ["evntprov/EVENT_FILTER_LEVEL_KW"]
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
 - EVENT_FILTER_LEVEL_KW
product: Windows
targetos: Windows
req.typenames: EVENT_FILTER_LEVEL_KW, *PEVENT_FILTER_LEVEL_KW
req.redist: 
ms.custom: 19H1
---

# EVENT_FILTER_LEVEL_KW structure


## -description


The <b>EVENT_FILTER_LEVEL_KW</b> structure defines event IDs used in an <a href="https://docs.microsoft.com/windows/desktop/api/evntprov/ns-evntprov-_event_filter_descriptor">EVENT_FILTER_DESCRIPTOR</a> structure for a stack walk level-keyword filter.

This filter is only applied to events that are otherwise enabled
on the logging session, via a level/keyword in the enable call.


## -struct-fields




### -field MatchAnyKeyword

Bitmask of keywords that determine the category of events to filter on.


### -field MatchAllKeyword

This bitmask is optional. This mask further restricts the category of events that you want to filter on. If the event's keyword meets the <b>MatchAnyKeyword</b> condition, the provider will filter the event only if all of the bits in this mask exist in the event's keyword. This mask is not used if <b>MatchAnyKeyword</b> is zero.


### -field Level

Defines the severity level of the event to filter on.


### -field FilterIn

<b>true</b> to filter the events matching the provided names in; <b>false</b> to filter them out.

If set to <b>true</b>, the filtered events will have stacks collected.

