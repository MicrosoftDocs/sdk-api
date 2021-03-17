---
UID: NF:rpcasync.RpcErrorStartEnumeration
title: RpcErrorStartEnumeration function (rpcasync.h)
description: The RpcErrorStartEnumeration function begins enumeration of extended error information.
helpviewer_keywords: ["RpcErrorStartEnumeration","RpcErrorStartEnumeration function [RPC]","_rpc_rpcerrorstartenumeration","rpc.rpcerrorstartenumeration","rpcasync/RpcErrorStartEnumeration"]
old-location: rpc\rpcerrorstartenumeration.htm
tech.root: Rpc
ms.assetid: 56c61902-4b34-4d92-b352-cd1837754aa3
ms.date: 12/05/2018
ms.keywords: RpcErrorStartEnumeration, RpcErrorStartEnumeration function [RPC], _rpc_rpcerrorstartenumeration, rpc.rpcerrorstartenumeration, rpcasync/RpcErrorStartEnumeration
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
 - RpcErrorStartEnumeration
 - rpcasync/RpcErrorStartEnumeration
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
 - RpcErrorStartEnumeration
---

# RpcErrorStartEnumeration function


## -description

The 
<b>RpcErrorStartEnumeration</b> function begins enumeration of extended error information.

## -parameters

### -param EnumHandle

Pointer to the enumeration handle, in the form of an 
<a href="/windows/desktop/api/rpcasync/ns-rpcasync-rpc_error_enum_handle">RPC_ERROR_ENUM_HANDLE</a> structure. The structure must be allocated by the caller, and cannot be freed until the operation is complete. All members are ignored on input.

## -returns

Successful completion returns RPC_S_OK.

Returns RPC_S_ENTRY_NOT_FOUND if no extended error information is on the thread. If an enumeration is in progress, starting a second enumeration starts from the beginning.

<div class="alert"><b>Note</b>  For a list of valid error codes, see 
<a href="/windows/desktop/Rpc/rpc-return-values">RPC Return Values</a>.</div>
<div> </div>

## -remarks

The RpcErrorStartEnumeration function call should be made immediately after the call that returned the error. Otherwise, extended error information may be overwritten by subsequent calls. Enumeration handles must be freed with the RpcErrorEndEnumeration function.

Once 
<b>RpcErrorStartEnumeration</b> is called, it is safe to use the enumeration handle from a different thread. The 
<b>RpcErrorStartEnumeration</b> function takes a snapshot of the extended error information, and the returning enumeration handle operates on the snapshot. However, enumeration functions are not synchronized between threads by RPC, and so the caller is responsible for doing so. Subsequent calls to 
<b>RpcErrorStartEnumeration</b> begins a new enumeration, and does not create a second enumeration for the same extended error information.

The RpcErrorStartEnumeration function may fail if there is not enough memory to begin the enumeration. The enumeration handle can be passed only to <b>RpcError</b>* functions, and cannot be used with other functions, such as <b>DuplicateHandle</b>.

Advancing the enumeration pointer on one enumeration has no effect on independently started enumerations.

## -see-also

<a href="/windows/desktop/Rpc/obtaining-extended-rpc-error-information">Obtaining Extended RPC Error Information</a>



<a href="/windows/desktop/api/rpcasync/ns-rpcasync-rpc_ee_info_param">RPC_EE_INFO_PARAM</a>



<a href="/windows/desktop/api/rpcasync/ns-rpcasync-rpc_error_enum_handle">RPC_ERROR_ENUM_HANDLE</a>



<a href="/windows/desktop/api/rpcasync/ns-rpcasync-rpc_extended_error_info">RPC_EXTENDED_ERROR_INFO</a>



<a href="/windows/desktop/api/rpcasync/nf-rpcasync-rpcerroraddrecord">RpcErrorAddRecord</a>



<a href="/windows/desktop/api/rpcasync/nf-rpcasync-rpcerrorclearinformation">RpcErrorClearInformation</a>



<a href="/windows/desktop/api/rpcasync/nf-rpcasync-rpcerrorendenumeration">RpcErrorEndEnumeration</a>



<a href="/windows/desktop/api/rpcasync/nf-rpcasync-rpcerrorgetnextrecord">RpcErrorGetNextRecord</a>



<a href="/windows/desktop/api/rpcasync/nf-rpcasync-rpcerrorgetnumberofrecords">RpcErrorGetNumberOfRecords</a>



<a href="/windows/desktop/api/rpcasync/nf-rpcasync-rpcerrorloaderrorinfo">RpcErrorLoadErrorInfo</a>



<a href="/windows/desktop/api/rpcasync/nf-rpcasync-rpcerrorresetenumeration">RpcErrorResetEnumeration</a>



<a href="/windows/desktop/api/rpcasync/nf-rpcasync-rpcerrorsaveerrorinfo">RpcErrorSaveErrorInfo</a>