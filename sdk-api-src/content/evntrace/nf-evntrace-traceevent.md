---
UID: NF:evntrace.TraceEvent
title: TraceEvent function (evntrace.h)
description: The TraceEvent function sends an event to an event tracing session.
helpviewer_keywords: ["TraceEvent","TraceEvent function [ETW]","_evt_traceevent","base.traceevent","etw.traceevent","evntrace/TraceEvent"]
old-location: etw\traceevent.htm
tech.root: ETW
ms.assetid: 9b21f6f0-dd9b-4f9c-a879-846901a3bab7
ms.date: 12/05/2018
ms.keywords: TraceEvent, TraceEvent function [ETW], _evt_traceevent, base.traceevent, etw.traceevent, evntrace/TraceEvent
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
req.lib: Advapi32.lib
req.dll: Advapi32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - TraceEvent
 - evntrace/TraceEvent
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
 - API-MS-Win-eventing-classicprovider-l1-1-0.dll
api_name:
 - TraceEvent
---

# TraceEvent function


## -description

The 
<b>TraceEvent</b> function sends an event to an event tracing session.

## -parameters

### -param TraceHandle [in]

Handle to the event tracing session that records the event. The provider obtains the handle when it calls the <a href="https://docs.microsoft.com/windows/desktop/ETW/gettraceloggerhandle">GetTraceLoggerHandle</a> function in its <a href="https://docs.microsoft.com/windows/desktop/ETW/controlcallback">ControlCallback</a> implementation.

### -param EventTrace [in]

Pointer to an 
<a href="https://docs.microsoft.com/windows/desktop/ETW/event-trace-header">EVENT_TRACE_HEADER</a> structure. Event-specific data is optionally appended to the structure. The largest event you can log is 64K. You must specify values for the following members of the 
<b>EVENT_TRACE_HEADER</b> structure. 



<ul>
<li><b>Size</b></li>
<li><b>Guid</b> or <b>GuidPtr</b></li>
<li><b>Flags</b></li>
</ul>
Depending on the complexity of the information your provider provides, you should also consider specifying values for the following members.

<ul>
<li><b>Class.Type</b></li>
<li><b>Class.Level</b></li>
</ul>

## -returns

If the function succeeds, the return value is ERROR_SUCCESS.

If the function fails, the return value is one of the 
<a href="https://docs.microsoft.com/windows/desktop/Debug/system-error-codes">system error codes</a>. The following table includes some common errors and their causes.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_FLAG_NUMBER</b></dt>
</dl>
</td>
<td width="60%">
The <b>Flags</b> member of the 
<a href="https://docs.microsoft.com/windows/desktop/ETW/event-trace-header">EVENT_TRACE_HEADER</a> structure is incorrect.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_HANDLE</b></dt>
</dl>
</td>
<td width="60%">
<i>SessionHandle</i> is not valid or specifies the NT Kernel Logger session handle.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NOT_ENOUGH_MEMORY</b></dt>
</dl>
</td>
<td width="60%">
The session ran out of free buffers to write to. This can occur during high event rates because the disk subsystem is overloaded or the number of buffers is too small. Rather than blocking until more buffers become available, <a href="https://docs.microsoft.com/windows/desktop/ETW/traceevent">TraceEvent</a> discards the event. 

Consider increasing the number and size of the buffers for the session, or reducing the number of events written or the size of the events.

<b>Windows 2000:  </b>Not supported.

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
One of the following is true:

<ul>
<li><i>SessionHandle</i> is <b>NULL</b>.</li>
<li><i>EventTrace</i> is <b>NULL</b>.</li>
<li>The <b>Size</b> member of the 
<a href="https://docs.microsoft.com/windows/desktop/ETW/event-trace-header">EVENT_TRACE_HEADER</a> structure is incorrect.</li>
</ul>
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
<a href="https://docs.microsoft.com/windows/desktop/ETW/event-trace-header">EVENT_TRACE_HEADER</a> structure. 

</td>
</tr>
</table>

## -remarks

Providers call this function.

Before the provider can call this function, the  provider 

<ul>
<li>Must call the 
<a href="https://docs.microsoft.com/windows/desktop/ETW/registertraceguids">RegisterTraceGuids</a> function to register itself and the event trace class.</li>
<li>Must be enabled. A controller calls the 
<a href="https://docs.microsoft.com/windows/desktop/ETW/enabletrace">EnableTrace</a> function to enable a provider.</li>
</ul>
The event is either written to a log file, sent to event trace consumers in real time, or both. The <b>LogFileMode</b> member of the 
<a href="https://docs.microsoft.com/windows/desktop/ETW/event-trace-properties">EVENT_TRACE_PROPERTIES</a> structure passed to the 
<a href="https://docs.microsoft.com/windows/desktop/ETW/starttrace">StartTrace</a> defines where the event is sent.

The trace events are written in the order in which they occur. 

To trace a set of related events, use the 
<a href="https://docs.microsoft.com/windows/desktop/ETW/traceeventinstance">TraceEventInstance</a> function.

 On Windows Vista, you should use the <a href="https://docs.microsoft.com/windows/desktop/api/evntprov/nf-evntprov-eventwrite">EventWrite</a> function to log events.


#### Examples

For an example that uses 
<b>TraceEvent</b>, see 
<a href="https://docs.microsoft.com/windows/desktop/ETW/tracing-events">Tracing Events</a>.

<div class="code"></div>

## -see-also

<a href="https://docs.microsoft.com/windows/desktop/ETW/event-trace-header">EVENT_TRACE_HEADER</a>



<a href="https://docs.microsoft.com/windows/desktop/ETW/enabletrace">EnableTrace</a>



<a href="https://docs.microsoft.com/windows/desktop/ETW/registertraceguids">RegisterTraceGuids</a>



<a href="https://docs.microsoft.com/windows/desktop/ETW/traceeventinstance">TraceEventInstance</a>

