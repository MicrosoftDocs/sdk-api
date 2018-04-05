---
UID: NF:rpcnsi.RpcNsBindingImportDone
title: RpcNsBindingImportDone function
author: windows-driver-content
description: The RpcNsBindingImportDone function signals that a client has finished looking for a compatible server and deletes the import context.
old-location: rpc\rpcnsbindingimportdone.htm
old-project: Rpc
ms.assetid: 093c988a-5d88-45b5-b69a-f26962118fdb
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: RpcNsBindingImportDone, RpcNsBindingImportDone function [RPC], _rpc_rpcnsbindingimportdone, rpc.rpcnsbindingimportdone, rpcnsi/RpcNsBindingImportDone
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
req.typenames: NDR_USER_MARSHAL_INFO_LEVEL1
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Rpcns4.dll
api_name:
-	RpcNsBindingImportDone
product: Windows
targetos: Windows
req.lib: Rpcns4.lib
req.dll: Rpcns4.dll
req.irql: 
req.product: Compute Cluster Pack Client Utilities
---

# RpcNsBindingImportDone function


## -description


The 
<b>RpcNsBindingImportDone</b> function signals that a client has finished looking for a compatible server and deletes the import context.
<div class="alert"><b>Note</b>  This function is not supported on Windows Vista and later operating systems.</div><div> </div>

## -parameters




### -param ImportContext

Pointer to a name-service handle to free. The name-service handle <i>ImportContext</i> points to is created by calling the 
<a href="https://msdn.microsoft.com/8dca0490-72aa-41e0-b747-863d53a705ea">RpcNsBindingImportBegin</a> function. 




An argument value of <b>NULL</b> is returned.


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



Typically, a client application calls 
<b>RpcNsBindingImportDone</b> after completing remote procedure calls to a server using a binding handle returned from the 
<a href="https://msdn.microsoft.com/c437cd19-0cf8-4fc9-b6fb-cb09cde9a82e">RpcNsBindingImportNext</a> function. However, a client application is responsible for calling 
<b>RpcNsBindingImportDone</b> for each import context that was created by calling the 
<a href="https://msdn.microsoft.com/8dca0490-72aa-41e0-b747-863d53a705ea">RpcNsBindingImportBegin</a>, regardless of the status returned from 
<b>RpcNsBindingImportNext</b> or the success in making remote procedure calls.




## -see-also




<a href="https://msdn.microsoft.com/8dca0490-72aa-41e0-b747-863d53a705ea">RpcNsBindingImportBegin</a>



<a href="https://msdn.microsoft.com/c437cd19-0cf8-4fc9-b6fb-cb09cde9a82e">RpcNsBindingImportNext</a>
 

 

