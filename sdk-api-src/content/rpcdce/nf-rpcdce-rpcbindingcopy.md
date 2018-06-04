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

# RpcBindingCopy function


## -description


The 
<b>RpcBindingCopy</b> function copies binding information and creates a new binding handle.


## -parameters




### -param SourceBinding

Server binding handle whose referenced binding information is copied.


### -param DestinationBinding

Returns a pointer to the server binding handle that refers to the copied binding information.


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
<dt><b>RPC_S_INVALID_BINDING</b></dt>
</dl>
</td>
<td width="60%">
The binding handle was invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>RPC_S_WRONG_KIND_OF_BINDING</b></dt>
</dl>
</td>
<td width="60%">
This was the wrong kind of binding for the operation.

</td>
</tr>
</table>
 

<div class="alert"><b>Note</b>  For a list of valid error codes, see 
<a href="https://msdn.microsoft.com/0223aa7a-b0cf-49e3-9f08-90be5ccffbd1">RPC Return Values</a>.</div>
<div> </div>



## -remarks



The 
<b>RpcBindingCopy</b> function copies the server-binding information referenced by the <i>SourceBinding</i> parameter. 
<b>RpcBindingCopy</b> uses the <i>DestinationBinding</i> parameter to return a new server binding handle for the copied binding information. 
<b>RpcBindingCopy</b> also copies the authentication information from the <i>SourceBinding</i> parameter to the <i>DestinationBinding</i> parameter.

An application uses 
<b>RpcBindingCopy</b> when it wants to prevent a change being made to binding information by one thread from affecting the binding information used by other threads.

Once an application calls 
<b>RpcBindingCopy</b>, operations performed on the <i>SourceBinding</i> binding handle do not affect the binding information referenced by the <i>DestinationBinding</i> binding handle. Similarly, operations performed on the <i>DestinationBinding</i> binding handle do not affect the binding information referenced by the <i>SourceBinding</i> binding handle.

If an application wants one thread's changes to binding information to affect the binding information used by other threads, the application should share a single binding handle across the threads. In this case, the application is responsible for binding-handle concurrency control.

When an application is finished using the binding handle specified by the <i>DestinationBinding</i> parameter, the application should call the 
<a href="https://msdn.microsoft.com/0f85e64f-b4a6-4982-8df5-88caa0a312f6">RpcBindingFree</a> function to release the memory used by the <i>DestinationBinding</i> binding handle and its referenced binding information.

<div class="alert"><b>Note</b>  Microsoft RPC supports 
<b>RpcBindingCopy</b> only in client applications, not in server applications.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/0f85e64f-b4a6-4982-8df5-88caa0a312f6">RpcBindingFree</a>
 

 

