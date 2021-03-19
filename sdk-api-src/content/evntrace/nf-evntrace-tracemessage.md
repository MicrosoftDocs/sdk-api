---
UID: NF:evntrace.TraceMessage
title: TraceMessage function (evntrace.h)
description: The TraceMessage function sends an informational message to an event tracing session.
helpviewer_keywords: ["PVOID","TRACE_MESSAGE_COMPONENTID","TRACE_MESSAGE_GUID","TRACE_MESSAGE_SEQUENCE","TRACE_MESSAGE_SYSTEMINFO","TRACE_MESSAGE_TIMESTAMP","TraceMessage","TraceMessage function [ETW]","_evt_tracemessage","base.tracemessage","etw.tracemessage","evntrace/TraceMessage","size_t"]
old-location: etw\tracemessage.htm
tech.root: ETW
ms.assetid: 5d81c851-d47e-43f8-97b0-87156f36119a
ms.date: 12/05/2018
ms.keywords: PVOID, TRACE_MESSAGE_COMPONENTID, TRACE_MESSAGE_GUID, TRACE_MESSAGE_SEQUENCE, TRACE_MESSAGE_SYSTEMINFO, TRACE_MESSAGE_TIMESTAMP, TraceMessage, TraceMessage function [ETW], _evt_tracemessage, base.tracemessage, etw.tracemessage, evntrace/TraceMessage, size_t
req.header: evntrace.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2003 [desktop apps \| UWP apps]
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
 - TraceMessage
 - evntrace/TraceMessage
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
 - API-MS-Win-eventing-classicprovider-l1-1-0.dll
api_name:
 - TraceMessage
---

# TraceMessage function


## -description

The 
<b>TraceMessage</b> function sends an informational message to an event tracing session.

## -parameters

### -param LoggerHandle [in]

Handle to the event tracing session that records the event. The provider obtains the handle when it calls the <a href="/windows/desktop/ETW/gettraceloggerhandle">GetTraceLoggerHandle</a> function in its <a href="/windows/desktop/ETW/controlcallback">ControlCallback</a> implementation.

### -param MessageFlags [in]

Adds additional information to the beginning of the provider-specific data section of the event. The provider-specific data section of the event will contain data only for those flags that are set. The variable list of argument data will follow this information. This parameter can be one or more of the following values. 



<table>
<tr>
<th>Flag</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="TRACE_MESSAGE_COMPONENTID"></a><a id="trace_message_componentid"></a><dl>
<dt><b>TRACE_MESSAGE_COMPONENTID</b></dt>
</dl>
</td>
<td width="60%">
 Include the component identifier in the message. The <i>MessageGuid</i> parameter contains the component identifier.

</td>
</tr>
<tr>
<td width="40%"><a id="TRACE_MESSAGE_GUID"></a><a id="trace_message_guid"></a><dl>
<dt><b>TRACE_MESSAGE_GUID</b></dt>
</dl>
</td>
<td width="60%">
Include the event trace class GUID in the message. The <i>MessageGuid</i> parameter contains the event trace class  GUID.

</td>
</tr>
<tr>
<td width="40%"><a id="TRACE_MESSAGE_SEQUENCE"></a><a id="trace_message_sequence"></a><dl>
<dt><b>TRACE_MESSAGE_SEQUENCE</b></dt>
</dl>
</td>
<td width="60%">
Include a sequence number in the message. The sequence number starts at one. To use this flag, the controller must have set the <b>EVENT_TRACE_USE_GLOBAL_SEQUENCE</b> or <b>EVENT_TRACE_USE_LOCAL_SEQUENCE</b> log file mode when creating the session.

</td>
</tr>
<tr>
<td width="40%"><a id="TRACE_MESSAGE_SYSTEMINFO"></a><a id="trace_message_systeminfo"></a><dl>
<dt><b>TRACE_MESSAGE_SYSTEMINFO</b></dt>
</dl>
</td>
<td width="60%">
Include the thread identifier and process identifier in the message.

</td>
</tr>
<tr>
<td width="40%"><a id="TRACE_MESSAGE_TIMESTAMP"></a><a id="trace_message_timestamp"></a><dl>
<dt><b>TRACE_MESSAGE_TIMESTAMP</b></dt>
</dl>
</td>
<td width="60%">
Include a time stamp in the message.

</td>
</tr>
</table>
 

<b>TRACE_MESSAGE_COMPONENTID</b> and <b>TRACE_MESSAGE_GUID</b> are mutually exclusive.

The information is included in the event data in the following order:

<ul>
<li>Sequence number</li>
<li>Event trace class GUID (or component identifier)</li>
<li>Time stamp</li>
<li>Thread identifier</li>
<li>Process identifier</li>
</ul>

### -param MessageGuid [in]

Class GUID or component ID that identifies the message. Depends if <i>MessageFlags</i> contains the <b>TRACE_MESSAGE_COMPONENTID</b> or <b>TRACE_MESSAGE_GUID</b> flag.

### -param MessageNumber [in]

Number that uniquely identifies each occurrence of the message. You must define the value specified for this parameter; the value should be meaningful to the application.

### -param ...

A list of variable arguments to be appended to the message. Use this list to specify your provider-specific event data. The list must be composed of pairs of arguments, as described in the following table. 



<table>
<tr>
<th>Data Type</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="PVOID"></a><a id="pvoid"></a><dl>
<dt><b>PVOID</b></dt>
</dl>
</td>
<td width="60%">
Pointer to the argument data.

</td>
</tr>
<tr>
<td width="40%"><a id="size_t"></a><a id="SIZE_T"></a><dl>
<dt><b>size_t</b></dt>
</dl>
</td>
<td width="60%">
The size of the argument data, in bytes.

</td>
</tr>
</table>
 

Terminate the list using an argument pair consisting of a pointer to <b>NULL</b> and zero.
						

The caller must ensure that the sum of the sizes of the arguments + 72 does not exceed the size of the event tracing session's buffer.

## -returns

If the function succeeds, the return value is ERROR_SUCCESS.
						

If the function fails, the return value is one of the 
<a href="/windows/desktop/Debug/system-error-codes">system error codes</a>. The following table includes some common errors and their causes.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_HANDLE</b></dt>
</dl>
</td>
<td width="60%">
Either the <i>SessionHandle</i> is <b>NULL</b> or specifies the NT Kernel Logger session handle.
							

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NOT_ENOUGH_MEMORY</b></dt>
</dl>
</td>
<td width="60%">
The session ran out of free buffers to write to. This can occur during high event rates because the disk subsystem is overloaded or the number of buffers is too small. Rather than blocking until more buffers become available, <a href="/windows/desktop/ETW/tracemessage">TraceMessage</a> discards the event.

<b>Windows 2000 and Windows XP:  </b>Not supported.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
The event is discarded because, although the buffer pool has not reached its maximum size, there is insufficient available memory to allocate an additional buffer and there is no buffer available to receive the event. 

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
<i>MessageFlags</i> contains a value that is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_MORE_DATA</b></dt>
</dl>
</td>
<td width="60%">
Data from a single event cannot span multiple buffers. A trace event is limited to the size of the event tracing session's buffer minus the size of the  
<a href="/windows/desktop/ETW/event-trace-header">EVENT_TRACE_HEADER</a> structure. 

</td>
</tr>
</table>

## -remarks

Providers call this function.

Using the <a href="/windows/desktop/ETW/traceevent">TraceEvent</a> function is the preferred way to log an event. On Windows Vista, you should use the <a href="/windows/desktop/api/evntprov/nf-evntprov-eventwrite">EventWrite</a> function to log events.

The trace events are written in the order in which they occur. 

If you need to access message tracing functionality from a wrapper function, call the 
<a href="/windows/desktop/ETW/tracemessageva">TraceMessageVa</a> version of this function.

Consumers will have to use the <a href="/windows/desktop/ETW/eventcallback">EventCallback</a> callback to receive and process the events if the <i>MessageFlags</i> parameter does not contain the TRACE_MESSAGE_GUID flag. If you do not specify the TRACE_MESSAGE_GUID flag, the consumer will not be able to use the <a href="/windows/desktop/ETW/eventclasscallback">EventClassCallback</a> because the <b>Header.Guid</b> member of the   <a href="/windows/desktop/ETW/event-trace">EVENT_TRACE</a> structure will not contain the event trace class GUID.

Note that the members of the <a href="/windows/desktop/ETW/event-trace">EVENT_TRACE</a> and <a href="/windows/desktop/ETW/event-trace-header">EVENT_TRACE_HEADER</a> structures that correspond to the <i>MessageFlags</i> flags are set only if the corresponding flag is specified. For example, the <b>ThreadId</b> and <b>ProcessId</b> members of <b>EVENT_TRACE_HEADER</b> are populated only if you specify the TRACE_MESSAGE_SYSTEMINFO flag.

## -see-also

<a href="/windows/desktop/ETW/traceevent">TraceEvent</a>



<a href="/windows/desktop/ETW/traceeventinstance">TraceEventInstance</a>



<a href="/windows/desktop/ETW/tracemessageva">TraceMessageVa</a>

