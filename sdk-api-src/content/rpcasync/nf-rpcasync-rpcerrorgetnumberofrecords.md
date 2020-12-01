---
UID: NF:rpcasync.RpcErrorGetNumberOfRecords
title: RpcErrorGetNumberOfRecords function (rpcasync.h)
description: The RpcErrorGetNumberOfRecords function returns the number of records in the extended error information.
helpviewer_keywords: ["RpcErrorGetNumberOfRecords","RpcErrorGetNumberOfRecords function [RPC]","_rpc_rpcerrorgetnumberofrecords","rpc.rpcerrorgetnumberofrecords","rpcasync/RpcErrorGetNumberOfRecords"]
old-location: rpc\rpcerrorgetnumberofrecords.htm
tech.root: Rpc
ms.assetid: 1b498cc8-9ee5-47bd-a484-33bf1c89413c
ms.date: 12/05/2018
ms.keywords: RpcErrorGetNumberOfRecords, RpcErrorGetNumberOfRecords function [RPC], _rpc_rpcerrorgetnumberofrecords, rpc.rpcerrorgetnumberofrecords, rpcasync/RpcErrorGetNumberOfRecords
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
 - RpcErrorGetNumberOfRecords
 - rpcasync/RpcErrorGetNumberOfRecords
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
 - RpcErrorGetNumberOfRecords
---

# RpcErrorGetNumberOfRecords function


## -description

The 
<b>RpcErrorGetNumberOfRecords</b> function returns the number of records in the extended error information.

## -parameters

### -param EnumHandle [in]

Pointer to the enumeration handle.

### -param Records [out]

Number of records for the extended error information.

## -returns

Successful completion returns RPC_S_OK. The <b>RpcErrorGetNumberOfRecords</b> function call cannot fail unless its parameters are invalid.

<div class="alert"><b>Note</b>  For a list of valid error codes, see 
<a href="/windows/desktop/Rpc/rpc-return-values">RPC Return Values</a>.</div>
<div> </div>

## -remarks

The 
<b>RpcErrorGetNumberOfRecords</b> function returns the total number of records in the extended error information, not the number of records from the current cursor location.

## -see-also

<a href="/windows/desktop/Rpc/obtaining-extended-rpc-error-information">Obtaining Extended RPC Error Information</a>



<a href="/windows/desktop/api/rpcasync/ns-rpcasync-rpc_error_enum_handle">RPC_ERROR_ENUM_HANDLE</a>



<a href="/windows/desktop/api/rpcasync/nf-rpcasync-rpcerrorstartenumeration">RpcErrorStartEnumeration</a>