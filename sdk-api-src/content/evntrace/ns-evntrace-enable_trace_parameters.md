---
UID: NS:evntrace._ENABLE_TRACE_PARAMETERS
title: ENABLE_TRACE_PARAMETERS (evntrace.h)
description: Defines the information used to enable a provider.
helpviewer_keywords: ["*PENABLE_TRACE_PARAMETERS","ENABLE_TRACE_PARAMETERS","ENABLE_TRACE_PARAMETERS structure [ETW]","EVENT_ENABLE_PROPERTY_EVENT_KEY","EVENT_ENABLE_PROPERTY_EXCLUDE_INPRIVATE","EVENT_ENABLE_PROPERTY_IGNORE_KEYWORD_0","EVENT_ENABLE_PROPERTY_PROCESS_START_KEY","EVENT_ENABLE_PROPERTY_PROVIDER_GROUP","EVENT_ENABLE_PROPERTY_SID","EVENT_ENABLE_PROPERTY_STACK_TRACE","EVENT_ENABLE_PROPERTY_TS_ID","PENABLE_TRACE_PARAMETERS","PENABLE_TRACE_PARAMETERS structure pointer [ETW]","_ENABLE_TRACE_PARAMETERS","etw.enable_trace_parameters","evntrace/ENABLE_TRACE_PARAMETERS","evntrace/PENABLE_TRACE_PARAMETERS"]
old-location: etw\enable_trace_parameters.htm
tech.root: ETW
ms.assetid: bc7cf886-f763-428a-9e75-031e8df26554
ms.date: 12/05/2018
ms.keywords: '*PENABLE_TRACE_PARAMETERS, ENABLE_TRACE_PARAMETERS, ENABLE_TRACE_PARAMETERS structure [ETW], EVENT_ENABLE_PROPERTY_EVENT_KEY, EVENT_ENABLE_PROPERTY_EXCLUDE_INPRIVATE, EVENT_ENABLE_PROPERTY_IGNORE_KEYWORD_0, EVENT_ENABLE_PROPERTY_PROCESS_START_KEY, EVENT_ENABLE_PROPERTY_PROVIDER_GROUP, EVENT_ENABLE_PROPERTY_SID, EVENT_ENABLE_PROPERTY_STACK_TRACE, EVENT_ENABLE_PROPERTY_TS_ID, PENABLE_TRACE_PARAMETERS, PENABLE_TRACE_PARAMETERS structure pointer [ETW], _ENABLE_TRACE_PARAMETERS, etw.enable_trace_parameters, evntrace/ENABLE_TRACE_PARAMETERS, evntrace/PENABLE_TRACE_PARAMETERS'
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
targetos: Windows
req.typenames: ENABLE_TRACE_PARAMETERS, *PENABLE_TRACE_PARAMETERS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _ENABLE_TRACE_PARAMETERS
 - evntrace/_ENABLE_TRACE_PARAMETERS
 - PENABLE_TRACE_PARAMETERS
 - evntrace/PENABLE_TRACE_PARAMETERS
 - ENABLE_TRACE_PARAMETERS
 - evntrace/ENABLE_TRACE_PARAMETERS
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
 - ENABLE_TRACE_PARAMETERS
---

# ENABLE_TRACE_PARAMETERS structure


## -description

The <b>ENABLE_TRACE_PARAMETERS</b> structure defines the information used to enable a provider.

## -struct-fields

### -field Version

Set to <b>ENABLE_TRACE_PARAMETERS_VERSION_2</b>.

### -field EnableProperty

Optional settings that ETW can include when writing the event. Some settings write extra data to the <a href="/windows/desktop/api/evntcons/ns-evntcons-event_header_extended_data_item">extended data item</a> section of each event. Other settings refine which events will be included. To use these optional settings, specify one or more of the following flags; otherwise, set to zero.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="EVENT_ENABLE_PROPERTY_IGNORE_KEYWORD_0"></a><a id="event_enable_property_ignore_keyword_0"></a><dl>
<dt><b>EVENT_ENABLE_PROPERTY_IGNORE_KEYWORD_0</b></dt>
</dl>
</td>
<td width="60%">
Filters out all events that do not have a non-zero keyword specified.

Supported on Windows 10, version 1507 and later. This is also supported on Windows 8.1 and Windows 7 with SP1 via a patch.

</td>
</tr>
<tr>
<td width="40%"><a id="EVENT_ENABLE_PROPERTY_PROVIDER_GROUP"></a><a id="event_enable_property_provider_group"></a><dl>
<dt><b>EVENT_ENABLE_PROPERTY_PROVIDER_GROUP</b></dt>
</dl>
</td>
<td width="60%">
Indicates that this call to <a href="/windows/desktop/ETW/enabletraceex2">EnableTraceEx2</a> should enable a <a href="/windows/desktop/ETW/provider-traits">Provider Group</a> rather than an individual Event Provider.

Supported on Windows 10, version 1507 and later. This is also supported on Windows 8.1 and Windows 7 with SP1 via a patch.

</td>
</tr>
<tr>
<td width="40%"><a id="EVENT_ENABLE_PROPERTY_PROCESS_START_KEY"></a><a id="event_enable_property_process_start_key"></a><dl>
<dt><b>EVENT_ENABLE_PROPERTY_PROCESS_START_KEY</b></dt>
</dl>
</td>
<td width="60%">
Include the Process Start Key in the extended data.

The Process Start Key is a sequence number that identifies the process. While the Process ID may be reused within a session, the Process Start Key is guaranteed uniqueness in the current boot session.

Supported on Windows 10, version 1507 and later. This is also supported on Windows 8.1 and Windows 7 with SP1 via a patch.

</td>
</tr>
<tr>
<td width="40%"><a id="EVENT_ENABLE_PROPERTY_EVENT_KEY"></a><a id="event_enable_property_event_key"></a><dl>
<dt><b>EVENT_ENABLE_PROPERTY_EVENT_KEY</b></dt>
</dl>
</td>
<td width="60%">
Include the Event Key in the extended data.

The Event Key is a unique identifier for the event instance that will be constant across multiple trace sessions listening to this event. It can be used to correlate simultaneous trace sessions.

Supported on Windows 10, version 1507 and later.

</td>
</tr>
<tr>
<td width="40%"><a id="EVENT_ENABLE_PROPERTY_EXCLUDE_INPRIVATE"></a><a id="event_enable_property_exclude_inprivate"></a><dl>
<dt><b>EVENT_ENABLE_PROPERTY_EXCLUDE_INPRIVATE</b></dt>
</dl>
</td>
<td width="60%">
Filters out all events that are either marked as an InPrivate event or come from a process that is marked as InPrivate.

InPrivate implies that the event or process contains some data that would be considered private or personal. It is up to the process or event to designate itself as InPrivate for this to work.

Supported on Windows 10, version 1507 and later.

</td>
</tr>
<tr>
<td width="40%"><a id="EVENT_ENABLE_PROPERTY_SID"></a><a id="event_enable_property_sid"></a><dl>
<dt><b>EVENT_ENABLE_PROPERTY_SID</b></dt>
</dl>
</td>
<td width="60%">
Include in the extended data the security identifier (SID) of the user.

Supported on Windows Vista and later.

</td>
</tr>
<tr>
<td width="40%"><a id="EVENT_ENABLE_PROPERTY_TS_ID"></a><a id="event_enable_property_ts_id"></a><dl>
<dt><b>EVENT_ENABLE_PROPERTY_TS_ID</b></dt>
</dl>
</td>
<td width="60%">
Include in the extended data the terminal session identifier.

Supported on Windows Vista and later.

</td>
</tr>
<tr>
<td width="40%"><a id="EVENT_ENABLE_PROPERTY_STACK_TRACE"></a><a id="event_enable_property_stack_trace"></a><dl>
<dt><b>EVENT_ENABLE_PROPERTY_STACK_TRACE</b></dt>
</dl>
</td>
<td width="60%">
Include in the extended data a call stack trace for events written using <a href="/windows/desktop/api/evntprov/nf-evntprov-eventwrite">EventWrite</a>.

If you set <b>EVENT_ENABLE_PROPERTY_STACK_TRACE</b>, ETW will drop the event if the total event size exceeds 64K. If the provider is logging events close in size to 64K maximum, it is possible that enabling stack capture will cause the event to be lost.

If the stack is longer than the maximum number of frames (192), the frames will be cut from the bottom of the stack.

For consumers,  the events will include the <a href="/windows/win32/api/evntcons/ns-evntcons-event_extended_item_stack_trace64">EVENT_EXTENDED_ITEM_STACK_TRACE32</a> or <a href="/windows/desktop/api/evntcons/ns-evntcons-event_extended_item_stack_trace64">EVENT_EXTENDED_ITEM_STACK_TRACE64</a> extended item. Note that on 64-bit computers, 32-bit processes will receive 64-bit stack traces.

Supported on Windows 7 and later.

</td>
</tr>
</table>

### -field ControlFlags

Reserved. Set to 0.

### -field SourceId

A GUID that uniquely identifies the session that is enabling or disabling the provider. If the provider does not implement <a href="/windows/desktop/api/evntprov/nc-evntprov-penablecallback">EnableCallback</a>, the GUID is not used.

### -field EnableFilterDesc

A pointer to an array of <a href="/windows/desktop/api/evntprov/ns-evntprov-event_filter_descriptor">EVENT_FILTER_DESCRIPTOR</a> structures that points to the filter data. The number of elements in the array is specified in the <b>FilterDescCount</b> member. There can only be one filter for a specific filter type as specified by the <b>Type</b> member of the <b>EVENT_FILTER_DESCRIPTOR</b> structure. 

For a schematized filter (a <b>Type</b> member equal to <b>EVENT_FILTER_TYPE_SCHEMATIZED</b>), the provider uses filter data to prevent events that match the filter criteria from being written to the session. The provider determines the layout of the data and how it applies the filter to the event's data. A session can pass only one schematized filter to the provider.

A session can call the <a href="/windows/desktop/api/tdh/nf-tdh-tdhenumerateproviderfilters">TdhEnumerateProviderFilters</a> function to determine the schematized filters that it can pass to the provider.

### -field FilterDescCount

The number of elements (filters) in the <a href="/windows/desktop/api/evntprov/ns-evntprov-event_filter_descriptor">EVENT_FILTER_DESCRIPTOR</a> array pointed to by <b>EnableFilterDesc</b> member. 

The <b>FilterDescCount</b>  member should match the number of <a href="/windows/desktop/api/evntprov/ns-evntprov-event_filter_descriptor">EVENT_FILTER_DESCRIPTOR</a> structures in the array pointed to by the <b>EnableFilterDesc</b> member.

.

## -remarks

The <b>ENABLE_TRACE_PARAMETERS</b> structure is a version 2 structure and replaces the <a href="/windows/desktop/ETW/enable-trace-parameters-v1">ENABLE_TRACE_PARAMETERS_V1</a> structure for use with the <a href="/windows/desktop/ETW/enabletraceex2">EnableTraceEx2</a> function.

On Windows 8.1,Windows Server 2012 R2, and later, event payload , scope, and stack walk filters can be used by the <a href="/windows/desktop/ETW/enabletraceex2">EnableTraceEx2</a> function and the <b>ENABLE_TRACE_PARAMETERS</b> and <a href="/windows/desktop/api/evntprov/ns-evntprov-event_filter_descriptor">EVENT_FILTER_DESCRIPTOR</a> structures to filter on specific conditions in a logger session. For more information on event payload filters, see the <b>EnableTraceEx2</b>, <a href="/windows/desktop/api/tdh/nf-tdh-tdhcreatepayloadfilter">TdhCreatePayloadFilter</a>, and <a href="/windows/desktop/api/tdh/nf-tdh-tdhaggregatepayloadfilters">TdhAggregatePayloadFilters</a> functions and the <b>EVENT_FILTER_DESCRIPTOR</b> and <a href="/windows/desktop/api/tdh/ns-tdh-payload_filter_predicate">PAYLOAD_FILTER_PREDICATE</a> structures. 

Typically, on 64-bit computers, you cannot capture the kernel stack in certain contexts when page faults are not allowed. To enable walking the kernel stack on x64, set the <b>DisablePagingExecutive</b> Memory Management registry value to 1. The <b>DisablePagingExecutive</b> registry value is located under the following registry key:<b>HKEY_LOCAL_MACHINE\System\CurrentControlSet\Control\Session Manager\Memory Management</b></p>You should consider the cost of setting this registry value before doing so.

## -see-also

<a href="/windows/desktop/ETW/enable-trace-parameters-v1">ENABLE_TRACE_PARAMETERS_V1</a>



<a href="/windows/desktop/api/evntprov/ns-evntprov-event_filter_descriptor">EVENT_FILTER_DESCRIPTOR</a>



<a href="/windows/desktop/api/evntprov/ns-evntprov-event_filter_event_id">EVENT_FILTER_EVENT_ID</a>



<a href="/windows/desktop/ETW/enabletraceex2">EnableTraceEx2</a>



<a href="/windows/desktop/api/tdh/ns-tdh-payload_filter_predicate">PAYLOAD_FILTER_PREDICATE</a>



<a href="/windows/desktop/api/tdh/nf-tdh-tdhaggregatepayloadfilters">TdhAggregatePayloadFilters</a>



<a href="/windows/desktop/api/tdh/nf-tdh-tdhcreatepayloadfilter">TdhCreatePayloadFilter</a>



<a href="/windows/desktop/api/tdh/nf-tdh-tdhenumerateproviderfilters">TdhEnumerateProviderFilters</a>