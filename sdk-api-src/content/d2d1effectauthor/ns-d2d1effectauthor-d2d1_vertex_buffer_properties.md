---
UID: NS:d2d1effectauthor.D2D1_VERTEX_BUFFER_PROPERTIES
title: D2D1_VERTEX_BUFFER_PROPERTIES (d2d1effectauthor.h)
description: Defines the properties of a vertex buffer that are standard for all vertex shader definitions.
helpviewer_keywords: ["D2D1_VERTEX_BUFFER_PROPERTIES","D2D1_VERTEX_BUFFER_PROPERTIES structure [Direct2D]","d2d1effectauthor/D2D1_VERTEX_BUFFER_PROPERTIES","direct2d.d2d1_vertex_buffer_properties"]
old-location: direct2d\d2d1_vertex_buffer_properties.htm
tech.root: Direct2D
ms.assetid: d2f46c31-10f3-4318-8185-40a6bbd8ef8a
ms.date: 12/05/2018
ms.keywords: D2D1_VERTEX_BUFFER_PROPERTIES, D2D1_VERTEX_BUFFER_PROPERTIES structure [Direct2D], d2d1effectauthor/D2D1_VERTEX_BUFFER_PROPERTIES, direct2d.d2d1_vertex_buffer_properties
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
req.type-library: D2d1.lib; D2d1.dll
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: D2D1_VERTEX_BUFFER_PROPERTIES
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D2D1_VERTEX_BUFFER_PROPERTIES
 - d2d1effectauthor/D2D1_VERTEX_BUFFER_PROPERTIES
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - LibDef
api_location:
 - D2d1.lib
 - D2d1.dll
api_name:
 - D2D1_VERTEX_BUFFER_PROPERTIES
---

# D2D1_VERTEX_BUFFER_PROPERTIES structure


## -description

Defines the properties of a vertex buffer that are standard for all vertex shader definitions.

## -struct-fields

### -field inputCount

The number of inputs to the vertex shader.

### -field usage

Indicates how frequently the vertex buffer is likely to be updated.

### -field data

The initial contents of the vertex buffer.

### -field byteWidth

The size of the vertex buffer, in bytes.

## -remarks

If <b>usage</b> is dynamic, the system might return a system memory buffer and copy these vertices into the rendering vertex buffer for each element.

If the initialization data is not specified, the buffer will be uninitialized.

## -see-also

<a href="/windows/desktop/api/d2d1effectauthor/ne-d2d1effectauthor-d2d1_vertex_usage">D2D1_VERTEX_USAGE</a>



<a href="/windows/desktop/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectcontext-createvertexbuffer">ID2D1EffectContext::CreateVertexBuffer</a>



<a href="/windows/desktop/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectcontext-loadvertexshader">ID2D1EffectContext::LoadVertexShader</a>