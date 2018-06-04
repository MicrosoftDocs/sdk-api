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

# RpcSsSwapClientAllocFree function


## -description


The 
<b>RpcSsSwapClientAllocFree</b> function exchanges the memory allocation and release mechanisms used by the client stubs with those supplied by the client.


## -parameters




### -param ClientAlloc

TBD


### -param ClientFree

TBD


### -param OldClientAlloc

TBD


### -param OldClientFree

TBD




#### - pfnAllocate

New function to allocate memory.


#### - pfnFree

New function to release memory.


#### - pfnOldAllocate

Returns the previous memory-allocation function.


#### - pfnOldFree

Returns the previous memory-freeing function.


## -returns



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>RPC_S_OK</b></dt>
</dl>
</td>
<td width="60%">
The call succeeded.

</td>
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



<b>RpcSsSwapClientAllocFree</b> exchanges the current memory allocation and memory freeing mechanisms with those supplied by the client.

<div class="alert"><b>Note</b>  <b>RpcSsSwapClientAllocFree</b> raises exceptions, unlike 
<a href="https://msdn.microsoft.com/f07df5ec-0798-4cd2-a2f5-73e6245a7020">RpcSmSwapClientAllocFree</a>, which returns the error code.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/f07df5ec-0798-4cd2-a2f5-73e6245a7020">RpcSmSwapClientAllocFree</a>



<a href="https://msdn.microsoft.com/d1c1af46-63c5-4e50-abfb-c4f251972427">RpcSsAllocate</a>



<a href="https://msdn.microsoft.com/f004ea19-3d1c-485f-99be-da59cbe478d2">RpcSsFree</a>



<a href="https://msdn.microsoft.com/a63dab9e-0644-4a24-9762-8cc8a4f6ea05">RpcSsSetClientAllocFree</a>
 

 

