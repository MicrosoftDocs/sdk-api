---
UID: NF:objidl.IRpcChannelBuffer.FreeBuffer
title: IRpcChannelBuffer::FreeBuffer (objidl.h)
description: The IRpcChannelBuffer::FreeBuffer method (objidl.h) frees a previously allocated RPC channel buffer. 
helpviewer_keywords: ["FreeBuffer","FreeBuffer method [COM]","FreeBuffer method [COM]","IRpcChannelBuffer interface","IRpcChannelBuffer interface [COM]","FreeBuffer method","IRpcChannelBuffer.FreeBuffer","IRpcChannelBuffer::FreeBuffer","_com_irpcchannelbuffer_freebuffer","com.irpcchannelbuffer_freebuffer","objidlbase/IRpcChannelBuffer::FreeBuffer"]
old-location: com\irpcchannelbuffer_freebuffer.htm
tech.root: com
ms.assetid: bcdd4783-4a75-42d0-86a9-ab2605abbbe1
ms.date: 08/12/2022
ms.keywords: FreeBuffer, FreeBuffer method [COM], FreeBuffer method [COM],IRpcChannelBuffer interface, IRpcChannelBuffer interface [COM],FreeBuffer method, IRpcChannelBuffer.FreeBuffer, IRpcChannelBuffer::FreeBuffer, _com_irpcchannelbuffer_freebuffer, com.irpcchannelbuffer_freebuffer, objidlbase/IRpcChannelBuffer::FreeBuffer
req.header: objidl.h
req.include-header: ObjIdl.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: ObjIdl.idl
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
 - IRpcChannelBuffer::FreeBuffer
 - objidl/IRpcChannelBuffer::FreeBuffer
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - objidlbase.h
api_name:
 - IRpcChannelBuffer.FreeBuffer
---

# IRpcChannelBuffer::FreeBuffer


## -description

Frees a previously allocated RPC channel buffer.

## -parameters

### -param pMessage [in, out]

A pointer to an <a href="/windows/desktop/api/objidl/ns-objidl-rpcolemessage">RPCOLEMESSAGE</a> data structure.

## -returns

This method can return the standard return values E_INVALIDARG, E_OUTOFMEMORY, E_UNEXPECTED, E_FAIL, and S_OK.

## -see-also

<a href="/windows/desktop/api/objidl/nn-objidl-irpcchannelbuffer">IRpcChannelBuffer</a>
