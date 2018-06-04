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

# RpcSsDisableAllocate function


## -description


The 
<b>RpcSsDisableAllocate</b> function frees resources and memory within the stub memory–management environment.


## -parameters






## -returns



<div class="alert"><b>Note</b>  For a list of valid error codes, see 
<a href="https://msdn.microsoft.com/0223aa7a-b0cf-49e3-9f08-90be5ccffbd1">RPC Return Values</a>.</div>
<div> </div>



## -remarks



<b>RpcSsDisableAllocate</b> frees all the resources used by a call to 
<a href="https://msdn.microsoft.com/18060ed2-2250-47c7-8579-238edea44c66">RpcSsEnableAllocate</a>. It also releases memory that was allocated by a call to 
<a href="https://msdn.microsoft.com/d1c1af46-63c5-4e50-abfb-c4f251972427">RpcSsAllocate</a> after the call to 
<b>RpcSsEnableAllocate</b>.


<a href="https://msdn.microsoft.com/18060ed2-2250-47c7-8579-238edea44c66">RpcSsEnableAllocate</a> and 
<b>RpcSsDisableAllocate</b> must be used together as matching pairs.




## -see-also




<a href="https://msdn.microsoft.com/229cab16-eabf-49d3-a61e-3c06e001d0ac">RpcSmDisableAllocate</a>



<a href="https://msdn.microsoft.com/d1c1af46-63c5-4e50-abfb-c4f251972427">RpcSsAllocate</a>



<a href="https://msdn.microsoft.com/18060ed2-2250-47c7-8579-238edea44c66">RpcSsEnableAllocate</a>
 

 

