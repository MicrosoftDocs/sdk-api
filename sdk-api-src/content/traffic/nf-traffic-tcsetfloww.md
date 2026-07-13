---
UID: NF:traffic.TcSetFlowW
title: TcSetFlowW function (traffic.h)
description: The TcSetFlow function sets individual parameters for a given flow. (Unicode)
helpviewer_keywords: ["TcSetFlow", "TcSetFlow function [QOS]", "TcSetFlowW", "_gqos_tcsetflow", "qos.tcsetflow", "traffic/TcSetFlow", "traffic/TcSetFlowW"]
old-location: qos\tcsetflow.htm
tech.root: QOS
ms.assetid: 9989e26c-7e79-43b7-a5b8-f203c27b2a1e
ms.date: 12/05/2018
ms.keywords: TcSetFlow, TcSetFlow function [QOS], TcSetFlowA, TcSetFlowW, _gqos_tcsetflow, qos.tcsetflow, traffic/TcSetFlow, traffic/TcSetFlowA, traffic/TcSetFlowW
req.header: traffic.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: TcSetFlowW (Unicode) and TcSetFlowA (ANSI)
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
 - TcSetFlowW
 - traffic/TcSetFlowW
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
 - TcSetFlow
 - TcSetFlowA
 - TcSetFlowW
---

# TcSetFlowW function


## -description

The 
<b>TcSetFlow</b> function sets individual parameters for a given flow.

## -parameters

### -param pFlowName [in]

Name of the flow being set. The value for this parameter is obtained by a previous call to the 
<a href="/previous-versions/windows/desktop/api/traffic/nf-traffic-tcenumerateflows">TcEnumerateFlows</a> function or the 
<a href="/previous-versions/windows/desktop/api/traffic/nf-traffic-tcgetflownamea">TcGetFlowName</a> function.

### -param pGuidParam [in]

Pointer to the globally unique identifier (GUID) that corresponds to the parameter to be set. A list of available GUIDs can be found in 
<a href="/previous-versions/windows/desktop/qos/guid">GUID</a>.

### -param BufferSize [in]

Size of the client-provided buffer, in bytes.

### -param Buffer [in]

Pointer to a client-provided buffer. Buffer must contain the value to which the traffic control parameter provided in <i>pGuidParam</i> should be set.

## -returns

The 
<b>TcSetFlow</b> function has the following return values.

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
<dt><b>ERROR_NOT_READY</b></dt>
</dl>
</td>
<td width="60%">
The flow is currently being modified.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NOT_ENOUGH_MEMORY</b></dt>
</dl>
</td>
<td width="60%">
The buffer size was insufficient for the GUID.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
Invalid parameter.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NOT_SUPPORTED</b></dt>
</dl>
</td>
<td width="60%">
Setting the GUID for the provided flow is not supported.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_WMI_INSTANCE_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
The instance name was not found, likely due to the flow or the interface being in the process of being closed.

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
</table>

## -remarks

Use of the 
<b>TcSetFlow</b> function requires administrative privilege.




> [!NOTE]
> The traffic.h header defines TcSetFlow as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).
