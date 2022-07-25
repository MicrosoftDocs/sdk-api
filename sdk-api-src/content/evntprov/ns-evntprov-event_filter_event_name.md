---
UID: NS:evntprov._EVENT_FILTER_EVENT_NAME
title: EVENT_FILTER_EVENT_NAME (evntprov.h)
description:
  Defines event IDs used in an EVENT_FILTER_DESCRIPTOR structure for an event
  name or stalk walk name filter.
helpviewer_keywords:
  [
    "*PEVENT_FILTER_EVENT_NAME",
    "EVENT_FILTER_EVENT_NAME",
    "EVENT_FILTER_EVENT_NAME structure [ETW]",
    "etw.event_filter_event_name",
    "evntprov/EVENT_FILTER_EVENT_NAME",
  ]
old-location: etw\event_filter_event_name.htm
tech.root: ETW
ms.assetid: 85E8C8F8-31D4-42F1-9267-15F74E473D57
ms.date: 12/05/2018
ms.keywords:
  "*PEVENT_FILTER_EVENT_NAME, EVENT_FILTER_EVENT_NAME, EVENT_FILTER_EVENT_NAME
  structure [ETW], etw.event_filter_event_name, evntprov/EVENT_FILTER_EVENT_NAME"
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
targetos: Windows
req.typenames: EVENT_FILTER_EVENT_NAME, *PEVENT_FILTER_EVENT_NAME
req.redist:
ms.custom: 19H1
f1_keywords:
  - _EVENT_FILTER_EVENT_NAME
  - evntprov/_EVENT_FILTER_EVENT_NAME
  - PEVENT_FILTER_EVENT_NAME
  - evntprov/PEVENT_FILTER_EVENT_NAME
  - EVENT_FILTER_EVENT_NAME
  - evntprov/EVENT_FILTER_EVENT_NAME
dev_langs:
  - c++
topic_type:
  - APIRef
  - kbSyntax
api_type:
  - HeaderDef
api_location:
  - Evntprov.h
api_name:
  - EVENT_FILTER_EVENT_NAME
---

# EVENT_FILTER_EVENT_NAME structure

## -description

The **EVENT_FILTER_EVENT_NAME** structure defines event IDs used in an
[EVENT_FILTER_DESCRIPTOR](/windows/desktop/api/evntprov/ns-evntprov-event_filter_descriptor)
structure for an event name or stalk walk name filter.

This filter will only be applied to events that are otherwise enabled on the
logging session, via level/keyword in the enable call.

## -struct-fields

### -field MatchAnyKeyword

Bitmask of keywords that determine the category of events to filter on.

### -field MatchAllKeyword

This bitmask is optional. This mask further restricts the category of events
that you want to filter on. If the event's keyword meets the **MatchAnyKeyword**
condition, the provider will filter the event only if all of the bits in this
mask exist in the event's keyword. This mask is not used if **MatchAnyKeyword**
is zero.

### -field Level

Defines the severity level of the event to filter on.

### -field FilterIn

**True** to filter the events matching the provided names in; **false** to
filter them out.

When used for the **EVENT_FILTER_TYPE_STACKWALK_NAME**filter type, the filtered
in events will have stacks collected for them.

### -field NameCount

The number of names in the **Names** member.

### -field Names

An **NameCount** long array of null-terminated, UTF-8 event names.

## -remarks
