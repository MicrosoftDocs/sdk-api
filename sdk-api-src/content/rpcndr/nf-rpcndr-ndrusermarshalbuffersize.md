---
UID: NF:rpcndr.NdrUserMarshalBufferSize
title: NdrUserMarshalBufferSize function
author: windows-sdk-content
description: The NdrUserMarshalBufferSize function calculates the size of the buffer, in bytes, needed to marshal the user marshal object.
old-location: rpc\ndrusermarshalbuffersize.htm
old-project: rpc
ms.assetid: 6c3f9073-3695-4eec-a973-e40aa55f9504
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: NdrUserMarshalBufferSize, NdrUserMarshalBufferSize function [RPC], rpc.ndrusermarshalbuffersize, rpcndr/NdrUserMarshalBufferSize
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: rpcndr.h
req.include-header: Rpc.h
req.redist: 
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
 - NdrUserMarshalBufferSize
product: Windows
targetos: Windows
req.lib: RpcRT4.lib
req.dll: RpcRT4.dll
req.irql: 
req.product: ADAM
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



