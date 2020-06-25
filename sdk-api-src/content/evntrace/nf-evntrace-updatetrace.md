---
UID: NF:evntrace.UpdateTrace
title: UpdateTrace macro (evntrace.h)
description: The UpdateTrace function updates the property setting of the specified event tracing session. The ControlTrace function supersedes this function.
helpviewer_keywords: ["UpdateTrace","UpdateTrace function [ETW]","UpdateTraceA","UpdateTraceW","_evt_updatetrace","base.updatetrace","etw.updatetrace","evntrace/UpdateTrace","evntrace/UpdateTraceA","evntrace/UpdateTraceW"]
old-location: etw\updatetrace.htm
tech.root: ETW
ms.assetid: 40e6deaf-7363-45eb-80d0-bc3f33760875
ms.date: 12/05/2018
ms.keywords: UpdateTrace, UpdateTrace function [ETW], UpdateTraceA, UpdateTraceW, _evt_updatetrace, base.updatetrace, etw.updatetrace, evntrace/UpdateTrace, evntrace/UpdateTraceA, evntrace/UpdateTraceW
f1_keywords:
- evntrace/UpdateTrace
dev_langs:
- c++
req.header: evntrace.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: UpdateTraceW (Unicode) and UpdateTraceA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Advapi32.lib
req.dll: Advapi32.dll
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- DllExport
api_location:
- Advapi32.dll
- API-MS-Win-eventing-Legacy-l1-1-0.dll
- advapi32legacy.dll
api_name:
- UpdateTrace
- UpdateTraceA
- UpdateTraceW
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# UpdateTrace macro


## -description


The 
<b>UpdateTrace</b> function updates the property setting of the specified event tracing session. 
			

The 
<a href="https://docs.microsoft.com/windows/desktop/ETW/controltrace">ControlTrace</a> function supersedes this function.


## -parameters




### -param a [in]

Handle to the event tracing session to update, or <b>NULL</b>. You must specify <i>SessionHandle</i> if <i>SessionName</i> is <b>NULL</b>. However, ETW ignores the handle if <i>SessionName</i> is not <b>NULL</b>. The handle is returned by the 
<a href="https://docs.microsoft.com/windows/desktop/ETW/starttrace">StartTrace</a> function.


### -param b [in]

Pointer to a null-terminated string that specifies the name of the event tracing session to update, or <b>NULL</b>. You must specify <i>SessionName</i> if <i>SessionHandle</i> is <b>NULL</b>.

To specify the NT Kernel Logger session, set <i>SessionName</i> to <b>KERNEL_LOGGER_NAME</b>.


### -param c [in, out]

Pointer to an 
initialized 
<a href="https://docs.microsoft.com/windows/desktop/ETW/event-trace-properties">EVENT_TRACE_PROPERTIES</a> structure. 

On input, the members must specify the new values for the properties to update. For information on which properties you can update, see Remarks.

On output, the structure members contains the updated settings and statistics for the event tracing session.


## -remarks



Controllers call this function.

On input, the members must specify the new values for the properties to update. You can update the following properties.

<table>
<tr>
<th>Member</th>
<th>Use</th>
</tr>
<tr>
<td><b>EnableFlags</b></td>
<td>Set this member to 0 to disable all kernel providers. Otherwise, you must specify the kernel providers that you want to enable or keep enabled. Applies only to NT Kernel Logger sessions.</td>
</tr>
<tr>
<td><b>FlushTimer</b></td>
<td>Set this member if you want to change the time to wait before flushing buffers. If this member is 0, the member is not updated.</td>
</tr>
<tr>
<td><b>LogFileNameOffset</b></td>
<td>Set this member if you want to switch to another log file. If this member is 0, the file name is not updated. If the offset is not zero and you do not change the log file name, the function returns an error.</td>
</tr>
<tr>
<td><b>LogFileMode</b></td>
<td>Set this member if you want to turn <b>EVENT_TRACE_REAL_TIME_MODE</b> on and off. To turn real time consuming off, set this member to 0. To turn real time consuming on, set this member to <b>EVENT_TRACE_REAL_TIME_MODE</b> and it will be OR'd with the current modes.</td>
</tr>
<tr>
<td><b>MaximumBuffers</b></td>
<td>Set set this member if you want to change the maximum number of buffers that ETW uses. If this member is 0, the member is not updated.</td>
</tr>
</table>
 

For private logger sessions, you can only update <b>LogFileNameOffset</b> and <b>FlushTimer</b>.

If you are using a newly initialized <a href="https://docs.microsoft.com/windows/desktop/ETW/event-trace-properties">EVENT_TRACE_PROPERTIES</a> structure, the only members you need to specify, other than the members you are updating, are <b>Wnode.BufferSize</b>, <b>Wnode.Guid</b>, and <b>Wnode.Flags</b>.

If you use the property structure you passed to <a href="https://docs.microsoft.com/windows/desktop/ETW/starttrace">StartTrace</a>, make sure the  <b>LogFileNameOffset</b> member is 0 unless you are changing the log file name.

If you call the <a href="https://docs.microsoft.com/windows/desktop/ETW/controltrace">ControlTrace</a> function to query the current session properties and then update those properties to update the session, make sure you set <b>LogFileNameOffset</b> to 0 (unless you are changing the log file name) and set <a href="https://docs.microsoft.com/windows/desktop/ETW/event-trace-properties">EVENT_TRACE_PROPERTIES.Wnode.Flags</a> to <b>WNODE_FLAG_TRACED_GUID</b>.

To obtain the property settings and session statistics for an event tracing session, call the 
<a href="https://docs.microsoft.com/windows/desktop/ETW/controltrace">ControlTrace</a> function.


#### Examples

For an example that uses 
<b>UpdateTrace</b>, see 
<a href="https://docs.microsoft.com/windows/desktop/ETW/updating-an-event-tracing-session">Updating an Event Tracing Session</a>.

<div class="code"></div>



## -see-also




<a href="https://docs.microsoft.com/windows/desktop/ETW/controltrace">ControlTrace</a>
 

 

