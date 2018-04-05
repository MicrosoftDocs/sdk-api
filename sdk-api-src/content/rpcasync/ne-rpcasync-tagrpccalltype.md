---
UID: NE:rpcasync.tagRpcCallType
title: tagRpcCallType
author: windows-driver-content
description: Specifies the set of RPC call types.
old-location: rpc\rpccalltype.htm
old-project: Rpc
ms.assetid: b7b95f51-ced4-423f-88b7-b1ec705af66f
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: RpcCallType, RpcCallType enumeration [RPC], rctGuaranteed, rctInvalid, rctNormal, rctTraining, rpc.rpccalltype, rpcasync/RpcCallType, rpcasync/rctGuaranteed, rpcasync/rctInvalid, rpcasync/rctNormal, rpcasync/rctTraining, tagRpcCallType
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
req.header: rpcasync.h
req.include-header: Rpc.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista, Windows XP with SP2 [desktop apps only]
req.target-min-winversvr: Windows Server 2008, Windows Server 2003 with SP1 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: RpcCallType
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Rpcasync.h
api_name:
-	RpcCallType
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Compute Cluster Pack Client Utilities
---

# tagRpcCallType enumeration


## -description


The <b>RpcCallType</b> enumeration specifies the set of RPC call types.


## -enum-fields




### -field rctInvalid

The remote procedure call is invalid.


### -field rctNormal

The remote procedure call has no special properties.


### -field rctTraining

The remote procedure call is used for "training" RPC.


### -field rctGuaranteed

The remote procedure call has guaranteed execution.


## -see-also




<a href="https://msdn.microsoft.com/eccc4b78-19f8-415f-bd0f-b1f9f454435e">RPC_CALL_ATTRIBUTES_V2</a>
 

 

