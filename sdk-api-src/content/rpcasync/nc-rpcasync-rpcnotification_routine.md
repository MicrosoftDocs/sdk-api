---
UID: NC:rpcasync.RPCNOTIFICATION_ROUTINE
title: RPCNOTIFICATION_ROUTINE (rpcasync.h)
description: The RPCNOTIFICATION_ROUTINE function provides programs that utilize asynchronous RPC with the ability to customize responses to asynchronous events.
helpviewer_keywords: ["RPCNOTIFICATION_ROUTINE","RPCNOTIFICATION_ROUTINE callback","RPCNOTIFICATION_ROUTINE callback function [RPC]","RpcnotificationRoutine","_rpc_rpcnotification_routine","rpc.rpcnotification_routine","rpcasync/RPCNOTIFICATION_ROUTINE"]
old-location: rpc\rpcnotification_routine.htm
tech.root: Rpc
ms.assetid: 679d7a40-5803-4c18-950b-e6763cbf10f2
ms.date: 12/05/2018
ms.keywords: RPCNOTIFICATION_ROUTINE, RPCNOTIFICATION_ROUTINE callback, RPCNOTIFICATION_ROUTINE callback function [RPC], RpcnotificationRoutine, _rpc_rpcnotification_routine, rpc.rpcnotification_routine, rpcasync/RPCNOTIFICATION_ROUTINE
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - RPCNOTIFICATION_ROUTINE
 - rpcasync/RPCNOTIFICATION_ROUTINE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - rpcasync.h
api_name:
 - RPCNOTIFICATION_ROUTINE
---

# RPCNOTIFICATION_ROUTINE callback function


## -description

The 
<b>RPCNOTIFICATION_ROUTINE</b> function provides programs that utilize asynchronous RPC with the ability to customize responses to asynchronous events.

## -parameters

### -param pAsync

Pointer to a structure that contains the current state of the asynchronous RPC run-time library. For more information, see 
<a href="/windows/desktop/api/rpcasync/ns-rpcasync-rpc_async_state">RPC_ASYNC_STATE</a>.

### -param Context

Reserved for future use. Windows 2000 currently sets this parameter to <b>NULL</b>.

### -param Event

A value from the 
<a href="/windows/desktop/api/rpcasync/ne-rpcasync-rpc_async_event">RPC_ASYNC_EVENT</a> enumerated type that identifies the current asynchronous event.

## -remarks

For each 
<a href="/windows/desktop/Rpc/asynchronous-rpc">asynchronous remote procedure call</a> that a client program executes, it can specify an 
<a href="/windows/desktop/Sync/asynchronous-procedure-calls">asynchronous procedure call (APC)</a>. The RPC run-time library will invoke the APC when the asynchronous remote procedure call completes. The APC function must match the prototype specified by 
<b>RPCNOTIFICATION_ROUTINE</b>.

## -see-also

<a href="/windows/desktop/Rpc/asynchronous-rpc">Asynchronous RPC</a>



<a href="/windows/desktop/api/rpcasync/ns-rpcasync-rpc_async_state">RPC_ASYNC_STATE</a>
