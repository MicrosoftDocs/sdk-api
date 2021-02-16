---
UID: NS:evntrace._EVENT_INSTANCE_HEADER
title: EVENT_INSTANCE_HEADER (evntrace.h)
description: The EVENT_INSTANCE_HEADER structure contains standard event tracing information common to all events.
helpviewer_keywords: ["*PEVENT_INSTANCE_HEADER","EVENT_INSTANCE_HEADER","EVENT_INSTANCE_HEADER structure [ETW]","EVENT_TRACE_TYPE_CHECKPOINT","EVENT_TRACE_TYPE_DC_END","EVENT_TRACE_TYPE_DC_START","EVENT_TRACE_TYPE_DEQUEUE","EVENT_TRACE_TYPE_END","EVENT_TRACE_TYPE_EXTENSION","EVENT_TRACE_TYPE_INFO","EVENT_TRACE_TYPE_REPLY","EVENT_TRACE_TYPE_START","TRACE_LEVEL_ERROR","TRACE_LEVEL_FATAL","TRACE_LEVEL_INFORMATION","TRACE_LEVEL_VERBOSE","TRACE_LEVEL_WARNING","WNODE_FLAG_USE_GUID_PTR","WNODE_FLAG_USE_MOF_PTR","_EVENT_INSTANCE_HEADER","_evt_event_instance_header","base.event_instance_header","etw.event_instance_header","evntrace/EVENT_INSTANCE_HEADER"]
old-location: etw\event_instance_header.htm
tech.root: ETW
ms.assetid: 2a79d937-2a3b-4426-b31f-a1a3ce86a334
ms.date: 12/05/2018
ms.keywords: '*PEVENT_INSTANCE_HEADER, EVENT_INSTANCE_HEADER, EVENT_INSTANCE_HEADER structure [ETW], EVENT_TRACE_TYPE_CHECKPOINT, EVENT_TRACE_TYPE_DC_END, EVENT_TRACE_TYPE_DC_START, EVENT_TRACE_TYPE_DEQUEUE, EVENT_TRACE_TYPE_END, EVENT_TRACE_TYPE_EXTENSION, EVENT_TRACE_TYPE_INFO, EVENT_TRACE_TYPE_REPLY, EVENT_TRACE_TYPE_START, TRACE_LEVEL_ERROR, TRACE_LEVEL_FATAL, TRACE_LEVEL_INFORMATION, TRACE_LEVEL_VERBOSE, TRACE_LEVEL_WARNING, WNODE_FLAG_USE_GUID_PTR, WNODE_FLAG_USE_MOF_PTR, _EVENT_INSTANCE_HEADER, _evt_event_instance_header, base.event_instance_header, etw.event_instance_header, evntrace/EVENT_INSTANCE_HEADER'
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
req.typenames: EVENT_INSTANCE_HEADER, *PEVENT_INSTANCE_HEADER
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _EVENT_INSTANCE_HEADER
 - evntrace/_EVENT_INSTANCE_HEADER
 - PEVENT_INSTANCE_HEADER
 - evntrace/PEVENT_INSTANCE_HEADER
 - EVENT_INSTANCE_HEADER
 - evntrace/EVENT_INSTANCE_HEADER
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
 - EVENT_INSTANCE_HEADER
---

## -description

The <b>EVENT_INSTANCE_HEADER</b> structure contains standard event tracing information common to all events. The structure also contains registration handles for the event trace class and related parent event, which you use to trace instances of a transaction or hierarchical relationships between related events.

## -struct-fields

### -field Size

Total number of bytes of the event. <b>Size</b> must include the size of the 
<b>EVENT_INSTANCE_HEADER</b> structure, plus the size of any event-specific data appended to this structure. The size must be less than the size of the event tracing session's buffer minus 72 (0x48).

### -field DUMMYUNIONNAME

A union of various structures and members.

### -field DUMMYUNIONNAME.FieldTypeFlags

Reserved.

### -field DUMMYUNIONNAME.DUMMYSTRUCTNAME

Reserved.

### -field DUMMYUNIONNAME.DUMMYSTRUCTNAME.HeaderType

Reserved.

### -field DUMMYUNIONNAME.DUMMYSTRUCTNAME.MarkerFlags

Reserved.

### -field DUMMYUNIONNAME2

A union of Class in two forms.

### -field DUMMYUNIONNAME2.Version

This is a roll-up of the members of <b>Class</b>. The low-order byte contains the Type, the next byte contains the Level, and the last two bytes contain the version.

### -field DUMMYUNIONNAME2.Class

The Class structure.

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

If your event trace class GUID supports multiple event types, consumers will use the event type to determine the event and how to interpret its contents.

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

On output, contains the time the event occurred, in 100-nanosecond intervals since midnight, January 1, 1601.

### -field RegHandle

Handle to a registered event trace class. Set this property before calling the <a href="/windows/desktop/ETW/traceeventinstance">TraceEventInstance</a> function.

The 
<a href="/windows/desktop/ETW/registertraceguids">RegisterTraceGuids</a> function creates this handle (see the <i>TraceGuidReg</i> parameter).

### -field InstanceId

On output, contains the event trace instance identifier associated with <b>RegHandle</b>.

### -field ParentInstanceId

On output, contains the event trace instance identifier associated with <b>ParentRegHandle</b>.

### -field DUMMYUNIONNAME3

A union of structs and members.

### -field DUMMYUNIONNAME3.DUMMYSTRUCTNAME

A structure containing the following members.

### -field DUMMYUNIONNAME3.DUMMYSTRUCTNAME.KernelTime

Elapsed execution time for kernel-mode instructions, in CPU ticks. If you are using a private session, use the value in the <b>ProcessorTime</b> member instead.

### -field DUMMYUNIONNAME3.DUMMYSTRUCTNAME.UserTime

Elapsed execution time for user-mode instructions, in CPU ticks. If you are using a private session, use the value in the <b>ProcessorTime</b> member instead.

### -field DUMMYUNIONNAME3.ProcessorTime

For private sessions, the elapsed execution time for user-mode instructions, in CPU ticks.

### -field DUMMYUNIONNAME3.DUMMYSTRUCTNAME2

A union of structs and members.

### -field DUMMYUNIONNAME3.DUMMYSTRUCTNAME2.EventId

The event identifier.

### -field DUMMYUNIONNAME3.DUMMYSTRUCTNAME2.Flags

Must contain <b>WNODE_FLAG_TRACED_GUID</b>, and may also contain any combination of the following.

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

### -field ParentRegHandle

Handle to a registered event trace class of a parent event. Set this property before calling the <a href="/windows/desktop/ETW/traceeventinstance">TraceEventInstance</a> function if you want to trace a hierarchical relationship (parent element/child element) between related events.

The 
<a href="/windows/desktop/ETW/registertraceguids">RegisterTraceGuids</a> function creates this handle (see the <i>TraceGuidReg</i> parameter).


#### - ClientContext

Reserved.

## -remarks

Be sure to initialize the memory for this structure to zero before setting any members.

## -see-also

<a href="/windows/desktop/ETW/traceeventinstance">TraceEventInstance</a>