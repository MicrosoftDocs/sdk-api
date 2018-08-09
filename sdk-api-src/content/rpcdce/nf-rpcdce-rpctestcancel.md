---
UID: NF:rpcdce.RpcTestCancel
title: RpcTestCancel function
author: windows-sdk-content
description: The RpcTestCancel function checks for a cancel indication.
old-location: rpc\rpctestcancel.htm
old-project: rpc
ms.assetid: 1fd3b84d-ea45-4267-ac30-e4e2cf037c92
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: RpcTestCancel, RpcTestCancel function [RPC], _rpc_rpctestcancel, rpc.rpctestcancel, rpcdce/RpcTestCancel
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: rpcdce.h
req.include-header: Rpc.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps]
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
 - RpcTestCancel
product: Windows
targetos: Windows
req.lib: Rpcrt4.lib
req.dll: Rpcrt4.dll
req.irql: 
req.product: ADAM
---

# RpcTestCancel function


## -description


The 
<b>RpcTestCancel</b> function checks for a cancel indication.


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
The call has been canceled.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>Other values</b></dt>
</dl>
</td>
<td width="60%">
The call has not been canceled.

</td>
</tr>
</table>
 

<div class="alert"><b>Note</b>  For a list of valid error codes, see 
<a href="https://msdn.microsoft.com/0223aa7a-b0cf-49e3-9f08-90be5ccffbd1">RPC Return Values</a>.</div>
<div> </div>
It is not unusual for the 
<b>RpcTestCancel</b> function to return the value ERROR_ACCESS_DENIED. This indicates that the remote procedure call has not been canceled.




## -remarks



An application server stub calls 
<b>RpcTestCancel</b> to determine whether a call has been canceled. If the call has been canceled, RPC_S_OK is returned; otherwise, another value is returned.

This function should be called periodically by the server stub so that it can respond to cancels in a timely fashion. If the function returns RPC_S_OK, the stub should clean up its data structures and return to the client.




## -see-also




<a href="https://msdn.microsoft.com/de4b45a8-0516-4185-a342-364e0f5a633e">RpcServerTestCancel</a>
 

 

