---
UID: NF:traffic.TcQueryFlowA
title: TcQueryFlowA function (traffic.h)
description: The TcQueryFlow function queries traffic control for the value of a specific flow parameter based on the name of the flow. The name of a flow can be retrieved from the TcEnumerateFlows function or from the TcGetFlowName function. (ANSI)
helpviewer_keywords: ["TcQueryFlowA", "traffic/TcQueryFlowA"]
old-location: qos\tcqueryflow.htm
tech.root: QOS
ms.assetid: 3662fdac-9d8c-4e8d-a56e-2b34d9597211
ms.date: 12/05/2018
ms.keywords: TcQueryFlow, TcQueryFlow function [QOS], TcQueryFlowA, TcQueryFlowW, _gqos_tcqueryflow, qos.tcqueryflow, traffic/TcQueryFlow, traffic/TcQueryFlowA, traffic/TcQueryFlowW
req.header: traffic.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: TcQueryFlowW (Unicode) and TcQueryFlowA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Traffic.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - TcQueryFlowA
 - traffic/TcQueryFlowA
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
 - TcQueryFlow
 - TcQueryFlowA
 - TcQueryFlowW
---

# TcQueryFlowA function


## -description

The 
<b>TcQueryFlow</b> function queries traffic control for the value of a specific flow parameter based on the name of the flow. The name of a flow can be retrieved from the 
<a href="/previous-versions/windows/desktop/api/traffic/nf-traffic-tcenumerateflows">TcEnumerateFlows</a> function or from the 
<a href="/previous-versions/windows/desktop/api/traffic/nf-traffic-tcgetflownamea">TcGetFlowName</a> function.

## -parameters

### -param pFlowName [in]

Name of the flow being queried.

### -param pGuidParam [in]

Pointer to the globally unique identifier (GUID) that corresponds to the flow parameter of interest. A list of traffic control's GUIDs can be found in 
<a href="/previous-versions/windows/desktop/qos/guid">GUID</a>.

### -param pBufferSize [in, out]

Pointer to the size of the client-provided buffer or the number of bytes used by traffic control. For input, points to the size of <i>Buffer</i>, in bytes. For output, points to the actual amount of buffer space written with returned flow-parameter data, in bytes.

### -param Buffer [out]

Pointer to the client-provided buffer in which the returned flow parameter is written.

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
<dt><b>ERROR_INSUFFICIENT_BUFFER</b></dt>
</dl>
</td>
<td width="60%">
The provided buffer is too small to hold the results.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NOT_SUPPORTED</b></dt>
</dl>
</td>
<td width="60%">
The requested GUID is not supported.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_WMI_GUID_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
The device did not register for this GUID.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_WMI_INSTANCE_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
The instance name was not found, likely because the flow or the interface is in the process of being closed.

</td>
</tr>
</table>

## -remarks

Use of the 
<b>TcQueryFlow</b> function requires administrative privilege.





> [!NOTE]
> The traffic.h header defines TcQueryFlow as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/previous-versions/windows/desktop/qos/guid">GUID</a>



<a href="/previous-versions/windows/desktop/api/traffic/nf-traffic-tcenumerateflows">TcEnumerateFlows</a>



<a href="/previous-versions/windows/desktop/api/traffic/nf-traffic-tcgetflownamea">TcGetFlowName</a>
