---
UID: NF:rpcdce.RpcServerRegisterIf
title: RpcServerRegisterIf function
author: windows-sdk-content
description: The RpcServerRegisterIf function registers an interface with the RPC run-time library.
old-location: rpc\rpcserverregisterif.htm
tech.root: Rpc
ms.assetid: f7f6a7c3-ce6c-4b8b-9853-596c39a0e76d
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: RpcServerRegisterIf, RpcServerRegisterIf function [RPC], _rpc_rpcserverregisterif, rpc.rpcserverregisterif, rpcdce/RpcServerRegisterIf
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
 - RpcServerRegisterIf
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# RpcServerRegisterIf function


## -description


The 
<b>RpcServerRegisterIf</b> function registers an interface with the RPC run-time library.
			
		


## -parameters




### -param IfSpec

MIDL-generated structure indicating the interface to register.


### -param MgrTypeUuid

Pointer to a type UUID to associate with the <i>MgrEpv</i> parameter. Specifying a null parameter value (or a nil UUID) registers <i>IfSpec</i> with a nil-type UUID.


### -param MgrEpv

Manager routines' entry-point vector (EPV). To use the MIDL-generated default EPV, specify a null value. For more information, please see <a href="https://msdn.microsoft.com/396e76de-065f-471e-ade9-34770b16a958">RPC_MGR_EPV</a>.


## -returns



Returns RPC_S_OK upon success.

<div class="alert"><b>Note</b>  For a list of valid error codes, see 
<a href="https://msdn.microsoft.com/0223aa7a-b0cf-49e3-9f08-90be5ccffbd1">RPC Return Values</a>.</div>
<div> </div>



## -remarks



A server can register an unlimited number of interfaces with the RPC run-time library. Registration makes an interface available to clients using a binding handle to the server. To register an interface, the server application code calls 
<b>RpcServerRegisterIf</b>. For each implementation of an interface that a server offers, it must register a separate manager EPV.

When calling 
<b>RpcServerRegisterIf</b>, the server provides the following information:

<ul>
<li>Interface specification 


The interface specification is a data structure that the MIDL compiler generates. The server specifies the interface using the <i>IfSpec</i> parameter.

</li>
<li>Manager type UUID and manager EPV 


The manager type UUID and the manager EPV determine which manager routine executes when a server receives a remote procedure call request from a client.

The server specifies the manager type UUID and EPV using the <i>MgrTypeUuid</i> and <i>MgrEpv</i> parameters. Note that when specifying a non-nil manager-type UUID, the server must also call the 
<a href="https://msdn.microsoft.com/2fb22b97-97ce-403a-bfcb-101bb63f906f">RpcObjectSetType</a> function to register objects of this non-nil type.

</li>
</ul>
If your server application needs to register an auto-listen interface or use a callback function for authentication purposes, use 
<a href="https://msdn.microsoft.com/1666bc0a-72bf-40da-b054-c10b477c4367">RpcServerRegisterIfEx</a>.




## -see-also




<a href="https://msdn.microsoft.com/c22e3fa8-98be-461a-b06d-292d3f655ffc">Registering Interfaces</a>



<a href="https://msdn.microsoft.com/fd82fb9f-da0e-46fb-9c11-a75a9b6ee858">RpcBindingFromStringBinding</a>



<a href="https://msdn.microsoft.com/5dcf341f-e392-4608-b741-8fa07cabd50b">RpcBindingSetObject</a>



<a href="https://msdn.microsoft.com/c89d04d7-f607-48cc-8cb6-b6aebab41671">RpcNsBindingExport</a>



<a href="https://msdn.microsoft.com/8dca0490-72aa-41e0-b747-863d53a705ea">RpcNsBindingImportBegin</a>



<a href="https://msdn.microsoft.com/75b7e901-706a-4e3d-b958-d04a0709b993">RpcNsBindingLookupBegin</a>



<a href="https://msdn.microsoft.com/2fb22b97-97ce-403a-bfcb-101bb63f906f">RpcObjectSetType</a>



<a href="https://msdn.microsoft.com/0c05ec68-4f1f-4a54-b6cd-776e9993b7da">RpcServerRegisterIf2</a>



<a href="https://msdn.microsoft.com/D685B7A6-7E22-419F-B476-F0372836D16A">RpcServerRegisterIf3</a>



<a href="https://msdn.microsoft.com/1666bc0a-72bf-40da-b054-c10b477c4367">RpcServerRegisterIfEx</a>



<a href="https://msdn.microsoft.com/bcaf4a0d-8a0d-4016-ab6e-9e1a0fd65d4b">RpcServerUnregisterIf</a>



<a href="https://msdn.microsoft.com/f01eab2c-cd33-4427-9f0c-903e4d3474e9">RpcServerUnregisterIfEx</a>
 

 

