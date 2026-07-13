---
UID: NF:evntprov.EventWriteEx
title: EventWriteEx function (evntprov.h)
description:
  Writes an ETW event with an activity ID, an optional related activity ID,
  session filters, and special options.
helpviewer_keywords:
  [
    "EventWriteEx",
    "EventWriteEx function [ETW]",
    "etw.eventwriteex",
    "evntprov/EventWriteEx",
  ]
old-location: etw\eventwriteex.htm
tech.root: ETW
ms.assetid: 00b907cb-45cd-48c7-bea4-4d8a39b4fa24
ms.date: 12/05/2018
ms.keywords:
  EventWriteEx, EventWriteEx function [ETW], etw.eventwriteex,
  evntprov/EventWriteEx
req.header: evntprov.h
req.include-header:
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps \| UWP apps]
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
  - EventWriteEx
  - evntprov/EventWriteEx
dev_langs:
  - c++
topic_type:
  - APIRef
  - kbSyntax
api_type:
  - DllExport
api_location:
 - api-ms-win-downlevel-advapi32-l1-1-0.dll
 - Advapi32.dll
 - API-MS-Win-DownLevel-AdvApi32-l1-1-1.dll
 - KernelBase.dll
 - API-MS-Win-eventing-provider-l1-1-0.dll
 - API-MS-Win-Eventing-Provider-L1-1-1.dll
api_name:
  - EventWriteEx
---

# EventWriteEx function

## -description

Writes an ETW event with an activity ID, an optional related activity ID,
session filters, and special options.

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

### -param Filter [in]

A 64-bit bitmask value. Each set bit indicates that this event should be
excluded from a particular trace session.

The _Filter_ parameter is used with event providers that perform custom event
filtering based on the _FilterData_ from
[EnableCallback](/windows/desktop/api/evntprov/nc-evntprov-penablecallback).

Set _Filter_ to zero if you do not support custom event filters or if the event
should be written to all trace sessions. Otherwise, set _Filter_ to the
bitwise-OR of the identifiers of sessions that should NOT receive the event.

### -param Flags [in]

Set _Flags_ to zero for normal event handling.

Set _Flags_ to a combination of **EVENT_WRITE_FLAG** values for special event
handling.

- **EVENT_WRITE_FLAG_INPRIVATE** (0x2)

  Indicates that this event should be excluded from any logger that has set the
  **EVENT_ENABLE_PROPERTY_EXCLUDE_INPRIVATE** option.

### -param ActivityId [in, optional]

An optional pointer to a 128-bit activity ID for this event. If this is
non-NULL, **EventWriteEx** will use the specified value for the event's activity
ID. If this is NULL, **EventWriteEx** will use the current thread's activity ID.

Trace processing tools can use the event's activity ID to organize events into
groups called activities. For additional information about the activity ID, see
[EventActivityIdControl](/windows/desktop/api/evntprov/nf-evntprov-eventactivityidcontrol).

### -param RelatedActivityId [in, optional]

An optional pointer to a 128-bit activity ID that is the parent of this event's
activity. If this is non-NULL, **EventWriteEx** will use the specified value for
the event's related activity ID. If this is NULL, the event will not have a
related activity ID. The related activity ID is usually set on the activity's
START event (the first event of the activity, logged with Opcode = START).

Trace processing tools can use the event's related activity ID to determine the
relationship between activities, e.g. the related activity is the parent of the
newly-started activity. For additional information about the related activity
ID, see
[EventActivityIdControl](/windows/desktop/api/evntprov/nf-evntprov-eventactivityidcontrol).

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

Most event providers will not call **EventWriteEx** directly. Instead, most
event providers are implemented using an ETW framework that wraps the calls to
**EventRegister**, **EventWriteEx**, and **EventUnregister**. For example, you
might
[write an event manifest](/windows/win32/etw/writing-manifest-based-events) and
then use the [Message Compiler](/windows/win32/wes/message-compiler--mc-exe-) to
generate C/C++ code for the events, or you might use
[TraceLogging](/windows/win32/tracelogging/trace-logging-portal) to avoid the
need for a manifest.

**EventWriteEx** will route the event to the appropriate trace sessions based on
the ProviderId (determined from the _RegHandle_), Level, Keyword, and other
event characteristics. If no trace sessions are recording this event, this
function will do nothing and return **ERROR_SUCCESS**.

To reduce the performance impact of events that are not recorded by any trace
session, you can call
[EventEnabled](/windows/win32/api/evntprov/nf-evntprov-eventenabled) to
determine whether any trace session is recording your event before preparing the
data and calling **EventWriteEx**.

A provider can define filters that a session uses to filter events based on
event data. The core filters are based on level and keywords. Event providers
can support more-complex filters. The event provider can receive filter
information from the _FilterData_ parameter of
[EnableCallback](/windows/desktop/api/evntprov/nc-evntprov-penablecallback). The
provider can evaluate the filter and use the _Filter_ parameter of
**EventWriteEx** to indicate that certain trace sessions did not pass the filter
and should therefore not receive the event.

## -see-also

[EventActivityIdControl](/windows/desktop/api/evntprov/nf-evntprov-eventactivityidcontrol)

[EventRegister](/windows/desktop/api/evntprov/nf-evntprov-eventregister)

[EventWrite](/windows/desktop/api/evntprov/nf-evntprov-eventwrite)

[EventWriteTransfer](/windows/desktop/api/evntprov/nf-evntprov-eventwritetransfer)

[Writing Manifest-based Events](/windows/desktop/ETW/writing-manifest-based-events).
