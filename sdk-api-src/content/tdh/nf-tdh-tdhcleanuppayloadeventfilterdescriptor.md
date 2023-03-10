---
UID: NF:tdh.TdhCleanupPayloadEventFilterDescriptor
title: TdhCleanupPayloadEventFilterDescriptor function (tdh.h)
description: Frees the aggregated structure of payload filters created using the TdhAggregatePayloadFilters function.
helpviewer_keywords: ["TdhCleanupPayloadEventFilterDescriptor","TdhCleanupPayloadEventFilterDescriptor function [ETW]","etw.tdhcleanuppayloadeventfilterdescriptor","tdh/TdhCleanupPayloadEventFilterDescriptor"]
old-location: etw\tdhcleanuppayloadeventfilterdescriptor.htm
tech.root: ETW
ms.assetid: AA08AFD5-EC1A-44BF-9BCB-EEA69A959853
ms.date: 12/05/2018
ms.keywords: TdhCleanupPayloadEventFilterDescriptor, TdhCleanupPayloadEventFilterDescriptor function [ETW], etw.tdhcleanuppayloadeventfilterdescriptor, tdh/TdhCleanupPayloadEventFilterDescriptor
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
 - TdhCleanupPayloadEventFilterDescriptor
 - tdh/TdhCleanupPayloadEventFilterDescriptor
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
 - TdhCleanupPayloadEventFilterDescriptor
---

# TdhCleanupPayloadEventFilterDescriptor function


## -description

The <b>TdhCleanupPayloadEventFilterDescriptor</b> function frees the aggregated structure of payload filters created using the <a href="/windows/desktop/api/tdh/nf-tdh-tdhaggregatepayloadfilters">TdhAggregatePayloadFilters</a> function.

## -parameters

### -param EventFilterDescriptor [in, out]

A pointer to an <a href="/windows/desktop/api/evntprov/ns-evntprov-event_filter_descriptor">EVENT_FILTER_DESCRIPTOR</a> structure that contains aggregated filters where the allocated memory is to be freed. The <b>EVENT_FILTER_DESCRIPTOR</b> structure  passed was created by calling the <a href="/windows/desktop/api/tdh/nf-tdh-tdhaggregatepayloadfilters">TdhAggregatePayloadFilters</a> function.  

If the call is successful, allocated memory is released for the aggregated filters and the fields in the returned <a href="/windows/desktop/api/evntprov/ns-evntprov-event_filter_descriptor">EVENT_FILTER_DESCRIPTOR</a> structure are re-initialized

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
</table>

## -remarks

On Windows 8.1,Windows Server 2012 R2, and later, event payload filters can be used by the <a href="/windows/desktop/ETW/enabletraceex2">EnableTraceEx2</a> function to filter on specific content of the event in a logger session. 

The <b>TdhCleanupPayloadEventFilterDescriptor</b> function is used to free memory allocated that is returned by the <a href="/windows/desktop/api/tdh/nf-tdh-tdhaggregatepayloadfilters">TdhAggregatePayloadFilters</a> function. 


#### Examples

For an example that uses 
the <b>TdhCleanupPayloadEventFilterDescriptor</b>  function to free memory used by aggregate payload filters, see 
the example for the <a href="/windows/desktop/ETW/enabletraceex2">EnableTraceEx2</a> function.

<div class="code"></div>

## -see-also
<a href="/windows/desktop/ETW/enable-trace-parameters">ENABLE_TRACE_PARAMETERS</a>



<a href="/windows/desktop/api/evntprov/ns-evntprov-event_filter_descriptor">EVENT_FILTER_DESCRIPTOR</a>



<a href="/windows/desktop/ETW/enabletraceex2">EnableTraceEx2</a>



<a href="/windows/desktop/api/tdh/nf-tdh-tdhaggregatepayloadfilters">TdhAggregatePayloadFilters</a>



<a href="/windows/desktop/api/tdh/nf-tdh-tdhcreatepayloadfilter">TdhCreatePayloadFilter</a>



<a href="/windows/desktop/api/tdh/nf-tdh-tdhdeletepayloadfilter">TdhDeletePayloadFilter</a>