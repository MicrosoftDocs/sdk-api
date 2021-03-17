---
UID: NF:rpcasync.RpcErrorAddRecord
title: RpcErrorAddRecord function (rpcasync.h)
description: The RpcErrorAddRecord function adds extended error information to a chain of extended error information records.
helpviewer_keywords: ["RpcErrorAddRecord","RpcErrorAddRecord function [RPC]","_rpc_rpcerroraddrecord","rpc.rpcerroraddrecord","rpcasync/RpcErrorAddRecord"]
old-location: rpc\rpcerroraddrecord.htm
tech.root: Rpc
ms.assetid: b82708ef-0760-49b0-87d2-3d55a07b351f
ms.date: 12/05/2018
ms.keywords: RpcErrorAddRecord, RpcErrorAddRecord function [RPC], _rpc_rpcerroraddrecord, rpc.rpcerroraddrecord, rpcasync/RpcErrorAddRecord
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
 - RpcErrorAddRecord
 - rpcasync/RpcErrorAddRecord
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
 - RpcErrorAddRecord
---

# RpcErrorAddRecord function


## -description

The 
<b>RpcErrorAddRecord</b> function adds extended error information to a chain of extended error information records.

## -parameters

### -param ErrorInfo [in]

Error information to be added, in the form of an 
<a href="/windows/desktop/api/rpcasync/ns-rpcasync-rpc_extended_error_info">RPC_EXTENDED_ERROR_INFO</a> structure.

## -returns

Successful completion returns RPC_S_OK.

<div class="alert"><b>Note</b>  For a list of valid error codes, see 
<a href="/windows/desktop/Rpc/rpc-return-values">RPC Return Values</a>.</div>
<div> </div>

## -remarks

The 
<b>RpcErrorAddRecord</b> function enables applications or servers other than the RPC Runtime to add extended error information to a chain of extended error information records.

Responsibility for the strings pointed to by <i>ErrorInfo</i> belong to the caller; the 
<b>RpcErrorAddRecord</b> function makes a copy of those strings, if necessary. The following restrictions on the members of <i>ErrorInfo</i> must be observed:

<b>Version</b> must be set to a valid version, such as RPC_EEINFO_VERSION.

<b>ComputerName</b> must be set to <b>NULL</b>. Any other value results in ERROR_INVALID_PARAMETER.

<b>ProcessID</b> must be set to zero. Any other value results in ERROR_INVALID_PARAMETER.

<b>SystemTime</b> or <b>FileTime</b> is ignored on input, and is set by the RPC Runtime.

<b>GeneratingComponent</b> must be set to zero. Any other value results in ERROR_INVALID_PARAMETER. The RPC Runtime sets this to EEInfoGCApplication.

<b>Status</b> can be set to the error code the caller wants to add to the chain.

<b>DetectionLocation</b> must be set to zero. Any other value results in ERROR_INVALID_PARAMETER.

<b>NumberOfParameters</b> indicates the number of parameters in the Parameters array. This value must be equal or greater than zero or MaxNumberOfEEInfoParams. The RPC Runtime does not use any memory after the specified number of parameters, so callers can safely allocate memory for less than MaxNumberOfEEInfoParams parameters.

<b>Parameters</b> represents the parameters for the extended error information record. The only restriction on Parameters is that <b>Pval</b> is used to represent pointers, and is always 64 bits. Use <b>Pval</b> regardless of whether the system used is 32 bits or 64 bits. Do not use <b>Lval</b>.

## -see-also

<a href="/windows/desktop/Rpc/obtaining-extended-rpc-error-information">Obtaining Extended RPC Error Information</a>



<a href="/windows/desktop/api/rpcasync/ns-rpcasync-rpc_extended_error_info">RPC_EXTENDED_ERROR_INFO</a>



<a href="/windows/desktop/api/rpcasync/nf-rpcasync-rpcerrorgetnextrecord">RpcErrorGetNextRecord</a>



<a href="/windows/desktop/api/rpcasync/nf-rpcasync-rpcerrorstartenumeration">RpcErrorStartEnumeration</a>