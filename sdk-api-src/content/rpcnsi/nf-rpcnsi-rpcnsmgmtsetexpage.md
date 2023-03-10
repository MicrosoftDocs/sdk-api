---
UID: NF:rpcnsi.RpcNsMgmtSetExpAge
title: RpcNsMgmtSetExpAge function (rpcnsi.h)
description: The RpcNsMgmtSetExpAge function modifies the application's global expiration age for local copies of name-service data.
helpviewer_keywords: ["RpcNsMgmtSetExpAge","RpcNsMgmtSetExpAge function [RPC]","_rpc_rpcnsmgmtsetexpage","rpc.rpcnsmgmtsetexpage","rpcnsi/RpcNsMgmtSetExpAge"]
old-location: rpc\rpcnsmgmtsetexpage.htm
tech.root: Rpc
ms.assetid: 9433e8c3-2c52-4994-8661-6af089fa9bc9
ms.date: 12/05/2018
ms.keywords: RpcNsMgmtSetExpAge, RpcNsMgmtSetExpAge function [RPC], _rpc_rpcnsmgmtsetexpage, rpc.rpcnsmgmtsetexpage, rpcnsi/RpcNsMgmtSetExpAge
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
 - RpcNsMgmtSetExpAge
 - rpcnsi/RpcNsMgmtSetExpAge
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
 - RpcNsMgmtSetExpAge
---

# RpcNsMgmtSetExpAge function


## -description

The 
<b>RpcNsMgmtSetExpAge</b> function modifies the application's global expiration age for local copies of name-service data.
<div class="alert"><b>Note</b>  This function is not supported on Windows Vista and later operating systems.</div><div> </div>

## -parameters

### -param ExpirationAge

Pointer to the default expiration age, in seconds. This value is used by all name service–next operations. An expiration age of 0 causes an immediate update of the local name-service data. 




To reset the expiration age to an RPC-assigned default value of two hours, specify a value of RPC_C_NS_DEFAULT_EXP_AGE.

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
<tr>
<td width="40%">
<dl>
<dt><b>RPC_S_NAME_SERVICE_UNAVAILABLE</b></dt>
</dl>
</td>
<td width="60%">
The name service is unavailable.

</td>
</tr>
</table>
 

<div class="alert"><b>Note</b>  For a list of valid error codes, see 
<a href="/windows/desktop/Rpc/rpc-return-values">RPC Return Values</a>.</div>
<div> </div>

## -remarks

The 
<b>RpcNsMgmtSetExpAge</b> function modifies the global expiration age of an application. The expiration age is the amount of time that a local copy of data from a name-service attribute can exist before a request from the application for the attribute requires updating the local copy. When an application begins running, the RPC run-time library specifies a default expiration age of two hours. The default is global to the application. Typically, you should avoid using 
<b>RpcNsMgmtSetExpAge</b>. Instead, you should rely on the default expiration age.

An expiration age is used by Pointer next operations (which read data from name-service attributes). A next operation typically starts by looking for a local copy of the attribute data being requested by an application. In the absence of a local copy, the next operation creates one with fresh attribute data from the name-service database. If a local copy already exists, the operation compares its actual age to the expiration age being used by the application. If the actual age exceeds the expiration age, the operation automatically tries to update the local copy with fresh attribute data. If updating is impossible, the old local data remains in place and the next operation fails, returning the RPC_S_NAME_SERVICE_UNAVAILABLE status code.

Setting the expiration age to a small value causes the Pointer next operations to frequently update local data for any name-service attribute requested by your application. For example, setting the expiration age to 0 forces all next operations to update local data for the name-service attribute requested by your application. Therefore, setting small expiration ages can create performance problems for your application and increase network traffic. Furthermore, if your application is using a remote name-service server, a small expiration age can adversely affect network performance for all applications.

## -see-also

<a href="/windows/desktop/api/rpcnsi/nf-rpcnsi-rpcnsmgmthandlesetexpage">RpcNsMgmtHandleSetExpAge</a>