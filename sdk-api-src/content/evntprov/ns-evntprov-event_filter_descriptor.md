---
UID: NS:evntprov._EVENT_FILTER_DESCRIPTOR
title: EVENT_FILTER_DESCRIPTOR (evntprov.h)
author: windows-sdk-content
description: Defines the filter data that a session passes to the provider's enable callback function.
old-location: etw\event_filter_descriptor.htm
tech.root: ETW
ms.assetid: 9318868a-29d8-4a5e-9579-c06a7c0fd78f
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: "*PEVENT_FILTER_DESCRIPTOR, EVENT_FILTER_DESCRIPTOR, EVENT_FILTER_DESCRIPTOR structure [ETW], EVENT_FILTER_TYPE_EVENT_ID, EVENT_FILTER_TYPE_EVENT_NAME, EVENT_FILTER_TYPE_EXECUTABLE_NAME, EVENT_FILTER_TYPE_NONE, EVENT_FILTER_TYPE_PACKAGE_APP_ID, EVENT_FILTER_TYPE_PACKAGE_ID, EVENT_FILTER_TYPE_PAYLOAD, EVENT_FILTER_TYPE_PID, EVENT_FILTER_TYPE_SCHEMATIZED, EVENT_FILTER_TYPE_STACKWALK, EVENT_FILTER_TYPE_STACKWALK_LEVEL_KW, EVENT_FILTER_TYPE_STACKWALK_NAME, EVENT_FILTER_TYPE_SYSTEM_FLAGS, EVENT_FILTER_TYPE_TRACEHANDLE, PEVENT_FILTER_DESCRIPTOR, PEVENT_FILTER_DESCRIPTOR structure pointer [ETW], _EVENT_FILTER_DESCRIPTOR, base.event_filter_descriptor, etw.event_filter_descriptor, evntprov/EVENT_FILTER_DESCRIPTOR, evntprov/PEVENT_FILTER_DESCRIPTOR"
ms.topic: struct
req.header: evntprov.h
req.include-header: 
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Evntprov.h
api_name:
 - EVENT_FILTER_DESCRIPTOR
product: Windows
targetos: Windows
req.typenames: EVENT_FILTER_DESCRIPTOR, *PEVENT_FILTER_DESCRIPTOR
req.redist: 
---

# EVENT_FILTER_DESCRIPTOR structure


## -description


The <b>EVENT_FILTER_DESCRIPTOR</b> structure defines the filter data that a session passes to the provider's enable callback function.


## -struct-fields




### -field Ptr

A pointer to the filter data for the filter type specified in the <b>Type</b> member. 

If the <b>Type</b> member is set to  <b>EVENT_FILTER_TYPE_PID</b>, the <b>Ptr</b> member points to an array of process IDs (PIDs). For other values of the <b>Type</b> member, the <b>Ptr</b> member points to a single structure or entry, not an array.

If the <b>Type</b> member is set to  <b>EVENT_FILTER_TYPE_EVENT_ID</b>, the <b>Ptr</b> member points to a <a href="https://msdn.microsoft.com/D660D140-BE86-44F6-B1D2-E1B97300BD11">EVENT_FILTER_EVENT_ID</a> structure that contains an array of event IDs and a Boolean value that determines whether tracing is enabled or disabled for the specified event IDs.

If the <b>Type</b> member is set to  <b>EVENT_FILTER_TYPE_STACKWALK</b>, the <b>Ptr</b> member points to a <a href="https://msdn.microsoft.com/D660D140-BE86-44F6-B1D2-E1B97300BD11">EVENT_FILTER_EVENT_ID</a> structure that contains an array of event IDs and a Boolean value that determines whether stack tracing is enabled or disabled for the specified event IDs.

If the <b>Type</b> member is set to  <b>EVENT_FILTER_TYPE_SCHEMATIZED</b>, see the <a href="https://msdn.microsoft.com/364a253d-f4c4-494a-af43-487c70912542">EVENT_FILTER_HEADER</a> structure for details on constructing the filter.


### -field Size

The size of the data, in bytes. 

The maximum data size limit varies based on the specified <b>Type</b> member (the type of the filter). The maximum data size, in bytes,  for many of the filter types is limited to <b>MAX_EVENT_FILTER_DATA_SIZE</b> defined in the <i>evntprov.h</i> header file to 1024.  


### -field Type

A provider-defined value that identifies the filter. For filters defined in an instrumentation  manifest, set this member to <b>EVENT_FILTER_TYPE_SCHEMATIZED</b>.

The possible values for this member are defined in the <i>Evntprov.h</i> header file.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="EVENT_FILTER_TYPE_NONE"></a><a id="event_filter_type_none"></a><dl>
<dt><b>EVENT_FILTER_TYPE_NONE</b></dt>
<dt>0x00000000</dt>
</dl>
</td>
<td width="60%">
No filters.

</td>
</tr>
<tr>
<td width="40%"><a id="EVENT_FILTER_TYPE_SCHEMATIZED"></a><a id="event_filter_type_schematized"></a><dl>
<dt><b>EVENT_FILTER_TYPE_SCHEMATIZED</b></dt>
<dt>0x80000000</dt>
</dl>
</td>
<td width="60%">
A schematized filter.

This is the traditional filtering setup also called provider-side filtering. The controller defines  a custom set of filters as a binary object that is passed to the provider in the <a href="https://msdn.microsoft.com/d75f18e1-e5fa-4039-bb74-76dea334b0fd">EnableTrace</a>, <a href="https://msdn.microsoft.com/1c675bf7-f292-49b1-8b60-720499a497fd">EnableTraceEx</a>, or <a href="https://msdn.microsoft.com/3aceffb6-614f-4cad-bbec-f181f0cbdbff">EnableTraceEx2</a> call. It is incumbent on the controller and provider to define and interpret these  filters and the controller should only log applicable events. This requires a close coupling of the controller and provider since the type and format of the binary object of what can be filtered is not defined. The <a href="https://msdn.microsoft.com/bc0f4286-1f6e-4d99-ad84-af8ab5dbba2b">TdhEnumerateProviderFilters</a> function can be used to retrieve the filters defined in a manifest.

For more information on schematized filters, see <a href="https://msdn.microsoft.com/b43912af-0e9c-414b-b3fa-03e7e35e493c">Defining Filters</a>. 

</td>
</tr>
<tr>
<td width="40%"><a id="EVENT_FILTER_TYPE_SYSTEM_FLAGS"></a><a id="event_filter_type_system_flags"></a><dl>
<dt><b>EVENT_FILTER_TYPE_SYSTEM_FLAGS</b></dt>
<dt>0x80000001</dt>
</dl>
</td>
<td width="60%">
Reserved for internal use.

</td>
</tr>
<tr>
<td width="40%"><a id="EVENT_FILTER_TYPE_TRACEHANDLE"></a><a id="event_filter_type_tracehandle"></a><dl>
<dt><b>EVENT_FILTER_TYPE_TRACEHANDLE</b></dt>
<dt>0x80000002</dt>
</dl>
</td>
<td width="60%">
Used to capture a rundown of a particular trace session. The <i>ControlCode</i> parameter passed to the <a href="https://msdn.microsoft.com/1c675bf7-f292-49b1-8b60-720499a497fd">EnableTraceEx</a> function must be set to  <b>EVENT_CONTROL_CODE_CAPTURE_STATE</b>  and the<i> ProviderId</i> parameter must be the  <b>SystemTraceControlGuid</b>.  The <b>EVENT_FILTER_DESCRIPTOR</b> structure should point to a single <b>TRACEHANDLE</b> that represents a current ETW session.  A rundown will be performed for that particular session.

</td>
</tr>
<tr>
<td width="40%"><a id="EVENT_FILTER_TYPE_PID"></a><a id="event_filter_type_pid"></a><dl>
<dt><b>EVENT_FILTER_TYPE_PID</b></dt>
<dt>0x80000004</dt>
</dl>
</td>
<td width="60%">
The process ID. This is one of the scope filters.

Filtering ETW events based on process IDs will result in an event stream (file or real-time) that contains the events from the providers in the specified processes only. It will only enable the provider in the processes whose PIDs are provided. The list of PIDs is the PIDs of the processes running at the time when <a href="https://msdn.microsoft.com/3aceffb6-614f-4cad-bbec-f181f0cbdbff">EnableTraceEx2</a> is called and will enable the provider in all the processes (for which PIDs are provided) at that particular time. The list of PIDs will not be stored in the session. So when a process is terminated and then reappears, the provider in it will not get automatically enabled to the trace session. The PIDs based filter-blob is only valid for a kernel mode logger session because the private logger session runs inside a user-mode process.

The maximum number of process IDs that can be filtered is  limited by <b>MAX_EVENT_FILTER_PID_COUNT</b> defined in the <i>evntprov.h</i> header file to 8.

In case a process ID filter is provided, then the provider will be enabled in the user-mode processes only. In case, the same provider is registered by a kernel-mode driver, it will not be enabled.

This is used with <a href="https://msdn.microsoft.com/2EEDB53B-75BC-48AC-A70D-9AEAED526C40">EVENT_TRACE_PROPERTIES_V2</a> for system wide private loggers.

</td>
</tr>
<tr>
<td width="40%"><a id="EVENT_FILTER_TYPE_EXECUTABLE_NAME"></a><a id="event_filter_type_executable_name"></a><dl>
<dt><b>EVENT_FILTER_TYPE_EXECUTABLE_NAME</b></dt>
<dt>0x80000008</dt>
</dl>
</td>
<td width="60%">
The executable file name. This is one of the scope filters.

This is used with <a href="https://msdn.microsoft.com/2EEDB53B-75BC-48AC-A70D-9AEAED526C40">EVENT_TRACE_PROPERTIES_V2</a> for system wide private loggers.

</td>
</tr>
<tr>
<td width="40%"><a id="EVENT_FILTER_TYPE_PACKAGE_ID"></a><a id="event_filter_type_package_id"></a><dl>
<dt><b>EVENT_FILTER_TYPE_PACKAGE_ID</b></dt>
<dt>0x80000010</dt>
</dl>
</td>
<td width="60%">
The package ID. This is one of the scope filters

This can be used to filter providers to events emitted from a particular Windows Store app package.

</td>
</tr>
<tr>
<td width="40%"><a id="EVENT_FILTER_TYPE_PACKAGE_APP_ID"></a><a id="event_filter_type_package_app_id"></a><dl>
<dt><b>EVENT_FILTER_TYPE_PACKAGE_APP_ID</b></dt>
<dt>0x80000020</dt>
</dl>
</td>
<td width="60%">
The package relative app ID (PRAID). This is one of the scope filters

This can be used to filter providers to events emitted from a particular Windows Store app package.

</td>
</tr>
<tr>
<td width="40%"><a id="EVENT_FILTER_TYPE_PAYLOAD"></a><a id="event_filter_type_payload"></a><dl>
<dt><b>EVENT_FILTER_TYPE_PAYLOAD</b></dt>
<dt>0x80000100</dt>
</dl>
</td>
<td width="60%">
The event payload (the content of the event).

The maximum data size, in bytes,  for an event payload filter is limited to <b>MAX_EVENT_FILTER_PAYLOAD_SIZE</b> defined in the <i>evntprov.h</i> header file to 4096.

</td>
</tr>
<tr>
<td width="40%"><a id="EVENT_FILTER_TYPE_EVENT_ID"></a><a id="event_filter_type_event_id"></a><dl>
<dt><b>EVENT_FILTER_TYPE_EVENT_ID</b></dt>
<dt>0x80000200</dt>
</dl>
</td>
<td width="60%">
The event ID.

This feature allows enabling or disabling filtering for a list of events. The provided filter includes a <a href="https://msdn.microsoft.com/D660D140-BE86-44F6-B1D2-E1B97300BD11">EVENT_FILTER_EVENT_ID</a> structure that contains an array of event IDs and a Boolean value that indicates whether to enable or disable from filtering for the specified events. Each event write call will go through this array quickly to find out whether enable or disable logging the event.


When applied to a TraceLogging provider this filter will be ignored as TraceLogging events do not have static event IDs.

The maximum number of event IDs allowed in the <a href="https://msdn.microsoft.com/D660D140-BE86-44F6-B1D2-E1B97300BD11">EVENT_FILTER_EVENT_ID</a> structure is limited by <b>MAX_EVENT_FILTER_EVENT_ID_COUNT</b> defined in the <i>evntprov.h</i> header file to 64.

</td>
</tr>
<tr>
<td width="40%"><a id="EVENT_FILTER_TYPE_EVENT_NAME"></a><a id="event_filter_type_event_name"></a><dl>
<dt><b>EVENT_FILTER_TYPE_EVENT_NAME</b></dt>
<dt>0x80000400</dt>
</dl>
</td>
<td width="60%">
The TraceLogging event name.

This feature allows enabling or disabling of TraceLogging events based on their names. The provided filter includes an <a href="https://msdn.microsoft.com/85E8C8F8-31D4-42F1-9267-15F74E473D57">EVENT_FILTER_EVENT_NAME</a> structure that contains an array of event names, keyword bitmasks, and level to filter on, and a Boolean value that indicates whether to enable or disable the described events. 
When applied to a non-TraceLogging provider, this filter is ignored as those events do not have names specified in their payload.

<div class="alert"><b>Note</b>  Available on Windows 10, version 1709 and later.</div>
<div> </div>
</td>
</tr>
<tr>
<td width="40%"><a id="EVENT_FILTER_TYPE_STACKWALK"></a><a id="event_filter_type_stackwalk"></a><dl>
<dt><b>EVENT_FILTER_TYPE_STACKWALK</b></dt>
<dt>0x80001000</dt>
</dl>
</td>
<td width="60%">
A stack walk.

When stack walking is enabled for a provider, then the stack is captured for all the events generated by the provider. Most of the time, the user is only interested in stack from only certain number of events. 

This feature allows enabling or disabling stack walking on a list of events. The provided filter includes a <a href="https://msdn.microsoft.com/D660D140-BE86-44F6-B1D2-E1B97300BD11">EVENT_FILTER_EVENT_ID</a> structure that contains an array of event IDs and a Boolean value that indicates whether to enable or disable stack capturing for the specified events. Each event write call will go through this array quickly to find out whether the stack should be captured or not.


When applied to a TraceLogging provider, this filter will be ignored as TraceLogging events do not have static event IDs.

If you choose to use this filter, you still must specify <b>EVENT_ENABLE_PROPERTY_STACK_TRACE</b> in the <a href="https://msdn.microsoft.com/bc7cf886-f763-428a-9e75-031e8df26554">ENABLE_TRACE_PARAMETERS</a> structure when enabling the provider for any stacks to be collected from a provider.

The maximum number of event IDs allowed in the <a href="https://msdn.microsoft.com/D660D140-BE86-44F6-B1D2-E1B97300BD11">EVENT_FILTER_EVENT_ID</a> structure is limited by <b>MAX_EVENT_FILTER_EVENT_ID_COUNT</b> defined in the <i>evntprov.h</i> header file to 64.

<div class="alert"><b>Note</b>  Available on Windows 10, version 1709 and later.</div>
<div> </div>
</td>
</tr>
<tr>
<td width="40%"><a id="EVENT_FILTER_TYPE_STACKWALK_NAME"></a><a id="event_filter_type_stackwalk_name"></a><dl>
<dt><b>EVENT_FILTER_TYPE_STACKWALK_NAME</b></dt>
<dt>0x80002000</dt>
</dl>
</td>
<td width="60%">
A TraceLogging event name.

This feature allows filtering of stack collection for TraceLogging events based on the event names. The provided filter includes an <a href="https://msdn.microsoft.com/85E8C8F8-31D4-42F1-9267-15F74E473D57">EVENT_FILTER_EVENT_NAME</a> structure that contains an array of event names, keyword bitmasks, and level to filter on, and a Boolean value that indicates whether to collect stacks or not for the described events.
 


When applied to a non-TraceLogging provider, this filter is ignored as those events do not have names specified in their payload.

If you choose to use this filter, you still must specify <b>EVENT_ENABLE_PROPERTY_STACK_TRACE</b> on the <a href="https://msdn.microsoft.com/bc7cf886-f763-428a-9e75-031e8df26554">ENABLE_TRACE_PARAMETERS</a> structure when enabling the provider for any stacks to be collected from a provider at all.

<div class="alert"><b>Note</b>  Available on Windows 10, version 1709 and later.</div>
<div> </div>
</td>
</tr>
<tr>
<td width="40%"><a id="EVENT_FILTER_TYPE_STACKWALK_LEVEL_KW"></a><a id="event_filter_type_stackwalk_level_kw"></a><dl>
<dt><b>EVENT_FILTER_TYPE_STACKWALK_LEVEL_KW</b></dt>
<dt>0x80004000</dt>
</dl>
</td>
<td width="60%">
Event level and keyword.

This feature allows filtering of stack collection for events based on their level and keyword. The provided filter includes an <a href="https://msdn.microsoft.com/2FE25C55-8028-4894-9DD8-FC997B7D9ADB">EVENT_FILTER_LEVEL_KW</a> 
structure that contains keyword bitmasks and level to filter on, as well as a Boolean value that indicates whether to collect stacks or not for the described events.
 


If you choose to use this filter, you still must specify <b>EVENT_ENABLE_PROPERTY_STACK_TRACE</b> on the <a href="https://msdn.microsoft.com/bc7cf886-f763-428a-9e75-031e8df26554">ENABLE_TRACE_PARAMETERS</a> structure when enabling the provider for any stacks to be collected from a provider at all.



<div class="alert"><b>Note</b>  Available on Windows 10, version 1709 and later.</div>
<div> </div>
</td>
</tr>
</table>
 


## -remarks



The provider determines the layout of the data and its purpose.

On Windows 8.1,Windows Server 2012 R2, and later, event payload, scope, and stack walk filters can be used by the <a href="https://msdn.microsoft.com/3aceffb6-614f-4cad-bbec-f181f0cbdbff">EnableTraceEx2</a> function and the <a href="https://msdn.microsoft.com/bc7cf886-f763-428a-9e75-031e8df26554">ENABLE_TRACE_PARAMETERS</a> and <b>EVENT_FILTER_DESCRIPTOR</b> structures to filter on specific conditions in a logger session. For more information on event payload filters, see the <b>EnableTraceEx2</b>, <a href="https://msdn.microsoft.com/B5132FF2-9DE3-40F3-82F0-90FE0640F646">TdhCreatePayloadFilter</a>, and <a href="https://msdn.microsoft.com/B9093E64-1796-4AF2-AB45-84F278813B66">TdhAggregatePayloadFilters</a> functions and the <b>ENABLE_TRACE_PARAMETERS</b> and <a href="https://msdn.microsoft.com/6B8C03C9-2936-4FEE-AEF4-ABC368B1CB75">PAYLOAD_FILTER_PREDICATE</a> structures. 




## -see-also




<a href="https://msdn.microsoft.com/b43912af-0e9c-414b-b3fa-03e7e35e493c">Defining Filters</a>



<a href="https://msdn.microsoft.com/bc7cf886-f763-428a-9e75-031e8df26554">ENABLE_TRACE_PARAMETERS</a>



<a href="https://msdn.microsoft.com/D660D140-BE86-44F6-B1D2-E1B97300BD11">EVENT_FILTER_EVENT_ID</a>



<a href="https://msdn.microsoft.com/f339323e-9da9-495f-aac5-f44969a018eb">EnableCallback</a>



<a href="https://msdn.microsoft.com/d75f18e1-e5fa-4039-bb74-76dea334b0fd">EnableTrace</a>



<a href="https://msdn.microsoft.com/1c675bf7-f292-49b1-8b60-720499a497fd">EnableTraceEx</a>



<a href="https://msdn.microsoft.com/3aceffb6-614f-4cad-bbec-f181f0cbdbff">EnableTraceEx2</a>



<a href="https://msdn.microsoft.com/6B8C03C9-2936-4FEE-AEF4-ABC368B1CB75">PAYLOAD_FILTER_PREDICATE</a>



<a href="https://msdn.microsoft.com/B9093E64-1796-4AF2-AB45-84F278813B66">TdhAggregatePayloadFilters</a>



<a href="https://msdn.microsoft.com/B5132FF2-9DE3-40F3-82F0-90FE0640F646">TdhCreatePayloadFilter</a>
 

 

