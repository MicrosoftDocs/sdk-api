---
UID: NF:evntrace.TraceEvent
title: TraceEvent function
author: windows-sdk-content
description: The TraceEvent function sends an event to an event tracing session.
old-location: etw\traceevent.htm
tech.root: ETW
ms.assetid: 9b21f6f0-dd9b-4f9c-a879-846901a3bab7
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: TraceEvent, TraceEvent function [ETW], _evt_traceevent, base.traceevent, etw.traceevent, evntrace/TraceEvent
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# TraceEvent function


## -description


The 
<b>TraceEvent</b> function sends an event to an event tracing session. 


## -parameters




### -param TraceHandle

TBD


### -param EventTrace [in]

Pointer to an 
<a href="https://msdn.microsoft.com/33c2de6b-afc2-4323-8d81-2970e66edf5e">EVENT_TRACE_HEADER</a> structure. Event-specific data is optionally appended to the structure. The largest event you can log is 64K. You must specify values for the following members of the 
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

#### - SessionHandle [in]

Handle to the event tracing session that records the event. The provider obtains the handle when it calls the <a href="https://msdn.microsoft.com/050d3a01-0087-40f1-af35-b9ceeaf47813">GetTraceLoggerHandle</a> function in its <a href="https://msdn.microsoft.com/e9f70ae6-906f-4e55-bca7-4355f1ca6091">ControlCallback</a> implementation.


## -returns



If the function succeeds, the return value is ERROR_SUCCESS.

If the function fails, the return value is one of the 
<a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">system error codes</a>. The following table includes some common errors and their causes.

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
<a href="https://msdn.microsoft.com/33c2de6b-afc2-4323-8d81-2970e66edf5e">EVENT_TRACE_HEADER</a> structure is incorrect.

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
The session ran out of free buffers to write to. This can occur during high event rates because the disk subsystem is overloaded or the number of buffers is too small. Rather than blocking until more buffers become available, <a href="https://msdn.microsoft.com/9b21f6f0-dd9b-4f9c-a879-846901a3bab7">TraceEvent</a> discards the event. 

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
<a href="https://msdn.microsoft.com/33c2de6b-afc2-4323-8d81-2970e66edf5e">EVENT_TRACE_HEADER</a> structure is incorrect.</li>
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
<a href="https://msdn.microsoft.com/33c2de6b-afc2-4323-8d81-2970e66edf5e">EVENT_TRACE_HEADER</a> structure. 

</td>
</tr>
</table>
 




## -remarks



Providers call this function.

Before the provider can call this function, the  provider 

<ul>
<li>Must call the 
<a href="https://msdn.microsoft.com/c9158292-281b-4a02-b280-956e340d225c">RegisterTraceGuids</a> function to register itself and the event trace class.</li>
<li>Must be enabled. A controller calls the 
<a href="https://msdn.microsoft.com/d75f18e1-e5fa-4039-bb74-76dea334b0fd">EnableTrace</a> function to enable a provider.</li>
</ul>
The event is either written to a log file, sent to event trace consumers in real time, or both. The <b>LogFileMode</b> member of the 
<a href="https://msdn.microsoft.com/0c967971-8df1-4679-a8a9-a783f5b35860">EVENT_TRACE_PROPERTIES</a> structure passed to the 
<a href="https://msdn.microsoft.com/c040514a-733d-44b9-8300-a8341d2630b3">StartTrace</a> defines where the event is sent.

The trace events are written in the order in which they occur. 

To trace a set of related events, use the 
<a href="https://msdn.microsoft.com/e8361bdc-21dd-47a0-bdbf-56f4d6195689">TraceEventInstance</a> function.

 On Windows Vista, you should use the <a href="https://msdn.microsoft.com/93070eb7-c167-4419-abff-e861877dad07">EventWrite</a> function to log events.


#### Examples

For an example that uses 
<b>TraceEvent</b>, see 
<a href="https://msdn.microsoft.com/21f62b5d-0a2d-468c-af88-2fab1512f0ec">Tracing Events</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/33c2de6b-afc2-4323-8d81-2970e66edf5e">EVENT_TRACE_HEADER</a>



<a href="https://msdn.microsoft.com/d75f18e1-e5fa-4039-bb74-76dea334b0fd">EnableTrace</a>



<a href="https://msdn.microsoft.com/c9158292-281b-4a02-b280-956e340d225c">RegisterTraceGuids</a>



<a href="https://msdn.microsoft.com/e8361bdc-21dd-47a0-bdbf-56f4d6195689">TraceEventInstance</a>
 

 

