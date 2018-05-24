---
UID: NF:rpcndr.NdrUserMarshalBufferSize
title: NdrUserMarshalBufferSize function
author: windows-driver-content
description: The NdrUserMarshalBufferSize function calculates the size of the buffer, in bytes, needed to marshal the user marshal object.
old-location: rpc\ndrusermarshalbuffersize.htm
old-project: Rpc
ms.assetid: 6c3f9073-3695-4eec-a973-e40aa55f9504
ms.author: windowsdriverdev
ms.date: 5/18/2018
ms.keywords: NdrUserMarshalBufferSize, NdrUserMarshalBufferSize function [RPC], rpc.ndrusermarshalbuffersize, rpcndr/NdrUserMarshalBufferSize
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
-	NdrUserMarshalBufferSize
product: Windows
targetos: Windows
req.lib: RpcRT4.lib
req.dll: RpcRT4.dll
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# NdrUserMarshalBufferSize function


## -description


The <b>NdrUserMarshalBufferSize</b> function calculates the size of the buffer, in bytes, needed to marshal the user marshal object.


## -parameters




### -param pStubMsg [in, out]

Pointer to a <a href="https://msdn.microsoft.com/9bd021f6-10c9-4e77-be75-9a89a3a016e0">MIDL_STUB_MESSAGE</a> structure that maintains the current status of the RPC stub. The <b>BufferLength</b> member contains the size of the buffer. Structure is for internal use only; do not modify.


### -param pMemory [in]

Pointer to the user marshal object to be calculated.


### -param pFormat [in]

Pointer to the format string description.


## -returns



This function does not return a value.



