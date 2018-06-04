---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
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
 

 

