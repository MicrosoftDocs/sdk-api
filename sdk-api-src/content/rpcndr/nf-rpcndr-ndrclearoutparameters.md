---
UID: NF:rpcndr.NdrClearOutParameters
title: NdrClearOutParameters function
author: windows-driver-content
description: The NdrClearOutParameters function frees resources of the out parameter and clears its memory if the RPC call to the server fails.
old-location: rpc\ndrclearoutparameters.htm
old-project: Rpc
ms.assetid: f0ae23d5-3ec0-4e41-8c2c-5b6eb9bbb1b8
ms.author: windowsdriverdev
ms.date: 5/18/2018
ms.keywords: NdrClearOutParameters, NdrClearOutParameters
, NdrClearOutParameters function [RPC], rpc.ndrclearoutparameters, rpcndr/NdrClearOutParameters
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: rpcndr.h
req.include-header: Rpc.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps | UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: RPC_MESSAGE, *PRPC_MESSAGE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	RpcRT4.dll
api_name:
-	NdrClearOutParameters
product: Windows
targetos: Windows
req.lib: RpcRT4.lib
req.dll: RpcRT4.dll
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# NdrClearOutParameters function


## -description


The <b>NdrClearOutParameters</b> function frees resources of the out parameter and clears its memory if the RPC call to the server fails.


## -parameters




### -param pStubMsg [in]

Pointer to <a href="https://msdn.microsoft.com/9bd021f6-10c9-4e77-be75-9a89a3a016e0">MIDL_STUB_MESSAGE</a> structure that maintains the current status of the RPC stub. The structure is for internal use only and should not be modified.


### -param pFormat [in]

Pointer to the format string description.


### -param ArgAddr [in, out]

Pointer to the out parameter to be freed.


## -returns



This function does not return a value.



