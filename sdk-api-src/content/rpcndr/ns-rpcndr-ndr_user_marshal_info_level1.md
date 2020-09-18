---
UID: NS:rpcndr._NDR_USER_MARSHAL_INFO_LEVEL1
title: NDR_USER_MARSHAL_INFO_LEVEL1 (rpcndr.h)
description: The NDR_USER_MARSHAL_INFO_LEVEL1 structure holds information about the state of an RPC call that can be passed to wire_marshal and user_marshal helper functions.
helpviewer_keywords: ["NDR_USER_MARSHAL_INFO_LEVEL1","NDR_USER_MARSHAL_INFO_LEVEL1 structure [RPC]","_rpc_ndr_user_marshal_info_level1","rpc.ndr_user_marshal_info_level1","rpcndr/NDR_USER_MARSHAL_INFO_LEVEL1"]
old-location: rpc\ndr_user_marshal_info_level1.htm
tech.root: Rpc
ms.assetid: fe664968-ce70-4bc4-9caa-3e4d241d253c
ms.date: 12/05/2018
ms.keywords: NDR_USER_MARSHAL_INFO_LEVEL1, NDR_USER_MARSHAL_INFO_LEVEL1 structure [RPC], _rpc_ndr_user_marshal_info_level1, rpc.ndr_user_marshal_info_level1, rpcndr/NDR_USER_MARSHAL_INFO_LEVEL1
req.header: rpcndr.h
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: NDR_USER_MARSHAL_INFO_LEVEL1
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _NDR_USER_MARSHAL_INFO_LEVEL1
 - rpcndr/_NDR_USER_MARSHAL_INFO_LEVEL1
 - NDR_USER_MARSHAL_INFO_LEVEL1
 - rpcndr/NDR_USER_MARSHAL_INFO_LEVEL1
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Rpcndr.h
api_name:
 - NDR_USER_MARSHAL_INFO_LEVEL1
---

# NDR_USER_MARSHAL_INFO_LEVEL1 structure


## -description

The 
<b>NDR_USER_MARSHAL_INFO_LEVEL1</b> structure holds information about the state of an RPC call that can be passed to 
<a href="/windows/desktop/Midl/wire-marshal">wire_marshal</a> and 
<a href="/windows/desktop/Midl/user-marshal">user_marshal</a> helper functions.

## -struct-fields

### -field Buffer

Pointer to the beginning of the marshaling buffer available for use by the helper function. If no buffer is available, this field is null.

### -field BufferSize

Size, in bytes, of the marshaling buffer available for use by the helper function. If no buffer is available, <i>BufferSize</i> is zero.

### -field pfnAllocate

Function used by RPC to allocate memory for the application. An example of the use of this function is to create a node.

### -field pfnFree

Function used by RPC to free memory for the application. An example of the use of this function is to free a node.

### -field pRpcChannelBuffer

If the current call is for a COM interface, this member is a pointer to the channel buffer that RPC uses for the call. Otherwise, this member is null.

### -field Reserved

Reserved for future use.