---
UID: NF:evntprov.EventWrite
title: EventWrite function (evntprov.h)
description: Writes an ETW event that uses the current thread's activity ID.
helpviewer_keywords:
  [
    "EventWrite",
    "EventWrite function [ETW]",
    "base.eventwrite_func",
    "etw.eventwrite_func",
    "evntprov/EventWrite",
  ]
old-location: etw\eventwrite_func.htm
tech.root: ETW
ms.assetid: 93070eb7-c167-4419-abff-e861877dad07
ms.date: 12/05/2018
ms.keywords:
  EventWrite, EventWrite function [ETW], base.eventwrite_func,
  etw.eventwrite_func, evntprov/EventWrite
req.header: evntprov.h
req.include-header:
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps \| UWP apps]
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
  - EventWrite
  - evntprov/EventWrite
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
  - API-MS-Win-eventing-provider-l1-1-0.dll
  - API-MS-Win-Eventing-Provider-L1-1-1.dll
  - bcrypt.dll
api_name:
  - EventWrite
---

# EventWrite function

## -description

Writes an ETW event that uses the current thread's activity ID.

## -parameters

### -param RegHandle [in]

Registration handle of the provider. The handle comes from
[EventRegister](/windows/desktop/api/evntprov/nf-evntprov-eventregister). The
generated event will use the ProviderId associated with the handle.

### -param EventDescriptor [in]

[EVENT_DESCRIPTOR](/windows/desktop/api/evntprov/ns-evntprov-event_descriptor)
with event information (metadata) including ID, Version, Level, Keyword,
Channel, Opcode, and Task.

> [!Important]
> ProviderId, Level and Keyword are the primary means for
> filtering events. Other kinds of filtering are possible but have much higher
> overhead. Always assign a nonzero level and keyword to every event.

### -param UserDataCount [in]

Number of
[EVENT_DATA_DESCRIPTOR](/windows/desktop/api/evntprov/ns-evntprov-event_data_descriptor)
structures in _UserData_. The maximum number is 128.

### -param UserData [in, optional]

An array of _UserDataCount_
[EVENT_DATA_DESCRIPTOR](/windows/desktop/api/evntprov/ns-evntprov-event_data_descriptor)
structures that describe the data to be included in the event. _UserData_ may be
**NULL** if _UserDataCount_ is zero.

Each **EVENT_DATA_DESCRIPTOR** describes one block of memory to be included in
the event. The specified blocks will be concatenated in order with no padding or
alignment to form the event content. If using manifest-based decoding, the event
content must match the layout specified in the template associated with the
event in the manifest.

## -returns

Returns **ERROR_SUCCESS** if successful or an error code. Possible error codes
include the following:

- **ERROR_INVALID_PARAMETER**: One or more of the parameters is not valid.
- **ERROR_INVALID_HANDLE**: The registration handle of the provider is not
  valid.
- **ERROR_ARITHMETIC_OVERFLOW**: The event size is larger than the allowed
  maximum (64KB - header).
- **ERROR_MORE_DATA**: The session buffer size is too small for the event.
- **ERROR_NOT_ENOUGH_MEMORY**: Occurs when filled buffers are trying to flush to
  disk, but disk IOs are not happening fast enough. This happens when the disk
  is slow and event traffic is heavy. Eventually, there are no more free (empty)
  buffers and the event is dropped.
- **STATUS_LOG_FILE_FULL**: The real-time playback file is full. Events are not
  logged to the session until a real-time consumer consumes the events from the
  playback file.

The error code is primarily intended for use in debugging and diagnostic
scenarios. Most production code should continue to run and continue to report
events even if an ETW event could not be written, so release builds should
usually ignore the error code.

## -remarks

Most event providers will not call **EventWrite** directly. Instead, most event
providers are implemented using an ETW framework that wraps the calls to
**EventRegister**, **EventWrite**, and **EventUnregister**. For example, you
might
[write an event manifest](/windows/win32/etw/writing-manifest-based-events) and
then use the [Message Compiler](/windows/win32/wes/message-compiler--mc-exe-) to
generate C/C++ code for the events, or you might use
[TraceLogging](/windows/win32/tracelogging/trace-logging-portal) to avoid the
need for a manifest.

**EventWrite** will route the event to the appropriate trace sessions based on
the ProviderId (determined from the _RegHandle_), Level, Keyword, and other
event characteristics. If no trace sessions are recording this event, this
function will do nothing and return **ERROR_SUCCESS**.

To reduce the performance impact of events that are not recorded by any trace
session, you can call
[EventEnabled](/windows/win32/api/evntprov/nf-evntprov-eventenabled) to
determine whether any trace session is recording your event before preparing the
data and calling **EventWrite**.

**EventWrite** sets the event's activity ID to the current thread's activity ID.
**EventWrite** does not include a related activity ID in the event. To specify a
different activity ID or to add a related activity ID, use
[EventWriteTransfer](/windows/win32/api/evntprov/nf-evntprov-eventwritetransfer).

**EventWrite** is equivalent to
[EventWriteEx](/windows/win32/api/evntprov/nf-evntprov-eventwriteex) with 0 for
_Filter_, 0 for _Flags_, **NULL** for _ActivityId_, and **NULL** for
_RelatedActivityId_.

## -see-also

[EventActivityIdControl](/windows/desktop/api/evntprov/nf-evntprov-eventactivityidcontrol)

[EventRegister](/windows/desktop/api/evntprov/nf-evntprov-eventregister)

[EventWriteTransfer](/windows/desktop/api/evntprov/nf-evntprov-eventwritetransfer)

[EventWriteEx](/windows/win32/api/evntprov/nf-evntprov-eventwriteex)

[Writing Manifest-based Events](/windows/desktop/ETW/writing-manifest-based-events).
