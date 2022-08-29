---
UID: NF:objidlbase.IRpcChannelBuffer.GetBuffer
title: IRpcChannelBuffer::GetBuffer (objidlbase.h)
description: The IRpcChannelBuffer::GetBuffer (objidlbase.h) method retrieves a buffer into which data can be marshaled for transmission.
helpviewer_keywords: ["GetBuffer","GetBuffer method [COM]","GetBuffer method [COM]","IRpcChannelBuffer interface","IRpcChannelBuffer interface [COM]","GetBuffer method","IRpcChannelBuffer.GetBuffer","IRpcChannelBuffer::GetBuffer","_com_irpcchannelbuffer_getbuffer","com.irpcchannelbuffer_getbuffer","objidlbase/IRpcChannelBuffer::GetBuffer"]
old-location: com\irpcchannelbuffer_getbuffer.htm
tech.root: com
ms.assetid: 775a15df-8bcf-4c1b-a8b9-5c7c03106c09
ms.date: 08/13/2022
ms.keywords: GetBuffer, GetBuffer method [COM], GetBuffer method [COM],IRpcChannelBuffer interface, IRpcChannelBuffer interface [COM],GetBuffer method, IRpcChannelBuffer.GetBuffer, IRpcChannelBuffer::GetBuffer, _com_irpcchannelbuffer_getbuffer, com.irpcchannelbuffer_getbuffer, objidlbase/IRpcChannelBuffer::GetBuffer
req.header: objidlbase.h
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
 - IRpcChannelBuffer::GetBuffer
 - objidlbase/IRpcChannelBuffer::GetBuffer
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
 - IRpcChannelBuffer.GetBuffer
---

# IRpcChannelBuffer::GetBuffer


## -description

Retrieves a buffer into which data can be marshaled for transmission.

## -parameters

### -param pMessage [in, out]

A pointer to an <a href="/windows/desktop/api/objidl/ns-objidl-rpcolemessage">RPCOLEMESSAGE</a> data structure.

### -param riid [in]

A reference to the identifier of the interface to be marshaled.

## -returns

This method can return the standard return values E_INVALIDARG, E_OUTOFMEMORY, E_UNEXPECTED, E_FAIL, and S_OK.

## -see-also

<a href="/windows/desktop/api/objidl/nn-objidl-irpcchannelbuffer">IRpcChannelBuffer</a>
