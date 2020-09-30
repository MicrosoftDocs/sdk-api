---
UID: NF:traffic.TcDeleteFlow
title: TcDeleteFlow function (traffic.h)
description: The TcDeleteFlow function deletes a flow that has been added with the TcAddFlow function. Clients should delete all filters associated with a flow before deleting it, otherwise, an error will be returned and the function will not delete the flow.
helpviewer_keywords: ["TcDeleteFlow","TcDeleteFlow function [QOS]","_gqos_tcdeleteflow","qos.tcdeleteflow","traffic/TcDeleteFlow"]
old-location: qos\tcdeleteflow.htm
tech.root: QOS
ms.assetid: 6e62b55e-9919-44be-a9ae-f1319cc82d76
ms.date: 12/05/2018
ms.keywords: TcDeleteFlow, TcDeleteFlow function [QOS], _gqos_tcdeleteflow, qos.tcdeleteflow, traffic/TcDeleteFlow
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
 - TcDeleteFlow
 - traffic/TcDeleteFlow
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
 - TcDeleteFlow
---

# TcDeleteFlow function


## -description

The 
<b>TcDeleteFlow</b> function deletes a flow that has been added with the 
<a href="/previous-versions/windows/desktop/api/traffic/nf-traffic-tcaddflow">TcAddFlow</a> function. Clients should delete all filters associated with a flow before deleting it, otherwise, an error will be returned and the function will not delete the flow.

Traffic control clients that have registered a <b>DeleteFlowComplete</b> handler (a mechanism for allowing traffic control to call the 
<a href="/previous-versions/windows/desktop/api/traffic/nc-traffic-tci_del_flow_complete_handler">ClDeleteFlowComplete</a> callback function to alert clients of completed flow deletions) can expect a return value of ERROR_SIGNAL_PENDING.

## -parameters

### -param FlowHandle [in]

Handle for the flow, as received from a previous call to the 
<a href="/previous-versions/windows/desktop/api/traffic/nf-traffic-tcaddflow">TcAddFlow</a> function.

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
<a href="/previous-versions/windows/desktop/api/traffic/nc-traffic-tci_del_flow_complete_handler">ClDeleteFlowComplete</a> function when the flow has been added, or when the process has been completed.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_HANDLE</b></dt>
</dl>
</td>
<td width="60%">
The flow handle is invalid or <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NOT_READY</b></dt>
</dl>
</td>
<td width="60%">
Action performed on the flow by a previous function call to 
<a href="/previous-versions/windows/desktop/api/traffic/nf-traffic-tcmodifyflow">TcModifyFlow</a>, 
<a href="/previous-versions/windows/desktop/api/traffic/nf-traffic-tcdeleteflow">TcDeleteFlow</a>, or 
<a href="/previous-versions/windows/desktop/api/traffic/nf-traffic-tcaddflow">TcAddFlow</a> has not yet completed.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_TC_SUPPORTED_OBJECTS_EXIST</b></dt>
</dl>
</td>
<td width="60%">
At least one filter associated with this flow exists.

</td>
</tr>
</table>

## -remarks

If the 
<b>TcDeleteFlow</b> function returns ERROR_SIGNAL_PENDING, the 
<a href="/previous-versions/windows/desktop/api/traffic/nc-traffic-tci_del_flow_complete_handler">ClDeleteFlowComplete</a> function will be called on a different thread than the thread that called the 
<b>TcDeleteFlow</b> function.

<div class="alert"><b>Note</b>  Use of the 
<b>TcDeleteFlow</b> function requires administrative privilege.</div>
<div> </div>

## -see-also

<a href="/previous-versions/windows/desktop/api/traffic/nc-traffic-tci_del_flow_complete_handler">ClDeleteFlowComplete</a>



<a href="/previous-versions/windows/desktop/api/traffic/nf-traffic-tcaddflow">TcAddFlow</a>



<a href="/previous-versions/windows/desktop/api/traffic/nf-traffic-tcenumerateflows">TcEnumerateFlows</a>