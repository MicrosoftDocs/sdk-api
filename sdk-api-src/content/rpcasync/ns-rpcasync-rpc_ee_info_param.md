---
UID: NS:rpcasync.tagRPC_EE_INFO_PARAM
title: RPC_EE_INFO_PARAM (rpcasync.h)
description: The RPC_EE_INFO_PARAM structure is used to store extended error information.
helpviewer_keywords: ["RPC_EE_INFO_PARAM","RPC_EE_INFO_PARAM structure [RPC]","_rpc_rpc_ee_info_param","rpc.rpc_ee_info_param","rpcasync/RPC_EE_INFO_PARAM"]
old-location: rpc\rpc_ee_info_param.htm
tech.root: Rpc
ms.assetid: a201f8f3-6e74-4550-9738-d5415340994b
ms.date: 12/05/2018
ms.keywords: RPC_EE_INFO_PARAM, RPC_EE_INFO_PARAM structure [RPC], _rpc_rpc_ee_info_param, rpc.rpc_ee_info_param, rpcasync/RPC_EE_INFO_PARAM
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
req.typenames: RPC_EE_INFO_PARAM
req.redist: 
ms.custom: 19H1
f1_keywords:
 - tagRPC_EE_INFO_PARAM
 - rpcasync/tagRPC_EE_INFO_PARAM
 - RPC_EE_INFO_PARAM
 - rpcasync/RPC_EE_INFO_PARAM
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
 - RPC_EE_INFO_PARAM
---

# RPC_EE_INFO_PARAM structure


## -description

The 
<b>RPC_EE_INFO_PARAM</b> structure is used to store extended error information.

## -struct-fields

### -field ParameterType

Type of parameter being provided as extended error information. This value determines which union member(s) is used. Valid values are the following: 




<ul>
<li><b>eeptAnsiString</b> to specify an ANSI string, indicating the value is provided in <b>AnsiString</b>.</li>
<li><b>eeptUnicodeString</b> to specify a Unicode string, indicating the value is provided in <b>UnicodeString</b>.</li>
<li><b>eeptLongVal</b> to specify a LONG value, indicating the value is provided in <b>LVal</b>.</li>
<li><b>eeptShortVal</b> to specify a SHORT value, indicating the values is provided in <b>SVal</b>.</li>
<li><b>eeptPointerVal</b> to specify a pointer value, indicating the values is provided in <b>PVal</b>.</li>
<li><b>eeptBinary</b> is used by the RPC Runtime and should not be used or specified by applications.</li>
<li><b>eeptNone</b> indicates the parameter contained either a Unicode or ANSI string, but was truncated due to lack of memory or network fragment length limitations.</li>
</ul>

### -field u

### -field u.AnsiString

ANSI string representing the extended error information.

### -field u.UnicodeString

Unicode string representing the extended error information.

### -field u.LVal

Long value representing the extended error information.

### -field u.SVal

Short value representing the extended error information.

### -field u.PVal

ULONGLONG value representing the extended error information.

### -field u.BVal

Reserved.

## -remarks

The 
<b>RPC_EE_INFO_PARAM</b> structure is used in conjunction with the <b>RpcError</b>* functions to investigate and create extended RPC error information.

## -see-also

<a href="/windows/desktop/Rpc/obtaining-extended-rpc-error-information">Obtaining Extended RPC Error Information</a>



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



<a href="/windows/desktop/api/rpcasync/nf-rpcasync-rpcerrorstartenumeration">RpcErrorStartEnumeration</a>