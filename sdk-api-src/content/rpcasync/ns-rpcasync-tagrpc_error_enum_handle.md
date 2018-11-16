---
UID: NS:rpcasync.tagRPC_ERROR_ENUM_HANDLE
title: tagRPC_ERROR_ENUM_HANDLE
author: windows-sdk-content
description: The RPC_ERROR_ENUM_HANDLE structure provides an enumeration handle used by RpcError* functions for processing extended error information.
old-location: rpc\rpc_error_enum_handle.htm
tech.root: Rpc
ms.assetid: d6fbd0ad-b63e-4fb8-bebb-1b2b2552a8c8
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: RPC_ERROR_ENUM_HANDLE, RPC_ERROR_ENUM_HANDLE structure [RPC], _rpc_rpc_error_enum_handle, rpc.rpc_error_enum_handle, rpcasync/RPC_ERROR_ENUM_HANDLE, tagRPC_ERROR_ENUM_HANDLE
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: rpcasync.h
req.include-header: Rpc.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Rpcasync.h
api_name:
 - RPC_ERROR_ENUM_HANDLE
product: Windows
targetos: Windows
req.typenames: RPC_ERROR_ENUM_HANDLE
req.redist: 
---

# tagRPC_ERROR_ENUM_HANDLE structure


## -description


The 
<b>RPC_ERROR_ENUM_HANDLE</b> structure provides an enumeration handle used by <b>RpcError</b>* functions for processing extended error information. All members of the 
<b>RPC_ERROR_ENUM_HANDLE</b> structure are used internally by the RPC Runtime, and should not be read or changed by applications. Applications should treat the 
<b>RPC_ERROR_ENUM_HANDLE</b> as an opaque value used as a handle.


## -struct-fields


## -see-also




<a href="https://msdn.microsoft.com/7a386def-c640-42f4-9869-b6a1c522984a">Obtaining Extended RPC Error Information</a>



<a href="https://msdn.microsoft.com/a201f8f3-6e74-4550-9738-d5415340994b">RPC_EE_INFO_PARAM</a>



<a href="https://msdn.microsoft.com/1e906192-c9f1-41c2-bf7f-9967a3d0e1d3">RPC_EXTENDED_ERROR_INFO</a>



<a href="https://msdn.microsoft.com/b82708ef-0760-49b0-87d2-3d55a07b351f">RpcErrorAddRecord</a>



<a href="https://msdn.microsoft.com/ff96904c-285d-4d39-af3b-bf295c29e62f">RpcErrorClearInformation</a>



<a href="https://msdn.microsoft.com/04da6e7d-bbdb-47d3-9924-604ddf56d177">RpcErrorEndEnumeration</a>



<a href="https://msdn.microsoft.com/cc2d3aa0-2956-4710-ad31-a347d9ef9043">RpcErrorGetNextRecord</a>



<a href="https://msdn.microsoft.com/1b498cc8-9ee5-47bd-a484-33bf1c89413c">RpcErrorGetNumberOfRecords</a>



<a href="https://msdn.microsoft.com/cbd171ee-cef3-4880-a26d-81267cb813e9">RpcErrorLoadErrorInfo</a>



<a href="https://msdn.microsoft.com/fb41b923-7fd3-4058-9f5f-df4018d9b872">RpcErrorResetEnumeration</a>



<a href="https://msdn.microsoft.com/59a3ba71-10bd-47d1-91b0-eba5ffa5051b">RpcErrorSaveErrorInfo</a>



<a href="https://msdn.microsoft.com/56c61902-4b34-4d92-b352-cd1837754aa3">RpcErrorStartEnumeration</a>
 

 

