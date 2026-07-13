---
UID: NF:evntrace.TraceMessageVa
title: TraceMessageVa function (evntrace.h)
description:
  A RegisterTraceGuids-based ("Classic") event provider uses the TraceMessageVa
  function to send a message-based (TMF-based WPP) event to an event tracing
  session using va_list parameters.
helpviewer_keywords:
  [
    "PVOID",
    "TRACE_MESSAGE_GUID",
    "TRACE_MESSAGE_SEQUENCE",
    "TRACE_MESSAGE_SYSTEMINFO",
    "TRACE_MESSAGE_TIMESTAMP",
    "TraceMessageVa",
    "TraceMessageVa function [ETW]",
    "_evt_tracemessageva",
    "base.tracemessageva",
    "etw.tracemessageva",
    "evntrace/TraceMessageVa",
    "size_t",
  ]
old-location: etw\tracemessageva.htm
tech.root: ETW
ms.assetid: 2cfb7226-fd29-432e-abfd-bd10c6344a67
ms.date: 12/05/2018
ms.keywords:
  PVOID, TRACE_MESSAGE_GUID, TRACE_MESSAGE_SEQUENCE, TRACE_MESSAGE_SYSTEMINFO,
  TRACE_MESSAGE_TIMESTAMP, TraceMessageVa, TraceMessageVa function [ETW],
  _evt_tracemessageva, base.tracemessageva, etw.tracemessageva,
  evntrace/TraceMessageVa, size_t
req.header: evntrace.h
req.include-header:
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
  - TraceMessageVa
  - evntrace/TraceMessageVa
dev_langs:
  - c++
topic_type:
  - APIRef
  - kbSyntax
api_type:
  - DllExport
api_location:
  - Advapi32.dll
  - API-MS-Win-DownLevel-AdvApi32-l1-1-0.dll
  - KernelBase.dll
  - API-MS-Win-DownLevel-AdvApi32-l1-1-1.dll
  - API-MS-Win-eventing-classicprovider-l1-1-0.dll
api_name:
  - TraceMessageVa
---

# TraceMessageVa function

## -description

A
[RegisterTraceGuids](/windows/win32/api/evntrace/nf-evntrace-registertraceguidsa)-based
("Classic") event provider uses the **TraceMessageVa** function to send a
message-based (TMF-based WPP) event to an event tracing session using va_list
parameters.

## -parameters

### -param LoggerHandle [in]

Handle to the event tracing session that records the event. The provider obtains
the handle when it calls the
[GetTraceLoggerHandle](/windows/desktop/ETW/gettraceloggerhandle) function in
its [ControlCallback](/windows/desktop/ETW/controlcallback) implementation.

### -param MessageFlags [in]

Adds additional information to the beginning of the provider-specific data
section of the event. The provider-specific data section of the event will
contain data only for those flags that are set. The variable list of argument
data will follow this information. This parameter can be one or more of the
following values.

- **TRACE_MESSAGE_GUID**: Include the event trace class GUID in the message. The
  _MessageGuid_ parameter contains the event trace class GUID.

- **TRACE_MESSAGE_SEQUENCE**: Include a sequence number in the message. The
  sequence number starts at one. To use this flag, the controller must have set
  the **EVENT_TRACE_USE_GLOBAL_SEQUENCE** or **EVENT_TRACE_USE_LOCAL_SEQUENCE**
  log file mode when creating the session.

- **TRACE_MESSAGE_SYSTEMINFO**: Include the thread identifier and process
  identifier in the message.

- **TRACE_MESSAGE_TIMESTAMP**: Include a time stamp in the message.

The information is included in the event data in the following order:

- Sequence number
- Event trace class GUID
- Time stamp
- Thread identifier
- Process identifier

### -param MessageGuid [in]

Class GUID that identifies the event trace message.

### -param MessageNumber [in]

Number that uniquely identifies each occurrence of the message. You must define
the value specified for this parameter; the value should be meaningful to the
application.

### -param MessageArgList [in]

List of variable arguments to be appended to the message. The list must be
composed of pairs of arguments, as follows.

- **PVOID**: Pointer to the argument data.
- **size_t**: The size of the argument data, in bytes.

Terminate the list using an argument pair consisting of a pointer to **NULL**
and zero.

The caller must ensure that the sum of the sizes of the arguments + 72 does not
exceed the size of the event tracing session's buffer.

## -returns

If the function succeeds, the return value is ERROR_SUCCESS.

If the function fails, the return value is one of the
[system error codes](/windows/win32/debug/system-error-codes). The following
table includes some common errors and their causes.

- **ERROR_INVALID_HANDLE**

  Either the _LoggerHandle_ is **NULL** or specifies the NT Kernel Logger
  session handle.

- **ERROR_NOT_ENOUGH_MEMORY**

  The session ran out of free buffers to write to. This can occur during high
  event rates because the disk subsystem is overloaded or the number of buffers
  is too small. Rather than blocking until more buffers become available,
  [TraceMessage](/windows/desktop/ETW/tracemessage) discards the event.

  **Windows 2000 and Windows XP:** Not supported.

- **ERROR_OUTOFMEMORY**

  The event is discarded because, although the buffer pool has not reached its
  maximum size, there is insufficient available memory to allocate an additional
  buffer and there is no buffer available to receive the event.

- **ERROR_INVALID_PARAMETER**

  _MessageFlags_ contains a value that is not valid.

- **ERROR_MORE_DATA**

  Data from a single event cannot span multiple buffers. A trace event is
  limited to the size of the event tracing session's buffer minus the size of
  the [EVENT_TRACE_HEADER](/windows/desktop/ETW/event-trace-header) structure.

## -remarks

TMF-based WPP providers call this function.

> [!Note]
> Most developers will not call this function directly. WPP providers
> use wrapper functions generated by tracewpp.exe instead of calling ETW APIs.

If you do not need to access the message tracing functionality from a wrapper
function, you can call the [TraceMessage](/windows/desktop/ETW/tracemessage)
version of this function.

Consumers will have to use the
[EventCallback](/windows/desktop/ETW/eventcallback) callback to receive and
process the events if the _MessageFlags_ parameter does not contain the
TRACE_MESSAGE_GUID flag. If you do not specify the TRACE_MESSAGE_GUID flag, the
consumer will not be able to use the
[EventClassCallback](/windows/desktop/ETW/eventclasscallback) because the
**Header.Guid** member of the [EVENT_TRACE](/windows/desktop/ETW/event-trace)
structure will not contain the event trace class GUID.

Note that the members of the [EVENT_TRACE](/windows/desktop/ETW/event-trace) and
[EVENT_TRACE_HEADER](/windows/desktop/ETW/event-trace-header) structures that
correspond to the _MessageFlags_ flags are set only if the corresponding flag is
specified. For example, the **ThreadId** and **ProcessId** members of
**EVENT_TRACE_HEADER** are populated only if you specify the
TRACE_MESSAGE_SYSTEMINFO flag.

## -see-also

[TraceEvent](/windows/desktop/ETW/traceevent)

[TraceEventInstance](/windows/desktop/ETW/traceeventinstance)

[TraceMessage](/windows/desktop/ETW/tracemessage)
