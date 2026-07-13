---
UID: NC:evntrace.PEVENT_RECORD_CALLBACK
title: PEVENT_RECORD_CALLBACK (evntrace.h)
description:
  ETW event consumers implement this callback to receive events from a trace
  processing session. The PEVENT_RECORD_CALLBACK type defines a pointer to this
  callback function. EventRecordCallback is a placeholder for the
  application-defined function name.
helpviewer_keywords:
  [
    "EventRecordCallback",
    "EventRecordCallback callback function [ETW]",
    "PEVENT_RECORD_CALLBACK",
    "PEVENT_RECORD_CALLBACK callback",
    "etw.eventrecordcallback",
    "evntrace/EventRecordCallback",
  ]
old-location: etw\eventrecordcallback.htm
tech.root: ETW
ms.assetid: 80a30faf-af1f-4440-8a17-9df44bdb2291
ms.date: 12/05/2018
ms.keywords:
  EventRecordCallback, EventRecordCallback callback function [ETW],
  PEVENT_RECORD_CALLBACK, PEVENT_RECORD_CALLBACK callback,
  etw.eventrecordcallback, evntrace/EventRecordCallback
req.header: evntrace.h
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
targetos: Windows
req.typenames:
req.redist:
ms.custom: 19H1
f1_keywords:
  - PEVENT_RECORD_CALLBACK
  - evntrace/PEVENT_RECORD_CALLBACK
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
  - EventRecordCallback
---

# PEVENT_RECORD_CALLBACK callback function

## -description

Consumers implement this callback to receive events from a trace processing
session.

The **PEVENT_RECORD_CALLBACK** type defines a pointer to this callback function.
**EventRecordCallback** is a placeholder for the application-defined function
name.

## -parameters

### -param EventRecord [in]

Pointer to an
[EVENT_RECORD](/windows/win32/api/evntcons/ns-evntcons-event_record) structure
that contains the event information.

## -remarks

To specify the function that ETW calls to deliver events, set the
**EventRecordCallback**, **Context**, and **ProcessTraceMode** members of the
[EVENT_TRACE_LOGFILE](/windows/win32/api/evntrace/ns-evntrace-event_trace_logfilea)
structure that you pass to the
[OpenTrace](/windows/win32/api/evntrace/nf-evntrace-opentracea) function.

- Set **EventRecordCallback** to the address of your callback function.
- Set **Context** to a value that should be included in the **UserContext**
  field of each **EVENT_RECORD** provided to your callback.
- Set **ProcessTraceMode** to the flags to be used when processing the trace. To
  use **EventRecordCallback**, you must include
  **PROCESS_TRACE_MODE_EVENT_RECORD** in the **ProcessTraceMode** value.

> [!Note]
> If your **EventRecordCallback** function is receiving garbled data
> from **ProcessTrace**, double-check the flags specified in the
> `ProcessTraceMode` field of the `EVENT_TRACE_LOGFILE` structure that was
> provided to **OpenTrace**. `EVENT_TRACE_LOGFILE`'s **EventCallback** and
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
**EventHeader.ProviderId** set to `EventTraceGuid` and
**EventHeader.EventDescriptor.Opcode** set based on the content of the synthetic
event. For example, the first event from each trace file will be a synthetic
event with Opcode 0 containing
[TRACE_LOGFILE_HEADER](/windows/win32/api/evntrace/ns-evntrace-trace_logfile_header)
information.

All the other events you receive contain provider-specific event data. You use
the **EventHeader.ProviderId** and **EventHeader.EventDescriptor** members of
[EVENT_RECORD](/windows/win32/api/evntcons/ns-evntcons-event_record) to
determine the type of event you received.

- If the event comes from a well-known provider and you know the layout of the
  data, you can use your own system for decoding the events.
- If the **EventHeader.Flags** field includes the
  `EVENT_HEADER_FLAG_TRACE_MESSAGE` flag, the event is a WPP message. If the
  appropriate decoding information (TMF or PDB file) is available, the event can
  be decoded using
  [TdhGetProperty](/windows/win32/api/tdh/nf-tdh-tdhgetproperty) or
  [TdhGetWppProperty](/windows/win32/api/tdh/nf-tdh-tdhgetwppproperty).
- Otherwise, the event may be a MOF-based, manifest-based, or TraceLogging
  event. If the appropriate decoding information is available, the event can be
  decoded using
  [TdhGetEventInformation](/windows/win32/api/tdh/nf-tdh-tdhgeteventinformation).
  - If the event uses MOF-based decoding, **TdhGetEventInformation** will look
    for event decoding information in the system's WMI data store.
  - If the event uses manifest-based decoding, **TdhGetEventInformation** will
    look for event decoding information in the system's registered manifests or
    in manifests or binaries loaded into the per-process decoding context by
    [TdhLoadManifest](/windows/win32/api/tdh/nf-tdh-tdhloadmanifest) or
    [TdhLoadManifestFromBinary](/windows/win32/api/tdh/nf-tdh-tdhloadmanifestfrombinary).
  - If the event uses TraceLogging-based decoding, **TdhGetEventInformation**
    will use decoding information from within the event.

In most cases, events will be delivered to your callback in the order in which
they occurred (timestamp order). However, in certain circumstances, the events
might not be delivered in their original order.

- If the trace is using system time for the session timestamp (i.e. the trace
  session was started with `properties.Wnode.ClientContext` set to 2) and the
  system clock is adjusted backwards while the session is collecting events,
  some of the events may be delivered out-of-order. To avoid this, set
  ClientContext to 0 to get the default timestamp (QPC time).
- If the trace is collected using timestamps from an imprecise clock then events
  with the same timestamp from different CPUs may be delivered out-of-order.
  This most frequently occurs when the trace uses system time for the session
  timestamp because system time ticks. This issue can be avoided by starting the
  session with `EVENT_TRACE_NO_PER_PROCESSOR_BUFFERING` in the
  [LogFileMode](/windows/win32/etw/logging-mode-constants) flags, though this
  can have a substantial negative impact on tracing performance. **Starting with
  Windows 10:** The system time clock type uses
  [GetSystemTimePreciseAsFileTime](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getsystemtimepreciseasfiletime)
  to reduce the likelihood of this issue.
- If the trace is corrupt, was generated using low-level APIs that do not
  maintain the expected timestamp rules within the file, or uses timestamp
  override options when writing events, some of the events may be delivered
  out-of-order.

> **Technical details:** Events are stored in buffers. Each buffer is assigned
> to a buffer stream, typically one stream for each CPU. The ProcessTrace
> implementation assumes that all events in a buffer are sorted by timestamp and
> that each buffer contains events for a single span of time that does not
> overlap the span of any other buffer in that buffer's stream. When these
> assumptions are not met,[ProcessTrace](nf-evntrace-processtrace.md)may deliver events out-of-order.

When a real-time trace collection session has no associated trace processing
sessions, collected events will be buffered by the system until the buffer is
full. When a trace processing session connects to a real-time trace collection
session, the trace processing session will receive the synthetic events for the
session, then the buffered events, and then it will begin receiving the
newly-generated real-time events. If a second real-time processing session
connects to the same trace collection session, it will receive the synthetic
events and the newly-generated real-time events (the second trace processing
session will not receive older events).

> [!Important]
> When processing events from a real-time session, if the
> processing callback takes too much time to process each event and events
> arrive too quickly, it will get behind. The system will buffer events to
> prevent data loss but this increases system resource usage (e.g. memory and
> disk usage). Avoid this problem by using session filters (e.g. level and
> keyword filters for each provider) to reduce the rate of incoming events,
> doing early filtering in your callback to skip events that don't need full
> processing, and optimizing your callback to return as quickly as possible to
> avoid blocking the processing thread.

For additional details on interpreting the event data, see
[Consuming Events](/windows/win32/etw/consuming-events) and
[Retrieving Event Data Using TDH](/windows/desktop/ETW/retrieving-event-data-using-tdh).

## -see-also

[BufferCallback](/windows/desktop/ETW/buffercallback)

[Consuming Events](/windows/win32/etw/consuming-events)

[Retrieving Event Data Using TDH](/windows/desktop/ETW/retrieving-event-data-using-tdh)

[EVENT_TRACE_LOGFILE](/windows/desktop/ETW/event-trace-logfile)

[OpenTrace](/windows/win32/api/evntrace/nf-evntrace-opentracea)

[ProcessTrace](/windows/desktop/ETW/processtrace)
