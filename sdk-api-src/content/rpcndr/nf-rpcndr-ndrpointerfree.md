---
UID: NF:rpcndr.NdrPointerFree
title: NdrPointerFree function
author: windows-sdk-content
description: The NdrPointerFree function frees memory.
old-location: rpc\ndrpointerfree.htm
old-project: Rpc
ms.assetid: 8b90ae12-af0f-41f8-9b8d-4b354de511be
ms.author: windowssdkdev
ms.date: 05/18/2018
ms.keywords: NdrPointerFree, NdrPointerFree function [RPC], rpc.ndrpointerfree, rpcndr/NdrPointerFree
ms.prod: windows
ms.technology: windows-sdk
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
-	NdrPointerFree
product: Windows
targetos: Windows
req.lib: RpcRT4.lib
req.dll: RpcRT4.dll
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# NdrPointerFree function


## -description


The <b>NdrPointerFree</b> function frees memory.


## -parameters




### -param pStubMsg [in, out]

Pointer to a <a href="https://msdn.microsoft.com/9bd021f6-10c9-4e77-be75-9a89a3a016e0">MIDL_STUB_MESSAGE</a> structure that maintains the current status of the RPC stub.  This structure is for internal use only and should not be modified.


### -param pMemory [in]

Pointer to memory to be freed.


### -param pFormat [in]

Pointer to the format string description.


## -returns



This function does not return a value.



