---
UID: NF:rpcdce.RpcMgmtInqComTimeout
title: RpcMgmtInqComTimeout function
author: windows-sdk-content
description: The RpcMgmtInqComTimeout function returns the binding-communications time-out value in a binding handle.
old-location: rpc\rpcmgmtinqcomtimeout.htm
old-project: Rpc
ms.assetid: e7bb9955-68a7-49fe-bcdb-2450518ffe0a
ms.author: windowssdkdev
ms.date: 05/18/2018
ms.keywords: RpcMgmtInqComTimeout, RpcMgmtInqComTimeout function [RPC], _rpc_rpcmgmtinqcomtimeout, rpc.rpcmgmtinqcomtimeout, rpcdce/RpcMgmtInqComTimeout
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
req.typenames: RPC_CALL_LOCAL_ADDRESS_V1, *PRPC_CALL_LOCAL_ADDRESS_V1
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Rpcrt4.dll
api_name:
-	RpcMgmtInqComTimeout
product: Windows
targetos: Windows
req.lib: Rpcrt4.lib
req.dll: Rpcrt4.dll
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# RpcMgmtInqComTimeout function


## -description


The 
<b>RpcMgmtInqComTimeout</b> function returns the binding-communications time-out value in a binding handle.


## -parameters




### -param Binding

Specifies a binding.


### -param Timeout

Returns a pointer to the time-out value from the <i>Binding</i> parameter.


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
<dt><b>RPC_S_INVALID_BINDING</b></dt>
</dl>
</td>
<td width="60%">
The binding handle was invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>RPC_S_WRONG_KIND_OF_BINDING</b></dt>
</dl>
</td>
<td width="60%">
This was the wrong kind of binding for the operation.

</td>
</tr>
</table>
 

<div class="alert"><b>Note</b>  For a list of valid error codes, see 
<a href="https://msdn.microsoft.com/0223aa7a-b0cf-49e3-9f08-90be5ccffbd1">RPC Return Values</a>.</div>
<div> </div>



## -remarks



A client application calls 
<b>RpcMgmtInqComTimeout</b> to view the time-out value in a server binding handle. The time-out value specifies the relative amount of time that should be spent to wait for a response from the server before giving up. For a table of the time-out values, see 
<a href="https://msdn.microsoft.com/bf5f3f08-ab29-4732-9ce3-d6d7ad699369">Binding Time-out Constants</a>. For more information on how the COM time-out operates, and when to use it, see 
<a href="https://msdn.microsoft.com/af7c67ea-32af-40b0-b74b-0a339e5088c4">RPC and the Network</a>.

A client also calls 
<a href="https://msdn.microsoft.com/3ea6fe6a-2064-4f53-852a-041281b62bbd">RpcMgmtSetComTimeout</a> to change the time-out value.




## -see-also




<a href="https://msdn.microsoft.com/bf5f3f08-ab29-4732-9ce3-d6d7ad699369">Binding
		  Time-out Constants</a>



<a href="https://msdn.microsoft.com/478b9f33-db01-4a1d-9b5b-dc2662ee8d7b">RpcMgmtInqStats</a>



<a href="https://msdn.microsoft.com/3ea6fe6a-2064-4f53-852a-041281b62bbd">RpcMgmtSetComTimeout</a>
 

 

