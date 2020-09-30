---
UID: NF:rpcnsi.RpcNsMgmtInqExpAge
title: RpcNsMgmtInqExpAge function (rpcnsi.h)
description: The RpcNsMgmtInqExpAge function returns the global expiration age for local copies of name-service data.
helpviewer_keywords: ["RpcNsMgmtInqExpAge","RpcNsMgmtInqExpAge function [RPC]","_rpc_rpcnsmgmtinqexpage","rpc.rpcnsmgmtinqexpage","rpcnsi/RpcNsMgmtInqExpAge"]
old-location: rpc\rpcnsmgmtinqexpage.htm
tech.root: Rpc
ms.assetid: b9e27fba-c4ee-4a0e-ab95-af4c975e9123
ms.date: 12/05/2018
ms.keywords: RpcNsMgmtInqExpAge, RpcNsMgmtInqExpAge function [RPC], _rpc_rpcnsmgmtinqexpage, rpc.rpcnsmgmtinqexpage, rpcnsi/RpcNsMgmtInqExpAge
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
 - RpcNsMgmtInqExpAge
 - rpcnsi/RpcNsMgmtInqExpAge
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
 - RpcNsMgmtInqExpAge
---

# RpcNsMgmtInqExpAge function


## -description

The 
<b>RpcNsMgmtInqExpAge</b> function returns the global expiration age for local copies of name-service data.
<div class="alert"><b>Note</b>  This function is not supported on Windows Vista and later operating systems.</div><div> </div>

## -parameters

### -param ExpirationAge

Pointer to the default expiration age, in seconds. This value is used by all name service next operations.

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
<b>RpcNsMgmtInqExpAge</b> function returns the expiration age that the application is using. The expiration age is the amount of time in seconds that a local copy of data from a name-service attribute can exist before a request from the application for the attribute requires updating the local copy. When an application begins running, the RPC run-time library specifies a default expiration age of two hours. The default is global to the application.

An expiration age is used by Pointer next operations (which read data from name-service attributes). A next operation typically starts by looking for a local copy of the attribute data being requested by an application. In the absence of a local copy, the next operation creates one with fresh attribute data from the name-service database. If a local copy already exists, the operation compares its actual age to the expiration age being used by the application. If the actual age exceeds the expiration age, the operation automatically tries to update the local copy with fresh attribute data. If updating is impossible, the old local data remains in place and the next operation fails.

Applications typically should use only the default expiration age. For special cases, however, an application can substitute a user-supplied global expiration age for the default by calling 
<a href="/windows/desktop/api/rpcnsi/nf-rpcnsi-rpcnsmgmtsetexpage">RpcNsMgmtSetExpAge</a>. The 
<b>RpcNsMgmtInqExpAge</b> function returns the current global expiration age, whether a default or a user-supplied value. An application can also override the global expiration age temporarily by calling the 
<a href="/windows/desktop/api/rpcnsi/nf-rpcnsi-rpcnsmgmthandlesetexpage">RpcNsMgmtHandleSetExpAge</a> function.

## -see-also

<a href="/windows/desktop/api/rpcnsi/nf-rpcnsi-rpcnsmgmthandlesetexpage">RpcNsMgmtHandleSetExpAge</a>



<a href="/windows/desktop/api/rpcnsi/nf-rpcnsi-rpcnsmgmtsetexpage">RpcNsMgmtSetExpAge</a>