---
UID: NF:evntrace.ProcessTrace
title: ProcessTrace function (evntrace.h)
description:
  Delivers events from one or more trace processing sessions to the consumer.
helpviewer_keywords:
  [
    "ProcessTrace",
    "ProcessTrace function [ETW]",
    "_evt_processtrace",
    "base.processtrace",
    "etw.processtrace",
    "evntrace/ProcessTrace",
  ]
old-location: etw\processtrace.htm
tech.root: ETW
ms.assetid: aea25a95-f435-4068-9b15-7473f31ebf16
ms.date: 12/05/2018
ms.keywords:
  ProcessTrace, ProcessTrace function [ETW], _evt_processtrace,
  base.processtrace, etw.processtrace, evntrace/ProcessTrace
req.header: evntrace.h
req.include-header:
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps]
req.kmdf-ver:
req.umdf-ver:
req.ddi-compliance:
req.unicode-ansi:
req.idl:
req.max-support:
req.namespace:
req.assembly:
req.type-library:
req.lib: AdvAPI32.Lib
  Sechost.lib on Windows 8.1 and Windows Server 2012 R2; Advapi32.lib on
  Windows 8, Windows Server 2012, Windows 7, Windows Server 2008 R2, Windows
  Server 2008, Windows Vista and Windows XP
req.dll:
  Sechost.dll on Windows 8.1 and Windows Server 2012 R2; Advapi32.dll on
  Windows 8, Windows Server 2012, Windows 7, Windows Server 2008 R2, Windows
  Server 2008, Windows Vista and Windows XP
req.irql:
targetos: Windows
req.typenames:
req.redist:
ms.custom: 19H1
f1_keywords:
  - ProcessTrace
  - evntrace/ProcessTrace
dev_langs:
  - c++
topic_type:
  - APIRef
  - kbSyntax
api_type:
  - DllExport
api_location:
 - api-ms-win-eventing-consumer-l1-1-2.dll
 - api-ms-win-eventing-consumer-l1-1-1.dll
 - api-ms-win-downlevel-advapi32-l2-1-0.dll
 - Sechost.dll
 - Advapi32.dll
 - API-MS-Win-DownLevel-AdvAPI32-l2-1-1.dll
 - API-MS-Win-Eventing-Consumer-l1-1-0.dll
 - KernelBase.dll
api_name:
  - ProcessTrace
---

# ProcessTrace function

## -description

The **ProcessTrace** function delivers events from one or more ETW trace
processing sessions to the consumer.

## -parameters

### -param HandleArray [in]

Pointer to an array of trace processing session handles obtained from earlier
calls to the [OpenTrace](/windows/win32/api/evntrace/nf-evntrace-opentracea)
function.

The array can contain up to 64 handles to file processing sessions or it can
contain one handle to a real-time processing session. The array cannot contain
both file processing session handles and real-time processing session handles.

### -param HandleCount [in]

Number of elements in _HandleArray_.

### -param StartTime [in]

Pointer to an optional
[FILETIME](/windows/win32/api/minwinbase/ns-minwinbase-filetime) structure that
specifies the beginning time period for which you want to receive events. The
function does not deliver events with timestamps prior to _StartTime_.

### -param EndTime [in]

Pointer to an optional
[FILETIME](/windows/win32/api/minwinbase/ns-minwinbase-filetime) structure that
specifies the ending time period for which you want to receive events. The
function does not deliver events with timestamps after _EndTime_.

**Windows Server 2003:** This value is ignored for real-time event delivery.

## -returns

If the function succeeds, the return value is ERROR_SUCCESS.

If the function fails, the return value is one of the
[system error codes](/windows/win32/debug/system-error-codes). The following are
some common errors and their causes.

- **ERROR_BAD_LENGTH**

  _HandleCount_ is not valid or the number of handles is greater than 64.

- **ERROR_INVALID_HANDLE**

  An element of _HandleArray_ is not a valid event tracing session handle.

- **ERROR_INVALID_TIME**

  _EndTime_ is less than _StartTime_.

- **ERROR_INVALID_PARAMETER**

  _HandleArray_ is **NULL**, contains both file processing sessions and
  real-time processing sessions, or contains more than one real-time processing
  session.

- **ERROR_NOACCESS**

  An exception occurred in one of the callback functions that receives the
  events.

- **ERROR_CANCELLED**

  Indicates the consumer canceled processing by returning **FALSE** in their
  [BufferCallback](/windows/win32/api/evntrace/nc-evntrace-pevent_trace_buffer_callbacka)
  function.

- **ERROR_WMI_INSTANCE_NOT_FOUND**

  The trace collection session from which you are trying to consume events in
  real time is not running or does not have the real-time trace mode enabled.

## -remarks

Trace consumers call this function to process the events from one or more trace
processing sessions. This function blocks until processing ends.

Before calling **ProcessTrace**, use
[OpenTrace](/windows/win32/api/evntrace/nf-evntrace-opentracea) to open handles
to trace processing sessions.

The **ProcessTrace** function delivers the events from the sessions by invoking
the consumer's
[BufferCallback](/windows/win32/api/evntrace/nc-evntrace-pevent_trace_buffer_callbacka),
[EventCallback](/windows/win32/api/evntrace/nc-evntrace-pevent_callback), and
[EventRecordCallback](/windows/win32/api/evntrace/nc-evntrace-pevent_record_callback)
callback functions.

The **ProcessTrace** function attempts to deliver events in order based on the
event's timestamp (i.e. it tries to deliver events oldest to newest). In certain
cases, **ProcessTrace** might deliver events out of order.

- If the clock used for the event timestamps is adjusted backwards during trace
  collection, the delivery order of the events is unpredictable. To avoid this
  issue, [use the QPC clock](/windows/win32/etw/wnode-header) instead of the
  system time clock when collecting the trace.
- If multiple events are collected with the same timestamp on different CPUs,
  the delivery order of the events is unpredictable.
- If an event has an invalid timestamp (e.g. due to file corruption), the
  delivery order of that event and other events in the trace may be
  unpredictable.

The **ProcessTrace** function blocks the thread until it delivers all events,
the
[BufferCallback](/windows/win32/api/evntrace/nc-evntrace-pevent_trace_buffer_callbacka)
function returns **FALSE**, or you call
[CloseTrace](/windows/win32/api/evntrace/nf-evntrace-closetrace). In addition,
if the consumer is consuming events in real time, the **ProcessTrace** function
returns after the controller stops the trace session. (Note that there may be a
delay of several seconds before the function returns.)

**Windows Server 2003:** You can call
[CloseTrace](/windows/win32/api/evntrace/nf-evntrace-closetrace) only after
**ProcessTrace** returns.

### Examples

For an example that uses **ProcessTrace**, see
[Using TdhFormatProperty to Consume Event Data](/windows/win32/etw/using-tdhformatproperty-to-consume-event-data).

## -see-also

[BufferCallback](/windows/win32/api/evntrace/nc-evntrace-pevent_trace_buffer_callbacka)

[EventCallback](/windows/win32/api/evntrace/nc-evntrace-pevent_callback)

[EventRecordCallback](/windows/win32/api/evntrace/nc-evntrace-pevent_record_callback)

[OpenTrace](/windows/win32/api/evntrace/nf-evntrace-opentracea)
