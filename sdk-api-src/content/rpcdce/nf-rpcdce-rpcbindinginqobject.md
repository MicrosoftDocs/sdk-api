---
UID: NF:rpcdce.RpcBindingInqObject
title: RpcBindingInqObject function
author: windows-sdk-content
description: The RpcBindingInqObject function returns the object UUID from a binding handle.
old-location: rpc\rpcbindinginqobject.htm
tech.root: Rpc
ms.assetid: e2d489f9-d976-4dc3-8a91-dfc04f547165
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: RpcBindingInqObject, RpcBindingInqObject function [RPC], _rpc_rpcbindinginqobject, rpc.rpcbindinginqobject, rpcdce/RpcBindingInqObject
ms.topic: function
req.header: rpcdce.h
req.include-header: Rpc.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
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
 - RpcBindingInqObject
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# RpcBindingInqObject function


## -description


The 
<b>RpcBindingInqObject</b> function returns the object UUID from a binding handle.


## -parameters




### -param Binding

Client or server binding handle.


### -param ObjectUuid

Returns a pointer to the object 
<a href="https://msdn.microsoft.com/72cf12f5-49cd-440d-9665-73211509d050">UUID</a> found in the <i>Binding</i> parameter. <i>ObjectUuid</i> is a unique identifier of an object to which a remote procedure call can be made.


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
</table>
 

<div class="alert"><b>Note</b>  For a list of valid error codes, see 
<a href="https://msdn.microsoft.com/0223aa7a-b0cf-49e3-9f08-90be5ccffbd1">RPC Return Values</a>.</div>
<div> </div>



## -remarks



An application calls the 
<b>RpcBindingInqObject</b> function to see the object 
<a href="https://msdn.microsoft.com/72cf12f5-49cd-440d-9665-73211509d050">UUID</a> associated with a client or server binding handle.




## -see-also




<a href="https://msdn.microsoft.com/5dcf341f-e392-4608-b741-8fa07cabd50b">RpcBindingSetObject</a>
 

 

