---
UID: NS:rpcasync._RPC_CALL_LOCAL_ADDRESS_V1
title: RPC_CALL_LOCAL_ADDRESS_V1 (rpcasync.h)
description: Contains information about the local address on which a call was made.
helpviewer_keywords: ["*PRPC_CALL_LOCAL_ADDRESS_V1","RPC_CALL_LOCAL_ADDRESS","RPC_CALL_LOCAL_ADDRESS structure [RPC]","RPC_CALL_LOCAL_ADDRESS_V1","RPC_CALL_LOCAL_ADDRESS_V1 structure [RPC]","RPC_CALL_LOCAL_ADDRESS_V1_A","RPC_CALL_LOCAL_ADDRESS_V1_W","rpc.rpc_call_local_address_v1","rpcasync/RPC_CALL_LOCAL_ADDRESS","rpcasync/RPC_CALL_LOCAL_ADDRESS_V1","rpcasync/RPC_CALL_LOCAL_ADDRESS_V1_A","rpcasync/RPC_CALL_LOCAL_ADDRESS_V1_W"]
old-location: rpc\rpc_call_local_address_v1.htm
tech.root: Rpc
ms.assetid: 2dda59dc-d2e5-4d98-a12a-f86557dcb1c0
ms.date: 12/05/2018
ms.keywords: '*PRPC_CALL_LOCAL_ADDRESS_V1, RPC_CALL_LOCAL_ADDRESS, RPC_CALL_LOCAL_ADDRESS structure [RPC], RPC_CALL_LOCAL_ADDRESS_V1, RPC_CALL_LOCAL_ADDRESS_V1 structure [RPC], RPC_CALL_LOCAL_ADDRESS_V1_A, RPC_CALL_LOCAL_ADDRESS_V1_W, rpc.rpc_call_local_address_v1, rpcasync/RPC_CALL_LOCAL_ADDRESS, rpcasync/RPC_CALL_LOCAL_ADDRESS_V1, rpcasync/RPC_CALL_LOCAL_ADDRESS_V1_A, rpcasync/RPC_CALL_LOCAL_ADDRESS_V1_W'
req.header: rpcasync.h
req.include-header: Rpc.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: RPC_CALL_LOCAL_ADDRESS_V1_W (Unicode) and RPC_CALL_LOCAL_ADDRESS_V1_A (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: RPC_CALL_LOCAL_ADDRESS_V1, *PRPC_CALL_LOCAL_ADDRESS_V1
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _RPC_CALL_LOCAL_ADDRESS_V1
 - rpcasync/_RPC_CALL_LOCAL_ADDRESS_V1
 - PRPC_CALL_LOCAL_ADDRESS_V1
 - rpcasync/PRPC_CALL_LOCAL_ADDRESS_V1
 - RPC_CALL_LOCAL_ADDRESS_V1
 - rpcasync/RPC_CALL_LOCAL_ADDRESS_V1
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
 - RPC_CALL_LOCAL_ADDRESS_V1
 - RPC_CALL_LOCAL_ADDRESS_V1_A
 - RPC_CALL_LOCAL_ADDRESS_V1_W
---

# RPC_CALL_LOCAL_ADDRESS_V1 structure


## -description

The <b>RPC_CALL_LOCAL_ADDRESS_V1</b> structure  contains information about the local address on which a call was made.

## -struct-fields

### -field Version

Version of the <b>RPC_CALL_LOCAL_ADDRESS</b> structure. For this structure, this value must be set to 1.

### -field Buffer

Pointer to a user-supplied opaque data block that contains the local address.

### -field BufferSize

On input, this member contains the size of the buffer pointed to by the <b>Buffer</b> member, in bytes. On output, it contains the actual number of bytes written to buffer. For example, if the buffer is allocated a size of 8 bytes, but the local address written to it is 4, this parameter will specify 8 on input and contain 4 on output.

### -field AddressFormat

<a href="/windows/desktop/api/rpcasync/ne-rpcasync-rpclocaladdressformat">RpcLocalAddressFormat</a> enumeration values that specifies the format of the local address written to <b>Buffer</b>. For this version of the structure, only IPv4 and IPv6 addresses  are supported; if another is specified, RPC_S_CANNOT_SUPPORT is returned.

## -see-also

<a href="/windows/desktop/api/rpcasync/ns-rpcasync-rpc_call_attributes_v2_a">RPC_CALL_ATTRIBUTES_V2</a>