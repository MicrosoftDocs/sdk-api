---
UID: NF:traffic.TcAddFilter
title: TcAddFilter function (traffic.h)
description: The TcAddFilter function associates a new filter with an existing flow that allows packets matching the filter to be directed to the associated flow.
helpviewer_keywords: ["TcAddFilter","TcAddFilter function [QOS]","_gqos_tcaddfilter","qos.tcaddfilter","traffic/TcAddFilter"]
old-location: qos\tcaddfilter.htm
tech.root: QOS
ms.assetid: c6d7c346-c353-4224-a8b5-56910e447902
ms.date: 12/05/2018
ms.keywords: TcAddFilter, TcAddFilter function [QOS], _gqos_tcaddfilter, qos.tcaddfilter, traffic/TcAddFilter
req.header: traffic.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Traffic.lib
req.dll: Traffic.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - TcAddFilter
 - traffic/TcAddFilter
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Traffic.dll
api_name:
 - TcAddFilter
---

# TcAddFilter function


## -description

The 
<b>TcAddFilter</b> function associates a new filter with an existing flow that allows packets matching the filter to be directed to the associated flow.

Filters include a pattern and a mask. The pattern specifies particular parameter values, while the mask specifies which parameters and parameter subfields apply to a given filter. When a pattern/mask combination is applied to a set of packets, matching packets are directed to the flow to which the corresponding filter is associated.

Traffic control returns a handle to the newly added filter, in the pFilterHandle parameter, by which clients can refer to the added filter. Pending flows, such as those processing a 
<a href="/previous-versions/windows/desktop/api/traffic/nf-traffic-tcaddflow">TcAddFlow</a> or 
<a href="/previous-versions/windows/desktop/api/traffic/nf-traffic-tcmodifyflow">TcModifyFlow</a> request for which a callback routine has not been completed, cannot have filters associated to them; only flows that have been completed and are stable can apply associated filters.

The relationship between filters and flows is many to one. Multiple filters can be applied to a single flow; however, a filter can only apply to one flow. For example, flow A can have filters X, Y and Z applied to it, but as long as flow A is active, filters X, Y and Z cannot apply to any other flows.

## -parameters

### -param FlowHandle [in]

Handle for the flow, as received from a previous call to the 
<a href="/previous-versions/windows/desktop/api/traffic/nf-traffic-tcaddflow">TcAddFlow</a> function.

### -param pGenericFilter [in]

Pointer to a description of the filter to be installed.

### -param pFilterHandle [out]

Pointer to a buffer where traffic control returns the filter handle. This filter handle is used by the client in subsequent calls to refer to the added filter.

## -returns

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>NO_ERROR</b></dt>
</dl>
</td>
<td width="60%">
The function executed without errors.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_HANDLE</b></dt>
</dl>
</td>
<td width="60%">
The flow handle is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
A parameter is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_ADDRESS_TYPE</b></dt>
</dl>
</td>
<td width="60%">
An invalid address type has been provided.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_DUPLICATE_FILTER</b></dt>
</dl>
</td>
<td width="60%">
An identical filter exists on a flow on this interface.

<div class="alert"><b>Note</b>   In Windows Vista, this code will not be returned.</div>
<div> </div>
</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_FILTER_CONFLICT</b></dt>
</dl>
</td>
<td width="60%">
A conflicting filter exists on a flow on this interface.

<div class="alert"><b>Note</b>   In Windows Vista, this code will not be returned.</div>
<div> </div>
</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NOT_ENOUGH_MEMORY</b></dt>
</dl>
</td>
<td width="60%">
The system is out of memory.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NOT READY</b></dt>
</dl>
</td>
<td width="60%">
The flow is either being installed, modified, or deleted, and is not in a state that accepts filters.

</td>
</tr>
</table>

## -remarks

Filters can be of different types. They are typically used to filter packets belonging to different network layers. Filter types installed on an interface generally correspond to the address types of the network layer addresses associated with the interface. The address type should be specified in the filter structure.

Filters may be rejected for various reasons, including possible conflicts with the requested filter as well as filters already associated with the flow. Error codes specific to traffic control are provided to help the user diagnose the reason behind a rejection to the 
<b>TcAddFilter</b> function.

<div class="alert"><b>Note</b>  Use of the 
<b>TcAddFilter</b> function requires administrative privilege.</div>
<div> </div>
In Windows Vista, overlapping and identical filters can be created.  In these situations, the more specific filter takes precedence.

## -see-also

<a href="/previous-versions/windows/desktop/api/traffic/nf-traffic-tcaddflow">TcAddFlow</a>