---
UID: NS:evntrace._EVENT_TRACE_LOGFILEW
title: EVENT_TRACE_LOGFILEW (evntrace.h)
description: The EVENT_TRACE_LOGFILEW (Unicode) structure (evntrace.h) stores information about a trace data source.
helpviewer_keywords:
  [
    "*PEVENT_TRACE_LOGFILEW",
    "EVENT_TRACE_LOGFILE",
    "EVENT_TRACE_LOGFILE structure [ETW]",
    "EVENT_TRACE_LOGFILEA",
    "EVENT_TRACE_LOGFILEW",
    "PEVENT_TRACE_LOGFILE",
    "PEVENT_TRACE_LOGFILE structure pointer [ETW]",
    "PROCESS_TRACE_MODE_EVENT_RECORD",
    "PROCESS_TRACE_MODE_RAW_TIMESTAMP",
    "PROCESS_TRACE_MODE_REAL_TIME",
    "_EVENT_TRACE_LOGFILEA",
    "_EVENT_TRACE_LOGFILEW",
    "_evt_event_trace_logfile",
    "base.event_trace_logfile",
    "etw.event_trace_logfile",
    "evntrace/EVENT_TRACE_LOGFILE",
    "evntrace/EVENT_TRACE_LOGFILEA",
    "evntrace/EVENT_TRACE_LOGFILEW",
    "evntrace/PEVENT_TRACE_LOGFILE",
  ]
old-location: etw\event_trace_logfile.htm
tech.root: ETW
ms.assetid: 179451e9-7e3c-4d3a-bcc6-3ad9d382229a
ms.date: 08/04/2022
ms.keywords:
  "*PEVENT_TRACE_LOGFILEW, EVENT_TRACE_LOGFILE, EVENT_TRACE_LOGFILE structure
  [ETW], EVENT_TRACE_LOGFILEA, EVENT_TRACE_LOGFILEW, PEVENT_TRACE_LOGFILE,
  PEVENT_TRACE_LOGFILE structure pointer [ETW], PROCESS_TRACE_MODE_EVENT_RECORD,
  PROCESS_TRACE_MODE_RAW_TIMESTAMP, PROCESS_TRACE_MODE_REAL_TIME,
  _EVENT_TRACE_LOGFILEA, _EVENT_TRACE_LOGFILEW, _evt_event_trace_logfile,
  base.event_trace_logfile, etw.event_trace_logfile,
  evntrace/EVENT_TRACE_LOGFILE, evntrace/EVENT_TRACE_LOGFILEA,
  evntrace/EVENT_TRACE_LOGFILEW, evntrace/PEVENT_TRACE_LOGFILE"
req.header: evntrace.h
req.include-header:
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver:
req.umdf-ver:
req.ddi-compliance:
req.unicode-ansi: EVENT_TRACE_LOGFILEW (Unicode) and EVENT_TRACE_LOGFILEA (ANSI)
req.idl:
req.max-support:
req.namespace:
req.assembly:
req.type-library:
req.lib:
req.dll:
req.irql:
targetos: Windows
req.typenames: EVENT_TRACE_LOGFILEW, *PEVENT_TRACE_LOGFILEW
req.redist:
ms.custom: 19H1
f1_keywords:
  - _EVENT_TRACE_LOGFILEW
  - evntrace/_EVENT_TRACE_LOGFILEW
  - PEVENT_TRACE_LOGFILEW
  - evntrace/PEVENT_TRACE_LOGFILEW
  - EVENT_TRACE_LOGFILEW
  - evntrace/EVENT_TRACE_LOGFILEW
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
  - EVENT_TRACE_LOGFILE
  - EVENT_TRACE_LOGFILEA
  - EVENT_TRACE_LOGFILEW
---

# EVENT_TRACE_LOGFILEW structure

## -description

The **EVENT_TRACE_LOGFILE** structure stores information about a trace data
source.

The **EVENT_TRACE_LOGFILE** structure is used when calling
[OpenTrace](/windows/win32/api/evntrace/nf-evntrace-opentracew). The user
provides an **EVENT_TRACE_LOGFILE** structure with information about the trace
data source (either the name of an ETL file or the name of an active real-time
logger session), trace processing flags, and the callback functions that will
receive trace data. On success, **OpenTrace** fills in the remaining fields of
the structure to return details about the trace data source.

When [ProcessTrace](/windows/win32/api/evntrace/nf-evntrace-processtrace)
processes a buffer, it invokes the user-defined **BufferCallback** with a
**EVENT_TRACE_LOGFILE** structure to provide information about the event
processing session and the buffer.

## -struct-fields

### -field LogFileName

Name of the log file being processed, or **NULL** if processing data from a
real-time tracing session. Specify a value for this member if you are calling
**OpenTrace** to consume data from a log file.

When calling **OpenTrace**, if _LoggerName_ is non-**NULL** then _LogFileName_
must be **NULL**.

When calling **OpenTrace**, the user consuming the events must have permissions
to read the file.

> [!Note]
> The filename provided to OpenTrace via the _LogFileName_ field must be
> the full file name, including any suffixes. Some trace file creation APIs can
> silently add a suffix to the user-specified filename. For example, if the
> controller logged events to a private session (the controller set the
> **LogFileMode** member of
> [EVENT_TRACE_PROPERTIES](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties)
> to **EVENT_TRACE_PRIVATE_LOGGER_MODE** when calling **StartTrace**), the
> generated ETL file will include a process ID suffix, e.g. `mytrace.etl_123`.
> This can also occur if the file was created using the
> **EVENT_TRACE_FILE_MODE_NEWFILE** mode, in which case the generated ETL file
> will include a sequence number.

### -field LoggerName

Name of the real-time event tracing session, or **NULL** if processing data from
a log file. Specify a value for this member if you are calling **OpenTrace** to
consume data from a real-time session.

When calling **OpenTrace**, if _LogFileName_ is non-**NULL** then _LoggerName_
must be **NULL**.

You can only consume events in real time if the trace controller has set the
**LogFileMode** member of
[EVENT_TRACE_PROPERTIES](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties)
to include the **EVENT_TRACE_REAL_TIME_MODE** flag.

Only users with administrative privileges, users in the Performance Log Users
group, and applications running as LocalSystem, LocalService, NetworkService can
consume events in real time. To grant a restricted user the ability to consume
events in real time, add them to the Performance Log Users group or call
[EventAccessControl](/windows/desktop/api/evntcons/nf-evntcons-eventaccesscontrol).

**Windows XP and Windows 2000:** Anyone can consume real time events.

### -field CurrentTime

On output, the current time, in 100-nanosecond intervals since midnight, January
1, 1601.

### -field BuffersRead

On output, the number of buffers processed.

### -field DUMMYUNIONNAME

### -field DUMMYUNIONNAME.LogFileMode

Reserved. Do not use.

### -field DUMMYUNIONNAME.ProcessTraceMode

Modes for processing events. The modes are defined in the `evntcons.h` header
file. You can specify one or more of the following modes:

- **PROCESS_TRACE_MODE_EVENT_RECORD**

  Specify this mode if you want to receive events in the new
  [EVENT_RECORD](/windows/desktop/api/evntcons/ns-evntcons-event_record) format
  (strongly recommended). To receive events in the new format you must specify a
  callback in the **EventRecordCallback** member. If you do not specify this
  mode, you will receive events in the old format through the callback specified
  in the **EventCallback** member.

  **Prior to Windows Vista:** Not supported.

- **PROCESS_TRACE_MODE_RAW_TIMESTAMP**

  By default, **ProcessTrace** converts the event's **TimeStamp** from the
  original raw format (system time, QPC time, or CPU cycle counter) into system
  time (100-nanosecond intervals since midnight, January 1, 1601).

  Specify the **PROCESS_TRACE_MODE_RAW_TIMESTAMP** flag if you do not want the
  time stamp value in the **TimeStamp** member of
  [EVENT_HEADER](/windows/desktop/api/evntcons/ns-evntcons-event_header) and
  [EVENT_TRACE_HEADER](/windows/win32/api/evntrace/ns-evntrace-event_trace_header)
  converted to system time. If this flag is specified, **ProcessTrace** will
  leave the time stamp value in the original format that the controller
  specified in the **Wnode.ClientContext** member of
  [EVENT_TRACE_PROPERTIES](/windows/win32/api/evntrace/ns-evntrace-event_trace_properties).

  **Prior to Windows Vista:** Not supported.

- **PROCESS_TRACE_MODE_REAL_TIME**

  Specify this mode to receive events in real time. You must specify this mode
  if **LoggerName** is not **NULL**.

### -field CurrentEvent

On output, an [EVENT_TRACE](/windows/win32/api/evntrace/ns-evntrace-event_trace)
structure that contains the last event processed.

### -field LogfileHeader

On output, a
[TRACE_LOGFILE_HEADER](/windows/win32/api/evntrace/ns-evntrace-trace_logfile_header)
structure that contains general information about the session and the computer
on which the session ran.

### -field BufferCallback

Pointer to the
[BufferCallback](/windows/win32/api/evntrace/nc-evntrace-pevent_trace_buffer_callbackw)
function that receives buffer-related statistics for each buffer ETW flushes.
ETW calls this callback after it delivers all the events in the buffer. This
callback is optional.

### -field BufferSize

On output, contains the size of each buffer, in bytes.

### -field Filled

On output, contains the number of bytes in the buffer that contain valid
information.

### -field EventsLost

Not used.

### -field DUMMYUNIONNAME2

### -field DUMMYUNIONNAME2.EventCallback

Pointer to the
[EventCallback](/windows/win32/api/evntrace/nc-evntrace-pevent_callback)
function that ETW calls for each event in the buffer. This field is used only if
the _ProcessTraceMode_ field does not include the
`PROCESS_TRACE_MODE_EVENT_RECORD` flag.

> [!Note]
> The _EventCallback_ field will treated as an **EventRecordCallback**
> if the _ProcessTraceMode_ field includes the `PROCESS_TRACE_MODE_EVENT_RECORD`
> flag. If your _EventCallback_ is receiving garbled data from **ProcessTrace**,
> verify that the _ProcessTraceMode_ field does not include the
> `PROCESS_TRACE_MODE_EVENT_RECORD` flag.

> [!Tip]
> New code should use _EventRecordCallback_ instead of _EventCallback_.
> The _EventRecordCallback_ receives an **EVENT_RECORD** which contains more
> complete event information, can be used with decoding APIs such as
> [TdhGetEventInformation](/windows/win32/api/tdh/nf-tdh-tdhgeteventinformation),
> and has a context pointer that can be used by your callback.

### -field DUMMYUNIONNAME2.EventRecordCallback

Pointer to the
[EventRecordCallback](/windows/win32/api/evntrace/nc-evntrace-pevent_record_callback)
function that ETW calls for each event in the buffer. This field is used only if
the _ProcessTraceMode_ field includes the `PROCESS_TRACE_MODE_EVENT_RECORD`
flag.

> [!Note]
> The _EventRecordCallback_ field will treated as an **EventCallback**
> if the _ProcessTraceMode_ field does not include the
> `PROCESS_TRACE_MODE_EVENT_RECORD` flag. If your _EventRecordCallback_ is
> receiving garbled data from **ProcessTrace**, verify that the
> _ProcessTraceMode_ field includes the `PROCESS_TRACE_MODE_EVENT_RECORD` flag.

**Prior to Windows Vista:** Not supported.

### -field IsKernelTrace

On output, if this member is **TRUE**, the event tracing session is the NT
Kernel Logger. Otherwise, it is another event tracing session.

### -field Context

Context data that a consumer can specify when calling
[OpenTrace](/windows/win32/api/evntrace/nf-evntrace-opentracew). If the consumer
uses
[EventRecordCallback](/windows/win32/api/evntrace/nc-evntrace-pevent_record_callback)
to consume events, ETW sets the **UserContext** member of the
[EVENT_RECORD](/windows/desktop/api/evntcons/ns-evntcons-event_record) structure
to this value.

**Prior to Windows Vista:** Not supported.

## -remarks

Event consumers should:

1. Initialize the memory for this structure to zero.
1. If reading from an ETL file, set **LogFileName** to the path to the file.
   Otherwise (i.e. if reading from a real-time session), set **LoggerName** to
   the name of the session and set **ProcessTraceMode** to
   `PROCESS_TRACE_MODE_REAL_TIME`.
1. If using
   [EventRecordCallback](/windows/win32/api/evntrace/nc-evntrace-pevent_record_callback)
   (recommended), set **EventRecordCallback** to the address of your event
   record callback function, set **Context** to a value to be provided to your
   callback, and add `PROCESS_TRACE_MODE_EVENT_RECORD` to **ProcessTraceMode**.
   Otherwise (i.e. if using
   [EventCallback](/windows/win32/api/evntrace/nc-evntrace-pevent_callback)),
   set **EventCallback** to the address of your event callback function.
1. If you need a callback after each buffer is processed, set **BufferCallback**
   to the address of your buffer callback function.
1. If you want the original raw timestamp data instead of the processed
   timestamp, add `PROCESS_TRACE_MODE_RAW_TIMESTAMP` to **ProcessTraceMode**.
1. Call [OpenTrace](/windows/win32/api/evntrace/nf-evntrace-opentracew). Note
   that if successful, **OpenTrace** function will fill in members of this
   structure with information from the trace data source.
1. Call [ProcessTrace](/windows/win32/api/evntrace/nf-evntrace-processtrace)
   with the handle returned by **OpenTrace**.
   - **ProcessTrace** will invoke your event callback function for each event.
   - **ProcessTrace** will invoke your buffer callback function (if provided)
     after finishing each buffer and will include an instance of the
     **EVENT_TRACE_LOGFILE** structure with trace processing status information.
1. After trace processing completes, call
   [CloseTrace](/windows/win32/api/evntrace/nf-evntrace-closetrace) to close the
   handle that was returned by **OpenTrace**.

> [!NOTE]
> The evntrace.h header defines EVENT_TRACE_LOGFILE as an alias which
> automatically selects the ANSI or Unicode version of this function based on
> the definition of the UNICODE preprocessor constant. Mixing usage of the
> encoding-neutral alias with code that not encoding-neutral can lead to
> mismatches that result in compilation or runtime errors. For more information,
> see
> [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

[BufferCallback](/windows/win32/api/evntrace/nc-evntrace-pevent_trace_buffer_callbackw)

[EventRecordCallback](/windows/win32/api/evntrace/nc-evntrace-pevent_record_callback)

[OpenTrace](/windows/win32/api/evntrace/nf-evntrace-opentracew)
