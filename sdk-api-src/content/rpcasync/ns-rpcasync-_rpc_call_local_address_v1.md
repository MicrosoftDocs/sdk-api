---
UID: NS:rpcasync._RPC_CALL_LOCAL_ADDRESS_V1
title: "_RPC_CALL_LOCAL_ADDRESS_V1"
author: windows-sdk-content
description: Contains information about the local address on which a call was made.
old-location: rpc\rpc_call_local_address_v1.htm
tech.root: rpc
ms.assetid: 2dda59dc-d2e5-4d98-a12a-f86557dcb1c0
ms.author: windowssdkdev
ms.date: 09/14/2018
ms.keywords: "*PRPC_CALL_LOCAL_ADDRESS_V1, RPC_CALL_LOCAL_ADDRESS, RPC_CALL_LOCAL_ADDRESS structure [RPC], RPC_CALL_LOCAL_ADDRESS_V1, RPC_CALL_LOCAL_ADDRESS_V1 structure [RPC], RPC_CALL_LOCAL_ADDRESS_V1_A, RPC_CALL_LOCAL_ADDRESS_V1_W, _RPC_CALL_LOCAL_ADDRESS_V1, rpc.rpc_call_local_address_v1, rpcasync/RPC_CALL_LOCAL_ADDRESS, rpcasync/RPC_CALL_LOCAL_ADDRESS_V1, rpcasync/RPC_CALL_LOCAL_ADDRESS_V1_A, rpcasync/RPC_CALL_LOCAL_ADDRESS_V1_W"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
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
product: Windows
targetos: Windows
req.typenames: RPC_CALL_LOCAL_ADDRESS_V1, *PRPC_CALL_LOCAL_ADDRESS_V1
req.redist: 
---

# _RPC_CALL_LOCAL_ADDRESS_V1 structure


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


<a href="https://msdn.microsoft.com/c05610ba-6b00-45e4-b28f-9ce288d08df8">RpcLocalAddressFormat</a> enumeration values that specifies the format of the local address written to <b>Buffer</b>. For this version of the structure, only IPv4 and IPv6 addresses  are supported; if another is specified, RPC_S_CANNOT_SUPPORT is returned.


## -see-also




<a href="https://msdn.microsoft.com/eccc4b78-19f8-415f-bd0f-b1f9f454435e">RPC_CALL_ATTRIBUTES_V2</a>
 

 

