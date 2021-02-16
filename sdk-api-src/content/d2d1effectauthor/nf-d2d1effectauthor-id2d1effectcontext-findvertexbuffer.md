---
UID: NF:d2d1effectauthor.ID2D1EffectContext.FindVertexBuffer
title: ID2D1EffectContext::FindVertexBuffer (d2d1effectauthor.h)
description: This finds the given vertex buffer if it has already been created with ID2D1EffectContext::CreateVertexBuffer with the same GUID.
helpviewer_keywords: ["FindVertexBuffer","FindVertexBuffer method [Direct2D]","FindVertexBuffer method [Direct2D]","ID2D1EffectContext interface","ID2D1EffectContext interface [Direct2D]","FindVertexBuffer method","ID2D1EffectContext.FindVertexBuffer","ID2D1EffectContext::FindVertexBuffer","d2d1effectauthor/ID2D1EffectContext::FindVertexBuffer","direct2d.id2d1contextinternal_findvertexbuffer"]
old-location: direct2d\id2d1contextinternal_findvertexbuffer.htm
tech.root: Direct2D
ms.assetid: 8CAC0872-2368-4926-8FF9-87D73136986F
ms.date: 12/05/2018
ms.keywords: FindVertexBuffer, FindVertexBuffer method [Direct2D], FindVertexBuffer method [Direct2D],ID2D1EffectContext interface, ID2D1EffectContext interface [Direct2D],FindVertexBuffer method, ID2D1EffectContext.FindVertexBuffer, ID2D1EffectContext::FindVertexBuffer, d2d1effectauthor/ID2D1EffectContext::FindVertexBuffer, direct2d.id2d1contextinternal_findvertexbuffer
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
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ID2D1EffectContext::FindVertexBuffer
 - d2d1effectauthor/ID2D1EffectContext::FindVertexBuffer
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - d2d1.lib
 - d2d1.dll
api_name:
 - ID2D1EffectContext.FindVertexBuffer
---

# ID2D1EffectContext::FindVertexBuffer


## -description

This finds the given vertex buffer if it has already been created with <a href="/windows/desktop/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectcontext-createvertexbuffer">ID2D1EffectContext::CreateVertexBuffer</a> with the same GUID.

## -parameters

### -param resourceId [in]

Type: <b>const GUID*</b>

The unique id that identifies the vertex buffer.

### -param buffer [out]

Type: <b><a href="/windows/desktop/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1vertexbuffer">ID2D1VertexBuffer</a>**</b>

The returned vertex buffer that can be used as a resource in a <a href="/windows/desktop/Direct2D/direct2d-portal">Direct2D</a> effect.

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
<td>E_NOTFOUND</td>
<td>The requested vertex buffer was not found.</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1effectcontext">ID2D1EffectContext</a>