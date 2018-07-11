---
UID: NF:rpcdce.RpcMgmtSetAuthorizationFn
title: RpcMgmtSetAuthorizationFn function
author: windows-sdk-content
description: The RpcMgmtSetAuthorizationFn function establishes an authorization function for processing remote calls to a server's management functions.
old-location: rpc\rpcmgmtsetauthorizationfn.htm
old-project: rpc
ms.assetid: bb381a52-17e4-4ebe-9a1a-a561c12d73d4
ms.author: windowssdkdev
ms.date: 05/31/2018
ms.keywords: RpcMgmtSetAuthorizationFn, RpcMgmtSetAuthorizationFn function [RPC], _rpc_rpcmgmtsetauthorizationfn, rpc.rpcmgmtsetauthorizationfn, rpcdce/RpcMgmtSetAuthorizationFn
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: rpcdce.h
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
tech.root: 
req.typenames: RPC_CALL_LOCAL_ADDRESS_V1, *PRPC_CALL_LOCAL_ADDRESS_V1
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Rpcrt4.dll
api_name:
 - RpcMgmtSetAuthorizationFn
product: Windows
targetos: Windows
req.lib: Rpcrt4.lib
req.dll: Rpcrt4.dll
req.irql: 
req.product: ADAM
---

# RpcMgmtSetAuthorizationFn function


## -description


The 
<b>RpcMgmtSetAuthorizationFn</b> function establishes an authorization function for processing remote calls to a server's management functions.


## -parameters




### -param AuthorizationFn

Specifies an authorization function. The RPC server run-time library automatically calls this function whenever the server run-time receives a client request to execute one of the remote management functions. The server must implement this function. Applications specify a value of <b>NULL</b> to unregister a previously registered authorization function. After such a call, default authorizations are used.


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
<a href="https://msdn.microsoft.com/0223aa7a-b0cf-49e3-9f08-90be5ccffbd1">RPC Return Values</a>.</div>
<div> </div>



## -remarks



Server applications call the 
<b>RpcMgmtSetAuthorizationFn</b> function to establish an authorization function that controls access to the server's remote management functions. When a server has not called 
<b>RpcMgmtSetAuthorizationFn</b>, or calls with a <b>null</b> value for <i>AuthorizationFn</i>, the server run-time library uses the following default authorizations.

<table>
<tr>
<th>Remote function</th>
<th>Default authorization</th>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/f6d89f2c-ff51-44ab-9f8a-2f76cd3ac6db">RpcMgmtInqIfIds</a>
</td>
<td>Enabled</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/2666adb4-8a89-480e-8855-9179a7128e35">RpcMgmtInqServerPrincName</a>
</td>
<td>Enabled</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/478b9f33-db01-4a1d-9b5b-dc2662ee8d7b">RpcMgmtInqStats</a>
</td>
<td>Enabled</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/e4c5e8aa-764d-489f-ac98-ab40ca4a3534">RpcMgmtIsServerListening</a>
</td>
<td>Enabled</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/aeb6084a-e2ea-4468-85f8-2ae6cc4dbe84">RpcMgmtStopServerListening</a>
</td>
<td>Disabled</td>
</tr>
</table>
 


<div> </div>


In the preceding table, "Enabled" indicates that all clients can execute the remote function, and "Disabled" indicates that all clients are prevented from executing the remote function.




## -see-also




<a href="https://msdn.microsoft.com/9b7ab901-1dcf-458c-858f-f411825f324b">RPC_MGMT_AUTHORIZATION_FN</a>



<a href="https://msdn.microsoft.com/478b9f33-db01-4a1d-9b5b-dc2662ee8d7b">RpcMgmtInqStats</a>



<a href="https://msdn.microsoft.com/e4c5e8aa-764d-489f-ac98-ab40ca4a3534">RpcMgmtIsServerListening</a>



<a href="https://msdn.microsoft.com/aeb6084a-e2ea-4468-85f8-2ae6cc4dbe84">RpcMgmtStopServerListening</a>



<a href="https://msdn.microsoft.com/19fa750f-76f8-4005-992f-9c2707e48668">RpcMgmtWaitServerListen</a>
 

 

