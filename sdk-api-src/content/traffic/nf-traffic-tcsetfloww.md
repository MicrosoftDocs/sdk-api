---
UID: NF:traffic.TcSetFlowW
title: TcSetFlowW function
author: windows-sdk-content
description: The TcSetFlow function sets individual parameters for a given flow.
old-location: qos\tcsetflow.htm
old-project: QOS
ms.assetid: 9989e26c-7e79-43b7-a5b8-f203c27b2a1e
ms.author: windowssdkdev
ms.date: 03/23/2018
ms.keywords: TcSetFlow, TcSetFlow function [QOS], TcSetFlowA, TcSetFlowW, _gqos_tcsetflow, qos.tcsetflow, traffic/TcSetFlow, traffic/TcSetFlowA, traffic/TcSetFlowW
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
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
tech.root: 
req.typenames: TPMVSCMGR_ERROR
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Traffic.dll
api_name:
-	TcSetFlow
-	TcSetFlowA
-	TcSetFlowW
product: Windows
targetos: Windows
req.lib: 
req.dll: Traffic.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# TcSetFlowW function


## -description


The 
<b>TcSetFlow</b> function sets individual parameters for a given flow.


## -parameters




### -param pFlowName [in]

Name of the flow being set. The value for this parameter is obtained by a previous call to the 
<a href="https://msdn.microsoft.com/eae90fae-a29a-4005-b8c6-a5e2c9a6c07f">TcEnumerateFlows</a> function or the 
<a href="https://msdn.microsoft.com/49a78c9a-6aac-4348-9f26-dfd331dc83ec">TcGetFlowName</a> function.


### -param pGuidParam [in]

Pointer to the globally unique identifier (GUID) that corresponds to the parameter to be set. A list of available GUIDs can be found in 
<a href="https://msdn.microsoft.com/library/windows/hardware/dn922935">GUID</a>.


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



