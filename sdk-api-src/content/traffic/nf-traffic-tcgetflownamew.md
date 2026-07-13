---
UID: NF:traffic.TcGetFlowNameW
title: TcGetFlowNameW function (traffic.h)
description: The TcGetFlowName function provides the name of a flow that has been created by the calling client. (Unicode)
helpviewer_keywords: ["TcGetFlowName", "TcGetFlowName function [QOS]", "TcGetFlowNameW", "_gqos_tcgetflowname", "qos.tcgetflowname", "traffic/TcGetFlowName", "traffic/TcGetFlowNameW"]
old-location: qos\tcgetflowname.htm
tech.root: QOS
ms.assetid: 49a78c9a-6aac-4348-9f26-dfd331dc83ec
ms.date: 12/05/2018
ms.keywords: TcGetFlowName, TcGetFlowName function [QOS], TcGetFlowNameA, TcGetFlowNameW, _gqos_tcgetflowname, qos.tcgetflowname, traffic/TcGetFlowName, traffic/TcGetFlowNameA, traffic/TcGetFlowNameW
req.header: traffic.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: TcGetFlowNameW (Unicode) and TcGetFlowNameA (ANSI)
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
 - TcGetFlowNameW
 - traffic/TcGetFlowNameW
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
 - TcGetFlowName
 - TcGetFlowNameA
 - TcGetFlowNameW
---

# TcGetFlowNameW function


## -description

The 
<b>TcGetFlowName</b> function provides the name of a flow that has been created by the calling client. Flow properties and other characteristics of flows are provided based on the name of a flow. Flow names can also be retrieved by a call to the 
<a href="/previous-versions/windows/desktop/api/traffic/nf-traffic-tcenumerateflows">TcEnumerateFlows</a> function.

## -parameters

### -param FlowHandle [in]

Handle for the flow.

### -param StrSize [in]

Size of the string buffer provided in <i>pFlowName</i>.

### -param pFlowName [out]

Pointer to the output buffer holding the flow name.

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
One of the parameters is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INSUFFICIENT_BUFFER</b></dt>
</dl>
</td>
<td width="60%">
The buffer is too small to contain the results.

</td>
</tr>
</table>

## -remarks

Use of the 
<b>TcGetFlowName</b> function requires administrative privilege.





> [!NOTE]
> The traffic.h header defines TcGetFlowName as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/previous-versions/windows/desktop/api/traffic/nf-traffic-tcenumerateflows">TcEnumerateFlows</a>
