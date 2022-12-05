---
UID: NS:evntcons._EVENT_HEADER
title: EVENT_HEADER (evntcons.h)
description: The EVENT_HEADER structure (evntcons.h) defines information about the event.
helpviewer_keywords: ["*PEVENT_HEADER","EVENT_HEADER","EVENT_HEADER structure [ETW]","EVENT_HEADER_FLAG_32_BIT_HEADER","EVENT_HEADER_FLAG_64_BIT_HEADER","EVENT_HEADER_FLAG_CLASSIC_HEADER","EVENT_HEADER_FLAG_EXTENDED_INFO","EVENT_HEADER_FLAG_NO_CPUTIME","EVENT_HEADER_FLAG_PRIVATE_SESSION","EVENT_HEADER_FLAG_STRING_ONLY","EVENT_HEADER_FLAG_TRACE_MESSAGE","EVENT_HEADER_PROPERTY_FORWARDED_XML","EVENT_HEADER_PROPERTY_LEGACY_EVENTLOG","EVENT_HEADER_PROPERTY_XML","PEVENT_HEADER","PEVENT_HEADER structure pointer [ETW]","_EVENT_HEADER","base.event_header","etw.event_header","relogger/EVENT_HEADER","relogger/PEVENT_HEADER"]
old-location: etw\event_header.htm
tech.root: ETW
ms.assetid: 479091ae-7229-433b-b93b-8da6cc18df89
ms.date: 08/04/2022
ms.keywords: '*PEVENT_HEADER, EVENT_HEADER, EVENT_HEADER structure [ETW], EVENT_HEADER_FLAG_32_BIT_HEADER, EVENT_HEADER_FLAG_64_BIT_HEADER, EVENT_HEADER_FLAG_CLASSIC_HEADER, EVENT_HEADER_FLAG_EXTENDED_INFO, EVENT_HEADER_FLAG_NO_CPUTIME, EVENT_HEADER_FLAG_PRIVATE_SESSION, EVENT_HEADER_FLAG_STRING_ONLY, EVENT_HEADER_FLAG_TRACE_MESSAGE, EVENT_HEADER_PROPERTY_FORWARDED_XML, EVENT_HEADER_PROPERTY_LEGACY_EVENTLOG, EVENT_HEADER_PROPERTY_XML, PEVENT_HEADER, PEVENT_HEADER structure pointer [ETW], _EVENT_HEADER, base.event_header, etw.event_header, relogger/EVENT_HEADER, relogger/PEVENT_HEADER'
req.header: evntcons.h
req.include-header: Evntcons.h
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
req.typenames: EVENT_HEADER, *PEVENT_HEADER
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _EVENT_HEADER
 - evntcons/_EVENT_HEADER
 - PEVENT_HEADER
 - evntcons/PEVENT_HEADER
 - EVENT_HEADER
 - evntcons/EVENT_HEADER
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - relogger.h
api_name:
 - EVENT_HEADER
---

# EVENT_HEADER structure (evntcons.h)

## -description

Defines information about the event.

## -struct-fields

### -field Size

Size of the event record, in bytes.

### -field HeaderType

Reserved.

### -field Flags

Flags that provide information about the event such as the type of session it was logged to and if the event contains extended data. This member can contain one or more of the following flags.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="EVENT_HEADER_FLAG_EXTENDED_INFO"></a><a id="event_header_flag_extended_info"></a><dl>
<dt><b>EVENT_HEADER_FLAG_EXTENDED_INFO</b></dt>
</dl>
</td>
<td width="60%">
The <b>ExtendedData</b> member of <a href="/windows/desktop/api/evntcons/ns-evntcons-event_record">EVENT_RECORD</a> contains data.

</td>
</tr>
<tr>
<td width="40%"><a id="EVENT_HEADER_FLAG_PRIVATE_SESSION"></a><a id="event_header_flag_private_session"></a><dl>
<dt><b>EVENT_HEADER_FLAG_PRIVATE_SESSION</b></dt>
</dl>
</td>
<td width="60%">
The event was logged to a private session. Use <b>ProcessorTime</b> for  elapsed execution time.

</td>
</tr>
<tr>
<td width="40%"><a id="EVENT_HEADER_FLAG_STRING_ONLY"></a><a id="event_header_flag_string_only"></a><dl>
<dt><b>EVENT_HEADER_FLAG_STRING_ONLY</b></dt>
</dl>
</td>
<td width="60%">
The event data is a null-terminated Unicode string. You do not need a manifest to parse the <b>UserData</b> member of <a href="/windows/desktop/api/evntcons/ns-evntcons-event_record">EVENT_RECORD</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="EVENT_HEADER_FLAG_TRACE_MESSAGE"></a><a id="event_header_flag_trace_message"></a><dl>
<dt><b>EVENT_HEADER_FLAG_TRACE_MESSAGE</b></dt>
</dl>
</td>
<td width="60%">
The provider used <a href="/windows/desktop/ETW/tracemessage">TraceMessage</a> or <a href="/windows/desktop/ETW/tracemessageva">TraceMessageVa</a> to log the event. Most providers do not use these functions to write events, so this flag typically indicates that the event was written by <a href="/windows/desktop/ETW/windows-software-trace-preprocessor">Windows Software Trace Preprocessor</a> (WPP).

</td>
</tr>
<tr>
<td width="40%"><a id="EVENT_HEADER_FLAG_NO_CPUTIME"></a><a id="event_header_flag_no_cputime"></a><dl>
<dt><b>EVENT_HEADER_FLAG_NO_CPUTIME</b></dt>
</dl>
</td>
<td width="60%">
Use <b>ProcessorTime</b> for  elapsed execution time.

</td>
</tr>
<tr>
<td width="40%"><a id="EVENT_HEADER_FLAG_32_BIT_HEADER"></a><a id="event_header_flag_32_bit_header"></a><dl>
<dt><b>EVENT_HEADER_FLAG_32_BIT_HEADER</b></dt>
</dl>
</td>
<td width="60%">
Indicates that the provider was running on a 32-bit computer or in a WOW64 session.

</td>
</tr>
<tr>
<td width="40%"><a id="EVENT_HEADER_FLAG_64_BIT_HEADER"></a><a id="event_header_flag_64_bit_header"></a><dl>
<dt><b>EVENT_HEADER_FLAG_64_BIT_HEADER</b></dt>
</dl>
</td>
<td width="60%">
Indicates that the provider was running on a 64-bit computer.

</td>
</tr>
<tr>
<td width="40%"><a id="EVENT_HEADER_FLAG_CLASSIC_HEADER"></a><a id="event_header_flag_classic_header"></a><dl>
<dt><b>EVENT_HEADER_FLAG_CLASSIC_HEADER</b></dt>
</dl>
</td>
<td width="60%">
Indicates that provider used <a href="/windows/desktop/ETW/traceevent">TraceEvent</a> to log the event.

</td>
</tr>
</table>

### -field EventProperty

Indicates the source to use for parsing the event data.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="EVENT_HEADER_PROPERTY_XML"></a><a id="event_header_property_xml"></a><dl>
<dt><b>EVENT_HEADER_PROPERTY_XML</b></dt>
</dl>
</td>
<td width="60%">
Indicates that you need a manifest to parse the event data.

</td>
</tr>
<tr>
<td width="40%"><a id="EVENT_HEADER_PROPERTY_FORWARDED_XML"></a><a id="event_header_property_forwarded_xml"></a><dl>
<dt><b>EVENT_HEADER_PROPERTY_FORWARDED_XML</b></dt>
</dl>
</td>
<td width="60%">
Indicates that the event data contains within itself a fully-rendered XML description of the data, so you do  not need a manifest to parse the event data.

</td>
</tr>
<tr>
<td width="40%"><a id="EVENT_HEADER_PROPERTY_LEGACY_EVENTLOG"></a><a id="event_header_property_legacy_eventlog"></a><dl>
<dt><b>EVENT_HEADER_PROPERTY_LEGACY_EVENTLOG</b></dt>
</dl>
</td>
<td width="60%">
Indicates that you need a WMI MOF class to parse the event data.

</td>
</tr>
</table>

### -field ThreadId

Identifies the thread that generated the event.

### -field ProcessId

Identifies the process that generated the event.

### -field TimeStamp

Contains the time that the event occurred. The resolution is system time unless the <b>ProcessTraceMode</b> member of <a href="/windows/desktop/ETW/event-trace-logfile">EVENT_TRACE_LOGFILE</a> contains the PROCESS_TRACE_MODE_RAW_TIMESTAMP flag, in which case the resolution depends on the value of the <b>Wnode.ClientContext</b> member of <a href="/windows/desktop/ETW/event-trace-properties">EVENT_TRACE_PROPERTIES</a> at the time the controller created the session.

### -field ProviderId

GUID that uniquely identifies the provider that logged the event.

### -field EventDescriptor

Defines the information about the event such as the event identifier and severity level. For details, see <a href="/windows/desktop/api/evntprov/ns-evntprov-event_descriptor">EVENT_DESCRIPTOR</a>.

### -field DUMMYUNIONNAME

### -field DUMMYUNIONNAME.DUMMYSTRUCTNAME

### -field DUMMYUNIONNAME.DUMMYSTRUCTNAME.KernelTime

Elapsed execution time for kernel-mode instructions, in CPU time units. If you are using a private session, use the value in the <b>ProcessorTime</b> member instead.  For more information, see Remarks.

### -field DUMMYUNIONNAME.DUMMYSTRUCTNAME.UserTime

Elapsed execution time for user-mode instructions, in CPU time units. If you are using a private session, use the value in the <b>ProcessorTime</b> member instead. For more information, see Remarks.

### -field DUMMYUNIONNAME.ProcessorTime

For private sessions, the elapsed execution time for user-mode instructions, in CPU ticks.

### -field ActivityId

Identifier that relates two events. For details, see <a href="/windows/desktop/api/evntprov/nf-evntprov-eventwritetransfer">EventWriteTransfer</a>.

## -remarks

You can use the <b>KernelTime</b> and <b>UserTime</b> members to determine the CPU cost in units for a set of instructions (the values indicate the CPU usage charged to that thread at the time of logging). For example, if Event A and Event B are consecutively logged by the same thread and they have CPU usage numbers 150 and 175, then the activity that was performed by that thread between events A and B cost 25 CPU time units (175 – 150).

The <b>TimerResolution</b> of the <a href="/windows/desktop/ETW/trace-logfile-header">TRACE_LOGFILE_HEADER</a> structure contains the resolution of the CPU usage timer in 100-nanosecond units. You can use the timer resolution with the kernel time and user time values to determine the amount of CPU time that the set of instructions used. For example, if the timer resolution is 156,250, then 25 CPU time units is 0.39 seconds (156,250 * 25 * 100 / 1,000,000,000). This is the amount of CPU time (not elapsed wall clock time) used by the set of instructions between events A and B.

## -see-also

<a href="/windows/desktop/api/evntcons/ns-evntcons-event_record">EVENT_RECORD</a>
