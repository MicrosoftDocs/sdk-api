---
UID: NS:rpcasync.tagRPC_CALL_ATTRIBUTES_V2_W
title: RPC_CALL_ATTRIBUTES_V2_W (rpcasync.h)
description: The RPC_CALL_ATTRIBUTES_V2 structure provides parameters to the RpcServerInqCallAttributes function. Version 2 specifies support for local addresses and client process IDs. (Unicode)
helpviewer_keywords: ["RPC_CALL_ATTRIBUTES","RPC_CALL_ATTRIBUTES structure [RPC]","RPC_CALL_ATTRIBUTES_V2","RPC_CALL_ATTRIBUTES_V2 structure [RPC]","RPC_CALL_ATTRIBUTES_V2_A","RPC_CALL_ATTRIBUTES_V2_W","RPC_CALL_STATUS_CANCELLED","RPC_CALL_STATUS_DISCONNECTED","RPC_CALL_STATUS_IN_PROGRESS","RPC_QUERY_CALL_LOCAL_ADDRESS","RPC_QUERY_CLIENT_PID","RPC_QUERY_CLIENT_PRINCIPAL_NAME","RPC_QUERY_SERVER_PRINCIPAL_NAME","rpc.rpc_call_attributes_v2","rpcasync/RPC_CALL_ATTRIBUTES","rpcasync/RPC_CALL_ATTRIBUTES_V2","rpcasync/RPC_CALL_ATTRIBUTES_V2_A","rpcasync/RPC_CALL_ATTRIBUTES_V2_W"]
old-location: rpc\rpc_call_attributes_v2.htm
tech.root: Rpc
ms.assetid: eccc4b78-19f8-415f-bd0f-b1f9f454435e
ms.date: 12/05/2018
ms.keywords: RPC_CALL_ATTRIBUTES, RPC_CALL_ATTRIBUTES structure [RPC], RPC_CALL_ATTRIBUTES_V2, RPC_CALL_ATTRIBUTES_V2 structure [RPC], RPC_CALL_ATTRIBUTES_V2_A, RPC_CALL_ATTRIBUTES_V2_W, RPC_CALL_STATUS_CANCELLED, RPC_CALL_STATUS_DISCONNECTED, RPC_CALL_STATUS_IN_PROGRESS, RPC_QUERY_CALL_LOCAL_ADDRESS, RPC_QUERY_CLIENT_PID, RPC_QUERY_CLIENT_PRINCIPAL_NAME, RPC_QUERY_SERVER_PRINCIPAL_NAME, rpc.rpc_call_attributes_v2, rpcasync/RPC_CALL_ATTRIBUTES, rpcasync/RPC_CALL_ATTRIBUTES_V2, rpcasync/RPC_CALL_ATTRIBUTES_V2_A, rpcasync/RPC_CALL_ATTRIBUTES_V2_W
req.header: rpcasync.h
req.include-header: Rpc.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: RPC_CALL_ATTRIBUTES_V2_W (Unicode) and RPC_CALL_ATTRIBUTES_V2_A (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: RPC_CALL_ATTRIBUTES_V2_W
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagRPC_CALL_ATTRIBUTES_V2_W
 - rpcasync/tagRPC_CALL_ATTRIBUTES_V2_W
 - RPC_CALL_ATTRIBUTES_V2_W
 - rpcasync/RPC_CALL_ATTRIBUTES_V2_W
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
 - RPC_CALL_ATTRIBUTES_V2
 - RPC_CALL_ATTRIBUTES_V2_A
 - RPC_CALL_ATTRIBUTES_V2_W
---

# RPC_CALL_ATTRIBUTES_V2_W structure


## -description

The <b>RPC_CALL_ATTRIBUTES_V2</b> structure provides parameters to the 
<a href="/windows/desktop/api/rpcasync/nf-rpcasync-rpcserverinqcallattributesa">RpcServerInqCallAttributes</a> function.  Version 2 specifies support for local addresses and client process IDs.

## -struct-fields

### -field Version

Version of the <b>RPC_CALL_ATTRIBUTES</b> structure. For this structure, this value must be set to 2.

### -field Flags

Bitmasked flags that indicate which members of this structure should be populated by the call to  <a href="/windows/desktop/api/rpcasync/nf-rpcasync-rpcserverinqcallattributesa">RpcServerInqCallAttributes</a> to which this structure was passed.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="RPC_QUERY_SERVER_PRINCIPAL_NAME"></a><a id="rpc_query_server_principal_name"></a><dl>
<dt><b>RPC_QUERY_SERVER_PRINCIPAL_NAME</b></dt>
</dl>
</td>
<td width="60%">
Indicates that <a href="/windows/desktop/api/rpcasync/nf-rpcasync-rpcserverinqcallattributesa">RpcServerInqCallAttributes</a> should populate the <b>ServerPrincipalName</b> member of this structure.

</td>
</tr>
<tr>
<td width="40%"><a id="RPC_QUERY_CLIENT_PRINCIPAL_NAME"></a><a id="rpc_query_client_principal_name"></a><dl>
<dt><b>RPC_QUERY_CLIENT_PRINCIPAL_NAME</b></dt>
</dl>
</td>
<td width="60%">
Indicates that <a href="/windows/desktop/api/rpcasync/nf-rpcasync-rpcserverinqcallattributesa">RpcServerInqCallAttributes</a> should populate the <b>ClientPrincipalName</b> member of this structure.

</td>
</tr>
<tr>
<td width="40%"><a id="RPC_QUERY_CALL_LOCAL_ADDRESS"></a><a id="rpc_query_call_local_address"></a><dl>
<dt><b>RPC_QUERY_CALL_LOCAL_ADDRESS</b></dt>
</dl>
</td>
<td width="60%">
Indicates that <a href="/windows/desktop/api/rpcasync/nf-rpcasync-rpcserverinqcallattributesa">RpcServerInqCallAttributes</a> should populate the <b>CallLocalAddress</b> member of this structure.

</td>
</tr>
<tr>
<td width="40%"><a id="RPC_QUERY_CLIENT_PID"></a><a id="rpc_query_client_pid"></a><dl>
<dt><b>RPC_QUERY_CLIENT_PID</b></dt>
</dl>
</td>
<td width="60%">
Indicates that <a href="/windows/desktop/api/rpcasync/nf-rpcasync-rpcserverinqcallattributesa">RpcServerInqCallAttributes</a> should populate the <b>ClientPID</b> member of this structure. This flag is only supported for the ncalrpc protocol sequence.

</td>
</tr>
</table>

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

### -field KernelModeCaller

### -field ProtocolSequence

Constant that indicates the protocol sequence over which the call was made.

### -field IsClientLocal

<a href="/windows/desktop/api/rpcasync/ne-rpcasync-rpccallclientlocality">RpcCallClientLocality</a> enumeration value that indicates the locality of the client (local, remote, or unknown).

### -field ClientPID

Handle that contains the process ID of the calling client. This field is only supported for the ncalrpc protocol sequence, and is populated only when <b>RPC_QUERY_CLIENT_PID</b> is specified in the <i>Flags</i> parameter.

### -field CallStatus

Bit field that specifies the status of the RPC call.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="RPC_CALL_STATUS_IN_PROGRESS"></a><a id="rpc_call_status_in_progress"></a><dl>
<dt><b>RPC_CALL_STATUS_IN_PROGRESS</b></dt>
<dt>0x01</dt>
</dl>
</td>
<td width="60%">
The call is in progress.

</td>
</tr>
<tr>
<td width="40%"><a id="RPC_CALL_STATUS_CANCELLED"></a><a id="rpc_call_status_cancelled"></a><dl>
<dt><b>RPC_CALL_STATUS_CANCELLED</b></dt>
<dt>0x02</dt>
</dl>
</td>
<td width="60%">
The call was canceled.

</td>
</tr>
<tr>
<td width="40%"><a id="RPC_CALL_STATUS_DISCONNECTED"></a><a id="rpc_call_status_disconnected"></a><dl>
<dt><b>RPC_CALL_STATUS_DISCONNECTED</b></dt>
<dt>0x03</dt>
</dl>
</td>
<td width="60%">
The client has disconnected.

</td>
</tr>
</table>

### -field CallType

<a href="/windows/desktop/api/rpcasync/ne-rpcasync-rpccalltype">RpcCallType</a> enumeration value that indicates the  type of the RPC call.

### -field CallLocalAddress

Pointer to a <a href="/windows/desktop/api/rpcasync/ns-rpcasync-rpc_call_local_address_v1">RPC_CALL_LOCAL_ADDRESS</a> structure that contains information to the server about the local address on which the call was made. 

This field must not be <b>NULL</b> if <b>RPC_QUERY_CALL_LOCAL_ADDRESS</b> is specified in <i>Flags</i>; otherwise, RPC_S_INVALID_ARG is returned.

If the buffer supplied by the application is insufficient, <a href="/windows/desktop/api/rpcasync/nf-rpcasync-rpcserverinqcallattributesa">RpcServerInqCallAttributes</a> returns ERROR_MORE_DATA.

### -field OpNum

The opnum value associated with the call in the corresponding IDL file.

### -field InterfaceUuid

The interface UUID on which the call is made.


#### - KernelMode

Specifies whether or not the call came from kernel mode. Zero indicates the call is not coming from kernel mode; any other value indicates that it was made from kernel mode.

## -remarks

The 
<b>RPC_CALL_ATTRIBUTES</b> structure uses a versioning scheme to enable the 
<a href="/windows/desktop/api/rpcasync/nf-rpcasync-rpcserverinqcallattributesa">RpcServerInqCallAttributes</a> function to incorporate new capabilities without having to introduce new functions with suffix identifiers. For example, a second version of the 
<b>RPC_CALL_ATTRIBUTES</b>, identified with a simple #define in the header, can add new members to facilitate new functionality built into future versions of the 
<b>RpcServerInqCallAttributes</b> function, without having to release a corresponding alternative function.

The <b>Version</b> member indicates the version of the 
<b>RPC_CALL_ATTRIBUTES</b> structure (currently either <b>RPC_CALL_ATTRIBUTES_V1</b> or <b>RPC_CALL_ATTRIBUTES_V2</b>) being used by the calling application. This identification enables the RPC run time to provide backward compatibility for applications not using the most current version of the structure.

 Until the process terminates, <b>ClientPID</b> uniquely identifies that process on the client. When the process terminates, the process ID specified by <b>ClientPID</b> can be used by new processes.

## -see-also

<a href="/windows/desktop/api/rpcasync/nf-rpcasync-rpcserverinqcallattributesa">RpcServerInqCallAttributes</a>
