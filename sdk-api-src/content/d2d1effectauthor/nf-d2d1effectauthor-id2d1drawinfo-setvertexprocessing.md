---
UID: NF:d2d1effectauthor.ID2D1DrawInfo.SetVertexProcessing
title: ID2D1DrawInfo::SetVertexProcessing (d2d1effectauthor.h)
description: Sets a vertex buffer, a corresponding vertex shader, and options to control how the vertices are to be handled by the Direct2D context.
helpviewer_keywords: ["ID2D1DrawInfo interface [Direct2D]","SetVertexProcessing method","ID2D1DrawInfo.SetVertexProcessing","ID2D1DrawInfo::SetVertexProcessing","SetVertexProcessing","SetVertexProcessing method [Direct2D]","SetVertexProcessing method [Direct2D]","ID2D1DrawInfo interface","d2d1effectauthor/ID2D1DrawInfo::SetVertexProcessing","direct2d.id2d1drawinfo_setvertexprocessing"]
old-location: direct2d\id2d1drawinfo_setvertexprocessing.htm
tech.root: Direct2D
ms.assetid: 23DB679B-33E4-4FB1-B356-BBB1BA95E0EB
ms.date: 12/05/2018
ms.keywords: ID2D1DrawInfo interface [Direct2D],SetVertexProcessing method, ID2D1DrawInfo.SetVertexProcessing, ID2D1DrawInfo::SetVertexProcessing, SetVertexProcessing, SetVertexProcessing method [Direct2D], SetVertexProcessing method [Direct2D],ID2D1DrawInfo interface, d2d1effectauthor/ID2D1DrawInfo::SetVertexProcessing, direct2d.id2d1drawinfo_setvertexprocessing
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
 - ID2D1DrawInfo::SetVertexProcessing
 - d2d1effectauthor/ID2D1DrawInfo::SetVertexProcessing
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
 - ID2D1DrawInfo.SetVertexProcessing
---

# ID2D1DrawInfo::SetVertexProcessing


## -description

Sets a vertex buffer, a corresponding vertex shader, and options to control how the vertices are to be handled by the Direct2D context.

## -parameters

### -param vertexBuffer [in, optional]

Type: <b><a href="/windows/desktop/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1vertexbuffer">ID2D1VertexBuffer</a>*</b>

The vertex buffer, if this is cleared, the default vertex shader and mapping to the transform rectangles will be used.

### -param vertexOptions

Type: <b><a href="/windows/desktop/api/d2d1effectauthor/ne-d2d1effectauthor-d2d1_vertex_options">D2D1_VERTEX_OPTIONS</a></b>

Options that influence how the renderer will interact with the vertex shader.

### -param blendDescription [in, optional]

Type: <b>const <a href="/windows/desktop/api/d2d1effectauthor/ns-d2d1effectauthor-d2d1_blend_description">D2D1_BLEND_DESCRIPTION</a>*</b>

How the vertices will be blended with the output texture.

### -param vertexRange [in, optional]

Type: <b>const <a href="/windows/desktop/api/d2d1effectauthor/ns-d2d1effectauthor-d2d1_vertex_range">D2D1_VERTEX_RANGE</a>*</b>

The set of vertices to use from the buffer.

### -param vertexShader

Type: <b>GUID*</b>

The GUID of the vertex shader.

## -returns

Type: <b>HRESULT</b>

If the method succeeds, it returns <b>S_OK</b>. If it fails, it returns an <b>HRESULT</b> error code.

## -remarks

The vertex shaders associated with the vertex buffer through the vertex shader GUID must have been loaded through the <a href="/windows/desktop/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectcontext-loadvertexshader">ID2D1EffectContext::LoadVertexShader</a> method before this call is made.

If you pass the vertex option <a href="/windows/desktop/api/d2d1effectauthor/ne-d2d1effectauthor-d2d1_vertex_options">D2D1_VERTEX_OPTIONS_DO_NOT_CLEAR</a>, then the method fails unless the blend description is exactly this:




```cpp
D2D1_BLEND_DESCRIPTION blendDesc = 
        {
            D2D1_BLEND_ONE,
            D2D1_BLEND_ZERO,
            D2D1_BLEND_OPERATION_ADD,

            D2D1_BLEND_ONE,
            D2D1_BLEND_ZERO,
            D2D1_BLEND_OPERATION_ADD,

            { 1.0f, 1.0f, 1.0f, 1.0f }
        };
```


If this call fails, the corresponding <a href="/windows/desktop/api/d2d1_1/nn-d2d1_1-id2d1effect">ID2D1Effect</a> instance is placed into an error state and fails to draw.

  If blendDescription is NULL, a foreground-over blend mode is used.

## -see-also

<a href="/windows/desktop/api/d2d1effectauthor/nn-d2d1effectauthor-id2d1drawinfo">ID2D1DrawInfo</a>



<a href="/windows/desktop/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectcontext-createvertexbuffer">ID2D1EffectContext::CreateVertexBuffer</a>



<a href="/windows/desktop/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectcontext-loadvertexshader">ID2D1EffectContext::LoadVertexShader</a>