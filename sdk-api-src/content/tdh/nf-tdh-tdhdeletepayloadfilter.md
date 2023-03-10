---
UID: NF:tdh.TdhDeletePayloadFilter
title: TdhDeletePayloadFilter function (tdh.h)
description: Frees the memory allocated for a single payload filter by the TdhCreatePayloadFilter function.
helpviewer_keywords: ["TdhDeletePayloadFilter","TdhDeletePayloadFilter function [ETW]","etw.tdhdeletepayloadfilter","tdh/TdhDeletePayloadFilter"]
old-location: etw\tdhdeletepayloadfilter.htm
tech.root: ETW
ms.assetid: 50EB6A11-54AE-4D90-ABA4-13D8EADA1955
ms.date: 12/05/2018
ms.keywords: TdhDeletePayloadFilter, TdhDeletePayloadFilter function [ETW], etw.tdhdeletepayloadfilter, tdh/TdhDeletePayloadFilter
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
 - TdhDeletePayloadFilter
 - tdh/TdhDeletePayloadFilter
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
 - TdhDeletePayloadFilter
---

# TdhDeletePayloadFilter function


## -description

The <b>TdhDeletePayloadFilter</b> function frees the memory allocated for  a single payload filter by the <a href="/windows/desktop/api/tdh/nf-tdh-tdhcreatepayloadfilter">TdhCreatePayloadFilter</a> function.

## -parameters

### -param PayloadFilter [in, out]

A pointer to a single payload filter allocated by the <a href="/windows/desktop/api/tdh/nf-tdh-tdhcreatepayloadfilter">TdhCreatePayloadFilter</a> function.

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

On Windows 8.1,Windows Server 2012 R2, and later, event payload filters can be used by the <a href="/windows/desktop/ETW/enabletraceex2">EnableTraceEx2</a> function to filter on the specific  content of the event in a logger session. 

The <b>TdhDeletePayloadFilter</b> function is used to free memory allocated for a single payload filter that is returned by the <a href="/windows/desktop/api/tdh/nf-tdh-tdhcreatepayloadfilter">TdhCreatePayloadFilter</a> function.

## -see-also
<a href="/windows/desktop/ETW/enable-trace-parameters">ENABLE_TRACE_PARAMETERS</a>



<a href="/windows/desktop/api/evntprov/ns-evntprov-event_filter_descriptor">EVENT_FILTER_DESCRIPTOR</a>



<a href="/windows/desktop/ETW/enabletraceex2">EnableTraceEx2</a>



<a href="/windows/desktop/api/tdh/nf-tdh-tdhaggregatepayloadfilters">TdhAggregatePayloadFilters</a>



<a href="/windows/desktop/api/tdh/nf-tdh-tdhcleanuppayloadeventfilterdescriptor">TdhCleanupPayloadEventFilterDescriptor</a>



<a href="/windows/desktop/api/tdh/nf-tdh-tdhcreatepayloadfilter">TdhCreatePayloadFilter</a>