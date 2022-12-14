---
UID: NF:evntrace.TraceEventInstance
title: TraceEventInstance function (evntrace.h)
description:
  A RegisterTraceGuids-based ("Classic") event provider uses the
  TraceEventInstance function to send a structured event to an event tracing
  session with an instance identifier.
helpviewer_keywords:
  [
    "TraceEventInstance",
    "TraceEventInstance function [ETW]",
    "_evt_traceeventinstance",
    "base.traceeventinstance",
    "etw.traceeventinstance",
    "evntrace/TraceEventInstance",
  ]
old-location: etw\traceeventinstance.htm
tech.root: ETW
ms.assetid: e8361bdc-21dd-47a0-bdbf-56f4d6195689
ms.date: 12/05/2018
ms.keywords:
  TraceEventInstance, TraceEventInstance function [ETW],
  _evt_traceeventinstance, base.traceeventinstance, etw.traceeventinstance,
  evntrace/TraceEventInstance
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
req.lib: Advapi32.lib
req.dll: Advapi32.dll
req.irql:
targetos: Windows
req.typenames:
req.redist:
ms.custom: 19H1
f1_keywords:
  - TraceEventInstance
  - evntrace/TraceEventInstance
dev_langs:
  - c++
topic_type:
  - APIRef
  - kbSyntax
api_type:
  - DllExport
api_location:
  - Advapi32.dll
api_name:
  - TraceEventInstance
---

# TraceEventInstance function

## -description

A
[RegisterTraceGuids](/windows/win32/api/evntrace/nf-evntrace-registertraceguidsa)-based
("Classic") event provider uses the **TraceEventInstance** function to send a
structured event to an event tracing session with an instance identifier.

The event uses an instance identifier to associate the event with a transaction.
This function may also be used to trace hierarchical relationships between
related events.

## -parameters

### -param TraceHandle [in]

Handle to the event tracing session that records the event instance. The
provider obtains the handle when it calls the
[GetTraceLoggerHandle](/windows/desktop/ETW/gettraceloggerhandle) function in
its [ControlCallback](/windows/desktop/ETW/controlcallback) implementation.

### -param EventTrace [in]

Pointer to an
[EVENT_INSTANCE_HEADER](/windows/desktop/ETW/event-instance-header) structure.
Event-specific data is optionally appended to the structure. The largest event
you can log is 64K. You must specify values for the following members of the
**EVENT_INSTANCE_HEADER** structure.

- **Size**
- **Flags**
- **RegHandle**

Depending on the complexity of the information your provider provides, you
should also consider specifying values for the following members.

- **Class.Type**
- **Class.Level**

To trace hierarchical relationships between related events, also set the
**ParentRegHandle** member.

### -param InstInfo [in]

Pointer to an [EVENT_INSTANCE_INFO](/windows/desktop/ETW/event-instance-info)
structure, which contains the registration handle for this event trace class and
the instance identifier. Use the
[CreateTraceInstanceId](/windows/desktop/ETW/createtraceinstanceid) function to
initialize the structure.

### -param ParentInstInfo [in]

Pointer to an [EVENT_INSTANCE_INFO](/windows/desktop/ETW/event-instance-info)
structure, which contains the registration handle for the parent event trace
class and its instance identifier. Use the
[CreateTraceInstanceId](/windows/desktop/ETW/createtraceinstanceid) function to
initialize the structure. Set to **NULL** if you are not tracing a hierarchical
relationship.

## -returns

If the function succeeds, the return value is ERROR_SUCCESS.

If the function fails, the return value is one of the
[system error codes](/windows/win32/debug/system-error-codes). The following
are some common errors and their causes.

- **ERROR_INVALID_FLAGS**

  The **Flags** member of the
  [EVENT_INSTANCE_HEADER](/windows/desktop/ETW/event-instance-header) does not
  contain **WNODE_FLAG_TRACED_GUID**.

- **ERROR_OUTOFMEMORY**

  There was insufficient memory to complete the function call. The causes for
  this error code are described in the following Remarks section.

- **ERROR_INVALID_PARAMETER**

  One of the following is true:

  - _EventTrace_ is **NULL**.
  - _pInstInfo_ is **NULL**.
  - The members of _pInstInfo_ are **NULL**.
  - _TraceHandle_ is **NULL**.
  - The **Size** member of the
    [EVENT_INSTANCE_HEADER](/windows/desktop/ETW/event-instance-header) is
    incorrect.

- **ERROR_INVALID_HANDLE**

  _TraceHandle_ is not valid or specifies the NT Kernel Logger session handle.

- **ERROR_NOT_ENOUGH_MEMORY**

  The session ran out of free buffers to write to. This can occur during high
  event rates because the disk subsystem is overloaded or the number of buffers
  is too small. Rather than blocking until more buffers become available,
  [TraceEvent](/windows/desktop/ETW/traceevent) discards the event.

  **Windows 2000 and Windows XP:** Not supported.

- **ERROR_OUTOFMEMORY**

  The event is discarded because, although the buffer pool has not reached its
  maximum size, there is insufficient available memory to allocate an additional
  buffer and there is no buffer available to receive the event.

- **ERROR_MORE_DATA**

  Data from a single event cannot span multiple buffers. A trace event is
  limited to the size of the event tracing session's buffer minus the size of
  the [EVENT_INSTANCE_HEADER](/windows/desktop/ETW/event-instance-header)
  structure.

## -remarks

MOF-based ETW providers call this function.

> [!Note]
> Most developers will not call this function. This API supports
> MOF-based ETW, but MOF-based ETW is deprecated in favor of manifest-based ETW.
> In addition, most MOF-based providers use wrapper functions generated by
> MC.exe instead of directly calling ETW APIs.

Before the provider can call this function, the provider

- Must call the
  [RegisterTraceGuids](/windows/win32/api/evntrace/nf-evntrace-registertraceguidsa)
  function to register itself and the event trace class.
- Must call the
  [CreateTraceInstanceId](/windows/desktop/ETW/createtraceinstanceid) function
  to create an instance identifier for the registered event trace class.
- Must be enabled. A controller calls the
  [EnableTrace](/windows/desktop/ETW/enabletrace) function to enable a provider.

The event is either written to a log file, sent to event trace consumers in real
time, or both. The **LogFileMode** member of the
[EVENT_TRACE_PROPERTIES](/windows/desktop/ETW/event-trace-properties) structure
passed to the [StartTrace](/windows/desktop/ETW/starttrace) defines where the
event is sent.

The trace events are written in the order in which they occur.

To trace unrelated events, use the [TraceEvent](/windows/desktop/ETW/traceevent)
function.

**Windows XP:** Does not work correctly.

### Examples

For an example of generating related sets of events using
[CreateTraceInstanceId](/windows/desktop/ETW/createtraceinstanceid) and
**TraceEventInstance**, see
[Tracing Event Instances](/windows/desktop/ETW/tracing-event-instances).

## -see-also

[CreateTraceInstanceId](/windows/desktop/ETW/createtraceinstanceid)

[EVENT_INSTANCE_HEADER](/windows/desktop/ETW/event-instance-header)

[EVENT_INSTANCE_INFO](/windows/desktop/ETW/event-instance-info)

[RegisterTraceGuids](/windows/win32/api/evntrace/nf-evntrace-registertraceguidsa)

[TraceEvent](/windows/desktop/ETW/traceevent)
