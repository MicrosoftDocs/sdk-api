---
UID: NS:rpcasync.tagRPC_ERROR_ENUM_HANDLE
title: RPC_ERROR_ENUM_HANDLE (rpcasync.h)
description: The RPC_ERROR_ENUM_HANDLE structure provides an enumeration handle used by RpcError* functions for processing extended error information.
helpviewer_keywords: ["RPC_ERROR_ENUM_HANDLE","RPC_ERROR_ENUM_HANDLE structure [RPC]","_rpc_rpc_error_enum_handle","rpc.rpc_error_enum_handle","rpcasync/RPC_ERROR_ENUM_HANDLE"]
old-location: rpc\rpc_error_enum_handle.htm
tech.root: Rpc
ms.assetid: d6fbd0ad-b63e-4fb8-bebb-1b2b2552a8c8
ms.date: 12/05/2018
ms.keywords: RPC_ERROR_ENUM_HANDLE, RPC_ERROR_ENUM_HANDLE structure [RPC], _rpc_rpc_error_enum_handle, rpc.rpc_error_enum_handle, rpcasync/RPC_ERROR_ENUM_HANDLE
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
targetos: Windows
req.typenames: RPC_ERROR_ENUM_HANDLE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagRPC_ERROR_ENUM_HANDLE
 - rpcasync/tagRPC_ERROR_ENUM_HANDLE
 - RPC_ERROR_ENUM_HANDLE
 - rpcasync/RPC_ERROR_ENUM_HANDLE
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
 - RPC_ERROR_ENUM_HANDLE
---

# RPC_ERROR_ENUM_HANDLE structure


## -description

The 
<b>RPC_ERROR_ENUM_HANDLE</b> structure provides an enumeration handle used by <b>RpcError</b>* functions for processing extended error information. All members of the 
<b>RPC_ERROR_ENUM_HANDLE</b> structure are used internally by the RPC Runtime, and should not be read or changed by applications. Applications should treat the 
<b>RPC_ERROR_ENUM_HANDLE</b> as an opaque value used as a handle.

## -struct-fields

## -see-also

<a href="/windows/desktop/Rpc/obtaining-extended-rpc-error-information">Obtaining Extended RPC Error Information</a>



<a href="/windows/desktop/api/rpcasync/ns-rpcasync-rpc_ee_info_param">RPC_EE_INFO_PARAM</a>



<a href="/windows/desktop/api/rpcasync/ns-rpcasync-rpc_extended_error_info">RPC_EXTENDED_ERROR_INFO</a>



<a href="/windows/desktop/api/rpcasync/nf-rpcasync-rpcerroraddrecord">RpcErrorAddRecord</a>



<a href="/windows/desktop/api/rpcasync/nf-rpcasync-rpcerrorclearinformation">RpcErrorClearInformation</a>



<a href="/windows/desktop/api/rpcasync/nf-rpcasync-rpcerrorendenumeration">RpcErrorEndEnumeration</a>



<a href="/windows/desktop/api/rpcasync/nf-rpcasync-rpcerrorgetnextrecord">RpcErrorGetNextRecord</a>



<a href="/windows/desktop/api/rpcasync/nf-rpcasync-rpcerrorgetnumberofrecords">RpcErrorGetNumberOfRecords</a>



<a href="/windows/desktop/api/rpcasync/nf-rpcasync-rpcerrorloaderrorinfo">RpcErrorLoadErrorInfo</a>



<a href="/windows/desktop/api/rpcasync/nf-rpcasync-rpcerrorresetenumeration">RpcErrorResetEnumeration</a>



<a href="/windows/desktop/api/rpcasync/nf-rpcasync-rpcerrorsaveerrorinfo">RpcErrorSaveErrorInfo</a>



<a href="/windows/desktop/api/rpcasync/nf-rpcasync-rpcerrorstartenumeration">RpcErrorStartEnumeration</a>