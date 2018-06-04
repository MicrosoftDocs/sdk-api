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

# RpcSsSetClientAllocFree function


## -description


The 
<b>RpcSsSetClientAllocFree</b> function enables the memory allocation and release mechanisms used by the client stubs.


## -parameters




### -param ClientAlloc

TBD


### -param ClientFree

TBD




#### - pfnAllocate

Memory-allocation function.


#### - pfnFree

Memory-releasing function used with the memory-allocation function specified by <i>pfnAllocate</i>.


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



By overriding the default routines used by the client stub to manage memory, 
<b>RpcSsSetClientAllocFree</b> establishes the memory allocation and memory freeing mechanisms. Note that the default routines are free and malloc, unless the remote call occurs within manager code. In this case, the default memory–management routines are 
<a href="https://msdn.microsoft.com/f004ea19-3d1c-485f-99be-da59cbe478d2">RpcSsFree</a> and 
<a href="https://msdn.microsoft.com/d1c1af46-63c5-4e50-abfb-c4f251972427">RpcSsAllocate</a>.

Note that when 
<b>RpcSsSetClientAllocFree</b> reclaims the memory resources, it also makes the context handle <b>NULL</b>.

<div class="alert"><b>Note</b>  <b>RpcSsSetClientAllocFree</b> raises exceptions, unlike 
<a href="https://msdn.microsoft.com/f6b6db72-c9af-44d1-9f84-26aaaa17691c">RpcSmSetClientAllocFree</a>, which returns the error code.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/f6b6db72-c9af-44d1-9f84-26aaaa17691c">RpcSmSetClientAllocFree</a>



<a href="https://msdn.microsoft.com/d1c1af46-63c5-4e50-abfb-c4f251972427">RpcSsAllocate</a>



<a href="https://msdn.microsoft.com/f004ea19-3d1c-485f-99be-da59cbe478d2">RpcSsFree</a>
 

 

