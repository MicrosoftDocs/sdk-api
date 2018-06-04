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

# RpcNsBindingLookupDone function


## -description


The 
<b>RpcNsBindingLookupDone</b> function signifies that a client has finished looking for compatible servers and deletes the lookup context.
<div class="alert"><b>Note</b>  This function is not supported on Windows Vista and later operating systems.</div><div> </div>

## -parameters




### -param LookupContext

Pointer to the name-service handle to free. The name-service handle <i>LookupContext</i> points to is created by calling the 
<a href="https://msdn.microsoft.com/75b7e901-706a-4e3d-b958-d04a0709b993">RpcNsBindingLookupBegin</a> function. 




An argument value of <b>NULL</b> is returned.


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
</table>
 

<div class="alert"><b>Note</b>  For a list of valid error codes, see 
<a href="https://msdn.microsoft.com/0223aa7a-b0cf-49e3-9f08-90be5ccffbd1">RPC Return Values</a>.</div>
<div> </div>



## -remarks



The 
<b>RpcNsBindingLookupDone</b> function frees a lookup context created by calling the 
<a href="https://msdn.microsoft.com/75b7e901-706a-4e3d-b958-d04a0709b993">RpcNsBindingLookupBegin</a> function.

Typically, a client application calls 
<b>RpcNsBindingLookupDone</b> after completing remote procedure calls to a server using a binding handle returned from the 
<a href="https://msdn.microsoft.com/068913fb-f9ca-4e03-93d7-3484ba43472e">RpcNsBindingLookupNext</a> function. However, a client application is responsible for calling 
<b>RpcNsBindingLookupDone</b> for each created lookup context, regardless of the status returned from the 
<b>RpcNsBindingLookupNext</b> function or the success in making remote procedure calls.




## -see-also




<a href="https://msdn.microsoft.com/75b7e901-706a-4e3d-b958-d04a0709b993">RpcNsBindingLookupBegin</a>



<a href="https://msdn.microsoft.com/068913fb-f9ca-4e03-93d7-3484ba43472e">RpcNsBindingLookupNext</a>
 

 

