---
UID: NE:rpcasync.tagRpcLocalAddressFormat
title: RpcLocalAddressFormat (rpcasync.h)
description: Specifies the possible local IP address formats supported by RPC.
helpviewer_keywords: ["RpcLocalAddressFormat","RpcLocalAddressFormat enumeration [RPC]","rlafIPv4","rlafIPv6","rlafInvalid","rpc.rpclocaladdressformat","rpcasync/RpcLocalAddressFormat","rpcasync/rlafIPv4","rpcasync/rlafIPv6","rpcasync/rlafInvalid"]
old-location: rpc\rpclocaladdressformat.htm
tech.root: Rpc
ms.assetid: c05610ba-6b00-45e4-b28f-9ce288d08df8
ms.date: 12/05/2018
ms.keywords: RpcLocalAddressFormat, RpcLocalAddressFormat enumeration [RPC], rlafIPv4, rlafIPv6, rlafInvalid, rpc.rpclocaladdressformat, rpcasync/RpcLocalAddressFormat, rpcasync/rlafIPv4, rpcasync/rlafIPv6, rpcasync/rlafInvalid
req.header: rpcasync.h
req.include-header: Rpc.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista, Windows XP with SP2 [desktop apps only]
req.target-min-winversvr: Windows Server 2008, Windows Server 2003 with SP1 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: RpcLocalAddressFormat
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagRpcLocalAddressFormat
 - rpcasync/tagRpcLocalAddressFormat
 - RpcLocalAddressFormat
 - rpcasync/RpcLocalAddressFormat
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
 - RpcLocalAddressFormat
---

# RpcLocalAddressFormat enumeration


## -description

The <b>RpcLocalAddressFormat</b> enumeration specifies the possible local IP address formats supported by RPC.

## -enum-fields

### -field rlafInvalid:0

The address format is not supported.

### -field rlafIPv4

The address format is IP version 4.

### -field rlafIPv6

The address format is IP version 6.

## -see-also

<a href="/windows/desktop/api/rpcasync/ns-rpcasync-rpc_call_local_address_v1">RPC_CALL_LOCAL_ADDRESS_V1</a>
