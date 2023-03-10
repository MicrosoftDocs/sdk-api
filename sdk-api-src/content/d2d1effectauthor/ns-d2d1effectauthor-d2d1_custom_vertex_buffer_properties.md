---
UID: NS:d2d1effectauthor.D2D1_CUSTOM_VERTEX_BUFFER_PROPERTIES
title: D2D1_CUSTOM_VERTEX_BUFFER_PROPERTIES (d2d1effectauthor.h)
description: Defines a vertex shader and the input element description to define the input layout.
helpviewer_keywords: ["D2D1_CUSTOM_VERTEX_BUFFER_PROPERTIES","D2D1_CUSTOM_VERTEX_BUFFER_PROPERTIES structure [Direct2D]","d2d1effectauthor/D2D1_CUSTOM_VERTEX_BUFFER_PROPERTIES","direct2d.d2d1_custom_vertex_buffer_properties"]
old-location: direct2d\d2d1_custom_vertex_buffer_properties.htm
tech.root: Direct2D
ms.assetid: e3cebb2b-48fb-42b2-8eb4-b9676b581bac
ms.date: 12/05/2018
ms.keywords: D2D1_CUSTOM_VERTEX_BUFFER_PROPERTIES, D2D1_CUSTOM_VERTEX_BUFFER_PROPERTIES structure [Direct2D], d2d1effectauthor/D2D1_CUSTOM_VERTEX_BUFFER_PROPERTIES, direct2d.d2d1_custom_vertex_buffer_properties
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: D2D1_CUSTOM_VERTEX_BUFFER_PROPERTIES
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D2D1_CUSTOM_VERTEX_BUFFER_PROPERTIES
 - d2d1effectauthor/D2D1_CUSTOM_VERTEX_BUFFER_PROPERTIES
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - d2d1effectauthor.h
api_name:
 - D2D1_CUSTOM_VERTEX_BUFFER_PROPERTIES
---

## -description

Defines a vertex shader and the input element description to define the input layout. The combination is used to allow a custom vertex effect to create a custom vertex shader and pass it a custom layout.

## -struct-fields

### -field shaderBufferWithInputSignature

A pointer to the buffer.

### -field shaderBufferSize

The size of the buffer.

### -field inputElements

An array of input assembler stage data types.

### -field elementCount

The number of input elements in the vertex shader.

### -field stride

The vertex stride.

## -remarks

The vertex shader will be loaded by the <a href="/windows/desktop/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectcontext-createvertexbuffer">CreateVertexBuffer</a> call that accepts the vertex buffer properties.

This structure does not need to be specified if one of the standard vertex shaders is used.

## -see-also

<a href="/windows/desktop/api/d2d1effectauthor/ne-d2d1effectauthor-d2d1_vertex_usage">D2D1_VERTEX_USAGE</a>

<a href="/windows/desktop/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectcontext-createvertexbuffer">ID2D1EffectContext::CreateVertexBuffer</a>

<a href="/windows/desktop/api/d2d1effectauthor/nf-d2d1effectauthor-id2d1effectcontext-loadvertexshader">ID2D1EffectContext::LoadVertexShader</a>