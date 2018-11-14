---
UID: NF:rpcdce.RpcObjectSetInqFn
title: RpcObjectSetInqFn function
author: windows-sdk-content
description: The RpcObjectSetInqFn function registers an object-inquiry function. A null value turns off a previously registered object-inquiry function.
old-location: rpc\rpcobjectsetinqfn.htm
tech.root: rpc
ms.assetid: 358d3ab3-df16-486b-aeac-56a0ffc78272
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: RpcObjectSetInqFn, RpcObjectSetInqFn function [RPC], _rpc_rpcobjectsetinqfn, rpc.rpcobjectsetinqfn, rpcdce/RpcObjectSetInqFn
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
 - RpcObjectSetInqFn
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- RpcObjectSetInqFn
: 
---

# RpcObjectSetInqFn function


## -description


The 
<b>RpcObjectSetInqFn</b> function registers an object-inquiry function. A null value turns off a previously registered object-inquiry function.


## -parameters




### -param InquiryFn

Object-type inquiry function. See 
<a href="https://msdn.microsoft.com/163a5160-1b47-4b65-8f6c-8b009f548ed9">RPC_OBJECT_INQ_FN</a>. When an application calls 
<a href="https://msdn.microsoft.com/9146d4be-4a8a-4655-bd5b-e12f81fd4d23">RpcObjectInqType</a> and the RPC run-time library finds that the specified object is not registered, the run-time library automatically calls 
<b>RpcObjectSetInqFn</b> to determine the object's type.


## -returns



This function returns the following value.

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



A server application calls 
<b>RpcObjectSetInqFn</b> to override the default mapping function that maps object UUIDs to type UUIDs, which determine an object's type. If an application privately maintains an object/type registration, the specified inquiry function returns the type UUID of an object.

The RPC run-time library automatically calls the inquiry function when the application calls 
<a href="https://msdn.microsoft.com/9146d4be-4a8a-4655-bd5b-e12f81fd4d23">RpcObjectInqType</a> and the object of interest was not previously registered with 
<a href="https://msdn.microsoft.com/2fb22b97-97ce-403a-bfcb-101bb63f906f">RpcObjectSetType</a>. The <i>TypeUuid</i> and <i>Status</i> values of the 
<a href="https://msdn.microsoft.com/163a5160-1b47-4b65-8f6c-8b009f548ed9">RPC_OBJECT_INQ_FN</a> function are returned as the output from 
<a href="https://msdn.microsoft.com/9146d4be-4a8a-4655-bd5b-e12f81fd4d23">RpcObjectInqType</a>.




## -see-also




<a href="https://msdn.microsoft.com/9146d4be-4a8a-4655-bd5b-e12f81fd4d23">RpcObjectInqType</a>



<a href="https://msdn.microsoft.com/2fb22b97-97ce-403a-bfcb-101bb63f906f">RpcObjectSetType</a>
 

 

