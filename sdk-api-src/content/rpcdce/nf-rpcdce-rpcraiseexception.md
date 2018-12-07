---
UID: NF:rpcdce.RpcRaiseException
title: RpcRaiseException function
author: windows-sdk-content
description: Use the RpcRaiseException function to raise an exception. The function does not return to the caller.
old-location: rpc\rpcraiseexception.htm
tech.root: rpc
ms.assetid: 0bffc62e-a80e-4af1-a17a-ef4f00b9c4da
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: RpcRaiseException, RpcRaiseException function [RPC], _rpc_rpcraiseexception, rpc.rpcraiseexception, rpcdce/RpcRaiseException
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - RpcRaiseException
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# RpcRaiseException function


## -description


Use the 
<b>RpcRaiseException</b> function to raise an exception. The function does not return to the caller.


## -parameters




### -param exception

Exception code for the exception.


## -returns



This function does not return a value.

<div class="alert"><b>Note</b>  For a list of valid error codes, see 
<a href="https://msdn.microsoft.com/0223aa7a-b0cf-49e3-9f08-90be5ccffbd1">RPC Return Values</a>.</div>
<div> </div>



## -remarks



<b>RpcRaiseException</b> raises an exception. The exception handler can then handle the exception. For more information about handling exceptions, see 
<a href="https://msdn.microsoft.com/4882d29b-08f3-41ec-84c3-35df6c56fd31">Making RPC Function Calls</a>.




## -see-also




<a href="https://msdn.microsoft.com/6025da80-d334-4abd-9d7c-6cce139cd4d7">RpcAbnormalTermination</a>



<a href="https://msdn.microsoft.com/5bd57250-1fd7-4aeb-aa53-4fd2c8d84836">RpcExcept</a>



<a href="https://msdn.microsoft.com/332641ea-748f-47e5-bb0e-33d2bf4e04c9">RpcFinally</a>
 

 

