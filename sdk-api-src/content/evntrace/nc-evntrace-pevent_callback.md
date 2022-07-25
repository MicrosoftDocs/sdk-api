---
UID: NC:evntrace.PEVENT_CALLBACK
title: PEVENT_CALLBACK (evntrace.h)
description:
  ETW event consumers implement this callback to receive events from a trace
  processing session. The EventRecordCallback callback supersedes this callback.
helpviewer_keywords:
  [
    "EventCallback",
    "EventCallback callback function [ETW]",
    "PEVENT_CALLBACK",
    "PEVENT_CALLBACK callback",
    "_evt_eventcallback",
    "base.eventcallback",
    "etw.eventcallback",
    "evntrace/EventCallback",
  ]
old-location: etw\eventcallback.htm
tech.root: ETW
ms.assetid: 9312eaed-2997-4d44-952a-fcae3b262947
ms.date: 12/05/2018
ms.keywords:
  EventCallback, EventCallback callback function [ETW], PEVENT_CALLBACK,
  PEVENT_CALLBACK callback, _evt_eventcallback, base.eventcallback,
  etw.eventcallback, evntrace/EventCallback
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
req.typenames:
req.redist:
ms.custom: 19H1
f1_keywords:
  - PEVENT_CALLBACK
  - evntrace/PEVENT_CALLBACK
dev_langs:
  - c++
topic_type:
  - APIRef
  - kbSyntax
api_type:
  - UserDefined
api_location:
  - Evntrace.h
api_name:
  - EventCallback
---

# PEVENT_CALLBACK callback function

## -description

ETW event consumers implement this callback to receive events from a trace
processing session. This callback should not be used in new code. Instead,
implement
[EventRecordCallback](/windows/win32/api/evntrace/nc-evntrace-pevent_record_callback).

The **PEVENT_CALLBACK** type is a pointer to this callback function.
**EventCallback** is a placeholder for the application-defined function name.

## -parameters

### -param pEvent [in]

Pointer to an [EVENT_TRACE](/windows/win32/api/evntrace/ns-evntrace-event_trace)
structure that contains the event information.

## -remarks

> [!Note]
> This callback is obsolete because it receives incomplete information
> about the event and is not compatible with event decoding helper APIs such as
> [TdhGetEventInformation](/windows/win32/api/tdh/nf-tdh-tdhgeteventinformation).
> Instead of implementing **EventCallback**, implement
> [EventRecordCallback](/windows/win32/api/evntrace/nc-evntrace-pevent_record_callback).

To specify the function that ETW calls to deliver the events, set the
**EventCallback** member of the
[EVENT_TRACE_LOGFILE](/windows/win32/api/evntrace/ns-evntrace-event_trace_logfilea)
structure that you pass to the
[OpenTrace](/windows/win32/api/evntrace/nf-evntrace-opentracea) function.

> [!Note]
> If your **EventCallback** function is receiving garbled data from
> **ProcessTrace**, double-check the flags specified in the `ProcessTraceMode`
> field of the `EVENT_TRACE_LOGFILE` structure that was provided to
> **OpenTrace**. `EVENT_TRACE_LOGFILE`'s **EventCallback** and
> **EventRecordCallback** fields are overlapping members of a union. If the
> `ProcessTraceMode` field includes the `PROCESS_TRACE_MODE_EVENT_RECORD` flag,
> **ProcessTrace** will invoke your callback using the **EventRecordCallback**
> function signature. Otherwise, **ProcessTrace** will invoke your callback
> using the **EventCallback** function signature.

After using [OpenTrace](/windows/win32/api/evntrace/nf-evntrace-opentracea) to
create the trace processing session, call the
[ProcessTrace](/windows/win32/api/evntrace/nf-evntrace-processtrace) function to
begin receiving the events.

When **ProcessTrace** begins processing events from a trace, it may invoke your
callback with one or more synthetic events that contain data about the trace
(metadata) rather than data from logged events. These synthetic events have
**Header.Guid** set to `EventTraceGuid` and **Header.Class.Type** set based on
the content of the synthetic event. For example, the first event from each trace
file will be a synthetic event with type 0 containing
[TRACE_LOGFILE_HEADER](/windows/win32/api/evntrace/ns-evntrace-trace_logfile_header)
information.

All the other events you receive contain provider-specific event data. You use
the **Header.Guid** and **Header.Class.Type** members of
[EVENT_TRACE](/windows/win32/api/evntrace/ns-evntrace-event_trace) to determine
the type of event you received. It is possible to hard-code decoding logic for
well-known event types, but most events will be decoded using MOF schema
information registered on the system in the `\\root\wmi` namespace. For
information on using an event's MOF schema to interpret the event, see
[Consuming Events](/windows/win32/etw/consuming-events).

### Examples

For an example implementation of an **EventCallback** function, see
[Retrieving Event Data Using MOF](/windows/win32/etw/retrieving-event-data-using-mof).

## -see-also

[Consuming Events](/windows/win32/etw/consuming-events)

[BufferCallback](/windows/win32/api/evntrace/nc-evntrace-pevent_trace_buffer_callbacka)

[EventRecordCallback](/windows/win32/api/evntrace/nc-evntrace-pevent_record_callback)

[EVENT_TRACE_LOGFILE](/windows/win32/api/evntrace/ns-evntrace-event_trace_logfilea)

[OpenTrace](/windows/win32/api/evntrace/nf-evntrace-opentracea)

[ProcessTrace](/windows/win32/api/evntrace/nf-evntrace-processtrace)
