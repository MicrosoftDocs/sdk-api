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

# RpcCancelThreadEx function


## -description



			The 
<b>RpcCancelThreadEx</b> function stops the execution of a thread. The 
<b>RpcCancelThreadEx</b> function should not be used to stop the execution of an asynchronous RPC call; instead, use the 
<a href="https://msdn.microsoft.com/e55d586f-969b-4e9a-97d9-b6c74b2a8b6d">RpcAsyncCancelCall</a> function to stop the execution of an asynchronous RPC call.


## -parameters




### -param Thread

TBD


### -param Timeout

Number of seconds to wait for the thread to be canceled before this function returns. To specify that a client waits an indefinite amount of time, pass the value RPC_C_CANCEL_INFINITE_TIMEOUT.


#### - ThreadHandle

Handle of the thread to cancel.


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
<dt><b>RPC_S_ACCESS_DENIED</b></dt>
</dl>
</td>
<td width="60%">
Thread handle does not have privilege. Thread handles must have THREAD_SET_CONTEXT set properly for the function to execute properly.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>RPC_S_CANNOT_SUPPORT</b></dt>
</dl>
</td>
<td width="60%">
Called by an MS-DOS or Windows 3.<i>x</i> client.

</td>
</tr>
</table>
 

<div class="alert"><b>Note</b>  For a list of valid error codes, see 
<a href="https://msdn.microsoft.com/0223aa7a-b0cf-49e3-9f08-90be5ccffbd1">RPC Return Values</a>.</div>
<div> </div>



## -remarks



The 
<b>RpcCancelThreadEx</b> function allows one client thread to cancel an RPC in progress on another client thread. When the function is called, the server run-time is informed of the cancel operation. The server stub can determine if the call has been canceled by calling 
<a href="https://msdn.microsoft.com/1fd3b84d-ea45-4267-ac30-e4e2cf037c92">RpcTestCancel</a>. If the call has been canceled, the server stub should clean up and return control to the client.

Using the <i>Timeout</i> parameter, your application can specify the number of seconds to wait for a response. If the server does not return within this interval, the call fails at the client with an RPC_S_CALL_CANCELLED exception. The server stub continues to execute.

If you are using the named pipes protocol, <a href="https://msdn.microsoft.com/02961bb8-faf0-42e5-b134-dd2983e6d146">ncacn_np</a>, you must specify a finite time-out.

<div class="alert"><b>Note</b>  You can use 
<b>RpcCancelThreadEx</b> with any of the connection-oriented protocols (<b>ncacn_*</b>) except 
<a href="midl.ncacn_http">ncacn_http</a>, and with any of the datagram protocols except 
<a href="midl.ncadg_mq">ncadg_mq</a> and 
<a href="https://msdn.microsoft.com/0009f794-5c14-4484-9023-cb20c7030dc5">ncalrpc</a>.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/e55d586f-969b-4e9a-97d9-b6c74b2a8b6d">RpcAsyncCancelCall</a>



<a href="https://msdn.microsoft.com/4315562e-674b-40a4-a2d9-133e6ab27c25">RpcCancelThread</a>



<a href="https://msdn.microsoft.com/1fd3b84d-ea45-4267-ac30-e4e2cf037c92">RpcTestCancel</a>



<a href="midl.ncacn_http">ncacn_http</a>



<a href="https://msdn.microsoft.com/02961bb8-faf0-42e5-b134-dd2983e6d146">ncacn_np</a>



<a href="midl.ncadg_mq">ncadg_mq</a>



<a href="https://msdn.microsoft.com/0009f794-5c14-4484-9023-cb20c7030dc5">ncalrpc</a>
 

 

