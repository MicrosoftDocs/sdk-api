---
UID: NF:tdh.TdhCleanupPayloadEventFilterDescriptor
title: TdhCleanupPayloadEventFilterDescriptor function
author: windows-sdk-content
description: Frees the aggregated structure of payload filters created using the TdhAggregatePayloadFilters function.
old-location: etw\tdhcleanuppayloadeventfilterdescriptor.htm
tech.root: etw
ms.assetid: AA08AFD5-EC1A-44BF-9BCB-EEA69A959853
ms.author: windowssdkdev
ms.date: 10/04/2018
ms.keywords: TdhCleanupPayloadEventFilterDescriptor, TdhCleanupPayloadEventFilterDescriptor function [ETW], etw.tdhcleanuppayloadeventfilterdescriptor, tdh/TdhCleanupPayloadEventFilterDescriptor
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# TdhCleanupPayloadEventFilterDescriptor function


## -description


The <b>TdhCleanupPayloadEventFilterDescriptor</b> function frees the aggregated structure of payload filters created using the <a href="https://msdn.microsoft.com/B9093E64-1796-4AF2-AB45-84F278813B66">TdhAggregatePayloadFilters</a> function.




## -parameters




### -param EventFilterDescriptor [in, out]

A pointer to an <a href="https://msdn.microsoft.com/9318868a-29d8-4a5e-9579-c06a7c0fd78f">EVENT_FILTER_DESCRIPTOR</a> structure that contains aggregated filters where the allocated memory is to be freed. The <b>EVENT_FILTER_DESCRIPTOR</b> structure  passed was created by calling the <a href="https://msdn.microsoft.com/B9093E64-1796-4AF2-AB45-84F278813B66">TdhAggregatePayloadFilters</a> function.  

If the call is successful, allocated memory is released for the aggregated filters and the fields in the returned <a href="https://msdn.microsoft.com/9318868a-29d8-4a5e-9579-c06a7c0fd78f">EVENT_FILTER_DESCRIPTOR</a> structure are re-initialized


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



On Windows 8.1,Windows Server 2012 R2, and later, event payload filters can be used by the <a href="https://msdn.microsoft.com/3aceffb6-614f-4cad-bbec-f181f0cbdbff">EnableTraceEx2</a> function to filter on specific content of the event in a logger session. 

The <b>TdhCleanupPayloadEventFilterDescriptor</b> function is used to free memory allocated that is returned by the <a href="https://msdn.microsoft.com/B9093E64-1796-4AF2-AB45-84F278813B66">TdhAggregatePayloadFilters</a> function. 


#### Examples

For an example that uses 
the <b>TdhCleanupPayloadEventFilterDescriptor</b>  function to free memory used by aggregate payload filters, see 
the example for the <a href="https://msdn.microsoft.com/3aceffb6-614f-4cad-bbec-f181f0cbdbff">EnableTraceEx2</a> function.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/bc7cf886-f763-428a-9e75-031e8df26554">ENABLE_TRACE_PARAMETERS</a>



<a href="https://msdn.microsoft.com/9318868a-29d8-4a5e-9579-c06a7c0fd78f">EVENT_FILTER_DESCRIPTOR</a>



<a href="https://msdn.microsoft.com/3aceffb6-614f-4cad-bbec-f181f0cbdbff">EnableTraceEx2</a>



<a href="https://msdn.microsoft.com/B9093E64-1796-4AF2-AB45-84F278813B66">TdhAggregatePayloadFilters</a>



<a href="https://msdn.microsoft.com/B5132FF2-9DE3-40F3-82F0-90FE0640F646">TdhCreatePayloadFilter</a>



<a href="https://msdn.microsoft.com/50EB6A11-54AE-4D90-ABA4-13D8EADA1955">TdhDeletePayloadFilter</a>
 

 

