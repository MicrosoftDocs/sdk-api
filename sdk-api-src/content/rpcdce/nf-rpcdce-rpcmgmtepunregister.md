---
UID: NF:rpcdce.RpcMgmtEpUnregister
title: RpcMgmtEpUnregister function
author: windows-driver-content
description: The RpcMgmtEpUnregister function removes server address information from an endpoint map.
old-location: rpc\rpcmgmtepunregister.htm
old-project: Rpc
ms.assetid: b825a79d-7f9e-45f1-88d0-a3b733a7df78
ms.author: windowsdriverdev
ms.date: 5/1/2018
ms.keywords: RpcMgmtEpUnregister, RpcMgmtEpUnregister function [RPC], _rpc_rpcmgmtepunregister, rpc.rpcmgmtepunregister, rpcdce/RpcMgmtEpUnregister
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: rpcdce.h
req.include-header: Rpc.h
req.target-type: Windows
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
req.typenames: RPC_CALL_LOCAL_ADDRESS_V1, *PRPC_CALL_LOCAL_ADDRESS_V1
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Rpcrt4.dll
api_name:
-	RpcMgmtEpUnregister
product: Windows
targetos: Windows
req.lib: Rpcrt4.lib
req.dll: Rpcrt4.dll
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# RpcMgmtEpUnregister function


## -description


<p class="CCE_Message">[This function is  supported only on Windows NT and Windows Me/98/95; it returns EP_S_CANT_PERFORM_OP on other versions of Windows.]

The 
<b>RpcMgmtEpUnregister</b> function removes server address information from an endpoint map. 


## -parameters




### -param EpBinding

Host whose endpoint-map elements are to be unregistered. To remove elements from the same host as the calling application, the application specifies a value of <b>NULL</b>. To remove elements from another host, the application specifies a server binding handle for any server residing on that host. Note that the application can specify the same binding handle it is using to make other remote procedure calls.


### -param IfId

Interface identifier to remove from the endpoint map.


### -param Binding

Binding handle to remove.


### -param ObjectUuid

Optional object UUID to remove. The value <b>NULL</b> indicates there is no object UUID to remove.


## -returns



<table>
<tr>
<th>Return code</th>
<th>Description</th>
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
<dt><b>RPC_S_CANT_PERFORM_OP</b></dt>
</dl>
</td>
<td width="60%">
Cannot perform the requested operation.

</td>
</tr>
</table>
 

<div class="alert"><b>Note</b>  For a list of valid error codes, see 
<a href="https://msdn.microsoft.com/0223aa7a-b0cf-49e3-9f08-90be5ccffbd1">RPC Return Values</a>.</div>
<div> </div>



## -remarks



The 
<b>RpcMgmtEpUnregister</b> function unregisters an element from the endpoint map. A management program calls this function to remove addresses of servers that are no longer available, or to remove addresses of servers that support objects that are no longer offered.

The <i>EpBinding</i> parameter must be a full binding. The object UUID associated with the <i>EpBinding</i> parameter must be a nil UUID. Specifying a non-nil UUID causes the function to fail with the status code EPT_S_CANT_PERFORM_OP. Other than the host information and object UUID, all information in this argument is ignored.

An application calls 
<a href="https://msdn.microsoft.com/e1f79435-6868-453b-8237-da52e57ec96f">RpcMgmtEpEltInqNext</a> to view local endpoint-map elements. The application can then remove the elements using 
<b>RpcMgmtEpUnregister</b>.

<div class="alert"><b>Note</b>  Use this function with caution. Removing elements from the local endpoint map may make servers unavailable to client applications that do not already have a fully-bound binding handle to the server.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/35656cdd-b1ae-43d3-a5c7-92bdb7726d5b">RpcEpRegister</a>



<a href="https://msdn.microsoft.com/bb0485fc-0b25-4fc0-9a18-921a9de428ce">RpcEpUnregister</a>



<a href="https://msdn.microsoft.com/e1f79435-6868-453b-8237-da52e57ec96f">RpcMgmtEpEltInqNext</a>
 

 

