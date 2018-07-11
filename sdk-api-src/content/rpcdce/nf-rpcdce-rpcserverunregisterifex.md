---
UID: NF:rpcdce.RpcServerUnregisterIfEx
title: RpcServerUnregisterIfEx function
author: windows-sdk-content
description: The RpcServerUnregisterIfEx function removes an interface from the RPC run-time library registry. This function extends the functionality of the RpcServerUnregisterIf function.
old-location: rpc\rpcserverunregisterifex.htm
old-project: rpc
ms.assetid: f01eab2c-cd33-4427-9f0c-903e4d3474e9
ms.author: windowssdkdev
ms.date: 05/31/2018
ms.keywords: RpcServerUnregisterIfEx, RpcServerUnregisterIfEx function [RPC], _rpc_rpcserverunregisterifex, rpc.rpcserverunregisterifex, rpcdce/RpcServerUnregisterIfEx
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: rpcdce.h
req.include-header: Rpc.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: RPC_CALL_LOCAL_ADDRESS_V1, *PRPC_CALL_LOCAL_ADDRESS_V1
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Rpcrt4.dll
api_name:
 - RpcServerUnregisterIfEx
product: Windows
targetos: Windows
req.lib: Rpcrt4.lib
req.dll: Rpcrt4.dll
req.irql: 
req.product: ADAM
---

# RpcServerUnregisterIfEx function


## -description


The 
<b>RpcServerUnregisterIfEx</b> function removes an interface from the RPC run-time library registry. This function extends the functionality of the 
<a href="https://msdn.microsoft.com/bcaf4a0d-8a0d-4016-ab6e-9e1a0fd65d4b">RpcServerUnregisterIf</a> function.


## -parameters




### -param IfSpec [in]

Interface to remove from the registry. 




Specify a null value to remove all interfaces previously registered with the type UUID value specified in the <i>MgrTypeUuid</i> parameter.


### -param MgrTypeUuid [in]

Pointer to the type UUID of the manager entry-point vector (EPV) to remove from the registry. The value of <i>MgrTypeUuid</i> should be the same value as was provided in a call to the 
<a href="https://msdn.microsoft.com/f7f6a7c3-ce6c-4b8b-9853-596c39a0e76d">RpcServerRegisterIf</a> function, <a href="https://msdn.microsoft.com/0c05ec68-4f1f-4a54-b6cd-776e9993b7da">RpcServerRegisterIf2</a> function, or the 
<a href="https://msdn.microsoft.com/1666bc0a-72bf-40da-b054-c10b477c4367">RpcServerRegisterIfEx</a> function. 




Specify a null value to remove the interface specified in the <i>IfSpec</i> parameter for all previously registered type UUIDs from the registry.

Specify a nil UUID to remove the MIDL-generated default manager EPV from the registry. In this case, all manager EPVs registered with a non-nil type UUID remain registered.


### -param RundownContextHandles [in]

Specifies whether rundown is called for active context handles. If non-zero, the rundown is called once all calls on the interface have completed. If set to zero, the RPC run time assumes the server has already destroyed its portion of the context handle and it will not call the rundown routines.


## -returns



Returns RPC status. 
<b>RpcServerUnregisterIfEx</b> does not fail unless supplied with invalid values.

<div class="alert"><b>Note</b>  For a list of valid error codes, see 
<a href="https://msdn.microsoft.com/0223aa7a-b0cf-49e3-9f08-90be5ccffbd1">RPC Return Values</a>.</div>
<div> </div>



## -remarks



The 
<b>RpcServerUnregisterIfEx</b> function waits for all calls on a given interface to complete before unregistering the context handles.

The 
<b>RpcServerUnregisterIfEx</b> function supplies all the functionality provided in the 
<a href="https://msdn.microsoft.com/bcaf4a0d-8a0d-4016-ab6e-9e1a0fd65d4b">RpcServerUnregisterIf</a> function. In addition, the 
<b>RpcServerUnregisterIfEx</b> function unregisters all context handles registered by the given interface. The interface must use the <b>strict_context_handle</b> attribute, otherwise the results are undefined.

<b>RpcServerUnregisterIfEx</b> is the only function that provides safe unloading of a DLL with active context handles outside of process shutdown. It is available on Windows XP and later versions of Windows only.




## -see-also




<a href="https://msdn.microsoft.com/396e76de-065f-471e-ade9-34770b16a958">RPC_MGR_EPV</a>



<a href="https://msdn.microsoft.com/c22e3fa8-98be-461a-b06d-292d3f655ffc">Registering Interfaces</a>



<a href="https://msdn.microsoft.com/f7f6a7c3-ce6c-4b8b-9853-596c39a0e76d">RpcServerRegisterIf</a>



<a href="https://msdn.microsoft.com/0c05ec68-4f1f-4a54-b6cd-776e9993b7da">RpcServerRegisterIf2</a>



<a href="https://msdn.microsoft.com/1666bc0a-72bf-40da-b054-c10b477c4367">RpcServerRegisterIfEx</a>



<a href="https://msdn.microsoft.com/bcaf4a0d-8a0d-4016-ab6e-9e1a0fd65d4b">RpcServerUnregisterIf</a>



<a href="https://msdn.microsoft.com/a1f0408c-7739-4fca-b9b2-f045dad0c392">Using Context
		  Handles</a>
 

 

