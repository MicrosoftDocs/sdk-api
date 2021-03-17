---
UID: NS:evntrace._EVENT_TRACE_LOGFILEW
title: EVENT_TRACE_LOGFILEW (evntrace.h)
description: The EVENT_TRACE_LOGFILE structure specifies how the consumer wants to read events (from a log file or in real-time) and the callbacks that will receive the events.
helpviewer_keywords: ["*PEVENT_TRACE_LOGFILEW","EVENT_TRACE_LOGFILE","EVENT_TRACE_LOGFILE structure [ETW]","EVENT_TRACE_LOGFILEA","EVENT_TRACE_LOGFILEW","PEVENT_TRACE_LOGFILE","PEVENT_TRACE_LOGFILE structure pointer [ETW]","PROCESS_TRACE_MODE_EVENT_RECORD","PROCESS_TRACE_MODE_RAW_TIMESTAMP","PROCESS_TRACE_MODE_REAL_TIME","_EVENT_TRACE_LOGFILEA","_EVENT_TRACE_LOGFILEW","_evt_event_trace_logfile","base.event_trace_logfile","etw.event_trace_logfile","evntrace/EVENT_TRACE_LOGFILE","evntrace/EVENT_TRACE_LOGFILEA","evntrace/EVENT_TRACE_LOGFILEW","evntrace/PEVENT_TRACE_LOGFILE"]
old-location: etw\event_trace_logfile.htm
tech.root: ETW
ms.assetid: 179451e9-7e3c-4d3a-bcc6-3ad9d382229a
ms.date: 12/05/2018
ms.keywords: '*PEVENT_TRACE_LOGFILEW, EVENT_TRACE_LOGFILE, EVENT_TRACE_LOGFILE structure [ETW], EVENT_TRACE_LOGFILEA, EVENT_TRACE_LOGFILEW, PEVENT_TRACE_LOGFILE, PEVENT_TRACE_LOGFILE structure pointer [ETW], PROCESS_TRACE_MODE_EVENT_RECORD, PROCESS_TRACE_MODE_RAW_TIMESTAMP, PROCESS_TRACE_MODE_REAL_TIME, _EVENT_TRACE_LOGFILEA, _EVENT_TRACE_LOGFILEW, _evt_event_trace_logfile, base.event_trace_logfile, etw.event_trace_logfile, evntrace/EVENT_TRACE_LOGFILE, evntrace/EVENT_TRACE_LOGFILEA, evntrace/EVENT_TRACE_LOGFILEW, evntrace/PEVENT_TRACE_LOGFILE'
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

The 
<b>EVENT_TRACE_LOGFILE</b> structure specifies how the consumer wants to read events (from a log file or in real-time) and the callbacks that will receive the events. 

When ETW flushes a buffer, this structure contains information about the event tracing session and the buffer that ETW flushed.

## -struct-fields

### -field LogFileName

Name of the log file used by the event tracing session. Specify a value for this member if you are consuming from a log file. 


This member must be <b>NULL</b> if <b>LoggerName</b> is specified.

You must know the log file name the controller specified. If the controller logged events to a private session (the controller set the <b>LogFileMode</b> member of <a href="/windows/desktop/ETW/event-trace-properties">EVENT_TRACE_PROPERTIES</a> to  <b>EVENT_TRACE_PRIVATE_LOGGER_MODE</b>), the file name must include the process identifier that ETW appended to the log file name. For example, if the controller named the log file xyz.etl and the process identifier is 123, ETW uses xyz.etl_123 as the file name.

If the controller set the <b>LogFileMode</b> member of <a href="/windows/desktop/ETW/event-trace-properties">EVENT_TRACE_PROPERTIES</a> to  <b>EVENT_TRACE_FILE_MODE_NEWFILE</b>, the log file name must include the sequential serial number used to create each new log file.

The user consuming the events must have permissions to read the file.

### -field LoggerName

Name of the event tracing session. Specify a value for this member if you want to consume events in real time. This member must be <b>NULL</b> if <b>LogFileName</b> is specified.

You can only consume events in real  time if the controller set the <b>LogFileMode</b> member of <a href="/windows/desktop/ETW/event-trace-properties">EVENT_TRACE_PROPERTIES</a> to  <b>EVENT_TRACE_REAL_TIME_MODE</b>.

Only users with administrative privileges, users in the Performance Log Users group, and applications running as LocalSystem, LocalService, NetworkService can consume events in real time. To grant a restricted user the ability to consume events in real time, add them to the Performance Log Users group or call <a href="/windows/desktop/api/evntcons/nf-evntcons-eventaccesscontrol">EventAccessControl</a>.

<b>Windows XP and Windows 2000:  </b>Anyone can consume real time events.

### -field CurrentTime

On output, the current time, in 100-nanosecond intervals since midnight, January 1, 1601.

### -field BuffersRead

On output, the number of buffers processed.

### -field DUMMYUNIONNAME

### -field DUMMYUNIONNAME.LogFileMode

Reserved. Do not use.

### -field DUMMYUNIONNAME.ProcessTraceMode

Modes for processing events. The modes are defined in the Evntcons.h header file. You can specify one or more of the following modes:

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="PROCESS_TRACE_MODE_EVENT_RECORD"></a><a id="process_trace_mode_event_record"></a><dl>
<dt><b>PROCESS_TRACE_MODE_EVENT_RECORD</b></dt>
</dl>
</td>
<td width="60%">
Specify this mode if you want to receive events in the new <a href="/windows/desktop/api/evntcons/ns-evntcons-event_record">EVENT_RECORD</a> format. To receive events in the new format you must specify a callback in the <b>EventRecordCallback</b> member. If you do not specify this mode, you receive events in the old format through the callback specified in the <b>EventCallback</b> member.

<b>Prior to Windows Vista:  </b>Not supported.

</td>
</tr>
<tr>
<td width="40%"><a id="PROCESS_TRACE_MODE_RAW_TIMESTAMP"></a><a id="process_trace_mode_raw_timestamp"></a><dl>
<dt><b>PROCESS_TRACE_MODE_RAW_TIMESTAMP</b></dt>
</dl>
</td>
<td width="60%">
Specify this mode if you do not want the time stamp value in the <b>TimeStamp</b> member of <a href="/windows/desktop/api/evntcons/ns-evntcons-event_header">EVENT_HEADER</a> and <a href="/windows/desktop/ETW/event-trace-header">EVENT_TRACE_HEADER</a> converted to system time (leaves the time stamp value in the resolution that the controller specified in the <b>Wnode.ClientContext</b> member of <a href="/windows/desktop/ETW/event-trace-properties">EVENT_TRACE_PROPERTIES</a>).

<b>Prior to Windows Vista:  </b>Not supported.

</td>
</tr>
<tr>
<td width="40%"><a id="PROCESS_TRACE_MODE_REAL_TIME"></a><a id="process_trace_mode_real_time"></a><dl>
<dt><b>PROCESS_TRACE_MODE_REAL_TIME</b></dt>
</dl>
</td>
<td width="60%">
Specify this mode to receive events in real time (you must specify this mode if <b>LoggerName</b> is not <b>NULL</b>).

</td>
</tr>
</table>

### -field CurrentEvent

On output, an 
<a href="/windows/desktop/ETW/event-trace">EVENT_TRACE</a> structure that contains the last event processed.

### -field LogfileHeader

On output, a 
<a href="/windows/desktop/ETW/trace-logfile-header">TRACE_LOGFILE_HEADER</a> structure that contains general information about the session and the computer on which the session ran.

### -field BufferCallback

Pointer to the 
<a href="/windows/desktop/ETW/buffercallback">BufferCallback</a> function that receives buffer-related statistics for each buffer ETW flushes. ETW calls this callback after it delivers all the events in the buffer. This callback is optional.

### -field BufferSize

On output, contains the size of each buffer, in bytes.

### -field Filled

On output, contains the number of bytes in the buffer that contain valid information.

### -field EventsLost

Not used.

### -field DUMMYUNIONNAME2

### -field DUMMYUNIONNAME2.EventCallback

Pointer to the 
<a href="/windows/desktop/ETW/eventcallback">EventCallback</a> function that ETW calls for each event in the buffer. 

Specify this callback if you are consuming events from a provider that used one of the <a href="/windows/desktop/ETW/traceevent">TraceEvent</a> functions to log events.

### -field DUMMYUNIONNAME2.EventRecordCallback

Pointer to the 
<a href="/windows/desktop/ETW/eventrecordcallback">EventRecordCallback</a> function that ETW calls for each event in the buffer. 

Specify this callback if you are consuming events from a provider that used one of the <a href="/windows/desktop/api/evntprov/nf-evntprov-eventwrite">EventWrite</a> functions to log events.

<b>Prior to Windows Vista:  </b>Not supported.

### -field IsKernelTrace

On output, if this member is <b>TRUE</b>, the event tracing session is the NT Kernel Logger. Otherwise, it is another event tracing session.

### -field Context

Context data that a consumer can specify when calling <a href="/windows/desktop/ETW/opentrace">OpenTrace</a>. If the consumer uses <a href="/windows/desktop/ETW/eventrecordcallback">EventRecordCallback</a> to consume events, ETW sets the <b>UserContext</b> member of the <a href="/windows/desktop/api/evntcons/ns-evntcons-event_record">EVENT_RECORD</a> structure to this value.

<b>Prior to Windows Vista:  </b>Not supported.

## -remarks

Be sure to initialize the memory for this structure to zero before setting any members.

Consumers pass this structure to the 
<a href="/windows/desktop/ETW/opentrace">OpenTrace</a> function. 

When ETW flushes a buffer, it passes the structure to the 
consumer's <a href="/windows/desktop/ETW/buffercallback">BufferCallback</a> function.





> [!NOTE]
> The evntrace.h header defines EVENT_TRACE_LOGFILE as an alias which automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/ETW/buffercallback">BufferCallback</a>



<a href="/windows/desktop/ETW/opentrace">OpenTrace</a>