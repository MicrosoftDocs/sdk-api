---
UID: NS:evntrace._EVENT_TRACE_HEADER
title: EVENT_TRACE_HEADER (evntrace.h)
description: The EVENT_TRACE_HEADER structure contains standard event tracing information common to all events.
helpviewer_keywords: ["*PEVENT_TRACE_HEADER","EVENT_TRACE_HEADER","EVENT_TRACE_HEADER structure [ETW]","EVENT_TRACE_TYPE_CHECKPOINT","EVENT_TRACE_TYPE_DC_END","EVENT_TRACE_TYPE_DC_START","EVENT_TRACE_TYPE_DEQUEUE","EVENT_TRACE_TYPE_END","EVENT_TRACE_TYPE_EXTENSION","EVENT_TRACE_TYPE_INFO","EVENT_TRACE_TYPE_REPLY","EVENT_TRACE_TYPE_START","PEVENT_TRACE_HEADER","PEVENT_TRACE_HEADER structure pointer [ETW]","TRACE_LEVEL_ERROR","TRACE_LEVEL_FATAL","TRACE_LEVEL_INFORMATION","TRACE_LEVEL_VERBOSE","TRACE_LEVEL_WARNING","WNODE_FLAG_USE_GUID_PTR","WNODE_FLAG_USE_MOF_PTR","_EVENT_TRACE_HEADER","_evt_event_trace_header","base.event_trace_header","etw.event_trace_header","evntrace/EVENT_TRACE_HEADER","evntrace/PEVENT_TRACE_HEADER"]
old-location: etw\event_trace_header.htm
tech.root: ETW
ms.assetid: 33c2de6b-afc2-4323-8d81-2970e66edf5e
ms.date: 12/05/2018
ms.keywords: '*PEVENT_TRACE_HEADER, EVENT_TRACE_HEADER, EVENT_TRACE_HEADER structure [ETW], EVENT_TRACE_TYPE_CHECKPOINT, EVENT_TRACE_TYPE_DC_END, EVENT_TRACE_TYPE_DC_START, EVENT_TRACE_TYPE_DEQUEUE, EVENT_TRACE_TYPE_END, EVENT_TRACE_TYPE_EXTENSION, EVENT_TRACE_TYPE_INFO, EVENT_TRACE_TYPE_REPLY, EVENT_TRACE_TYPE_START, PEVENT_TRACE_HEADER, PEVENT_TRACE_HEADER structure pointer [ETW], TRACE_LEVEL_ERROR, TRACE_LEVEL_FATAL, TRACE_LEVEL_INFORMATION, TRACE_LEVEL_VERBOSE, TRACE_LEVEL_WARNING, WNODE_FLAG_USE_GUID_PTR, WNODE_FLAG_USE_MOF_PTR, _EVENT_TRACE_HEADER, _evt_event_trace_header, base.event_trace_header, etw.event_trace_header, evntrace/EVENT_TRACE_HEADER, evntrace/PEVENT_TRACE_HEADER'
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
req.typenames: EVENT_TRACE_HEADER, *PEVENT_TRACE_HEADER
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _EVENT_TRACE_HEADER
 - evntrace/_EVENT_TRACE_HEADER
 - PEVENT_TRACE_HEADER
 - evntrace/PEVENT_TRACE_HEADER
 - EVENT_TRACE_HEADER
 - evntrace/EVENT_TRACE_HEADER
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
 - EVENT_TRACE_HEADER
---

# EVENT_TRACE_HEADER structure


## -description

The 
<b>EVENT_TRACE_HEADER</b> structure contains standard event tracing information common to all events.

## -struct-fields

### -field Size

Total number of bytes of the event. <b>Size</b> includes the size of the 
header structure, plus the size of any event-specific data appended to the header. 

On input, the size must be less than the size of the event tracing session's buffer minus 72 (0x48).

On output, do not use this number in calculations.

### -field DUMMYUNIONNAME

### -field DUMMYUNIONNAME.FieldTypeFlags

 Reserved.

### -field DUMMYUNIONNAME.DUMMYSTRUCTNAME

### -field DUMMYUNIONNAME.DUMMYSTRUCTNAME.HeaderType

Reserved.

### -field DUMMYUNIONNAME.DUMMYSTRUCTNAME.MarkerFlags

Reserved.

### -field DUMMYUNIONNAME2

### -field DUMMYUNIONNAME2.Version

This is a roll-up of the members of <b>Class</b>. The low-order byte contains the Type, the next byte contains the Level, and the last two bytes contain the version.

### -field DUMMYUNIONNAME2.Class

### -field DUMMYUNIONNAME2.Class.Type

Type of event. A provider can define their own event types or use the predefined event types listed in the following table.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="EVENT_TRACE_TYPE_CHECKPOINT"></a><a id="event_trace_type_checkpoint"></a><dl>
<dt><b>EVENT_TRACE_TYPE_CHECKPOINT</b></dt>
</dl>
</td>
<td width="60%">
Checkpoint event. Use for an event that is not at the start or end of an activity.

</td>
</tr>
<tr>
<td width="40%"><a id="EVENT_TRACE_TYPE_DC_END"></a><a id="event_trace_type_dc_end"></a><dl>
<dt><b>EVENT_TRACE_TYPE_DC_END</b></dt>
</dl>
</td>
<td width="60%">
Data collection end event.

</td>
</tr>
<tr>
<td width="40%"><a id="EVENT_TRACE_TYPE_DC_START"></a><a id="event_trace_type_dc_start"></a><dl>
<dt><b>EVENT_TRACE_TYPE_DC_START</b></dt>
</dl>
</td>
<td width="60%">
Data collection start event.

</td>
</tr>
<tr>
<td width="40%"><a id="EVENT_TRACE_TYPE_DEQUEUE"></a><a id="event_trace_type_dequeue"></a><dl>
<dt><b>EVENT_TRACE_TYPE_DEQUEUE</b></dt>
</dl>
</td>
<td width="60%">
Dequeue event. Use when an activity is queued before it begins. Use EVENT_TRACE_TYPE_START to mark the time when a work item is queued. Use the dequeue event type to mark the time when work on the item actually begins. Use EVENT_TRACE_TYPE_END to mark the time when work on the item completes.

</td>
</tr>
<tr>
<td width="40%"><a id="EVENT_TRACE_TYPE_END"></a><a id="event_trace_type_end"></a><dl>
<dt><b>EVENT_TRACE_TYPE_END</b></dt>
</dl>
</td>
<td width="60%">
End event. Use to trace the final state of a multi-step event.

</td>
</tr>
<tr>
<td width="40%"><a id="EVENT_TRACE_TYPE_EXTENSION"></a><a id="event_trace_type_extension"></a><dl>
<dt><b>EVENT_TRACE_TYPE_EXTENSION</b></dt>
</dl>
</td>
<td width="60%">
Extension event. Use for an event that is a continuation of a previous event. For example, use the extension event type when an event trace records more data than can fit in a session buffer.

</td>
</tr>
<tr>
<td width="40%"><a id="EVENT_TRACE_TYPE_INFO"></a><a id="event_trace_type_info"></a><dl>
<dt><b>EVENT_TRACE_TYPE_INFO</b></dt>
</dl>
</td>
<td width="60%">
Informational event. This is the default event type.

</td>
</tr>
<tr>
<td width="40%"><a id="EVENT_TRACE_TYPE_REPLY"></a><a id="event_trace_type_reply"></a><dl>
<dt><b>EVENT_TRACE_TYPE_REPLY</b></dt>
</dl>
</td>
<td width="60%">
Reply event. Use when an application that requests resources can receive multiple responses. For example, if a client application requests a URL, and the web server replies by sending several files, each file received can be marked as a reply event.

</td>
</tr>
<tr>
<td width="40%"><a id="EVENT_TRACE_TYPE_START"></a><a id="event_trace_type_start"></a><dl>
<dt><b>EVENT_TRACE_TYPE_START</b></dt>
</dl>
</td>
<td width="60%">
Start event. Use to trace the initial state of a multi-step event.

</td>
</tr>
</table>
 

If you define your own event types, you should use numbers starting from 10. However, there is nothing to prevent you from using any numbers that you wish to use.  If your event trace class GUID supports multiple event types, consumers will use the event type to determine the event and how to interpret its contents.

### -field DUMMYUNIONNAME2.Class.Level

Provider-defined value that defines the severity level used to generate the event. The value ranges from 0 to 255. The controller specifies the severity level when it calls the <a href="/windows/desktop/ETW/enabletrace">EnableTrace</a> function. The provider retrieves the severity level by calling the <a href="/windows/desktop/ETW/gettraceenablelevel">GetTraceEnableLevel</a> function from its <a href="/windows/desktop/ETW/controlcallback">ControlCallback</a> implementation. The provider uses the value to set this member.

ETW defines the following severity levels. Selecting a level higher than 1 will also include events for lower levels. For example, if the controller specifies TRACE_LEVEL_WARNING (3), the provider also generates  TRACE_LEVEL_FATAL (1) and TRACE_LEVEL_ERROR (2) events.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="TRACE_LEVEL_FATAL"></a><a id="trace_level_fatal"></a><dl>
<dt><b>TRACE_LEVEL_FATAL</b></dt>
<dt>1</dt>
</dl>
</td>
<td width="60%">
Abnormal exit or termination events.

</td>
</tr>
<tr>
<td width="40%"><a id="TRACE_LEVEL_ERROR"></a><a id="trace_level_error"></a><dl>
<dt><b>TRACE_LEVEL_ERROR</b></dt>
<dt>2</dt>
</dl>
</td>
<td width="60%">
Severe error events.

</td>
</tr>
<tr>
<td width="40%"><a id="TRACE_LEVEL_WARNING"></a><a id="trace_level_warning"></a><dl>
<dt><b>TRACE_LEVEL_WARNING</b></dt>
<dt>3</dt>
</dl>
</td>
<td width="60%">
Warning events such as allocation failures.

</td>
</tr>
<tr>
<td width="40%"><a id="TRACE_LEVEL_INFORMATION"></a><a id="trace_level_information"></a><dl>
<dt><b>TRACE_LEVEL_INFORMATION</b></dt>
<dt>4</dt>
</dl>
</td>
<td width="60%">
Non-error events such as entry or exit events.

</td>
</tr>
<tr>
<td width="40%"><a id="TRACE_LEVEL_VERBOSE"></a><a id="trace_level_verbose"></a><dl>
<dt><b>TRACE_LEVEL_VERBOSE</b></dt>
<dt>5</dt>
</dl>
</td>
<td width="60%">
Detailed trace events.

</td>
</tr>
</table>

### -field DUMMYUNIONNAME2.Class.Version

Indicates the version of the event trace class that you are using to log the event. Specify zero if there is only one version of your event trace class. The version tells the consumer which MOF class to use to decipher the event data.

### -field ThreadId

On output, identifies the thread that generated the event. 




Note that on Windows 2000, <b>ThreadId</b> was a <b>ULONGLONG</b> value.

### -field ProcessId

 On output, identifies  the process that generated the event.

<b>Windows 2000:  </b>This member is not supported.

### -field TimeStamp

On output, contains the time that the event occurred. The resolution is system time unless the <b>ProcessTraceMode</b> member of <a href="/windows/desktop/ETW/event-trace-logfile">EVENT_TRACE_LOGFILE</a> contains the PROCESS_TRACE_MODE_RAW_TIMESTAMP flag, in which case the resolution depends on the value of the <b>Wnode.ClientContext</b> member of <a href="/windows/desktop/ETW/event-trace-properties">EVENT_TRACE_PROPERTIES</a> at the time the controller created the session.

### -field DUMMYUNIONNAME3

### -field DUMMYUNIONNAME3.Guid

Event trace class GUID. You can use the class GUID to identify a category of events and the <b>Class.Type</b> member to identify an event within the category of events. 

Alternatively, you can use the <b>GuidPtr</b> member to specify the class GUID.  




<b>Windows XP and Windows 2000:  </b>The class GUID must have been registered previously using the 
<a href="/windows/desktop/ETW/registertraceguids">RegisterTraceGuids</a> function.

### -field DUMMYUNIONNAME3.GuidPtr

Pointer to an event trace class GUID. Alternatively, you can use the <b>Guid</b> member to specify the class GUID. 


When the event is written, ETW uses the pointer to copy the GUID to the event (the GUID is included in the event, not the pointer).

If you use this member, the <b>Flags</b> member must also contain WNODE_FLAG_USE_GUID_PTR.

### -field DUMMYUNIONNAME4

### -field DUMMYUNIONNAME4.DUMMYSTRUCTNAME

### -field DUMMYUNIONNAME4.DUMMYSTRUCTNAME.KernelTime

Elapsed execution time for kernel-mode instructions, in CPU time units. If you are using a private session, use the value in the <b>ProcessorTime</b> member instead.  For more information, see Remarks.

### -field DUMMYUNIONNAME4.DUMMYSTRUCTNAME.UserTime

Elapsed execution time for user-mode instructions, in CPU time units. If you are using a private session, use the value in the <b>ProcessorTime</b> member instead. For more information, see Remarks.

### -field DUMMYUNIONNAME4.ProcessorTime

For private sessions, the elapsed execution time for user-mode instructions, in CPU ticks.

### -field DUMMYUNIONNAME4.DUMMYSTRUCTNAME2

### -field DUMMYUNIONNAME4.DUMMYSTRUCTNAME2.ClientContext

Reserved.

### -field DUMMYUNIONNAME4.DUMMYSTRUCTNAME2.Flags

You must set this member to WNODE_FLAG_TRACED_GUID, and may optionally specify any combination of the following.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="WNODE_FLAG_USE_GUID_PTR"></a><a id="wnode_flag_use_guid_ptr"></a><dl>
<dt><b>WNODE_FLAG_USE_GUID_PTR</b></dt>
</dl>
</td>
<td width="60%">
Specify if the <b>GuidPtr</b> member contains the class GUID. 



									

</td>
</tr>
<tr>
<td width="40%"><a id="WNODE_FLAG_USE_MOF_PTR"></a><a id="wnode_flag_use_mof_ptr"></a><dl>
<dt><b>WNODE_FLAG_USE_MOF_PTR</b></dt>
</dl>
</td>
<td width="60%">
Specify if an array of 
<a href="/windows/desktop/ETW/mof-field">MOF_FIELD</a> structures contains the event data appended to this structure. The number of elements in the array is limited to <b>MAX_MOF_FIELDS</b>.

</td>
</tr>
</table>

## -remarks

Be sure to initialize the memory for this structure to zero before setting any members.

You can use the <b>KernelTime</b> and <b>UserTime</b> members to determine the CPU cost in units for a set of instructions (the values indicate the CPU usage charged to that thread at the time of logging). For example, if Event A and Event B are consecutively logged by the same thread and they have CPU usage numbers 150 and 175, then the activity that was performed by that thread between events A and B cost 25 CPU time units (175 – 150).

The <b>TimerResolution</b> of the <a href="/windows/desktop/ETW/trace-logfile-header">TRACE_LOGFILE_HEADER</a> structure contains the resolution of the CPU usage timer in 100-nanosecond units. You can use the timer resolution with the kernel time and user time values to determine the amount of CPU time that the set of instructions used. For example, if the timer resolution is 156,250, then 25 CPU time units is 0.39 seconds (156,250 * 25 * 100 / 1,000,000,000). This is the amount of CPU time (not elapsed wall clock time) used by the set of instructions between events A and B. 

Note, however, that the CPU usage timer resolution is typically very low (around 10 or more milliseconds). Therefore, CPU usage numbers cannot be used to account for CPU time usage among threads with high accuracy. Rather, they are suitable for long term, statistical type of analysis.

## -see-also

<a href="/windows/desktop/ETW/event-trace">EVENT_TRACE</a>



<a href="/windows/desktop/ETW/eventcallback">EventCallback</a>



<a href="/windows/desktop/ETW/eventclasscallback">EventClassCallback</a>



<a href="/windows/desktop/ETW/traceevent">TraceEvent</a>