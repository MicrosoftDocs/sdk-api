---
UID: NF:rpcndr.NdrUserMarshalBufferSize
title: NdrUserMarshalBufferSize function (rpcndr.h)
description: The NdrUserMarshalBufferSize function calculates the size of the buffer, in bytes, needed to marshal the user marshal object.
helpviewer_keywords: ["NdrUserMarshalBufferSize","NdrUserMarshalBufferSize function [RPC]","rpc.ndrusermarshalbuffersize","rpcndr/NdrUserMarshalBufferSize"]
old-location: rpc\ndrusermarshalbuffersize.htm
tech.root: Rpc
ms.assetid: 6c3f9073-3695-4eec-a973-e40aa55f9504
ms.date: 12/05/2018
ms.keywords: NdrUserMarshalBufferSize, NdrUserMarshalBufferSize function [RPC], rpc.ndrusermarshalbuffersize, rpcndr/NdrUserMarshalBufferSize
f1_keywords:
- rpcndr/NdrUserMarshalBufferSize
dev_langs:
- c++
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
req.lib: RpcRT4.lib
req.dll: RpcRT4.dll
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- DllExport
api_location:
- RpcRT4.dll
api_name:
- NdrUserMarshalBufferSize
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# NdrUserMarshalBufferSize function


## -description


The <b>NdrUserMarshalBufferSize</b> function calculates the size of the buffer, in bytes, needed to marshal the user marshal object.


## -parameters




### -param pStubMsg [in, out]

Pointer to a <a href="https://docs.microsoft.com/windows/desktop/api/rpcndr/ns-rpcndr-midl_stub_message">MIDL_STUB_MESSAGE</a> structure that maintains the current status of the RPC stub. The <b>BufferLength</b> member contains the size of the buffer. Structure is for internal use only; do not modify.


### -param pMemory [in]

Pointer to the user marshal object to be calculated.


### -param pFormat [in]

Pointer to the format string description.


