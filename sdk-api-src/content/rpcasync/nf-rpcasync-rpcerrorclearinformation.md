---
UID: NF:rpcasync.RpcErrorClearInformation
title: RpcErrorClearInformation function
author: windows-driver-content
description: The RpcErrorClearInformation function clears all extended error information on the current thread.
old-location: rpc\rpcerrorclearinformation.htm
old-project: Rpc
ms.assetid: ff96904c-285d-4d39-af3b-bf295c29e62f
ms.author: windowsdriverdev
ms.date: 5/1/2018
ms.keywords: RpcErrorClearInformation, RpcErrorClearInformation function [RPC], _rpc_rpcerrorclearinformation, rpc.rpcerrorclearinformation, rpcasync/RpcErrorClearInformation
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: rpcasync.h
req.include-header: Rpc.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2003 [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: RPC_NOTIFICATION_TYPES
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Rpcrt4.dll
api_name:
-	RpcErrorClearInformation
product: Windows
targetos: Windows
req.lib: Rpcrt4.lib
req.dll: Rpcrt4.dll
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# RpcErrorClearInformation function


## -description


The 
<b>RpcErrorClearInformation</b> function clears all extended error information on the current thread.


## -parameters






## -returns



This function has no return values.

<div class="alert"><b>Note</b>  For a list of valid error codes, see 
<a href="https://msdn.microsoft.com/0223aa7a-b0cf-49e3-9f08-90be5ccffbd1">RPC Return Values</a>.</div>
<div> </div>



## -remarks



The RPC Runtime usually handles the clearing of extended error information. In only two cases should callers use 
<b>RpcErrorClearInformation</b>:

<ul>
<li>If the calling component adds records to the thread using the 
<a href="https://msdn.microsoft.com/b82708ef-0760-49b0-87d2-3d55a07b351f">RpcErrorAddRecord</a> function, then decides it has not encountered a fatal error and continues processing the original, or the error is not connected to the records is has added. In this case, the calling component needs to clear the error information from the thread to prevent the propagation of potentially misleading error information.</li>
<li>If the calling component attempts multiple retries of an operation that returns extended error information. When an RPC call starts, the RPC Runtime clears any extended error information on the thread. However, if the calling component calls 
<a href="https://msdn.microsoft.com/b82708ef-0760-49b0-87d2-3d55a07b351f">RpcErrorAddRecord</a> in a loop with many iterations, it may want to clear the error information, as the extended error information accumulates over time and can exhaust available memory.</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/7a386def-c640-42f4-9869-b6a1c522984a">Obtaining Extended RPC Error Information</a>



<a href="https://msdn.microsoft.com/b82708ef-0760-49b0-87d2-3d55a07b351f">RpcErrorAddRecord</a>



<a href="https://msdn.microsoft.com/cc2d3aa0-2956-4710-ad31-a347d9ef9043">RpcErrorGetNextRecord</a>



<a href="https://msdn.microsoft.com/56c61902-4b34-4d92-b352-cd1837754aa3">RpcErrorStartEnumeration</a>
 

 

