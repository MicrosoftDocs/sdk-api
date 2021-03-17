---
UID: NF:d2d1effectauthor.ID2D1EffectContext.CreateVertexBuffer
title: ID2D1EffectContext::CreateVertexBuffer (d2d1effectauthor.h)
description: Creates a vertex buffer or finds a standard vertex buffer and optionally initializes it with vertices.
helpviewer_keywords: ["CreateVertexBuffer","CreateVertexBuffer method [Direct2D]","CreateVertexBuffer method [Direct2D]","ID2D1EffectContext interface","ID2D1EffectContext interface [Direct2D]","CreateVertexBuffer method","ID2D1EffectContext.CreateVertexBuffer","ID2D1EffectContext::CreateVertexBuffer","d2d1effectauthor/ID2D1EffectContext::CreateVertexBuffer","direct2d.id2d1contextinternal_createvertexbuffer"]
old-location: direct2d\id2d1contextinternal_createvertexbuffer.htm
tech.root: Direct2D
ms.assetid: 8E59527F-B6CE-4E25-B7F7-2D03BC1ACAFD
ms.date: 12/05/2018
ms.keywords: CreateVertexBuffer, CreateVertexBuffer method [Direct2D], CreateVertexBuffer method [Direct2D],ID2D1EffectContext interface, ID2D1EffectContext interface [Direct2D],CreateVertexBuffer method, ID2D1EffectContext.CreateVertexBuffer, ID2D1EffectContext::CreateVertexBuffer, d2d1effectauthor/ID2D1EffectContext::CreateVertexBuffer, direct2d.id2d1contextinternal_createvertexbuffer
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
req.lib: D2D1.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ID2D1EffectContext::CreateVertexBuffer
 - d2d1effectauthor/ID2D1EffectContext::CreateVertexBuffer
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D2D1.lib
 - D2D1.dll
api_name:
 - ID2D1EffectContext.CreateVertexBuffer
---

# ID2D1EffectContext::CreateVertexBuffer


## -description

Creates a vertex buffer or finds a standard vertex buffer and optionally initializes it with vertices. The returned buffer can be specified in the render info to specify both a vertex shader and or to pass custom vertices to the standard vertex shader used by <a href="/windows/desktop/Direct2D/direct2d-portal">Direct2D</a>.

## -parameters

### -param vertexBufferProperties [in]

Type: <b>const <a href="/windows/desktop/api/d2d1effectauthor/ns-d2d1effectauthor-d2d1_vertex_buffer_properties">D2D1_VERTEX_BUFFER_PROPERTIES</a>*</b>

The properties used to describe the vertex buffer and vertex shader.

### -param resourceId [in, optional]

Type: <b>const GUID*</b>

The unique id that identifies the vertex buffer.

### -param customVertexBufferProperties [in, optional]

Type: <b>const <a href="/windows/desktop/api/d2d1effectauthor/ns-d2d1effectauthor-d2d1_custom_vertex_buffer_properties">D2D1_CUSTOM_VERTEX_BUFFER_PROPERTIES</a>*</b>

The properties used to define a custom vertex buffer. If you use a built-in vertex shader, you don't have to specify this property.

### -param buffer [out]

Type: <b><a href="/windows/desktop/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1vertexbuffer">ID2D1VertexBuffer</a>**</b>

The returned vertex buffer.

## -returns

Type: <b>HRESULT</b>

The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

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
<td>E_OUTOFMEMORY</td>
<td>Direct2D could not allocate sufficient memory to complete the call.</td>
</tr>
<tr>
<td>E_INVALIDARG</td>
<td>An invalid parameter was passed to the returning function.</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1effectcontext">ID2D1EffectContext</a>