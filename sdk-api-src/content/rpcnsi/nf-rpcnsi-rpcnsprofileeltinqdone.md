---
UID: NF:rpcnsi.RpcNsProfileEltInqDone
title: RpcNsProfileEltInqDone function (rpcnsi.h)
description: The RpcNsProfileEltInqDone function deletes the inquiry context for viewing the elements in a profile.
helpviewer_keywords: ["RpcNsProfileEltInqDone","RpcNsProfileEltInqDone function [RPC]","_rpc_rpcnsprofileeltinqdone","rpc.rpcnsprofileeltinqdone","rpcnsi/RpcNsProfileEltInqDone"]
old-location: rpc\rpcnsprofileeltinqdone.htm
tech.root: Rpc
ms.assetid: 957cdfb6-2b5a-4339-8197-897999df5ea0
ms.date: 12/05/2018
ms.keywords: RpcNsProfileEltInqDone, RpcNsProfileEltInqDone function [RPC], _rpc_rpcnsprofileeltinqdone, rpc.rpcnsprofileeltinqdone, rpcnsi/RpcNsProfileEltInqDone
req.header: rpcnsi.h
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
req.lib: Rpcns4.lib
req.dll: Rpcns4.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - RpcNsProfileEltInqDone
 - rpcnsi/RpcNsProfileEltInqDone
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Rpcns4.dll
api_name:
 - RpcNsProfileEltInqDone
---

# RpcNsProfileEltInqDone function


## -description

The 
<b>RpcNsProfileEltInqDone</b> function deletes the inquiry context for viewing the elements in a profile.
<div class="alert"><b>Note</b>  This function is not supported on Windows Vista and later operating systems.</div><div> </div>

## -parameters

### -param InquiryContext

Pointer to a name-service handle to free. The name-service handle that <i>InquiryContext</i> points to is created by calling the 
<a href="/windows/desktop/api/rpcnsi/nf-rpcnsi-rpcnsprofileeltinqbegina">RpcNsProfileEltInqBegin</a> function. 




An argument value of NULL is returned.

## -returns

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>RPC_S_OK</b></dt>
</dl>
</td>
<td width="60%">
The call succeeded.

</td>
</tr>
</table>
 

<div class="alert"><b>Note</b>  For a list of valid error codes, see 
<a href="/windows/desktop/Rpc/rpc-return-values">RPC Return Values</a>.</div>
<div> </div>

## -remarks

The 
<b>RpcNsProfileEltInqDone</b> function frees an inquiry context created by calling 
<a href="/windows/desktop/api/rpcnsi/nf-rpcnsi-rpcnsprofileeltinqbegina">RpcNsProfileEltInqBegin</a>.

An application calls 
<b>RpcNsProfileEltInqDone</b> after viewing profile elements using the 
<a href="/windows/desktop/api/rpcnsi/nf-rpcnsi-rpcnsprofileeltinqnexta">RpcNsProfileEltInqNext</a> function.

<div class="alert"><b>Note</b>  Windows 2000 Active Directory supports this function. Earlier versions of Windows NT support the use of this function with Cell Directory Service (CDS) only.</div>
<div> </div>

## -see-also

<a href="/windows/desktop/api/rpcnsi/nf-rpcnsi-rpcnsprofileeltinqbegina">RpcNsProfileEltInqBegin</a>



<a href="/windows/desktop/api/rpcnsi/nf-rpcnsi-rpcnsprofileeltinqnexta">RpcNsProfileEltInqNext</a>