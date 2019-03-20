---
UID: NF:traffic.TcModifyFlow
title: TcModifyFlow function (traffic.h)
author: windows-sdk-content
description: The TcModifyFlow function modifies an existing flow. When calling TcModifyFlow, new Flowspec parameters and any traffic control objects should be filled.
old-location: qos\tcmodifyflow.htm
tech.root: QOS
ms.assetid: e1b5d987-8365-4fea-a88b-0d574749b38a
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: TcModifyFlow, TcModifyFlow function [QOS], _gqos_tcmodifyflow, qos.tcmodifyflow, traffic/TcModifyFlow
ms.topic: function
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Traffic.dll
api_name:
 - TcModifyFlow
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# TcModifyFlow function


## -description


The 
<b>TcModifyFlow</b> function modifies an existing flow. When calling 
<b>TcModifyFlow</b>, new <i>Flowspec</i> parameters and any traffic control objects should be filled.

Traffic control clients that have registered a ModifyFlowComplete handler (a mechanism for allowing traffic control to call the 
<a href="https://msdn.microsoft.com/61afc465-d942-4db7-96ee-56f3f1c3cafa">ClModifyFlowComplete</a> callback function in order to alert clients of completed flow modifications) can expect a return value of ERROR_SIGNAL_PENDING.


## -parameters




### -param FlowHandle [in]

Handle for the flow, as received from a previous call to the 
<a href="https://msdn.microsoft.com/20b4f34b-a84e-4211-8d41-0efa0dbc6cd4">TcAddFlow</a> function.


### -param pGenericFlow [in]

Pointer to a description of the flow modifications.


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
<dt><b>ERROR_SIGNAL_PENDING</b></dt>
</dl>
</td>
<td width="60%">
The function is being executed asynchronously; the client will be called back through the client-exposed 
<a href="https://msdn.microsoft.com/61afc465-d942-4db7-96ee-56f3f1c3cafa">ClModifyFlowComplete</a> function when the flow has been added, or when the process has been completed.

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
<dt><b>ERROR_NOT_READY</b></dt>
</dl>
</td>
<td width="60%">
Action performed on the flow by a previous function call to the 
<a href="https://msdn.microsoft.com/20b4f34b-a84e-4211-8d41-0efa0dbc6cd4">TcAddFlow</a>, 
<a href="https://msdn.microsoft.com/e1b5d987-8365-4fea-a88b-0d574749b38a">TcModifyFlow</a>, or 
<a href="https://msdn.microsoft.com/6e62b55e-9919-44be-a9ae-f1319cc82d76">TcDeleteFlow</a> has not yet completed.

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
An unspecified or bad intserv service type has been provided.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_TOKEN_RATE</b></dt>
</dl>
</td>
<td width="60%">
An unspecified or bad <i>TokenRate</i> value has been provided.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PEAK_RATE</b></dt>
</dl>
</td>
<td width="60%">
The <i>PeakBandwidth</i> value is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_SD_MODE</b></dt>
</dl>
</td>
<td width="60%">
The <i>ShapeDiscardMode</i> is invalid.

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
<a href="https://msdn.microsoft.com/3d1035dc-0e46-46f4-abb3-26100356b60d">QOS_DIFFSERV</a> object was passed with an invalid parameter.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_DS_MAPPING_EXISTS</b></dt>
</dl>
</td>
<td width="60%">
Applies to Diffserv flows. Indicates that the 
<a href="https://msdn.microsoft.com/732cfbec-4175-4397-854f-0d2a930e11bc">QOS_DIFFSERV_RULE</a> specified in 
<a href="https://msdn.microsoft.com/88b162d9-003c-42ce-8f82-91ee1aa9e32e">TC_GEN_FLOW</a> already applies to an existing flow on the interface.

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
<a href="https://msdn.microsoft.com/2be833dc-d9e1-495d-831e-09c900c8adb2">QOS_SHAPING_RATE</a> was passed with an invalid ShapeRate.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_DS_CLASS</b></dt>
</dl>
</td>
<td width="60%">

<a href="https://msdn.microsoft.com/56eca8ef-2b6e-4380-869c-bf1a4c8fdb1f">QOS_DS_CLASS</a> is invalid.

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
<b>TcModifyFlow</b> function returns ERROR_SIGNAL_PENDING, the 
<a href="https://msdn.microsoft.com/61afc465-d942-4db7-96ee-56f3f1c3cafa">ClModifyFlowComplete</a> function will be called on a different thread than the thread that called the 
<b>TcModifyFlow</b> function.

<div class="alert"><b>Note</b>  Use of the 
<b>TcModifyFlow</b> function requires administrative privilege.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/61afc465-d942-4db7-96ee-56f3f1c3cafa">ClModifyFlowComplete</a>



<a href="https://msdn.microsoft.com/20b4f34b-a84e-4211-8d41-0efa0dbc6cd4">TcAddFlow</a>



<a href="https://msdn.microsoft.com/eae90fae-a29a-4005-b8c6-a5e2c9a6c07f">TcEnumerateFlows</a>
 

 

