---
UID: NF:rpcdce.RpcServerListen
title: RpcServerListen function
author: windows-driver-content
description: The RpcServerListen function signals the RPC run-time library to listen for remote procedure calls. This function will not affect auto-listen interfaces; use RpcServerRegisterIfEx if you need that functionality.
old-location: rpc\rpcserverlisten.htm
old-project: Rpc
ms.assetid: 430561b2-c74b-423c-8448-339cc71dbd68
ms.author: windowsdriverdev
ms.date: 4/24/2018
ms.keywords: RpcServerListen, RpcServerListen function [RPC], _rpc_rpcserverlisten, rpc.rpcserverlisten, rpcdce/RpcServerListen
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: RPC_CALL_LOCAL_ADDRESS_V1, *PRPC_CALL_LOCAL_ADDRESS_V1
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Rpcrt4.dll
api_name:
-	RpcServerListen
product: Windows
targetos: Windows
req.lib: Rpcrt4.lib
req.dll: Rpcrt4.dll
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# RpcServerListen function


## -description


The 
<b>RpcServerListen</b> function signals the RPC run-time library to listen for remote procedure calls. This function will not affect auto-listen interfaces; use 
<a href="https://msdn.microsoft.com/1666bc0a-72bf-40da-b054-c10b477c4367">RpcServerRegisterIfEx</a> if you need that functionality.


## -parameters




### -param MinimumCallThreads

Hint to the RPC run time that specifies the minimum number of call threads that should be created and maintained in the given server. This value is only a hint and is interpreted differently in different versions of Windows. In Windows XP, this value is the number of previously created threads in each thread pool that the RPC run time creates. An application should specify one for this parameter, and defer thread creation decisions to the RPC run time.


### -param MaxCalls

Recommended maximum number of concurrent remote procedure calls the server can execute. To allow efficient performance, the RPC run-time libraries interpret the <i>MaxCalls</i> parameter as a suggested limit rather than as an absolute upper bound. 




Use RPC_C_LISTEN_MAX_CALLS_DEFAULT to specify the default value.


### -param DontWait

Flag controlling the return from 
<b>RpcServerListen</b>. A value of nonzero indicates that 
<b>RpcServerListen</b> should return immediately after completing function processing. A value of zero indicates that 
<b>RpcServerListen</b> should not return until the 
<a href="https://msdn.microsoft.com/aeb6084a-e2ea-4468-85f8-2ae6cc4dbe84">RpcMgmtStopServerListening</a> function has been called and all remote calls have completed.


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
<dt><b>RPC_S_ALREADY_LISTENING</b></dt>
</dl>
</td>
<td width="60%">
The server is already listening.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>RPC_S_NO_PROTSEQS_REGISTERED</b></dt>
</dl>
</td>
<td width="60%">
There are no protocol sequences registered.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>RPC_S_MAX_CALLS_TOO_SMALL</b></dt>
</dl>
</td>
<td width="60%">
The maximum calls value is too small.

</td>
</tr>
</table>
 

<div class="alert"><b>Note</b>  For a list of valid error codes, see 
<a href="https://msdn.microsoft.com/0223aa7a-b0cf-49e3-9f08-90be5ccffbd1">RPC Return Values</a>.</div>
<div> </div>



## -remarks



A server calls 
<b>RpcServerListen</b> when the server is ready to process remote procedure calls. RPC allows a server to simultaneously process multiple calls. The <i>MaxCalls</i> parameter recommends the maximum number of concurrent remote procedure calls the server should execute.

The <i>MaxCalls</i> value should not be zero, and should be larger than <i>MinimumCallThreads</i>. Values larger than 0x7FFFFFFF are set to 0x7FFFFFFF without notice.

<b>Windows XP/2000:  </b>Setting the <i>MaxCalls</i> parameter to RPC_C_LISTEN_MAX_CALLS_DEFAULT removes the limit on concurrent remote procedure calls, rather than setting it to the constant-defined value of 1234. Removing the limit on maximum concurrent calls allows as many concurrent remote procedure calls as the computer can handle. This behavior enables increased efficiency in the RPC run time.

A server application is responsible for concurrency control between the server manager routines because each routine executes in a separate thread.

When the <i>DontWait</i> parameter has a value of zero, the RPC run-time library continues listening for remote procedure calls (that is, the routine does not return to the server application) until one of the following events occurs:

<ul>
<li>One of the server application's manager routines calls 
<a href="https://msdn.microsoft.com/aeb6084a-e2ea-4468-85f8-2ae6cc4dbe84">RpcMgmtStopServerListening</a>.</li>
<li>A client calls a remote procedure provided by the server that directs the server to call 
<a href="https://msdn.microsoft.com/aeb6084a-e2ea-4468-85f8-2ae6cc4dbe84">RpcMgmtStopServerListening</a>.</li>
<li>A client calls 
<a href="https://msdn.microsoft.com/aeb6084a-e2ea-4468-85f8-2ae6cc4dbe84">RpcMgmtStopServerListening</a> with a binding handle to the server.</li>
</ul>
After it receives a stop-listening request, the RPC run-time library stops accepting new remote procedure calls for all registered interfaces. Executing calls are allowed to complete, including callbacks. After all calls complete, 
<b>RpcServerListen</b> returns to the caller.

When the <i>DontWait</i> parameter has a nonzero value, 
<b>RpcServerListen</b> returns to the server immediately after processing all the instructions associated with the function. You can use the 
<a href="https://msdn.microsoft.com/19fa750f-76f8-4005-992f-9c2707e48668">RpcMgmtWaitServerListen</a> function to perform the wait operation usually associated with 
<b>RpcServerListen</b>.

<div class="alert"><b>Note</b>  The Microsoft RPC implementation of 
<b>RpcServerListen</b> includes two additional parameters that do not appear in the DCE specification: <i>DontWait</i> and <i>MinimumCallThreads</i>.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/aeb6084a-e2ea-4468-85f8-2ae6cc4dbe84">RpcMgmtStopServerListening</a>



<a href="https://msdn.microsoft.com/19fa750f-76f8-4005-992f-9c2707e48668">RpcMgmtWaitServerListen</a>



<a href="https://msdn.microsoft.com/f7f6a7c3-ce6c-4b8b-9853-596c39a0e76d">RpcServerRegisterIf</a>



<a href="https://msdn.microsoft.com/1666bc0a-72bf-40da-b054-c10b477c4367">RpcServerRegisterIfEx</a>



<a href="https://msdn.microsoft.com/e7379656-d6b7-4e5f-9251-7b112a40c6d5">RpcServerUseAllProtseqs</a>



<a href="https://msdn.microsoft.com/6f3f7726-3e12-4b0b-8454-25f06a29b245">RpcServerUseAllProtseqsIf</a>



<a href="https://msdn.microsoft.com/9b2c9cf0-fe96-4063-a893-f2793595af57">RpcServerUseProtseq</a>



<a href="https://msdn.microsoft.com/1914a90a-6dee-4517-9de1-d332124eb0a4">RpcServerUseProtseqEp</a>



<a href="https://msdn.microsoft.com/41c1fa20-266a-4071-91b3-d0fd8196871b">RpcServerUseProtseqIf</a>
 

 

