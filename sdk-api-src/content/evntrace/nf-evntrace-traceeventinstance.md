---
UID: NF:evntrace.TraceEventInstance
title: TraceEventInstance function
author: windows-sdk-content
description: The TraceEventInstance function sends an event to an event tracing session. The event uses an instance identifier to associate the event with a transaction. This function may also be used to trace hierarchical relationships between related events.
old-location: etw\traceeventinstance.htm
tech.root: etw
ms.assetid: e8361bdc-21dd-47a0-bdbf-56f4d6195689
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: TraceEventInstance, TraceEventInstance function [ETW], _evt_traceeventinstance, base.traceeventinstance, etw.traceeventinstance, evntrace/TraceEventInstance
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
api_name:
 - TraceEventInstance
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# TraceEventInstance function


## -description


The 
<b>TraceEventInstance</b> function sends an event to an event tracing session. The event uses an instance identifier to associate the event with a transaction. This function may also be used to trace hierarchical relationships between related events. 
			
		


## -parameters




### -param TraceHandle [in]

Handle to the event tracing session that records the event instance. The provider obtains the handle when it calls the <a href="https://msdn.microsoft.com/050d3a01-0087-40f1-af35-b9ceeaf47813">GetTraceLoggerHandle</a> function in its <a href="https://msdn.microsoft.com/e9f70ae6-906f-4e55-bca7-4355f1ca6091">ControlCallback</a> implementation.


### -param EventTrace [in]

Pointer to an 
<a href="https://msdn.microsoft.com/2a79d937-2a3b-4426-b31f-a1a3ce86a334">EVENT_INSTANCE_HEADER</a> structure. Event-specific data is optionally appended to the structure. The largest event you can log is 64K. You must specify values for the following members of the 
<b>EVENT_INSTANCE_HEADER</b> structure. 



<ul>
<li><b>Size</b></li>
<li><b>Flags</b></li>
<li><b>RegHandle</b></li>
</ul>
Depending on the complexity of the information your provider provides, you should also consider specifying values for the following members.

<ul>
<li><b>Class.Type</b></li>
<li><b>Class.Level</b></li>
</ul>
To trace hierarchical relationships between related events, also set the <b>ParentRegHandle</b> member.


### -param InstInfo [in]

Pointer to an 
<a href="https://msdn.microsoft.com/83a3802c-b992-43a2-a98a-bdee2ecfef24">EVENT_INSTANCE_INFO</a> structure, which contains the registration handle for this event trace class and the instance identifier. Use the  <a href="https://msdn.microsoft.com/ab890392-f1e4-4b4e-a46c-8c7c2bfd3897">CreateTraceInstanceId</a> function to initialize the structure.


### -param ParentInstInfo [in]

Pointer to an 
<a href="https://msdn.microsoft.com/83a3802c-b992-43a2-a98a-bdee2ecfef24">EVENT_INSTANCE_INFO</a> structure, which contains the registration handle for the parent event trace class and its instance identifier. Use the  <a href="https://msdn.microsoft.com/ab890392-f1e4-4b4e-a46c-8c7c2bfd3897">CreateTraceInstanceId</a> function to initialize the structure. Set to <b>NULL</b> if you are not tracing a hierarchical relationship.


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
<dt><b>ERROR_INVALID_FLAGS</b></dt>
</dl>
</td>
<td width="60%">
The <b>Flags</b> member of the 
<a href="https://msdn.microsoft.com/2a79d937-2a3b-4426-b31f-a1a3ce86a334">EVENT_INSTANCE_HEADER</a> does not contain <b>WNODE_FLAG_TRACED_GUID</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
There was insufficient memory to complete the function call. The causes for this error code are described in the following Remarks section.

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
<li><i>EventTrace</i> is <b>NULL</b>.</li>
<li><i>pInstInfo</i> is <b>NULL</b>.</li>
<li>The members of <i>pInstInfo</i> are <b>NULL</b>.</li>
<li><i>SessionHandle</i> is <b>NULL</b>.</li>
<li>The <b>Size</b> member of the 
<a href="https://msdn.microsoft.com/2a79d937-2a3b-4426-b31f-a1a3ce86a334">EVENT_INSTANCE_HEADER</a> is incorrect.</li>
</ul>
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
<dt><b>ERROR_MORE_DATA</b></dt>
</dl>
</td>
<td width="60%">
Data from a single event cannot span multiple buffers. A trace event is limited to the size of the event tracing session's buffer minus the size of the  
<a href="https://msdn.microsoft.com/2a79d937-2a3b-4426-b31f-a1a3ce86a334">EVENT_INSTANCE_HEADER</a> structure. 

</td>
</tr>
</table>
 




## -remarks



Providers call this function.

Before the provider can call this function, the  provider 

<ul>
<li>Must call the 
<a href="https://msdn.microsoft.com/c9158292-281b-4a02-b280-956e340d225c">RegisterTraceGuids</a> function to register itself and the event trace class.</li>
<li>Must call the <a href="https://msdn.microsoft.com/ab890392-f1e4-4b4e-a46c-8c7c2bfd3897">CreateTraceInstanceId</a> function to  create an instance identifier for the registered event trace class.</li>
<li>Must be enabled. A controller calls the 
<a href="https://msdn.microsoft.com/d75f18e1-e5fa-4039-bb74-76dea334b0fd">EnableTrace</a> function to enable a provider.</li>
</ul>
The event is either written to a log file, sent to event trace consumers in real time, or both. The <b>LogFileMode</b> member of the 
<a href="https://msdn.microsoft.com/0c967971-8df1-4679-a8a9-a783f5b35860">EVENT_TRACE_PROPERTIES</a> structure passed to the 
<a href="https://msdn.microsoft.com/c040514a-733d-44b9-8300-a8341d2630b3">StartTrace</a> defines where the event is sent.

The trace events are written in the order in which they occur. 

To trace unrelated events, use the 
<a href="https://msdn.microsoft.com/9b21f6f0-dd9b-4f9c-a879-846901a3bab7">TraceEvent</a> function.

<b>Windows XP:  </b>Does not work correctly.


#### Examples

For an example of generating related sets of events using 
<a href="https://msdn.microsoft.com/ab890392-f1e4-4b4e-a46c-8c7c2bfd3897">CreateTraceInstanceId</a> and 
<b>TraceEventInstance</b>, see 
<a href="https://msdn.microsoft.com/246e9443-3120-49bf-a6e3-64dddba348fa">Tracing Event Instances</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/ab890392-f1e4-4b4e-a46c-8c7c2bfd3897">CreateTraceInstanceId</a>



<a href="https://msdn.microsoft.com/2a79d937-2a3b-4426-b31f-a1a3ce86a334">EVENT_INSTANCE_HEADER</a>



<a href="https://msdn.microsoft.com/83a3802c-b992-43a2-a98a-bdee2ecfef24">EVENT_INSTANCE_INFO</a>



<a href="https://msdn.microsoft.com/c9158292-281b-4a02-b280-956e340d225c">RegisterTraceGuids</a>



<a href="https://msdn.microsoft.com/9b21f6f0-dd9b-4f9c-a879-846901a3bab7">TraceEvent</a>
 

 

