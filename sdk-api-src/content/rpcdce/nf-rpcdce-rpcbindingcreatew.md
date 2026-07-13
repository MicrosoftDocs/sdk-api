---
UID: NF:rpcdce.RpcBindingCreateW
title: RpcBindingCreateW function (rpcdce.h)
description: The RpcBindingCreate function creates a new fast RPC binding handle based on a supplied template. (Unicode)
helpviewer_keywords: ["RpcBindingCreate", "RpcBindingCreate function [RPC]", "RpcBindingCreateW", "rpc.rpcbindingcreate", "rpcdce/RpcBindingCreate", "rpcdce/RpcBindingCreateW"]
old-location: rpc\rpcbindingcreate.htm
tech.root: Rpc
ms.assetid: 0188512e-bff6-414b-a6eb-19bfe8e0b3a9
ms.date: 12/05/2018
ms.keywords: RpcBindingCreate, RpcBindingCreate function [RPC], RpcBindingCreateA, RpcBindingCreateW, rpc.rpcbindingcreate, rpcdce/RpcBindingCreate, rpcdce/RpcBindingCreateA, rpcdce/RpcBindingCreateW
req.header: rpcdce.h
req.include-header: Rpc.h
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
req.lib: Rpcrt4.lib
req.dll: Rpcrt4.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - RpcBindingCreateW
 - rpcdce/RpcBindingCreateW
dev_langs:
 - c++
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
---

# RpcBindingCreateW function


## -description

The <b>RpcBindingCreate</b> function creates a new fast RPC binding handle based on a supplied template.

## -parameters

### -param Template [in]

<a href="/windows/desktop/api/rpcdce/ns-rpcdce-rpc_binding_handle_template_v1_a">RPC_BINDING_HANDLE_TEMPLATE</a> structure that describes the binding handle to be created by this call. This data may be overwritten during the call, so the API does not maintain a reference to this data. The caller must free the memory used by this structure when the API returns.

### -param Security [in, optional]

<a href="/windows/desktop/api/rpcdce/ns-rpcdce-rpc_binding_handle_security_v1_a">RPC_BINDING_HANDLE_SECURITY</a> structure that describes the security options for this binding handle. This data may be overwritten during the call, so the API does not maintain a reference to this data. The caller must free the memory used by this structure when the API returns.

This parameter is optional. If this parameter is set to <b>NULL</b>, the default security settings for <a href="/windows/desktop/api/rpcdce/ns-rpcdce-rpc_binding_handle_security_v1_a">RPC_BINDING_HANDLE_SECURITY</a> will be used.

### -param Options [in, optional]

<a href="/windows/desktop/api/rpcdce/ns-rpcdce-rpc_binding_handle_options_v1">RPC_BINDING_HANDLE_OPTIONS</a> structure that describes additional options for the binding handle. This data may be overwritten during the call, so the API does not maintain a reference to this data. The caller must free the memory used by this structure when the API returns.

This parameter is optional. If this parameter is set to <b>NULL</b>, the default options for <a href="/windows/desktop/api/rpcdce/ns-rpcdce-rpc_binding_handle_options_v1">RPC_BINDING_HANDLE_OPTIONS</a> will be used.

### -param Binding [out]

<a href="/windows/desktop/Rpc/rpc-binding-handle">RPC_BINDING_HANDLE</a> structure that contains the newly-created binding handle. If this function did not return RPC_S_OK, then the contents of this structure are undefined. For non-local RPC calls, this handle must be passed to <a href="/windows/desktop/api/rpcasync/nf-rpcasync-rpcbindingbind">RpcBindingBind</a>.

## -returns

This function returns RPC_S_OK on success; otherwise, an RPC_S_* error code is returned. For information on these error codes, see <a href="/windows/desktop/Rpc/rpc-return-values">RPC Return Values</a>.

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
<a href="/windows/desktop/Rpc/rpc-return-values">RPC Return Values</a>.</div>
<div> </div>

## -remarks

The RPC binding handle returned by this API can be used with any other functions that accepts a binding handle as a parameter.

However, before any calls can be made on the binding handle, <a href="/windows/desktop/api/rpcasync/nf-rpcasync-rpcbindingbind">RpcBindingBind</a> must be called to make the binding handle available for remote calls. The <b>RpcBindingCreate</b> API does not touch the network or attempt to communicate with the RPC server -- rather, it simply builds an internal data structure based on the values supplied in the template. A successful return does not indicate that the RPC server is available, accessible, or correctly specified.





> [!NOTE]
> The rpcdce.h header defines RpcBindingCreate as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/Rpc/rpc-binding-handle">RPC_BINDING_HANDLE</a>



<a href="/windows/desktop/api/rpcasync/nf-rpcasync-rpcbindingbind">RpcBindingBind</a>
