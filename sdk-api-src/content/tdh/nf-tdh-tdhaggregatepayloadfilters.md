---
UID: NF:tdh.TdhAggregatePayloadFilters
title: TdhAggregatePayloadFilters function (tdh.h)
description: Aggregates multiple payload filters for a single provider into a single data structure for use with the EnableTraceEx2 function.
helpviewer_keywords: ["TdhAggregatePayloadFilters","TdhAggregatePayloadFilters function [ETW]","etw.tdhaggregatepayloadfilters","tdh/TdhAggregatePayloadFilters"]
old-location: etw\tdhaggregatepayloadfilters.htm
tech.root: ETW
ms.assetid: B9093E64-1796-4AF2-AB45-84F278813B66
ms.date: 12/05/2018
ms.keywords: TdhAggregatePayloadFilters, TdhAggregatePayloadFilters function [ETW], etw.tdhaggregatepayloadfilters, tdh/TdhAggregatePayloadFilters
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
 - TdhAggregatePayloadFilters
 - tdh/TdhAggregatePayloadFilters
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
 - TdhAggregatePayloadFilters
---

# TdhAggregatePayloadFilters function

## -description

The <b>TdhAggregatePayloadFilters</b> function aggregates multiple payload filters for a single provider into a single data structure for use with the <a href="/windows/desktop/ETW/enabletraceex2">EnableTraceEx2</a> function.

## -parameters

### -param PayloadFilterCount

The count of payload filters.

### -param PayloadFilterPtrs

An array of event payload single filters, each created by a call to the <a href="/windows/desktop/api/tdh/nf-tdh-tdhcreatepayloadfilter">TdhCreatePayloadFilter</a>  function.

### -param EventMatchALLFlags [in, optional]

An array of Boolean values  that correspond to each payload filter passed in the <i>PayloadFilterPtrs</i> parameter and indicates how events are handled when multiple conditions are specified..  This parameter only affects situations where multiple payload filters are being specified for the same event.  

When a Boolean value is <b>TRUE</b>, an event will be written to a session if any of the specified conditions specified in the filter are  <b>TRUE</b>. If this flag is set to <b>TRUE</b> on one or more filters for the same event Id or event version, then the event is only written if all the flagged filters for the event are satisfied.

When a Boolean value is <b>FALSE</b>, an event will be written to a session only if all of the specified conditions specified in the filter are  <b>TRUE</b>. If this flag is set to <b>FALSE</b> on one or more filters for the same event Id or event version, then the event is written if any of the non-flagged filters are satisfied.

### -param EventFilterDescriptor [out]

A pointer to an <a href="/windows/desktop/api/evntprov/ns-evntprov-event_filter_descriptor">EVENT_FILTER_DESCRIPTOR</a> structure to be used with the <a href="/windows/desktop/ETW/enabletraceex2">EnableTraceEx2</a> function.  The <b>EVENT_FILTER_DESCRIPTOR</b> structure will contain a pointer to the aggregated payload filters, which have been allocated by this function.  

When the caller is finished using this <a href="/windows/desktop/api/evntprov/ns-evntprov-event_filter_descriptor">EVENT_FILTER_DESCRIPTOR</a> structure with the <a href="/windows/desktop/ETW/enabletraceex2">EnableTraceEx2</a> function,  the  <a href="/windows/desktop/api/tdh/nf-tdh-tdhcleanuppayloadeventfilterdescriptor">TdhCleanupPayloadEventFilterDescriptor</a>  function should be called to free the allocated memory.

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

On Windows 8.1,Windows Server 2012 R2, and later, event payload filters can be used by the <a href="/windows/desktop/ETW/enabletraceex2">EnableTraceEx2</a> function to filter on the specific content of the event in a logger session. 

The <b>TdhAggregatePayloadFilters</b> function aggregates payload filters for a single provider into a single data structure for use with the <a href="/windows/desktop/ETW/enabletraceex2">EnableTraceEx2</a> function. The <b>TdhAggregatePayloadFilters</b> allocates and fills in an opaque data structure for an aggregated payload filter. When the aggregated payload filter is no longer needed, the <a href="/windows/desktop/api/tdh/nf-tdh-tdhcleanuppayloadeventfilterdescriptor">TdhCleanupPayloadEventFilterDescriptor</a> function is used to free memory allocated for the aggregated  payload filter in the  <a href="/windows/desktop/api/evntprov/ns-evntprov-event_filter_descriptor">EVENT_FILTER_DESCRIPTOR</a> structure returned.


#### Examples

For an example that uses 
the <b>TdhAggregatePayloadFilters</b> function to aggregate payload filters to use in filtering on specific conditions in a logger session, see 
the example for the <a href="/windows/desktop/ETW/enabletraceex2">EnableTraceEx2</a> function.

<div class="code"></div>

## -see-also
<a href="/windows/desktop/ETW/enable-trace-parameters">ENABLE_TRACE_PARAMETERS</a>



<a href="/windows/desktop/api/evntprov/ns-evntprov-event_filter_descriptor">EVENT_FILTER_DESCRIPTOR</a>



<a href="/windows/desktop/ETW/enabletraceex2">EnableTraceEx2</a>



<a href="/windows/desktop/api/tdh/nf-tdh-tdhcleanuppayloadeventfilterdescriptor">TdhCleanupPayloadEventFilterDescriptor</a>



<a href="/windows/desktop/api/tdh/nf-tdh-tdhcreatepayloadfilter">TdhCreatePayloadFilter</a>



<a href="/windows/desktop/api/tdh/nf-tdh-tdhdeletepayloadfilter">TdhDeletePayloadFilter</a>