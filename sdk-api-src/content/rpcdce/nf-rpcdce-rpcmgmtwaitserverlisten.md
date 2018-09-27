---
UID: NF:rpcdce.RpcMgmtWaitServerListen
title: RpcMgmtWaitServerListen function
author: windows-sdk-content
description: The RpcMgmtWaitServerListen function performs the wait operation usually associated with RpcServerListen.
old-location: rpc\rpcmgmtwaitserverlisten.htm
tech.root: rpc
ms.assetid: 19fa750f-76f8-4005-992f-9c2707e48668
ms.author: windowssdkdev
ms.date: 09/14/2018
ms.keywords: RpcMgmtWaitServerListen, RpcMgmtWaitServerListen function [RPC], _rpc_rpcmgmtwaitserverlisten, rpc.rpcmgmtwaitserverlisten, rpcdce/RpcMgmtWaitServerListen
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
 - RpcMgmtWaitServerListen
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# RpcMgmtWaitServerListen function


## -description


The 
<b>RpcMgmtWaitServerListen</b> function performs the <i>wait</i> operation usually associated with 
<a href="https://msdn.microsoft.com/430561b2-c74b-423c-8448-339cc71dbd68">RpcServerListen</a>.


## -parameters






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
All remote procedure calls are complete.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>RPC_S_ALREADY_LISTENING</b></dt>
</dl>
</td>
<td width="60%">
Another thread has called 
<b>RpcMgmtWaitServerListen</b> and has not yet returned.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>RPC_S_NOT_LISTENING</b></dt>
</dl>
</td>
<td width="60%">
The server application must call 
<a href="https://msdn.microsoft.com/430561b2-c74b-423c-8448-339cc71dbd68">RpcServerListen</a> before calling 
<b>RpcMgmtWaitServerListen</b>.

</td>
</tr>
</table>
 

<div class="alert"><b>Note</b>  For a list of valid error codes, see 
<a href="https://msdn.microsoft.com/0223aa7a-b0cf-49e3-9f08-90be5ccffbd1">RPC Return Values</a>.</div>
<div> </div>



## -remarks



When the 
<a href="https://msdn.microsoft.com/430561b2-c74b-423c-8448-339cc71dbd68">RpcServerListen</a> flag parameter <i>DontWait</i> has a nonzero value, the 
<a href="https://msdn.microsoft.com/430561b2-c74b-423c-8448-339cc71dbd68">RpcServerListen</a> function returns to the server application without performing the wait operation. In this case, the wait can be performed by 
<b>RpcMgmtWaitServerListen</b>.

Applications must call 
<a href="https://msdn.microsoft.com/430561b2-c74b-423c-8448-339cc71dbd68">RpcServerListen</a> with a nonzero value for the <i>DontWait</i> parameter before calling 
<b>RpcMgmtWaitServerListen</b>. The 
<b>RpcMgmtWaitServerListen</b> function returns after the server application calls 
<a href="https://msdn.microsoft.com/aeb6084a-e2ea-4468-85f8-2ae6cc4dbe84">RpcMgmtStopServerListening</a> and all active remote procedure calls complete, or after a fatal error occurs in the RPC run-time library.

<div class="alert"><b>Note</b>  <b>RpcMgmtWaitServerListen</b> is a Microsoft extension to the DCE API set.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/aeb6084a-e2ea-4468-85f8-2ae6cc4dbe84">RpcMgmtStopServerListening</a>



<a href="https://msdn.microsoft.com/430561b2-c74b-423c-8448-339cc71dbd68">RpcServerListen</a>
 

 

