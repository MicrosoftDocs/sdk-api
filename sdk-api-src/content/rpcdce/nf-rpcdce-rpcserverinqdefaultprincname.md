---
UID: NF:rpcdce.RpcServerInqDefaultPrincName
title: RpcServerInqDefaultPrincName function
author: windows-sdk-content
description: The RpcServerInqDefaultPrincName function obtains the default principal name for a given authentication service.
old-location: rpc\rpcserverinqdefaultprincname.htm
tech.root: rpc
ms.assetid: b265e0ae-cdef-450e-bf16-25da5bea7d5e
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: RpcServerInqDefaultPrincName, RpcServerInqDefaultPrincName function [RPC], RpcServerInqDefaultPrincNameA, RpcServerInqDefaultPrincNameW, _rpc_rpcserverinqdefaultprincname, rpc.rpcserverinqdefaultprincname, rpcdce/RpcServerInqDefaultPrincName, rpcdce/RpcServerInqDefaultPrincNameA, rpcdce/RpcServerInqDefaultPrincNameW
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: rpcdce.h
req.include-header: Rpc.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: RpcServerInqDefaultPrincNameW (Unicode) and RpcServerInqDefaultPrincNameA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Rpcrt4.lib
req.dll: Rpcrt4.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Rpcrt4.dll
api_name:
 - RpcServerInqDefaultPrincName
 - RpcServerInqDefaultPrincNameA
 - RpcServerInqDefaultPrincNameW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# RpcServerInqDefaultPrincName function


## -description


The 
<b>RpcServerInqDefaultPrincName</b> function obtains the default principal name for a given authentication service.


## -parameters




### -param AuthnSvc

Authentication service to use when the server receives a request for a remote procedure call.


### -param PrincName

Upon success, contains the default principal name for the given authentication service as specified by the <i>AuthnSvc</i> parameter. The authentication service in use defines the content of the name and its syntax. This principal name must be used as the <i>ServerPrincName</i> parameter of the <a href="https://msdn.microsoft.com/b7a7b57e-540b-460b-9eec-6246cc1fd9d3">RpcServerRegisterAuthInfo</a> function. If the function succeeds, <i>PrincName</i> must be freed using the <a href="https://msdn.microsoft.com/07226282-1091-4479-adc8-b2f604c645e7">RpcStringFree</a> function. If the function fails, the contents of <i>PrincName</i> is undefined and the caller has no obligation to free it.


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
There is insufficient memory to complete the operation.

</td>
</tr>
</table>
 

<div class="alert"><b>Note</b>  For a list of valid error codes, see 
<a href="https://msdn.microsoft.com/0223aa7a-b0cf-49e3-9f08-90be5ccffbd1">RPC Return Values</a>.</div>
<div> </div>



## -remarks



This function is the recommended way to obtain the server principal name to be passed to the <a href="https://msdn.microsoft.com/b7a7b57e-540b-460b-9eec-6246cc1fd9d3">RpcServerRegisterAuthInfo</a> function. While composing the server principal name is possible without using this function, calling the function is easier and more portable across operating system versions.




## -see-also




<a href="https://msdn.microsoft.com/2db946b6-6a0d-402c-89ef-68c7489aa7ee">RpcBindingSetAuthInfo</a>



<a href="https://msdn.microsoft.com/b7a7b57e-540b-460b-9eec-6246cc1fd9d3">RpcServerRegisterAuthInfo</a>
 

 

