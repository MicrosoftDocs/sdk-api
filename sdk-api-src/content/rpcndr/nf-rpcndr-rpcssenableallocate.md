---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# RpcSsEnableAllocate function


## -description


The 
<b>RpcSsEnableAllocate</b> function establishes the stub memory–management environment.


## -parameters






## -returns



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>RPC_S_OUT_OF_MEMORY</b></dt>
</dl>
</td>
<td width="60%">
The system is out of memory.

</td>
</tr>
</table>
 

<div class="alert"><b>Note</b>  For a list of valid error codes, see 
<a href="https://msdn.microsoft.com/0223aa7a-b0cf-49e3-9f08-90be5ccffbd1">RPC Return Values</a>.</div>
<div> </div>



## -remarks



In cases where the stub memory management is not enabled by the stub itself, an application calls 
<b>RpcSsEnableAllocate</b> to establish the stub memory–management environment. This environment must be established prior to making a call to 
<a href="https://msdn.microsoft.com/d1c1af46-63c5-4e50-abfb-c4f251972427">RpcSsAllocate</a>. For server manager code called from the stub, the memory-management environment is usually established by the stub itself. Otherwise, call 
<b>RpcSsEnableAllocate</b> before calling 
<b>RpcSsAllocate</b>. For more information, see 
<a href="https://msdn.microsoft.com/b56ccac1-84cb-4687-bdd2-21ee716b472a">Memory Management</a>, 
<a href="https://msdn.microsoft.com/f3b10f9c-7383-4665-96e3-1518f554f23e">RpcSsGetThreadHandle</a>, and 
<a href="https://msdn.microsoft.com/8984e253-ea78-4ca2-bf24-83100a0ac79d">RpcSsSetThreadHandle</a>.

<div class="alert"><b>Note</b>  The 
<b>RpcSsEnableAllocate</b> function raises exceptions, while the 
<a href="https://msdn.microsoft.com/a0b144fc-873e-4884-b842-ac0eea84487b">RpcSmEnableAllocate</a> function returns the error code.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/a0b144fc-873e-4884-b842-ac0eea84487b">RpcSmEnableAllocate</a>



<a href="https://msdn.microsoft.com/d1c1af46-63c5-4e50-abfb-c4f251972427">RpcSsAllocate</a>



<a href="https://msdn.microsoft.com/08121380-ff75-4f18-aae4-fdd01e1dfa8b">RpcSsDisableAllocate</a>
 

 

