---
UID: NF:tdh.TdhCreatePayloadFilter
title: TdhCreatePayloadFilter function (tdh.h)
description: Creates a single filter for a single payload to be used with the EnableTraceEx2 function.
helpviewer_keywords: ["TdhCreatePayloadFilter","TdhCreatePayloadFilter function [ETW]","etw.tdhcreatepayloadfilter","tdh/TdhCreatePayloadFilter"]
old-location: etw\tdhcreatepayloadfilter.htm
tech.root: ETW
ms.assetid: B5132FF2-9DE3-40F3-82F0-90FE0640F646
ms.date: 12/05/2018
ms.keywords: TdhCreatePayloadFilter, TdhCreatePayloadFilter function [ETW], etw.tdhcreatepayloadfilter, tdh/TdhCreatePayloadFilter
req.header: tdh.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Tdh.lib
req.dll: Tdh.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - TdhCreatePayloadFilter
 - tdh/TdhCreatePayloadFilter
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Tdh.dll
 - Ext-MS-Win-Eventing-Tdh-Ext-L1-1-0.dll
api_name:
 - TdhCreatePayloadFilter
---

# TdhCreatePayloadFilter function


## -description

The <b>TdhCreatePayloadFilter</b> function  creates  a single filter for a single payload to be used with the <a href="/windows/desktop/ETW/enabletraceex2">EnableTraceEx2</a> function.

## -parameters

### -param ProviderGuid [in]

A GUID that identifies the manifest provider of the <i>EventDescriptor</i> parameter.

### -param EventDescriptor [in]

A pointer to the event descriptor whose payload will be filtered.

### -param EventMatchANY [in]

A Boolean value that indicates how events are handled when multiple conditions are specified.

When this parameter is <b>TRUE</b>, an event will be written to a session if any of
        the specified conditions specified in the filter are  <b>TRUE</b>.

When this parameter is <b>FALSE</b>, an event will be written to a session only if all of
        the specified conditions specified in the filter are  <b>TRUE</b>.

### -param PayloadPredicateCount [in]

The number of conditions specified in the filter.
        This value must be less than or equal to the <b>ETW_MAX_PAYLOAD_PREDICATES</b> constant defined in the <i>Tdh.h</i> header file.

### -param PayloadPredicates [in]

A pointer to an array of  <a href="/windows/desktop/api/tdh/ns-tdh-payload_filter_predicate">PAYLOAD_FILTER_PREDICATE</a> structures that contain the list conditions that the filter specifies.

### -param PayloadFilter [out]

On success, this parameter returns a pointer to a single payload filter that is properly sized and built for the specified conditions.

When the caller is finished using the returned payload filter with the <a href="/windows/desktop/ETW/enabletraceex2">EnableTraceEx2</a> function,  the <a href="/windows/desktop/api/tdh/nf-tdh-tdhdeletepayloadfilter">TdhDeletePayloadFilter</a> function should be called to free the allocated memory.

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
<dt><b>ERROR_FILE_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
The metadata for the provider was not found.

</td>
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
<dt><b>ERROR_INSUFFICIENT_BUFFER</b></dt>
</dl>
</td>
<td width="60%">
The resulting payload filter would not fit within
        the <b>MAX_EVENT_FILTER_PAYLOAD_SIZE</b> limit imposed by the <a href="/windows/desktop/ETW/enabletraceex2">EnableTraceEx2</a> function
        on the <a href="/windows/desktop/api/evntprov/ns-evntprov-event_filter_descriptor">EVENT_FILTER_DESCRIPTOR</a> structures in a payload.


</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NOT_ENOUGH_MEMORY</b></dt>
</dl>
</td>
<td width="60%">
Unable to allocate memory to create the payload filter.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
The schema information for supplied provider GUID was not found.

</td>
</tr>
</table>

## -remarks

On Windows 8.1,Windows Server 2012 R2, and later, event payload filters can be used by the <a href="/windows/desktop/ETW/enabletraceex2">EnableTraceEx2</a> function to filter on the specific content of  event in a logger session. 

The <b>TdhCreatePayloadFilter</b> function is used to create a single payload filter for a single payload to be used with the <a href="/windows/desktop/ETW/enabletraceex2">EnableTraceEx2</a> function.  The <b>TdhCreatePayloadFilter</b> allocates and fills in an opaque data structure for a single payload filter. When the payload filter is no longer needed, the <a href="/windows/desktop/api/tdh/nf-tdh-tdhdeletepayloadfilter">TdhDeletePayloadFilter</a> function is used to free memory allocated for a payload filter. 

For a single provider, multiple events can have distinct payload filters.  There can also be multiple filters for the same event, with a payload being passed to the session if any or all of the event's filters pass it.

The <a href="/windows/desktop/ETW/enabletraceex2">EnableTraceEx2</a> function takes an array of <a href="/windows/desktop/api/evntprov/ns-evntprov-event_filter_descriptor">EVENT_FILTER_DESCRIPTOR</a> structures in  the <a href="/windows/desktop/ETW/enable-trace-parameters">ENABLE_TRACE_PARAMETERS</a> structures passed in the <i>EnableParameters</i> parameter. There can only be one entry in the array for each event filter type. The <a href="/windows/desktop/api/tdh/nf-tdh-tdhaggregatepayloadfilters">TdhAggregatePayloadFilters</a> function can be used  to aggregate a list of  payload filters for a single provider created using the <b>TdhCreatePayloadFilter</b> into a single data structure and return an <b>EVENT_FILTER_DESCRIPTOR</b> for use with the <b>EnableTraceEx2</b> function.


#### Examples

For an example that uses 
the <b>TdhCreatePayloadFilter</b> function to create payload filters to use in filtering on specific conditions in a logger session, see 
the example for the <a href="/windows/desktop/ETW/enabletraceex2">EnableTraceEx2</a> function.

<div class="code"></div>

## -see-also
<a href="/windows/desktop/ETW/enable-trace-parameters">ENABLE_TRACE_PARAMETERS</a>



<a href="/windows/desktop/api/evntprov/ns-evntprov-event_descriptor">EVENT_DESCRIPTOR</a>



<a href="/windows/desktop/api/evntprov/ns-evntprov-event_filter_descriptor">EVENT_FILTER_DESCRIPTOR</a>



<a href="/windows/desktop/ETW/enabletraceex2">EnableTraceEx2</a>



<a href="/windows/desktop/api/tdh/ns-tdh-payload_filter_predicate">PAYLOAD_FILTER_PREDICATE</a>



<a href="/windows/desktop/api/tdh/nf-tdh-tdhaggregatepayloadfilters">TdhAggregatePayloadFilters</a>



<a href="/windows/desktop/api/tdh/nf-tdh-tdhcleanuppayloadeventfilterdescriptor">TdhCleanupPayloadEventFilterDescriptor</a>



<a href="/windows/desktop/api/tdh/nf-tdh-tdhdeletepayloadfilter">TdhDeletePayloadFilter</a>