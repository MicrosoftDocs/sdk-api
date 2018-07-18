---
UID: NF:rpcndr.NdrUserMarshalFree
title: NdrUserMarshalFree function
author: windows-sdk-content
description: The NdrUserMarshalFree function frees the user marshal object.
old-location: rpc\ndrusermarshalfree.htm
old-project: rpc
ms.assetid: 3b850938-13f3-4173-86bb-8b01ac0c5809
ms.author: windowssdkdev
ms.date: 05/31/2018
ms.keywords: NdrUserMarshalFree, NdrUserMarshalFree function [RPC], rpc.ndrusermarshalfree, rpcndr/NdrUserMarshalFree
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: rpcndr.h
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
req.typenames: RPC_MESSAGE, *PRPC_MESSAGE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - RpcRT4.dll
api_name:
 - NdrUserMarshalFree
product: Windows
targetos: Windows
req.lib: RpcRT4.lib
req.dll: RpcRT4.dll
req.irql: 
req.product: ADAM
---

# NdrUserMarshalFree function


## -description


The <b>NdrUserMarshalFree</b> function frees the user marshal object.



## -parameters




### -param pStubMsg [in, out]

Pointer to a <a href="https://msdn.microsoft.com/9bd021f6-10c9-4e77-be75-9a89a3a016e0">MIDL_STUB_MESSAGE</a> structure that maintains the current status of the RPC stub. Structure is for internal use only; do not modify.


### -param pMemory [in]

Pointer to be freed.


### -param pFormat [in]

Pointer's format string description.


## -returns



This function does not return a value.




## -remarks



You should never free the top level object, it is freed by the system.



