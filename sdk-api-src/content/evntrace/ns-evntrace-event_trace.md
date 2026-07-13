---
UID: NS:evntrace._EVENT_TRACE
title: EVENT_TRACE (evntrace.h)
description:
  The EVENT_TRACE structure is used to deliver event information to an event
  trace consumer.
helpviewer_keywords:
  [
    "*PEVENT_TRACE",
    "EVENT_TRACE",
    "EVENT_TRACE structure [ETW]",
    "PEVENT_TRACE",
    "PEVENT_TRACE structure pointer [ETW]",
    "_EVENT_TRACE",
    "_evt_event_trace",
    "base.event_trace",
    "etw.event_trace",
    "evntrace/EVENT_TRACE",
    "evntrace/PEVENT_TRACE",
  ]
old-location: etw\event_trace.htm
tech.root: ETW
ms.assetid: d8a6b63e-0cd4-4d19-b0b3-16bb0d33e4c0
ms.date: 12/05/2018
ms.keywords:
  "*PEVENT_TRACE, EVENT_TRACE, EVENT_TRACE structure [ETW], PEVENT_TRACE,
  PEVENT_TRACE structure pointer [ETW], _EVENT_TRACE, _evt_event_trace,
  base.event_trace, etw.event_trace, evntrace/EVENT_TRACE, evntrace/PEVENT_TRACE"
req.header: evntrace.h
req.include-header:
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
req.typenames: EVENT_TRACE, *PEVENT_TRACE
req.redist:
ms.custom: 19H1
f1_keywords:
  - _EVENT_TRACE
  - evntrace/_EVENT_TRACE
  - PEVENT_TRACE
  - evntrace/PEVENT_TRACE
  - EVENT_TRACE
  - evntrace/EVENT_TRACE
dev_langs:
  - c++
topic_type:
  - APIRef
  - kbSyntax
api_type:
  - HeaderDef
api_location:
  - Evntrace.h
api_name:
  - EVENT_TRACE
---

# EVENT_TRACE structure

## -description

The **EVENT_TRACE** structure is used to deliver event information to an event
trace consumer.

## -struct-fields

### -field Header

An
[EVENT_TRACE_HEADER](/windows/win32/api/evntrace/ns-evntrace-event_trace_header)
structure that contains standard event tracing information.

### -field InstanceId

Instance identifier. Contains valid data when the provider calls the
[TraceEventInstance](/windows/win32/api/evntrace/nf-evntrace-traceeventinstance)
function to generate the event. Otherwise, the value is zero.

### -field ParentInstanceId

Instance identifier for a parent event. Contains valid data when the provider
calls the
[TraceEventInstance](/windows/win32/api/evntrace/nf-evntrace-traceeventinstance)
function to generate the event. Otherwise, the value is zero.

### -field ParentGuid

Class GUID of the parent event. Contains valid data when the provider calls the
[TraceEventInstance](/windows/win32/api/evntrace/nf-evntrace-traceeventinstance)
function to generate the event. Otherwise, the value is zero.

### -field MofData

Pointer to the beginning of the event-specific data for this event.

### -field MofLength

Number of bytes to which **MofData** points.

### -field DUMMYUNIONNAME

### -field DUMMYUNIONNAME.ClientContext

Reserved.

### -field DUMMYUNIONNAME.BufferContext

Provides information about the event such as the session identifier and
processor number of the CPU on which the provider process ran. For details, see
the
[ETW_BUFFER_CONTEXT](/windows/win32/api/evntrace/ns-evntrace-etw_buffer_context)
structure.

**Prior to Windows Vista:** Not supported.

## -remarks

[ProcessTrace](/windows/win32/api/evntrace/nf-evntrace-processtrace) passes this
structure to the consumer's
[EventCallback](/windows/win32/api/evntrace/nc-evntrace-pevent_callback)
callback function.

## -see-also

[EventCallback](/windows/win32/api/evntrace/nc-evntrace-pevent_callback)
