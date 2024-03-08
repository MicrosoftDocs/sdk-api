---
UID: NS:rpcasync.tagRPC_CALL_ATTRIBUTES_V1_W
title: RPC_CALL_ATTRIBUTES_V1_W (rpcasync.h)
description: The RPC_CALL_ATTRIBUTES_V1 structure provides parameters to the RpcServerInqCallAttributes function. Implemented in ANSI and UNICODE versions for Windows XP and Windows Server 2003 operating systems. (Unicode)
helpviewer_keywords: ["RPC_CALL_ATTRIBUTES_V1","RPC_CALL_ATTRIBUTES_V1 structure [RPC]","RPC_CALL_ATTRIBUTES_V1_A","RPC_CALL_ATTRIBUTES_V1_W","rpc.rpc_call_attributes_v1","rpcasync/RPC_CALL_ATTRIBUTES_V1","rpcasync/RPC_CALL_ATTRIBUTES_V1_A","rpcasync/RPC_CALL_ATTRIBUTES_V1_W"]
old-location: rpc\rpc_call_attributes_v1.htm
tech.root: Rpc
ms.assetid: 62988900-e794-4d91-861e-f72d854249fe
ms.date: 12/05/2018
ms.keywords: RPC_CALL_ATTRIBUTES_V1, RPC_CALL_ATTRIBUTES_V1 structure [RPC], RPC_CALL_ATTRIBUTES_V1_A, RPC_CALL_ATTRIBUTES_V1_W, rpc.rpc_call_attributes_v1, rpcasync/RPC_CALL_ATTRIBUTES_V1, rpcasync/RPC_CALL_ATTRIBUTES_V1_A, rpcasync/RPC_CALL_ATTRIBUTES_V1_W
req.header: rpcasync.h
req.include-header: Rpc.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: RPC_CALL_ATTRIBUTES_V1_W (Unicode) and RPC_CALL_ATTRIBUTES_V1_A (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: RPC_CALL_ATTRIBUTES_V1_W
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagRPC_CALL_ATTRIBUTES_V1_W
 - rpcasync/tagRPC_CALL_ATTRIBUTES_V1_W
 - RPC_CALL_ATTRIBUTES_V1_W
 - rpcasync/RPC_CALL_ATTRIBUTES_V1_W
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Rpcasync.h
api_name:
 - RPC_CALL_ATTRIBUTES_V1
 - RPC_CALL_ATTRIBUTES_V1_A
 - RPC_CALL_ATTRIBUTES_V1_W
---

# RPC_CALL_ATTRIBUTES_V1_W structure


## -description

The 
<b>RPC_CALL_ATTRIBUTES_V1</b> structure provides parameters to the 
<a href="/windows/desktop/api/rpcasync/nf-rpcasync-rpcserverinqcallattributesa">RpcServerInqCallAttributes</a> function. Implemented in ANSI and UNICODE versions for Windows XP and Windows Server 2003 operating systems.

## -struct-fields

### -field Version

Version of the 
<a href="/windows/desktop/api/rpcasync/nf-rpcasync-rpcserverinqcallattributesa">RpcServerInqCallAttributes</a> function being used by the calling application. See Remarks.

### -field Flags

Bitmask specifying valid flags to request RPC_QUERY_SERVER_PRINCIPAL_NAME or RPC_QUERY_CLIENT_PRINCIPAL_NAME. See Remarks.

### -field ServerPrincipalNameBufferLength

Length of <b>ServerPrincipalName</b>, in bytes. If insufficient, <b>ServerPrincipalName</b> is unchanged, and <b>ServerPrincipalNameBufferLength</b> indicates the required buffer length including the terminating <b>NULL</b> character, and ERROR_MORE_DATA is returned. If <b>ServerPrincipalNameBufferLength</b> is longer than necessary, upon return it is set to the actual length used, in bytes, including the terminating <b>NULL</b> character. See Remarks. 




If the protocol sequence does not support retrieving a server principal name, <b>ServerPrincipalNameBufferLength</b> is set to zero on return, and the buffer pointed by <b>ServerPrincipalName</b> is unmodified. <b>Windows XP:  </b>Only the <b>ncacn_*</b> group of protocol sequences support retrieving the server principal name.



If the RPC_QUERY_SERVER_PRINCIPAL_NAME flag is not specified, <b>ServerPrincipalNameBufferLength</b> is ignored. If <b>ServerPrincipalNameBufferLength</b> is nonzero and <b>ServerPrincipalName</b> is <b>NULL</b>, ERROR_INVALID_PARAMETER is returned.

### -field ServerPrincipalName

Pointer to the server principal name, if requested in <b>Flags</b> and supported by the protocol sequence. Upon any return value other than RPC_S_OK or ERROR_MORE_DATA, the content of <b>ServerPrincipalName</b> is undefined and may have been modified by RPC.

### -field ClientPrincipalNameBufferLength

Length of the buffer pointed to by <b>ClientPrincipalName</b>, in bytes. If insufficient, <b>ClientPrincipalName</b> is unchanged, and <b>ClientPrincipalNameBufferLength</b> indicates the required buffer length including the terminating <b>NULL</b> character, and ERROR_MORE_DATA is returned. If <b>ClientPrincipalNameBufferLength</b> is longer than necessary, upon return it is set to the actual length used, in bytes, including the terminating <b>NULL</b> character. 




If the protocol sequence does not support retrieving a client principal name, <b>ClientPrincipalNameBufferLength</b> is set to zero on return, and the buffer pointed by <b>ClientPrincipalName</b> is unmodified. <b>Windows XP:  </b>Only the <b>ncalrpc</b> protocol sequence supports retrieving the client principal name.



If the RPC_QUERY_CLIENT_PRINCIPAL_NAME flag is not specified, <b>ClientPrincipalNameBufferLength</b> is ignored. If <b>ClientPrincipalNameBufferLength</b> is nonzero and <b>ClientPrincipalName</b> is <b>NULL</b>, ERROR_INVALID_PARAMETER is returned.

### -field ClientPrincipalName

Pointer to the client principal name, if requested in <b>Flags</b> member and supported by the protocol sequence. Upon any return value other than RPC_S_OK or ERROR_MORE_DATA, the content of <b>ClientPrincipalName</b> is undefined and may have been modified by RPC.

### -field AuthenticationLevel

Authentication level for the call. See 
<a href="/windows/desktop/Rpc/authentication-level-constants">Authentication-Level Constants</a> for authentication levels supported by RPC.

### -field AuthenticationService

Authentication service, or security provider, used to make the remote procedure call.

### -field NullSession

Specifies whether a <b>Null</b> session is used. Zero indicates the call is not coming over a <b>Null</b> session; any other value indicates a <b>Null</b> session.

## -remarks

The 
<b>RPC_CALL_ATTRIBUTES</b> structure uses a versioning scheme to enable the 
<b>RpcServerInqCallAttributes</b> function to incorporate new capabilities without having to introduce new functions with suffix identifiers. For example, a second version of the 
<b>RPC_CALL_ATTRIBUTES</b>, identified with a simple #define in the header, can add new members to facilitate new functionality built into future versions of the 
<b>RpcServerInqCallAttributes</b> function, without having to release a corresponding alternative function.

The <b>Version</b> member indicates the version of the 
<b>RPC_CALL_ATTRIBUTES</b> structure (currently either <b>RPC_CALL_ATTRIBUTES_V1</b> or <b>RPC_CALL_ATTRIBUTES_V2</b>) being used by the calling application. This identification enables the RPC run time to provide backward compatibility for applications not using the most current version of the structure.

Specifying RPC_QUERY_SERVER_PRINCIPAL_NAME in the <b>Flags</b> member directs 
<b>RpcServerInqCallAttributes</b> to return the server principal name in <b>ServerPrincipalName</b>. If RPC_QUERY_SERVER_PRINCIPAL_NAME is not specified, 
<b>RpcServerInqCallAttributes</b> does not modify the pointer passed in <b>ServerPrincipalName</b> and does not store anything in that memory location. Specifying RPC_QUERY_CLIENT_PRINCIPAL_NAME in the <b>Flags</b> member directs 
<b>RpcServerInqCallAttributes</b> to return the client principal name in <b>ClientPrincipalName</b>. If RPC_QUERY_CLIENT_PRINCIPAL_NAME is not specified, 
<b>RpcServerInqCallAttributes</b> does not modify the pointer passed in <b>ClientPrincipalName</b> and does not store anything in that memory location.

The best processing mechanism when both client and server principal names are being retrieved is to store the length of <b>ClientPrincipalNameBufferLength</b> and <b>ServerPrincipalNameBufferLength</b>, and if ERROR_MORE_DATA is returned, compare the stored lengths with the lengths returned in those members. The member with a stored value smaller than or equal to the returned value has returned successfully, indicating that the other member had an insufficient buffer. In the subsequent call, omit the flag for the successfully returned principal name; this avoids processing associated with another retrieval and copy of the successfully returned principal name.

The 
<b>RPC_CALL_ATTRIBUTES_V1</b> structure is usually called in two ways:

<ul>
<li>First approach: zero is specified for the <b>ServerPrincipalNameBufferLength</b> or <b>ClientPrincipalNameBufferLength</b> member on the first 
<b>RpcServerInqCallAttributes</b> function call to retrieve the required buffer length, or to determine whether the protocol supports returning the principal name. Upon retrieving the required buffer length, a buffer is allocated of the required length and a second call is made to get the real length of the buffer.</li>
<li>Second approach: the caller begins with a reasonable buffer, often allocated on the stack, and if ERROR_MORE_DATA is returned, a buffer of the required length is allocated and the 
<a href="/windows/desktop/api/rpcasync/nf-rpcasync-rpcserverinqcallattributesa">RpcServerInqCallAttributes</a> function is called again.</li>
</ul>
The second method offers the best performance in most cases, since the caller does not need to perform a memory allocation.


#### Examples


```cpp
RPC_CALL_ATTRIBUTES CallAttributes;  // this maps to RPC_CALL_ATTRIBUTES_V1

memset(&CallAttributes, 0, sizeof(CallAttributes));
CallAttributes.Version = RPC_CALL_ATTRIBUTES_VERSION;    // maps to 1
CallAttributes.Flags = ;//....
Status = RpcServerInqCallAttributes(0, &CallAttributes);

```

## -see-also

<a href="/windows/desktop/Rpc/authentication-level-constants">Authentication-Level Constants</a>



<a href="/windows/desktop/api/rpcasync/nf-rpcasync-rpcserverinqcallattributesa">RpcServerInqCallAttributes</a>
