---
UID: NS:rpcndr._NDR_USER_MARSHAL_INFO_LEVEL1
title: "_NDR_USER_MARSHAL_INFO_LEVEL1"
author: windows-driver-content
description: The NDR_USER_MARSHAL_INFO_LEVEL1 structure holds information about the state of an RPC call that can be passed to wire_marshal and user_marshal helper functions.
old-location: rpc\ndr_user_marshal_info_level1.htm
old-project: Rpc
ms.assetid: fe664968-ce70-4bc4-9caa-3e4d241d253c
ms.author: windowsdriverdev
ms.date: 4/24/2018
ms.keywords: NDR_USER_MARSHAL_INFO_LEVEL1, NDR_USER_MARSHAL_INFO_LEVEL1 structure [RPC], _NDR_USER_MARSHAL_INFO_LEVEL1, _rpc_ndr_user_marshal_info_level1, rpc.ndr_user_marshal_info_level1, rpcndr/NDR_USER_MARSHAL_INFO_LEVEL1
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
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
req.typenames: NDR_USER_MARSHAL_INFO_LEVEL1
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Rpcndr.h
api_name:
-	NDR_USER_MARSHAL_INFO_LEVEL1
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# _NDR_USER_MARSHAL_INFO_LEVEL1 structure


## -description


The 
<b>NDR_USER_MARSHAL_INFO_LEVEL1</b> structure holds information about the state of an RPC call that can be passed to 
<a href="midl.wire_marshal">wire_marshal</a> and 
<a href="midl.user_marshal">user_marshal</a> helper functions.


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

