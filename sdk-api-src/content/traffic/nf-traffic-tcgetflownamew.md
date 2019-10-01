---
UID: NF:traffic.TcGetFlowNameW
title: TcGetFlowNameW function (traffic.h)
author: windows-sdk-content
description: The TcGetFlowName function provides the name of a flow that has been created by the calling client.
old-location: qos\tcgetflowname.htm
tech.root: QOS
ms.assetid: 49a78c9a-6aac-4348-9f26-dfd331dc83ec
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: TcGetFlowName, TcGetFlowName function [QOS], TcGetFlowNameA, TcGetFlowNameW, _gqos_tcgetflowname, qos.tcgetflowname, traffic/TcGetFlowName, traffic/TcGetFlowNameA, traffic/TcGetFlowNameW
ms.topic: function
f1_keywords: 
 - "traffic/TcGetFlowName"
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# TcGetFlowNameW function


## -description


The 
<b>TcGetFlowName</b> function provides the name of a flow that has been created by the calling client. Flow properties and other characteristics of flows are provided based on the name of a flow. Flow names can also be retrieved by a call to the 
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/traffic/nf-traffic-tcenumerateflows">TcEnumerateFlows</a> function.


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




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/traffic/nf-traffic-tcenumerateflows">TcEnumerateFlows</a>
 

 

