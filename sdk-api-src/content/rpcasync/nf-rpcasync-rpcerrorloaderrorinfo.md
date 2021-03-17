---
UID: NF:rpcasync.RpcErrorLoadErrorInfo
title: RpcErrorLoadErrorInfo function (rpcasync.h)
description: The RpcErrorLoadErrorInfo function converts a BLOB obtained by a call to RpcErrorSaveErrorInfo into extended error information.
helpviewer_keywords: ["RpcErrorLoadErrorInfo","RpcErrorLoadErrorInfo function [RPC]","_rpc_rpcerrorloaderrorinfo","rpc.rpcerrorloaderrorinfo","rpcasync/RpcErrorLoadErrorInfo"]
old-location: rpc\rpcerrorloaderrorinfo.htm
tech.root: Rpc
ms.assetid: cbd171ee-cef3-4880-a26d-81267cb813e9
ms.date: 12/05/2018
ms.keywords: RpcErrorLoadErrorInfo, RpcErrorLoadErrorInfo function [RPC], _rpc_rpcerrorloaderrorinfo, rpc.rpcerrorloaderrorinfo, rpcasync/RpcErrorLoadErrorInfo
req.header: rpcasync.h
req.include-header: Rpc.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2003 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
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
 - RpcErrorLoadErrorInfo
 - rpcasync/RpcErrorLoadErrorInfo
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
 - RpcErrorLoadErrorInfo
---

# RpcErrorLoadErrorInfo function


## -description

The 
<b>RpcErrorLoadErrorInfo</b> function converts a BLOB obtained by a call to 
<a href="/windows/desktop/api/rpcasync/nf-rpcasync-rpcerrorsaveerrorinfo">RpcErrorSaveErrorInfo</a> into extended error information.

## -parameters

### -param ErrorBlob [in]

Pointer to the BLOB containing the error information.

### -param BlobSize [in]

Size of <i>ErrorBlob</i>, in bytes.

### -param EnumHandle [out]

Pointer to the enumeration handle associated with the extended error information.

## -returns

Successful completion returns RPC_S_OK. The <b>RpcErrorLoadInfo</b> function call can fail if not enough memory is available.

<div class="alert"><b>Note</b>  For a list of valid error codes, see 
<a href="/windows/desktop/Rpc/rpc-return-values">RPC Return Values</a>.</div>
<div> </div>

## -remarks

The BLOB pointed to in <i>ErrorBlob</i> remains the responsibility of the caller. The resulting enumeration is ready for enumeration. EnumHandle is subject to the same requirements of the <i>EnumHandle</i> parameter for 
<a href="/windows/desktop/api/rpcasync/nf-rpcasync-rpcerrorstartenumeration">RpcErrorStartEnumeration</a>. Once enumeration is completed, resources allocated by the enumeration should be freed using the 
<a href="/windows/desktop/api/rpcasync/nf-rpcasync-rpcerrorendenumeration">RpcErrorEndEnumeration</a> function.

## -see-also

<a href="/windows/desktop/Rpc/obtaining-extended-rpc-error-information">Obtaining Extended RPC Error Information</a>



<a href="/windows/desktop/api/rpcasync/ns-rpcasync-rpc_error_enum_handle">RPC_ERROR_ENUM_HANDLE</a>



<a href="/windows/desktop/api/rpcasync/nf-rpcasync-rpcerrorendenumeration">RpcErrorEndEnumeration</a>



<a href="/windows/desktop/api/rpcasync/nf-rpcasync-rpcerrorsaveerrorinfo">RpcErrorSaveErrorInfo</a>



<a href="/windows/desktop/api/rpcasync/nf-rpcasync-rpcerrorstartenumeration">RpcErrorStartEnumeration</a>