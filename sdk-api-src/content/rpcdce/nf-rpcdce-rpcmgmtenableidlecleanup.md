---
UID: NF:rpcdce.RpcMgmtEnableIdleCleanup
title: RpcMgmtEnableIdleCleanup function
author: windows-sdk-content
description: The RpcMgmtEnableIdleCleanup function enables RPC to close idle resources, such as network connections, on the client.
old-location: rpc\rpcmgmtenableidlecleanup.htm
old-project: Rpc
ms.assetid: f24bf105-2cdb-4efa-b095-8479545fecb5
ms.author: windowssdkdev
ms.date: 05/30/2018
ms.keywords: RpcMgmtEnableIdleCleanup, RpcMgmtEnableIdleCleanup function [RPC], _rpc_rpcmgmtenableidlecleanup, rpc.rpcmgmtenableidlecleanup, rpcdce/RpcMgmtEnableIdleCleanup
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
 - RpcMgmtEnableIdleCleanup
product: Windows
targetos: Windows
req.lib: Rpcrt4.lib
req.dll: Rpcrt4.dll
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# RpcMgmtEnableIdleCleanup function


## -description


The 
<b>RpcMgmtEnableIdleCleanup</b> function enables RPC to close idle resources, such as network connections, on the client.


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
The call succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>RPC_S_OUT_OF_THREADS</b></dt>
</dl>
</td>
<td width="60%">
Out of threads.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>RPC_S_OUT_OF_RESOURCES</b></dt>
</dl>
</td>
<td width="60%">
Out of resources.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>RPC_S_OUT_OF_MEMORY</b></dt>
</dl>
</td>
<td width="60%">
Out of memory.

</td>
</tr>
</table>
 

<div class="alert"><b>Note</b>  For a list of valid error codes, see 
<a href="https://msdn.microsoft.com/0223aa7a-b0cf-49e3-9f08-90be5ccffbd1">RPC Return Values</a>.</div>
<div> </div>



## -remarks



<div class="alert"><b>Note</b>  <b>RpcMgmtEnableIdleCleanup</b> is a Microsoft extension to the OSF-DCE RPC specification.</div>
<div> </div>
Calling this function only is sufficient. Once called, idle resource cleanup cannot be turned off. In some cases, depending on Windows version and configuration, RPC Runtime may need to create a separate thread in order to perform such cleanup, which is why idle resource cleanup is not always turned on. On Windows XP and later versions of Windows, RPC Runtime is programmed to automatically turn on idle resource cleanup if idle resources reach a certain threshold.




## -see-also




<a href="https://msdn.microsoft.com/bcaf4a0d-8a0d-4016-ab6e-9e1a0fd65d4b">RpcServerUnregisterIf</a>
 

 

