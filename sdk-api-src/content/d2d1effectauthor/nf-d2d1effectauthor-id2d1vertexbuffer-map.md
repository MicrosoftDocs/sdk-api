---
UID: NF:d2d1effectauthor.ID2D1VertexBuffer.Map
title: ID2D1VertexBuffer::Map (d2d1effectauthor.h)
description: Maps the provided data into user memory.
helpviewer_keywords: ["ID2D1VertexBuffer interface [Direct2D]","Map method","ID2D1VertexBuffer.Map","ID2D1VertexBuffer::Map","Map","Map method [Direct2D]","Map method [Direct2D]","ID2D1VertexBuffer interface","d2d1effectauthor/ID2D1VertexBuffer::Map","direct2d.id2d1vertexbuffer_map"]
old-location: direct2d\id2d1vertexbuffer_map.htm
tech.root: Direct2D
ms.assetid: 3EFC0584-2F03-4B35-8C6C-E46CDD9D9057
ms.date: 12/05/2018
ms.keywords: ID2D1VertexBuffer interface [Direct2D],Map method, ID2D1VertexBuffer.Map, ID2D1VertexBuffer::Map, Map, Map method [Direct2D], Map method [Direct2D],ID2D1VertexBuffer interface, d2d1effectauthor/ID2D1VertexBuffer::Map, direct2d.id2d1vertexbuffer_map
req.header: d2d1effectauthor.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 and Platform Update for Windows 7 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 and Platform Update for Windows Server 2008 R2 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: D2d1.lib
req.dll: D2d1.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ID2D1VertexBuffer::Map
 - d2d1effectauthor/ID2D1VertexBuffer::Map
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D2d1.dll
api_name:
 - ID2D1VertexBuffer.Map
---

# ID2D1VertexBuffer::Map


## -description

Maps the provided data into user memory.

## -parameters

### -param data [out]

Type: <b>const BYTE**</b>

When this method returns, contains the address of a pointer to the available buffer.

### -param bufferSize

Type: <b>UINT32</b>

The desired size of the buffer.

## -returns

Type: <b>HRESULT</b>

The method returns an HRESULT. Possible values include, but are not limited to, those in the following table.


<table>
<tr>
<th>HRESULT</th>
<th>Description</th>
</tr>
<tr>
<td>S_OK</td>
<td>No error occurred.</td>
</tr>
<tr>
<td>E_INVALIDARG</td>
<td>An invalid parameter was passed to the returning function.</td>
</tr>
<tr>
<td>D3DERR_DEVICELOST</td>
<td>The device has been lost but cannot be reset at this time.</td>
</tr>
</table>

## -remarks

If <i>data</i> is larger than <i>bufferSize</i>, this method fails.

## -see-also

<a href="/windows/desktop/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectcontext-createvertexbuffer">ID2D1EffectContext::CreateVertexBuffer</a>



<a href="/windows/desktop/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1vertexbuffer">ID2D1VertexBuffer</a>