---
UID: NF:rpcdce.RpcServerRegisterIf3
title: RpcServerRegisterIf3 function
author: windows-sdk-content
description: The RpcServerRegisterIf3 function registers an interface with the RPC run-time library.
old-location: rpc\rpcserverregisterif3.htm
tech.root: rpc
ms.assetid: D685B7A6-7E22-419F-B476-F0372836D16A
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: RpcServerRegisterIf3, RpcServerRegisterIf3 function [RPC], rpc.rpcserverregisterif3, rpcdce/RpcServerRegisterIf3
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: rpcdce.h
req.include-header: Rpc.h
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
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
 - RpcServerRegisterIf3
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# RpcServerRegisterIf3 function


## -description


The 
<b>RpcServerRegisterIf3</b> function registers an interface with the RPC run-time library.


## -parameters




### -param IfSpec [in]

MIDL-generated  structure indicating the interface to register.


### -param MgrTypeUuid [in, optional]

Pointer to a type <b>UUID</b> to associate with the <i>MgrEpv</i> parameter. Specifying a <b>null</b> parameter value (or a nil <b>UUID</b>) registers <i>IfSpec</i> with a nil-type <b>UUID</b>.


### -param MgrEpv [in, optional]

Manager routines' entry-point vector (EPV). To use the MIDL-generated default EPV, specify a <b>null</b> value. For more information, please see <a href="https://msdn.microsoft.com/396e76de-065f-471e-ade9-34770b16a958">RPC_MGR_EPV</a>.


### -param Flags [in]

Flags. For a list of flag values, see 
<a href="https://msdn.microsoft.com/387311c0-13df-4497-a0ac-ce6aec0e726c">Interface Registration Flags</a>.


### -param MaxCalls [in]

Maximum number of concurrent remote procedure call requests the server can accept on an <b>auto-listen</b> interface. The <i>MaxCalls</i> parameter is only applicable on an <b>auto-listen</b> interface, and is ignored on interfaces that are not <b>auto-listen</b>. The RPC run-time library makes its best effort to ensure the server does not allow more concurrent call requests than the number of calls specified in <i>MaxCalls</i>. The actual number can be greater and can vary for each protocol sequence. 




Calls on other interfaces are governed by the value of the process-wide <i>MaxCalls</i> parameter specified in the 
<a href="https://msdn.microsoft.com/430561b2-c74b-423c-8448-339cc71dbd68">RpcServerListen</a> function call.

If the number of concurrent calls is not a concern, you can achieve slightly better server-side performance by specifying the default value using RPC_C_LISTEN_MAX_CALLS_DEFAULT. Doing so relieves the RPC run-time environment from enforcing an unnecessary restriction.


### -param MaxRpcSize [in]

Maximum size of incoming data blocks, in bytes. This parameter may be used to help prevent malicious denial-of-service attacks. If the data block of a remote procedure call is larger than <i>MaxRpcSize</i>, the RPC run-time library rejects the call and sends an RPC_S_ACCESS_DENIED error to the client. Specifying a value of (unsigned int) –1 for this parameter removes the limit on the size of incoming data blocks. This parameter has no effect on calls made over the <a href="https://msdn.microsoft.com/0009f794-5c14-4484-9023-cb20c7030dc5">ncalrpc</a> protocol.


### -param IfCallback [in, optional]

Security-callback function, or <b>NULL</b> for no callback. Each registered interface can have a different callback function. See the Remarks on <a href="https://msdn.microsoft.com/0c05ec68-4f1f-4a54-b6cd-776e9993b7da">RpcServerRegisterIf2</a>.


### -param SecurityDescriptor [in, optional]

Security descriptor for accessing the RPC interface. Each registered interface can have a different security descriptor.


## -returns



Returns RPC_S_OK upon success.

<div class="alert"><b>Note</b>  For a list of valid error codes, see 
<a href="https://msdn.microsoft.com/0223aa7a-b0cf-49e3-9f08-90be5ccffbd1">RPC Return Values</a>.</div>
<div> </div>



## -remarks



The parameters and effects of the 
<b>RpcServerRegisterIf3</b> function extend those of the 
<a href="https://msdn.microsoft.com/0c05ec68-4f1f-4a54-b6cd-776e9993b7da">RpcServerRegisterIf2</a> function. The difference is the ability to specify a security descriptor for controlling access to the registered RPC interface.

If both <i>SecurityDescriptor</i> and <i>IfCallbackFn</i> are specified, the security descriptor in <i>SecurityDescriptor</i> will be checked first and the callback in <i>IfCallbackFn</i> will be called after the access check against the security descriptor passes.

When calling <b>RpcServerRegisterIf3</b> with <i>SecurityDescriptor</i> set to <b>NULL</b>, or calling <a href="https://msdn.microsoft.com/f7f6a7c3-ce6c-4b8b-9853-596c39a0e76d">RpcServerRegisterIf</a>, <a href="https://msdn.microsoft.com/0c05ec68-4f1f-4a54-b6cd-776e9993b7da">RpcServerRegisterIf2</a>, or <a href="https://msdn.microsoft.com/1666bc0a-72bf-40da-b054-c10b477c4367">RpcServerRegisterIfEx</a> to register an interface, a default security descriptor will be used. The default security descriptor will not allow access from any AppContainer process to the interface if the RPC server is not an AppContainer process. The default security descriptor will not allow access from any process in other AppContainer processes to the interface if the RPC server is an AppContainer process. The default security descriptor will allow access from normal processes including Low integrity processes.




## -see-also




<a href="https://msdn.microsoft.com/c22e3fa8-98be-461a-b06d-292d3f655ffc">Registering Interfaces</a>



<a href="https://msdn.microsoft.com/993dfa23-4303-4601-b05d-70158e5e87ed">RpcGetAuthorizationContextForClient</a>



<a href="https://msdn.microsoft.com/f7f6a7c3-ce6c-4b8b-9853-596c39a0e76d">RpcServerRegisterIf</a>



<a href="https://msdn.microsoft.com/0c05ec68-4f1f-4a54-b6cd-776e9993b7da">RpcServerRegisterIf2</a>



<a href="https://msdn.microsoft.com/1666bc0a-72bf-40da-b054-c10b477c4367">RpcServerRegisterIfEx</a>



<a href="https://msdn.microsoft.com/bcaf4a0d-8a0d-4016-ab6e-9e1a0fd65d4b">RpcServerUnregisterIf</a>



<a href="https://msdn.microsoft.com/f01eab2c-cd33-4427-9f0c-903e4d3474e9">RpcServerUnregisterIfEx</a>
 

 

