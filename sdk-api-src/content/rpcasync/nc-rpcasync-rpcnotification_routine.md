---
UID: NC:rpcasync.RPCNOTIFICATION_ROUTINE
title: RPCNOTIFICATION_ROUTINE
author: windows-sdk-content
description: The RPCNOTIFICATION_ROUTINE function provides programs that utilize asynchronous RPC with the ability to customize responses to asynchronous events.
old-location: rpc\rpcnotification_routine.htm
tech.root: Rpc
ms.assetid: 679d7a40-5803-4c18-950b-e6763cbf10f2
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: RPCNOTIFICATION_ROUTINE, RPCNOTIFICATION_ROUTINE callback, RPCNOTIFICATION_ROUTINE callback function [RPC], RpcnotificationRoutine, _rpc_rpcnotification_routine, rpc.rpcnotification_routine, rpcasync/RPCNOTIFICATION_ROUTINE
ms.prod: windows
ms.technology: windows-sdk
ms.topic: callback
req.header: rpcasync.h
req.include-header: 
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - rpcasync.h
api_name:
 - RPCNOTIFICATION_ROUTINE
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# RPCNOTIFICATION_ROUTINE callback function


## -description


The 
<b>RPCNOTIFICATION_ROUTINE</b> function provides programs that utilize asynchronous RPC with the ability to customize responses to asynchronous events.


## -parameters




### -param *pAsync

Pointer to a structure that contains the current state of the asynchronous RPC run-time library. For more information, see 
<a href="https://msdn.microsoft.com/ad004f49-89a6-486c-80ec-5b85ab4b8db9">RPC_ASYNC_STATE</a>.


### -param *Context

Reserved for future use. Windows 2000 currently sets this parameter to <b>NULL</b>.


### -param Event

A value from the 
<a href="https://msdn.microsoft.com/6b173ec8-2b58-4a99-87cd-cdf1f92a35ad">RPC_ASYNC_EVENT</a> enumerated type that identifies the current asynchronous event.


## -returns



This function does not return a value.




## -remarks



For each 
<a href="https://msdn.microsoft.com/2586c10e-8284-419f-a200-4f6b11953688">asynchronous remote procedure call</a> that a client program executes, it can specify an 
<a href="https://msdn.microsoft.com/0197d78e-a4dc-414b-88ba-c5ec5f2ed614">asynchronous procedure call (APC)</a>. The RPC run-time library will invoke the APC when the asynchronous remote procedure call completes. The APC function must match the prototype specified by 
<b>RPCNOTIFICATION_ROUTINE</b>.




## -see-also




<a href="https://msdn.microsoft.com/2586c10e-8284-419f-a200-4f6b11953688">Asynchronous RPC</a>



<a href="https://msdn.microsoft.com/ad004f49-89a6-486c-80ec-5b85ab4b8db9">RPC_ASYNC_STATE</a>
 

 

