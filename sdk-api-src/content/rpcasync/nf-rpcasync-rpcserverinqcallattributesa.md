---
UID: NF:rpcasync.RpcServerInqCallAttributesA
title: RpcServerInqCallAttributesA function (rpcasync.h)
description: The RpcServerInqCallAttributes function is an RPC server call that obtains client security context attributes. (ANSI)
helpviewer_keywords: ["RpcServerInqCallAttributesA", "rpcasync/RpcServerInqCallAttributesA"]
old-location: rpc\rpcserverinqcallattributes.htm
tech.root: Rpc
ms.assetid: 563b70ed-bc9a-40be-a77b-17b993cc64f3
ms.date: 12/05/2018
ms.keywords: RpcServerInqCallAttributes, RpcServerInqCallAttributes function [RPC], RpcServerInqCallAttributesA, RpcServerInqCallAttributesW, _rpc_rpcserverinqcallattributes, rpc.rpcserverinqcallattributes, rpcasync/RpcServerInqCallAttributes, rpcasync/RpcServerInqCallAttributesA, rpcasync/RpcServerInqCallAttributesW
req.header: rpcasync.h
req.include-header: Rpc.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: RpcServerInqCallAttributesW (Unicode) and RpcServerInqCallAttributesA (ANSI)
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
 - RpcServerInqCallAttributesA
 - rpcasync/RpcServerInqCallAttributesA
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
 - RpcServerInqCallAttributes
 - RpcServerInqCallAttributesA
 - RpcServerInqCallAttributesW
---

# RpcServerInqCallAttributesA function


## -description

The 
<b>RpcServerInqCallAttributes</b> function is an RPC server call that obtains client security context attributes.

## -parameters

### -param ClientBinding [in]

Optional. For explicit binding within a server routine, <i>ClientBinding</i> is the binding handle with which the manager routine was called. See Remarks.

### -param RpcCallAttributes [in, out]

<a href="/windows/desktop/api/rpcasync/ns-rpcasync-rpc_call_attributes_v2_a">RPC_CALL_ATTRIBUTES_V2</a> structure that receives call attributes.

## -returns

Returns RPC_S_OK upon success, and <i>RpcCallAttributes</i> is filled. If ERROR_MORE_DATA is returned, one or more fields in <i>RpcCallAttributes</i> was of insufficient length and could not be filled. See Remarks in 
<a href="/windows/desktop/api/rpcasync/ns-rpcasync-rpc_call_attributes_v2_a">RPC_CALL_ATTRIBUTES_V2</a> for details on handling ERROR_MORE_DATA.

Upon failure, the contents of <i>RpcCallAttributes</i> is undefined and may be partially modified by RPC.

<div class="alert"><b>Note</b>  For a list of valid error codes, see 
<a href="/windows/desktop/Rpc/rpc-return-values">RPC Return Values</a>.</div>
<div> </div>

## -remarks

The 
<b>RpcServerInqCallAttributes</b> function uses a versioning scheme to incorporate new capabilities without having to introduce new functions with suffix identifiers. For example, a second version of the 
<a href="/windows/desktop/api/rpcasync/ns-rpcasync-rpc_call_attributes_v2_a">RPC_CALL_ATTRIBUTES_V2</a>, identified with a simple #define in the header, can add new members to facilitate new functionality built into future versions of the 
<b>RpcServerInqCallAttributes</b> function, without having to release a function called RpcServerInqCallAttributesEx.

If the 
<b>RpcServerInqCallAttributes</b> function is called outside a server routine, and if the function call queries the security context attributes for an asynchronous RPC call, <i>ClientBinding</i> can be retrieved by calling the 
<a href="/windows/desktop/api/rpcasync/nf-rpcasync-rpcasyncgetcallhandle">RpcAsyncGetCallHandle</a> function from the asynchronous handle.

The 
<b>RpcServerInqCallAttributes</b> function is not supported for datagram protocol sequences, such as ncadg_*. If invoked on a call that executes on a datagram protocol sequence, RPC_S_CANNOT_SUPPORT is returned.

The 
<b>RpcServerInqCallAttributes</b> function is thread-safe.


#### Examples


```cpp
RPC_CALL_ATTRIBUTES CallAttributes;  // this maps to RPC_CALL_ATTRIBUTES_V1

memset(&CallAttributes, 0, sizeof(CallAttributes));
CallAttributes.Version = RPC_CALL_ATTRIBUTES_VERSION;    // maps to 1
CallAttributes.Flags = ;//....
Status = RpcServerInqCallAttributes(0, &ClientContextAttributes);

```






> [!NOTE]
> The rpcasync.h header defines RpcServerInqCallAttributes as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/rpcasync/ns-rpcasync-rpc_call_attributes_v2_a">RPC_CALL_ATTRIBUTES_V2</a>



<a href="/windows/desktop/api/rpcasync/nf-rpcasync-rpcasyncgetcallhandle">RpcAsyncGetCallHandle</a>
