---
UID: NF:d2d1effectauthor.ID2D1VertexBuffer.Unmap
title: ID2D1VertexBuffer::Unmap (d2d1effectauthor.h)
description: Unmaps the vertex buffer.
helpviewer_keywords: ["ID2D1VertexBuffer interface [Direct2D]","Unmap method","ID2D1VertexBuffer.Unmap","ID2D1VertexBuffer::Unmap","Unmap","Unmap method [Direct2D]","Unmap method [Direct2D]","ID2D1VertexBuffer interface","d2d1effectauthor/ID2D1VertexBuffer::Unmap","direct2d.id2d1vertexbuffer_unmap"]
old-location: direct2d\id2d1vertexbuffer_unmap.htm
tech.root: Direct2D
ms.assetid: DD33E4D4-C020-4830-AD31-380E8E9217D0
ms.date: 12/05/2018
ms.keywords: ID2D1VertexBuffer interface [Direct2D],Unmap method, ID2D1VertexBuffer.Unmap, ID2D1VertexBuffer::Unmap, Unmap, Unmap method [Direct2D], Unmap method [Direct2D],ID2D1VertexBuffer interface, d2d1effectauthor/ID2D1VertexBuffer::Unmap, direct2d.id2d1vertexbuffer_unmap
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
 - ID2D1VertexBuffer::Unmap
 - d2d1effectauthor/ID2D1VertexBuffer::Unmap
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
 - ID2D1VertexBuffer.Unmap
---

# ID2D1VertexBuffer::Unmap


## -description

Unmaps the vertex buffer.



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
<td>D2DERR_WRONG_STATE</td>
<td>The object was not in the correct state to process the method.</td>
</tr>
</table>

## -remarks

After this method returns, the mapped memory from the vertex buffer is no longer accessible by the effect.

## -see-also

<a href="/windows/desktop/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectcontext-createvertexbuffer">ID2D1EffectContext::CreateVertexBuffer</a>



<a href="/windows/desktop/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1vertexbuffer">ID2D1VertexBuffer</a>
