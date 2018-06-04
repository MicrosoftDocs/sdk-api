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

# RpcMgmtSetServerStackSize function


## -description


The 
<b>RpcMgmtSetServerStackSize</b> function specifies the stack size for server threads created by the RPC run time.


## -parameters




### -param ThreadStackSize

Stack size allocated for each thread created by the RPC run time, in bytes. This value is applied to all threads created for the server, but not to threads already created. Select this value based on the stack requirements of the remote procedures offered by the server.


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
<dt><b>RPC_S_INVALID_ARG</b></dt>
</dl>
</td>
<td width="60%">
The argument was invalid.

</td>
</tr>
</table>
 

<div class="alert"><b>Note</b>  For a list of valid error codes, see 
<a href="https://msdn.microsoft.com/0223aa7a-b0cf-49e3-9f08-90be5ccffbd1">RPC Return Values</a>.</div>
<div> </div>



## -remarks



A server application calls the 
<b>RpcMgmtSetServerStackSize</b> function to specify the thread stack size to use when the RPC run-time library creates call threads for executing remote procedure calls.

Servers that know the stack requirements of all the manager functions in the interfaces it offers can call the 
<b>RpcMgmtSetServerStackSize</b> function to ensure that each call thread has the necessary stack size.

Calling 
<b>RpcMgmtSetServerStackSize</b> is optional. If a server does not call 
<b>RpcMgmtSetServerStackSize</b>, the default thread stack size from the executable image is used.




## -see-also




<a href="https://msdn.microsoft.com/430561b2-c74b-423c-8448-339cc71dbd68">RpcServerListen</a>
 

 

