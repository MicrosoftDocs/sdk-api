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

# RpcBindingInqOption function


## -description


RPC client processes use 
<b>RpcBindingInqOption</b> to determine current values of the binding options for a given binding handle.


## -parameters




### -param hBinding

Server binding about which to determine binding-option values.


### -param option

TBD


### -param pOptionValue

Memory location to place the value for the specified <i>Option</i>

<div class="alert"><b>Note</b>  For a list of binding options and their possible values, see 
<a href="https://msdn.microsoft.com/ff88e05d-b9f3-42ef-a44f-fee9261832c8">Binding Option Constants</a>.</div>
<div> </div>

#### - Option

Binding handle property to inquire about.


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
<dt><b>RPC_S_CANNOT_SUPPORT</b></dt>
</dl>
</td>
<td width="60%">
The function is not supported for either the operating system or the transport.

</td>
</tr>
</table>
 

<div class="alert"><b>Note</b>  For a list of valid error codes, see 
<a href="https://msdn.microsoft.com/0223aa7a-b0cf-49e3-9f08-90be5ccffbd1">RPC Return Values</a>.</div>
<div> </div>



## -remarks



Client processes call 
<b>RpcBindingInqOption</b> to determine the current settings of the binding handle options. To inquire about authentication settings clients call the 
<a href="https://msdn.microsoft.com/2834a6a8-8bd6-4829-84ea-e3f35c917ab7">RpcBindingInqAuthClient</a> function. .




## -see-also




<a href="https://msdn.microsoft.com/f1c8665b-3754-4c2e-b3ac-bba1f4b329e1">RPC Message
		  Queuing</a>



<a href="https://msdn.microsoft.com/2834a6a8-8bd6-4829-84ea-e3f35c917ab7">RpcBindingInqAuthClient</a>



<a href="https://msdn.microsoft.com/2db946b6-6a0d-402c-89ef-68c7489aa7ee">RpcBindingSetAuthInfo</a>



<a href="https://msdn.microsoft.com/bc721fb0-2271-4658-995b-a41e8eefc5d5">RpcBindingSetOption</a>



<a href="https://msdn.microsoft.com/ec616bf5-a845-4e7e-9f39-20947d2074f7">message</a>
 

 

