---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# TdhAggregatePayloadFilters function


## -description


The <b>TdhAggregatePayloadFilters</b> function aggregates multiple payload filters for a single provider into a single data structure for use with the <a href="https://msdn.microsoft.com/3aceffb6-614f-4cad-bbec-f181f0cbdbff">EnableTraceEx2</a> function.  


## -parameters




### -param PayloadFilterCount

The count of payload filters.


### -param PayloadFilterPtrs

An array of event payload single filters,
        each created by a call to the <a href="https://msdn.microsoft.com/B5132FF2-9DE3-40F3-82F0-90FE0640F646">TdhCreatePayloadFilter</a>  function.



### -param EventMatchALLFlags

TBD


### -param EventFilterDescriptor [out]

A pointer to an <a href="https://msdn.microsoft.com/9318868a-29d8-4a5e-9579-c06a7c0fd78f">EVENT_FILTER_DESCRIPTOR</a> structure to be used with the <a href="https://msdn.microsoft.com/3aceffb6-614f-4cad-bbec-f181f0cbdbff">EnableTraceEx2</a> function.  The <b>EVENT_FILTER_DESCRIPTOR</b> structure will
        contain a pointer to the aggregated payload filters, which have been
        allocated by this function.  

When the caller is finished using this
        <a href="https://msdn.microsoft.com/9318868a-29d8-4a5e-9579-c06a7c0fd78f">EVENT_FILTER_DESCRIPTOR</a> structure with the <a href="https://msdn.microsoft.com/3aceffb6-614f-4cad-bbec-f181f0cbdbff">EnableTraceEx2</a> function,  the  <a href="https://msdn.microsoft.com/AA08AFD5-EC1A-44BF-9BCB-EEA69A959853">TdhCleanupPayloadEventFilterDescriptor</a>  function should be called to free the allocated memory.



#### - EventMatchAllFlags [in, optional]

An array of Boolean values  that correspond to
        each payload filter passed in the <i>PayloadFilterPtrs</i> parameter and indicates how events are handled when multiple conditions are specified..  This parameter only affects situations where multiple
        payload filters are being specified for the same event.  

When a Boolean value is <b>TRUE</b>, an event will be written to a session if any of
        the specified conditions specified in the filter are  <b>TRUE</b>. If this flag is set to <b>TRUE</b> on one or more filters for
        the same event Id or event version, then the event is only written if all
        the flagged filters for the event are satisfied.


When a Boolean value is <b>FALSE</b>, an event will be written to a session only if all of
        the specified conditions specified in the filter are  <b>TRUE</b>. If this flag is set to <b>FALSE</b> on one or more filters for
        the same event Id or event version, then the event is written if any of
        the non-flagged filters are satisfied.



## -returns



Returns <b>ERROR_SUCCESS</b> if successful. Otherwise, this function returns one of the following return codes in addition to others.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
One or more of the parameters is not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NOT_ENOUGH_MEMORY</b></dt>
</dl>
</td>
<td width="60%">
Unable to allocate memory to create the aggregated payload filter.

</td>
</tr>
</table>
 




## -remarks



On Windows 8.1,Windows Server 2012 R2, and later, event payload filters can be used by the <a href="https://msdn.microsoft.com/3aceffb6-614f-4cad-bbec-f181f0cbdbff">EnableTraceEx2</a> function to filter on the specific content of the event in a logger session. 

The <b>TdhAggregatePayloadFilters</b> function aggregates payload filters for a single provider into a single data structure for use with the <a href="https://msdn.microsoft.com/3aceffb6-614f-4cad-bbec-f181f0cbdbff">EnableTraceEx2</a> function. The <b>TdhAggregatePayloadFilters</b> allocates and fills in an opaque data structure for an aggregated payload filter. When the aggregated payload filter is no longer needed, the <a href="https://msdn.microsoft.com/AA08AFD5-EC1A-44BF-9BCB-EEA69A959853">TdhCleanupPayloadEventFilterDescriptor</a> function is used to free memory allocated for the aggregated  payload filter in the  <a href="https://msdn.microsoft.com/9318868a-29d8-4a5e-9579-c06a7c0fd78f">EVENT_FILTER_DESCRIPTOR</a> structure returned.


#### Examples

For an example that uses 
the <b>TdhAggregatePayloadFilters</b> function to aggregate payload filters to use in filtering on specific conditions in a logger session, see 
the example for the <a href="https://msdn.microsoft.com/3aceffb6-614f-4cad-bbec-f181f0cbdbff">EnableTraceEx2</a> function.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/bc7cf886-f763-428a-9e75-031e8df26554">ENABLE_TRACE_PARAMETERS</a>



<a href="https://msdn.microsoft.com/9318868a-29d8-4a5e-9579-c06a7c0fd78f">EVENT_FILTER_DESCRIPTOR</a>



<a href="https://msdn.microsoft.com/3aceffb6-614f-4cad-bbec-f181f0cbdbff">EnableTraceEx2</a>



<a href="https://msdn.microsoft.com/AA08AFD5-EC1A-44BF-9BCB-EEA69A959853">TdhCleanupPayloadEventFilterDescriptor</a>



<a href="https://msdn.microsoft.com/B5132FF2-9DE3-40F3-82F0-90FE0640F646">TdhCreatePayloadFilter</a>



<a href="https://msdn.microsoft.com/50EB6A11-54AE-4D90-ABA4-13D8EADA1955">TdhDeletePayloadFilter</a>
 

 

