---
UID: NF:rpcdce.RpcObjectSetType
title: RpcObjectSetType function
author: windows-sdk-content
description: The RpcObjectSetType function assigns the type of an object.
old-location: rpc\rpcobjectsettype.htm
tech.root: rpc
ms.assetid: 2fb22b97-97ce-403a-bfcb-101bb63f906f
ms.author: windowssdkdev
ms.date: 09/13/2018
ms.keywords: RpcObjectSetType, RpcObjectSetType function [RPC], _rpc_rpcobjectsettype, rpc.rpcobjectsettype, rpcdce/RpcObjectSetType
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
 - RpcObjectSetType
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# RpcObjectSetType function


## -description


The 
<b>RpcObjectSetType</b> function assigns the type of an object.


## -parameters




### -param ObjUuid

Pointer to an object UUID to associate with the type UUID in the <i>TypeUuid</i> parameter.


### -param TypeUuid

Pointer to the type UUID of the <i>ObjUuid</i> parameter. 




Specify a parameter value of NULL or a nil UUID to reset the object type to the default association of object UUID/nil-type UUID.


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
<dt><b>RPC_S_INVALID_OBJECT</b></dt>
</dl>
</td>
<td width="60%">
The object is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>RPC_S_ALREADY_REGISTERED</b></dt>
</dl>
</td>
<td width="60%">
The object is already registered.

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



A server application calls 
<b>RpcObjectSetType</b> to assign a type UUID to an object UUID. By default, the RPC run-time library automatically assigns all object UUIDs with the nil-type UUID. A server application that contains one implementation of an interface (one manager entry-point vector [EPV]) does not need to call 
<b>RpcObjectSetType</b> provided that the server registered the interface with the nil-type UUID (see under 
<a href="https://msdn.microsoft.com/f7f6a7c3-ce6c-4b8b-9853-596c39a0e76d">RpcServerRegisterIf</a>).

A server application that contains multiple implementations of an interface (multiple manager EPVs—that is, multiple type UUIDs) calls 
<b>RpcObjectSetType</b> once for each different object UUID/non-nil type UUID association the server supports. Associating each object with a type UUID tells the RPC run-time library which manager EPV (interface implementation) to use when the server receives a remote procedure call for a non-nil object UUID.

The RPC run-time library allows an application to set the type for an unlimited number of objects. To remove the association between an object UUID and its type UUID (established by calling 
<b>RpcObjectSetType</b>), a server calls 
<b>RpcObjectSetType</b> again, specifying a null value or a nil UUID for the <i>TypeUuid</i> parameter. This resets the object UUID/type UUID association to the default association of object UUID/nil-type UUID. A server cannot assign a type to the nil object UUID. The RPC run-time library automatically assigns the nil object UUID a nil-type UUID.

For detailed information, see 
<a href="https://msdn.microsoft.com/c22e3fa8-98be-461a-b06d-292d3f655ffc">Registering Interfaces</a>.




## -see-also




<a href="https://msdn.microsoft.com/c22e3fa8-98be-461a-b06d-292d3f655ffc">Registering
		  Interfaces</a>



<a href="https://msdn.microsoft.com/f7f6a7c3-ce6c-4b8b-9853-596c39a0e76d">RpcServerRegisterIf</a>
 

 

