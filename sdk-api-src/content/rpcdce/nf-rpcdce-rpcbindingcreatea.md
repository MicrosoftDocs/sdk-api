---
UID: NF:rpcdce.RpcBindingCreateA
title: RpcBindingCreateA function
author: windows-sdk-content
description: The RpcBindingCreate function creates a new fast RPC binding handle based on a supplied template.
old-location: rpc\rpcbindingcreate.htm
old-project: rpc
ms.assetid: 0188512e-bff6-414b-a6eb-19bfe8e0b3a9
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: RpcBindingCreate, RpcBindingCreate function [RPC], RpcBindingCreateA, RpcBindingCreateW, rpc.rpcbindingcreate, rpcdce/RpcBindingCreate, rpcdce/RpcBindingCreateA, rpcdce/RpcBindingCreateW
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: rpcdce.h
req.include-header: Rpc.h
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: RpcBindingCreateW (Unicode) and RpcBindingCreateA (ANSI)
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
 - RpcBindingCreate
 - RpcBindingCreateA
 - RpcBindingCreateW
product: Windows
targetos: Windows
req.lib: Rpcrt4.lib
req.dll: Rpcrt4.dll
req.irql: 
req.product: ADAM
---

# RpcBindingCreateA function


## -description


The <b>RpcBindingCreate</b> function creates a new fast RPC binding handle based on a supplied template.


## -parameters




### -param Template [in]


<a href="https://msdn.microsoft.com/b5712e0b-1751-4e5f-8000-da2a330da202">RPC_BINDING_HANDLE_TEMPLATE</a> structure that describes the binding handle to be created by this call. This data may be overwritten during the call, so the API does not maintain a reference to this data. The caller must free the memory used by this structure when the API returns.


### -param Security [in, optional]


<a href="https://msdn.microsoft.com/b8ea2e96-2e7e-428c-a5cd-dfe9dd341063">RPC_BINDING_HANDLE_SECURITY</a> structure that describes the security options for this binding handle. This data may be overwritten during the call, so the API does not maintain a reference to this data. The caller must free the memory used by this structure when the API returns.

This parameter is optional. If this parameter is set to <b>NULL</b>, the default security settings for <a href="https://msdn.microsoft.com/b8ea2e96-2e7e-428c-a5cd-dfe9dd341063">RPC_BINDING_HANDLE_SECURITY</a> will be used.


### -param Options [in, optional]


<a href="https://msdn.microsoft.com/e2bd03cf-4d45-449f-9434-ec8ef405737b">RPC_BINDING_HANDLE_OPTIONS</a> structure that describes additional options for the binding handle. This data may be overwritten during the call, so the API does not maintain a reference to this data. The caller must free the memory used by this structure when the API returns.

This parameter is optional. If this parameter is set to <b>NULL</b>, the default options for <a href="https://msdn.microsoft.com/e2bd03cf-4d45-449f-9434-ec8ef405737b">RPC_BINDING_HANDLE_OPTIONS</a> will be used.


### -param Binding [out]


<a href="https://msdn.microsoft.com/3e07d9e9-04d8-4f94-8104-cd0ee89a9407">RPC_BINDING_HANDLE</a> structure that contains the newly-created binding handle. If this function did not return RPC_S_OK, then the contents of this structure are undefined. For non-local RPC calls, this handle must be passed to <a href="https://msdn.microsoft.com/dbc73a66-b1ca-4a53-b662-430b611f8c20">RpcBindingBind</a>.


## -returns



This function returns RPC_S_OK on success; otherwise, an RPC_S_* error code is returned. For information on these error codes, see <a href="https://msdn.microsoft.com/0223aa7a-b0cf-49e3-9f08-90be5ccffbd1">RPC Return Values</a>.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>RPC_S_OK</b></dt>
</dl>
</td>
<td width="60%">
The binding handle was successfully created.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>RPC_S_CANNOT_SUPPORT</b></dt>
</dl>
</td>
<td width="60%">
An obsolete feature of RPC was requested for this binding handle.

<div class="alert"><b>Note</b>  The only supported protocol sequences for this API is <b>ncalrpc</b>; choosing another protocol sequence results in the return of this error status code.</div>
<div> </div>
</td>
</tr>
</table>
 

<div class="alert"><b>Note</b>  For a list of valid error codes, see 
<a href="https://msdn.microsoft.com/0223aa7a-b0cf-49e3-9f08-90be5ccffbd1">RPC Return Values</a>.</div>
<div> </div>



## -remarks



The RPC binding handle returned by this API can be used with any other functions that accepts a binding handle as a parameter.

However, before any calls can be made on the binding handle, <a href="https://msdn.microsoft.com/dbc73a66-b1ca-4a53-b662-430b611f8c20">RpcBindingBind</a> must be called to make the binding handle available for remote calls. The <b>RpcBindingCreate</b> API does not touch the network or attempt to communicate with the RPC server -- rather, it simply builds an internal data structure based on the values supplied in the template. A successful return does not indicate that the RPC server is available, accessible, or correctly specified.




## -see-also




<a href="https://msdn.microsoft.com/3e07d9e9-04d8-4f94-8104-cd0ee89a9407">RPC_BINDING_HANDLE</a>



<a href="https://msdn.microsoft.com/dbc73a66-b1ca-4a53-b662-430b611f8c20">RpcBindingBind</a>
 

 

