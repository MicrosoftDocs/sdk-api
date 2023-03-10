---
UID: NF:traffic.TcAddFlow
title: TcAddFlow function (traffic.h)
description: The TcAddFlow function adds a new flow on the specified interface.
helpviewer_keywords: ["TcAddFlow","TcAddFlow function [QOS]","_gqos_tcaddflow","qos.tcaddflow","traffic/TcAddFlow"]
old-location: qos\tcaddflow.htm
tech.root: QOS
ms.assetid: 20b4f34b-a84e-4211-8d41-0efa0dbc6cd4
ms.date: 12/05/2018
ms.keywords: TcAddFlow, TcAddFlow function [QOS], _gqos_tcaddflow, qos.tcaddflow, traffic/TcAddFlow
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
 - TcAddFlow
 - traffic/TcAddFlow
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
 - TcAddFlow
---

# TcAddFlow function


## -description

The 
<b>TcAddFlow</b> function adds a new flow on the specified interface. Note that the successful addition of a flow does not necessarily indicate a change in the way traffic is handled; traffic handling changes are effected by attaching a filter to the added flow, using the 
<a href="/previous-versions/windows/desktop/api/traffic/nf-traffic-tcaddfilter">TcAddFilter</a> function.

Traffic control clients that have registered an <b>AddFlowComplete</b> handler (a mechanism for allowing traffic control to call the 
<a href="/previous-versions/windows/desktop/api/traffic/nc-traffic-tci_add_flow_complete_handler">ClAddFlowComplete</a> callback function in order to alert clients of completed flow additions) can expect a return value of ERROR_SIGNAL_PENDING. For more information, see 
<a href="/previous-versions/windows/desktop/qos/traffic-control-objects">Traffic Control Objects</a>.

## -parameters

### -param IfcHandle [in]

Handle associated with the interface on which the flow is to be added. This handle is obtained by a previous call to the 
<a href="/previous-versions/windows/desktop/api/traffic/nf-traffic-tcopeninterfacea">TcOpenInterface</a> function.

### -param ClFlowCtx [in]

Client provided–flow context handle. Used subsequently by traffic control when referring to the added flow.

### -param Flags [in]

Reserved for future use. Must be set to zero.

### -param pGenericFlow [in]

Pointer to a description of the flow being installed.

### -param pFlowHandle [out]

Pointer to a location into which traffic control will return the flow handle. This flow handle should be used in subsequent calls to traffic control to refer to the installed flow.

## -returns

There are many reasons why a request to add a flow might be rejected. Error codes returned by traffic control from calls to 
<b>TcAddFlow</b> are provided to aid in determining the reason for rejection.

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
<dt><b>ERROR_SIGNAL_PENDING</b></dt>
</dl>
</td>
<td width="60%">
The function is being executed asynchronously; the client will be called back through the client-exposed 
<a href="/previous-versions/windows/desktop/api/traffic/nc-traffic-tci_add_flow_complete_handler">ClAddFlowComplete</a> function when the flow has been added or when the process has been completed.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_HANDLE</b></dt>
</dl>
</td>
<td width="60%">
The interface handle is invalid.

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
<dt><b>ERROR_INVALID_SERVICE_TYPE</b></dt>
</dl>
</td>
<td width="60%">
An unspecified or bad <b>INTSERV</b> service type has been provided.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_TOKEN_RATE</b></dt>
</dl>
</td>
<td width="60%">
An unspecified or bad TOKENRATE value has been provided.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PEAK_RATE</b></dt>
</dl>
</td>
<td width="60%">
The PEAKBANDWIDTH value is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_SD_MODE</b></dt>
</dl>
</td>
<td width="60%">
The SHAPEDISCARDMODE is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_QOS_PRIORITY</b></dt>
</dl>
</td>
<td width="60%">
The priority value is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_TRAFFIC_CLASS</b></dt>
</dl>
</td>
<td width="60%">
The traffic class value is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NO_SYSTEM_RESOURCES</b></dt>
</dl>
</td>
<td width="60%">
There are not enough resources to accommodate the requested flow.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_TC_OBJECT_LENGTH_INVALID</b></dt>
</dl>
</td>
<td width="60%">
Bad length specified for the TC objects.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_DIFFSERV_FLOW</b></dt>
</dl>
</td>
<td width="60%">
Applies to Diffserv flows. Indicates that the 
<a href="/windows/desktop/api/qosobjs/ns-qosobjs-qos_diffserv">QOS_DIFFSERV</a> object was passed with an invalid parameter.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_DS_MAPPING_EXISTS</b></dt>
</dl>
</td>
<td width="60%">
Applies to Diffserv flows. Indicates that the QOS_DIFFSERV_RULE specified in 
<a href="/windows/desktop/api/traffic/ns-traffic-tc_gen_flow">TC_GEN_FLOW</a> already applies to an existing flow on the interface.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_SHAPE_RATE</b></dt>
</dl>
</td>
<td width="60%">
The 
<a href="/windows/desktop/api/qos/ns-qos-qos_shaping_rate">QOS_SHAPING_RATE</a> object was passed with an invalid <b>ShapingRate</b> member.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_DS_CLASS</b></dt>
</dl>
</td>
<td width="60%">
The QOS_DS_CLASS is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NETWORK_UNREACHABLE</b></dt>
</dl>
</td>
<td width="60%">
The network cable is not plugged into the adapter.

</td>
</tr>
</table>

## -remarks

If the 
<b>TcAddFlow</b> function returns ERROR_SIGNAL_PENDING, the 
<a href="/previous-versions/windows/desktop/api/traffic/nc-traffic-tci_add_flow_complete_handler">ClAddFlowComplete</a> function will be called on a different thread than the thread that called the 
<b>TcAddFlow</b> function.

Only the addition of a filter will affect traffic control. However, the addition of a flow will cause resources to be committed within traffic control components. This enables traffic control to prepare for handling traffic on the added flow.

Traffic control may delete a flow for various reasons, including the inability to accommodate the flow due to bandwidth restrictions, and adjusted policy requirements. Clients are notified of deleted flows through the 
<a href="/previous-versions/windows/desktop/api/traffic/nc-traffic-tci_notify_handler">ClNotifyHandler</a> callback function, with the TC_NOTIFY_FLOW_CLOSE event.

<div class="alert"><b>Note</b>  Use of the 
<b>TcAddFlow</b> function requires administrative privilege.</div>
<div> </div>

## -see-also

<a href="/previous-versions/windows/desktop/api/traffic/nc-traffic-tci_add_flow_complete_handler">ClAddFlowComplete</a>



<a href="/previous-versions/windows/desktop/api/traffic/nc-traffic-tci_notify_handler">ClNotifyHandler</a>



<a href="/windows/desktop/api/traffic/ns-traffic-tc_gen_flow">TC_GEN_FLOW</a>



<a href="/previous-versions/windows/desktop/api/traffic/nf-traffic-tcaddfilter">TcAddFilter</a>



<a href="/previous-versions/windows/desktop/api/traffic/nf-traffic-tcopeninterfacea">TcOpenInterface</a>