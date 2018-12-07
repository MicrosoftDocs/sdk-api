---
UID: NS:evntrace._ENABLE_TRACE_PARAMETERS_V1
title: "_ENABLE_TRACE_PARAMETERS_V1"
author: windows-sdk-content
description: Defines the information used to enable a provider.
old-location: etw\enable_trace_parameters_v1.htm
tech.root: etw
ms.assetid: 6FC5EF54-2D05-4246-A8E8-7FDA0ABA0D4B
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: "*PENABLE_TRACE_PARAMETERS_V1, ENABLE_TRACE_PARAMETERS_V1, ENABLE_TRACE_PARAMETERS_V1 structure [ETW], EVENT_ENABLE_PROPERTY_SID, EVENT_ENABLE_PROPERTY_STACK_TRACE, EVENT_ENABLE_PROPERTY_TS_ID, PENABLE_TRACE_PARAMETERS_V1, PENABLE_TRACE_PARAMETERS_V1 structure pointer [ETW], _ENABLE_TRACE_PARAMETERS_V1, etw.enable_trace_parameters_v1, evntrace/ENABLE_TRACE_PARAMETERS_V1, evntrace/PENABLE_TRACE_PARAMETERS_V1"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
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
product: Windows
targetos: Windows
req.typenames: ENABLE_TRACE_PARAMETERS_V1, *PENABLE_TRACE_PARAMETERS_V1
req.redist: 
---

# _ENABLE_TRACE_PARAMETERS_V1 structure


## -description


The <b>ENABLE_TRACE_PARAMETERS_V1</b> structure defines the information used to enable a provider.


## -struct-fields




### -field Version

Set to <b>ENABLE_TRACE_PARAMETERS_VERSION</b>.


### -field EnableProperty

Optional information that ETW can include when writing the event. The data is written to the <a href="https://msdn.microsoft.com/130dc14b-7488-48ab-a31d-310c0f4ee13f">extended data item</a> section of the event. To include the optional information, specify one or more of the following flags; otherwise, set to zero.

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
Include in the extended data a call stack trace for events written using <a href="https://msdn.microsoft.com/93070eb7-c167-4419-abff-e861877dad07">EventWrite</a>.

If you set <b>EVENT_ENABLE_PROPERTY_STACK_TRACE</b>, ETW will drop the event if the total event size exceeds 64K. If the provider is logging events close in size to 64K maximum, it is possible that enabling stack capture will cause the event to be lost.

If the stack is longer than the maximum number of frames (192), the frames will be cut from the bottom of the stack.

For consumers,  the events will include the <a href="https://msdn.microsoft.com/6898951a-5719-47aa-a219-97f82095686f">EVENT_EXTENDED_ITEM_STACK_TRACE32</a> or <a href="https://msdn.microsoft.com/3c9e0dcb-1eb9-4c9f-a4c8-5a93566be303">EVENT_EXTENDED_ITEM_STACK_TRACE64</a> extended item. Note that on 64-bit computers, 32-bit processes will receive 64-bit stack traces.

</td>
</tr>
</table>
 


### -field ControlFlags

Reserved. Set to 0.


### -field SourceId

A GUID that uniquely identifies the session that is enabling or disabling the provider. If the provider does not implement <a href="https://msdn.microsoft.com/f339323e-9da9-495f-aac5-f44969a018eb">EnableCallback</a>, the GUID is not used.


### -field EnableFilterDesc

An <a href="https://msdn.microsoft.com/9318868a-29d8-4a5e-9579-c06a7c0fd78f">EVENT_FILTER_DESCRIPTOR</a> structure that points to the filter data. The provider uses filter data to prevent events that match the filter criteria from being written to the session. The provider determines the layout of the data and how it applies the filter to the event's data. A session can pass only one filter to the provider.

A session can call the <a href="https://msdn.microsoft.com/bc0f4286-1f6e-4d99-ad84-af8ab5dbba2b">TdhEnumerateProviderFilters</a> function to determine the schematized filters that it can pass to the provider.


## -remarks



The <b>ENABLE_TRACE_PARAMETERS_V1</b> structure  is used with the <a href="https://msdn.microsoft.com/d75f18e1-e5fa-4039-bb74-76dea334b0fd">EnableTrace</a> and <a href="https://msdn.microsoft.com/1c675bf7-f292-49b1-8b60-720499a497fd">EnableTraceEx</a> functions. The <a href="https://msdn.microsoft.com/bc7cf886-f763-428a-9e75-031e8df26554">ENABLE_TRACE_PARAMETERS</a> structure is a version 2 structure and replaces the <b>ENABLE_TRACE_PARAMETERS_V1</b> structure for use with the <a href="https://msdn.microsoft.com/3aceffb6-614f-4cad-bbec-f181f0cbdbff">EnableTraceEx2</a> function.

Typically, on 64-bit computers, you cannot capture the kernel stack in certain contexts when page faults are not allowed. To enable walking the kernel stack on x64, set the <b>DisablePagingExecutive</b> Memory Management registry value to 1. The <b>DisablePagingExecutive</b> registry value is located under the following registry key:<b>HKEY_LOCAL_MACHINE\System\CurrentControlSet\Control\Session Manager\Memory Management</b></p>You should consider the cost of setting this registry value before doing so.




## -see-also




<a href="https://msdn.microsoft.com/bc7cf886-f763-428a-9e75-031e8df26554">ENABLE_TRACE_PARAMETERS</a>



<a href="https://msdn.microsoft.com/9318868a-29d8-4a5e-9579-c06a7c0fd78f">EVENT_FILTER_DESCRIPTOR</a>



<a href="https://msdn.microsoft.com/d75f18e1-e5fa-4039-bb74-76dea334b0fd">EnableTrace</a>



<a href="https://msdn.microsoft.com/1c675bf7-f292-49b1-8b60-720499a497fd">EnableTraceEx</a>



<a href="https://msdn.microsoft.com/3aceffb6-614f-4cad-bbec-f181f0cbdbff">EnableTraceEx2</a>
 

 

