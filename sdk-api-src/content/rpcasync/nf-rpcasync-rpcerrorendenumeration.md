---
UID: NF:rpcasync.RpcErrorEndEnumeration
title: RpcErrorEndEnumeration function (rpcasync.h)

description: The RpcErrorEndEnumeration function ends enumeration of extended error information and frees all resources allocated by RPC for the enumeration.
old-location: rpc\rpcerrorendenumeration.htm
tech.root: Rpc
ms.assetid: 04da6e7d-bbdb-47d3-9924-604ddf56d177

ms.date: 12/05/2018
ms.keywords: RpcErrorEndEnumeration, RpcErrorEndEnumeration function [RPC], _rpc_rpcerrorendenumeration, rpc.rpcerrorendenumeration, rpcasync/RpcErrorEndEnumeration
ms.topic: function
f1_keywords: 
 - "rpcasync/RpcErrorEndEnumeration"
dev_langs:
 - c++
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Rpcrt4.dll
api_name:
 - RpcErrorEndEnumeration
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# RpcErrorEndEnumeration function


## -description


The 
<b>RpcErrorEndEnumeration</b> function ends enumeration of extended error information and frees all resources allocated by RPC for the enumeration.


## -parameters




### -param EnumHandle

Pointer to the enumeration handle.


## -returns



Successful completion returns RPC_S_OK. The 
<b>RpcErrorEndEnumeration</b> function call cannot fail unless its parameters are invalid.

<div class="alert"><b>Note</b>  For a list of valid error codes, see 
<a href="https://docs.microsoft.com/windows/desktop/Rpc/rpc-return-values">RPC Return Values</a>.</div>
<div> </div>



## -remarks



The 
<b>RpcErrorEndEnumeration</b> function zeros out the enumeration handle to prevent further usage. If the CopyStrings option was not used during a previous call to the 
<a href="https://docs.microsoft.com/windows/desktop/api/rpcasync/nf-rpcasync-rpcerrorgetnextrecord">RpcErrorGetNextRecord</a> function, all non-empty <b>ComputerName</b> fields and <b>AnsiString</b> or <b>UnicodeString</b> values are invalid after this function is called.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/Rpc/obtaining-extended-rpc-error-information">Obtaining Extended RPC Error Information</a>



<a href="https://docs.microsoft.com/windows/desktop/api/rpcasync/ns-rpcasync-rpc_error_enum_handle">RPC_ERROR_ENUM_HANDLE</a>



<a href="https://docs.microsoft.com/windows/desktop/api/rpcasync/nf-rpcasync-rpcerrorgetnextrecord">RpcErrorGetNextRecord</a>



<a href="https://docs.microsoft.com/windows/desktop/api/rpcasync/nf-rpcasync-rpcerrorstartenumeration">RpcErrorStartEnumeration</a>
 

 

