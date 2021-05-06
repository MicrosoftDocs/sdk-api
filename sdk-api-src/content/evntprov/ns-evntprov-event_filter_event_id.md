---
UID: NS:evntprov._EVENT_FILTER_EVENT_ID
title: EVENT_FILTER_EVENT_ID (evntprov.h)
description:
  Defines event IDs used in an EVENT_FILTER_DESCRIPTOR structure for an event ID
  or stack walk filter.
helpviewer_keywords:
  [
    "*PEVENT_FILTER_EVENT_ID",
    "EVENT_FILTER_EVENT_ID",
    "EVENT_FILTER_EVENT_ID structure [ETW]",
    "PEVENT_FILTER_EVENT_ID",
    "PEVENT_FILTER_EVENT_ID structure pointer [ETW]",
    "etw.event_filter_event_id",
    "evntprov/EVENT_FILTER_EVENT_ID",
    "evntprov/PEVENT_FILTER_EVENT_ID",
  ]
old-location: etw\event_filter_event_id.htm
tech.root: ETW
ms.assetid: D660D140-BE86-44F6-B1D2-E1B97300BD11
ms.date: 12/05/2018
ms.keywords:
  "*PEVENT_FILTER_EVENT_ID, EVENT_FILTER_EVENT_ID, EVENT_FILTER_EVENT_ID
  structure [ETW], PEVENT_FILTER_EVENT_ID, PEVENT_FILTER_EVENT_ID structure
  pointer [ETW], etw.event_filter_event_id, evntprov/EVENT_FILTER_EVENT_ID,
  evntprov/PEVENT_FILTER_EVENT_ID"
req.header: evntprov.h
req.include-header:
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 R2 [desktop apps only]
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
req.typenames: EVENT_FILTER_EVENT_ID, *PEVENT_FILTER_EVENT_ID
req.redist:
ms.custom: 19H1
f1_keywords:
  - _EVENT_FILTER_EVENT_ID
  - evntprov/_EVENT_FILTER_EVENT_ID
  - PEVENT_FILTER_EVENT_ID
  - evntprov/PEVENT_FILTER_EVENT_ID
  - EVENT_FILTER_EVENT_ID
  - evntprov/EVENT_FILTER_EVENT_ID
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
  - EVENT_FILTER_EVENT_ID
---

# EVENT_FILTER_EVENT_ID structure

## -description

The **EVENT_FILTER_EVENT_ID** structure defines event IDs used in an
[EVENT_FILTER_DESCRIPTOR](/windows/desktop/api/evntprov/ns-evntprov-event_filter_descriptor)
structure for an event ID or stack walk filter.

## -struct-fields

### -field FilterIn

A value that indicates whether filtering should be enabled or disabled for the
event IDs passed in the **Events** member.

When this member is **TRUE**, filtering is enabled for the specified event IDs.
When this member is **FALSE**, filtering is disabled for the event IDs.

### -field Reserved

A reserved value.

### -field Count

The number of event IDs in the **Events** member.

### -field Events

An array of event IDs.

## -remarks

The **EVENT_FILTER_EVENT_ID** structure is used in the
[EVENT_FILTER_DESCRIPTOR](/windows/desktop/api/evntprov/ns-evntprov-event_filter_descriptor)
structure when the **Type** member of the **EVENT_FILTER_DESCRIPTOR** is set to
**EVENT_FILTER_TYPE_EVENT_ID** or **EVENT_FILTER_TYPE_STACKWALK**. This
corresponds to an event ID filter (one of the possible scope filters) or a stack
walk filter. The **EVENT_FILTER_EVENT_ID** structure contains an array of event
IDs and a Boolean value that indicates if filtering is enabled or disabled for
the specified event IDs.

## -see-also

[ENABLE_TRACE_PARAMETERS](/windows/desktop/ETW/enable-trace-parameters)

[EVENT_FILTER_DESCRIPTOR](/windows/desktop/api/evntprov/ns-evntprov-event_filter_descriptor)

[EnableTraceEx2](/windows/desktop/ETW/enabletraceex2)
