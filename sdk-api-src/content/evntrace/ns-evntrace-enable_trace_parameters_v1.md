---
UID: NS:evntrace._ENABLE_TRACE_PARAMETERS_V1
title: ENABLE_TRACE_PARAMETERS_V1 (evntrace.h)
description: Defines the information used to enable a provider.
old-location: etw\enable_trace_parameters_v1.htm
tech.root: ETW
ms.assetid: 6FC5EF54-2D05-4246-A8E8-7FDA0ABA0D4B
ms.date: 12/05/2018
ms.keywords: '*PENABLE_TRACE_PARAMETERS_V1, ENABLE_TRACE_PARAMETERS_V1, ENABLE_TRACE_PARAMETERS_V1 structure [ETW], EVENT_ENABLE_PROPERTY_SID, EVENT_ENABLE_PROPERTY_STACK_TRACE, EVENT_ENABLE_PROPERTY_TS_ID, PENABLE_TRACE_PARAMETERS_V1, PENABLE_TRACE_PARAMETERS_V1 structure pointer [ETW], _ENABLE_TRACE_PARAMETERS_V1, etw.enable_trace_parameters_v1, evntrace/ENABLE_TRACE_PARAMETERS_V1, evntrace/PENABLE_TRACE_PARAMETERS_V1'
ms.topic: struct
f1_keywords:
- evntrace/ENABLE_TRACE_PARAMETERS_V1
dev_langs:
- c++
req.header: evntrace.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
- Evntrace.h
api_name:
- ENABLE_TRACE_PARAMETERS_V1
targetos: Windows
req.typenames: ENABLE_TRACE_PARAMETERS_V1, *PENABLE_TRACE_PARAMETERS_V1
req.redist: 
ms.custom: 19H1
---

# ENABLE_TRACE_PARAMETERS_V1 structure


## -description


The <b>ENABLE_TRACE_PARAMETERS_V1</b> structure defines the information used to enable a provider.


## -struct-fields




### -field Version

Set to <b>ENABLE_TRACE_PARAMETERS_VERSION</b>.


### -field EnableProperty

Optional information that ETW can include when writing the event. The data is written to the <a href="https://docs.microsoft.com/windows/desktop/api/evntcons/ns-evntcons-event_header_extended_data_item">extended data item</a> section of the event. To include the optional information, specify one or more of the following flags; otherwise, set to zero.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="EVENT_ENABLE_PROPERTY_SID"></a><a id="event_enable_property_sid"></a><dl>
<dt><b>EVENT_ENABLE_PROPERTY_SID</b></dt>
</dl>
</td>
<td width="60%">
Include in the extended data the security identifier (SID) of the user.

</td>
</tr>
<tr>
<td width="40%"><a id="EVENT_ENABLE_PROPERTY_TS_ID"></a><a id="event_enable_property_ts_id"></a><dl>
<dt><b>EVENT_ENABLE_PROPERTY_TS_ID</b></dt>
</dl>
</td>
<td width="60%">
Include in the extended data the terminal session identifier.

</td>
</tr>
<tr>
<td width="40%"><a id="EVENT_ENABLE_PROPERTY_STACK_TRACE"></a><a id="event_enable_property_stack_trace"></a><dl>
<dt><b>EVENT_ENABLE_PROPERTY_STACK_TRACE</b></dt>
</dl>
</td>
<td width="60%">
Include in the extended data a call stack trace for events written using <a href="https://docs.microsoft.com/windows/desktop/api/evntprov/nf-evntprov-eventwrite">EventWrite</a>.

If you set <b>EVENT_ENABLE_PROPERTY_STACK_TRACE</b>, ETW will drop the event if the total event size exceeds 64K. If the provider is logging events close in size to 64K maximum, it is possible that enabling stack capture will cause the event to be lost.

If the stack is longer than the maximum number of frames (192), the frames will be cut from the bottom of the stack.

For consumers,  the events will include the <a href="https://docs.microsoft.com/windows/win32/api/evntcons/ns-evntcons-event_extended_item_stack_trace64">EVENT_EXTENDED_ITEM_STACK_TRACE32</a> or <a href="https://docs.microsoft.com/windows/desktop/api/evntcons/ns-evntcons-event_extended_item_stack_trace64">EVENT_EXTENDED_ITEM_STACK_TRACE64</a> extended item. Note that on 64-bit computers, 32-bit processes will receive 64-bit stack traces.

</td>
</tr>
</table>
 


### -field ControlFlags

Reserved. Set to 0.


### -field SourceId

A GUID that uniquely identifies the session that is enabling or disabling the provider. If the provider does not implement <a href="https://docs.microsoft.com/windows/desktop/api/evntprov/nc-evntprov-penablecallback">EnableCallback</a>, the GUID is not used.


### -field EnableFilterDesc

An <a href="https://docs.microsoft.com/windows/desktop/api/evntprov/ns-evntprov-event_filter_descriptor">EVENT_FILTER_DESCRIPTOR</a> structure that points to the filter data. The provider uses filter data to prevent events that match the filter criteria from being written to the session. The provider determines the layout of the data and how it applies the filter to the event's data. A session can pass only one filter to the provider.

A session can call the <a href="https://docs.microsoft.com/windows/desktop/api/tdh/nf-tdh-tdhenumerateproviderfilters">TdhEnumerateProviderFilters</a> function to determine the schematized filters that it can pass to the provider.


## -remarks



The <b>ENABLE_TRACE_PARAMETERS_V1</b> structure  is used with the <a href="https://docs.microsoft.com/windows/desktop/ETW/enabletrace">EnableTrace</a> and <a href="https://docs.microsoft.com/windows/desktop/ETW/enabletraceex-func">EnableTraceEx</a> functions. The <a href="https://docs.microsoft.com/windows/desktop/ETW/enable-trace-parameters">ENABLE_TRACE_PARAMETERS</a> structure is a version 2 structure and replaces the <b>ENABLE_TRACE_PARAMETERS_V1</b> structure for use with the <a href="https://docs.microsoft.com/windows/desktop/ETW/enabletraceex2">EnableTraceEx2</a> function.

Typically, on 64-bit computers, you cannot capture the kernel stack in certain contexts when page faults are not allowed. To enable walking the kernel stack on x64, set the <b>DisablePagingExecutive</b> Memory Management registry value to 1. The <b>DisablePagingExecutive</b> registry value is located under the following registry key:<b>HKEY_LOCAL_MACHINE\System\CurrentControlSet\Control\Session Manager\Memory Management</b></p>You should consider the cost of setting this registry value before doing so.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/ETW/enable-trace-parameters">ENABLE_TRACE_PARAMETERS</a>



<a href="https://docs.microsoft.com/windows/desktop/api/evntprov/ns-evntprov-event_filter_descriptor">EVENT_FILTER_DESCRIPTOR</a>



<a href="https://docs.microsoft.com/windows/desktop/ETW/enabletrace">EnableTrace</a>



<a href="https://docs.microsoft.com/windows/desktop/ETW/enabletraceex-func">EnableTraceEx</a>



<a href="https://docs.microsoft.com/windows/desktop/ETW/enabletraceex2">EnableTraceEx2</a>
 

 

