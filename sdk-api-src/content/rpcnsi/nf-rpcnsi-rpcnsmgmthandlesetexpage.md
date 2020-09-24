---
UID: NF:rpcnsi.RpcNsMgmtHandleSetExpAge
title: RpcNsMgmtHandleSetExpAge function (rpcnsi.h)
description: The RpcNsMgmtHandleSetExpAge function sets the expiration age of a name-service handle for local copies of name-service data.
helpviewer_keywords: ["RpcNsMgmtHandleSetExpAge","RpcNsMgmtHandleSetExpAge function [RPC]","_rpc_rpcnsmgmthandlesetexpage","rpc.rpcnsmgmthandlesetexpage","rpcnsi/RpcNsMgmtHandleSetExpAge"]
old-location: rpc\rpcnsmgmthandlesetexpage.htm
tech.root: Rpc
ms.assetid: d6607ffb-21a9-41ec-863f-f1514b115d4d
ms.date: 12/05/2018
ms.keywords: RpcNsMgmtHandleSetExpAge, RpcNsMgmtHandleSetExpAge function [RPC], _rpc_rpcnsmgmthandlesetexpage, rpc.rpcnsmgmthandlesetexpage, rpcnsi/RpcNsMgmtHandleSetExpAge
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
 - RpcNsMgmtHandleSetExpAge
 - rpcnsi/RpcNsMgmtHandleSetExpAge
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
 - RpcNsMgmtHandleSetExpAge
---

# RpcNsMgmtHandleSetExpAge function


## -description

The 
<b>RpcNsMgmtHandleSetExpAge</b> function sets the expiration age of a name-service handle for local copies of name-service data.
<div class="alert"><b>Note</b>  This function is not supported on Windows Vista and later operating systems.</div><div> </div>

## -parameters

### -param NsHandle

Name-service handle for which an expiration age is set. A name-service handle is returned from a name service begin operation.

### -param ExpirationAge

Integer value, in seconds, that sets the expiration age of local name-service data read by all next routines using the specified <i>NsHandle</i> parameter. 




An expiration age of 0 causes an immediate update of the local name-service data.

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
<b>RpcNsMgmtHandleSetExpAge</b> function sets a handle-expiration age for a specified name–service handle (<i>NsHandle</i>). The expiration age is the amount of time that a local copy of data from a name-service attribute can exist before a request from the application for the attribute requires updating the local copy. When an application begins running, the RPC run-time library specifies a default expiration age of two hours. The default is global to the application. A handle-expiration age applies only to a specific name-service handle and temporarily overrides the current global expiration age.

A handle-expiration age is used exclusively by Pointer next operations (which read data from name-service attributes). A next operation typically starts by looking for a local copy of the attribute data being requested by an application. In the absence of a local copy, the next operation creates one with fresh attribute data from the name-service database. If a local copy already exists, the operation compares its actual age to the expiration age being used by the application (which, in this case, is the expiration age set for the name-service handle). If the actual age exceeds the handle-expiration age, the operation automatically tries to update the local copy with fresh attribute data. If updating is impossible, the old local data remains in place and the next operation fails, returning the RPC_S_NAME_SERVICE_UNAVAILABLE status code.

The scope of a handle-expiration age is a single series of next operations. The 
<b>RpcNsMgmtHandleSetExpAge</b> function operates within the following context:

<ul>
<li>A begin operation creates a name-service handle.</li>
<li>A call to the 
<b>RpcNsMgmtHandleSetExpAge</b> function creates an expiration age for the handle.</li>
<li>A series of next operations for the name-service handle uses the handle expiration age.</li>
<li>A done operation for the name-service handle deletes both the handle and its expiration age.</li>
</ul>
<div class="alert"><b>Note</b>  Typically, you should avoid using 
<b>RpcNsMgmtHandleSetExpAge</b>. Instead, you should rely on the application's global expiration age. Setting the handle-expiration age to a small value causes the name service next operations to frequently update local data for any name-service attribute requested by your application. For example, setting the expiration age to 0 forces the next operation to update local data for the name-service attribute requested by your application. Therefore, setting a small handle-expiration age can create performance problems for your application. Furthermore, if your application is using a remote name-service server, a small expiration age can adversely affect network performance for all applications.</div>
<div> </div>
Limit use of 
<b>RpcNsMgmtHandleSetExpAge</b> to the following situations:

<ul>
<li>When you must always get accurate name-service data. 


For example, during management operations to update a profile, you may need to always see the profile's current contents. In this case, before beginning to inquire about a profile, your application should call the 
<b>RpcNsMgmtHandleSetExpAge</b> function and specify 0 for the <i>ExpirationAge</i> parameter.

</li>
<li>When a request using the default expiration age has failed, and your application needs to retry the operation. 


For example, a client application using name service import operations should first try to obtain bindings using the application's default expiration age. However, sometimes the import-next operation returns either no binding handles or an insufficient number of them. In this case, the client could retry the import operation and, after the 
<a href="/windows/desktop/api/rpcnsi/nf-rpcnsi-rpcnsbindingimportbegina">RpcNsBindingImportBegin</a> call, include an 
<b>RpcNsMgmtHandleSetExpAge</b> call and specify 0 for the <i>ExpirationAge</i> parameter. When the client calls the import-next function again, the small handle-expiration age causes the import-next operation to update the local attribute data.

</li>
</ul>

## -see-also

<a href="/windows/desktop/api/rpcnsi/nf-rpcnsi-rpcnsbindingimportbegina">RpcNsBindingImportBegin</a>



<a href="/windows/desktop/api/rpcnsi/nf-rpcnsi-rpcnsmgmtinqexpage">RpcNsMgmtInqExpAge</a>



<a href="/windows/desktop/api/rpcnsi/nf-rpcnsi-rpcnsmgmtsetexpage">RpcNsMgmtSetExpAge</a>