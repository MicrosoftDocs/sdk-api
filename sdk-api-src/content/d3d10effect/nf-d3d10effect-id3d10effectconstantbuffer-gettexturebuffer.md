---
UID: NF:d3d10effect.ID3D10EffectConstantBuffer.GetTextureBuffer
title: ID3D10EffectConstantBuffer::GetTextureBuffer (d3d10effect.h)
description: Get a texture-buffer.
helpviewer_keywords: ["512133ea-290f-b95c-7a3b-5a7dc0f29da0","GetTextureBuffer","GetTextureBuffer method [Direct3D 10]","GetTextureBuffer method [Direct3D 10]","ID3D10EffectConstantBuffer interface","ID3D10EffectConstantBuffer interface [Direct3D 10]","GetTextureBuffer method","ID3D10EffectConstantBuffer.GetTextureBuffer","ID3D10EffectConstantBuffer::GetTextureBuffer","d3d10effect/ID3D10EffectConstantBuffer::GetTextureBuffer","direct3d10.id3d10effectconstantbuffer_gettexturebuffer"]
old-location: direct3d10\id3d10effectconstantbuffer_gettexturebuffer.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10effectconstantbuffer_gettexturebuffer.htm
ms.date: 12/05/2018
ms.keywords: 512133ea-290f-b95c-7a3b-5a7dc0f29da0, GetTextureBuffer, GetTextureBuffer method [Direct3D 10], GetTextureBuffer method [Direct3D 10],ID3D10EffectConstantBuffer interface, ID3D10EffectConstantBuffer interface [Direct3D 10],GetTextureBuffer method, ID3D10EffectConstantBuffer.GetTextureBuffer, ID3D10EffectConstantBuffer::GetTextureBuffer, d3d10effect/ID3D10EffectConstantBuffer::GetTextureBuffer, direct3d10.id3d10effectconstantbuffer_gettexturebuffer
req.header: d3d10effect.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
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
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ID3D10EffectConstantBuffer::GetTextureBuffer
 - d3d10effect/ID3D10EffectConstantBuffer::GetTextureBuffer
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3D10Effect.h
api_name:
 - ID3D10EffectConstantBuffer.GetTextureBuffer
---

# ID3D10EffectConstantBuffer::GetTextureBuffer


## -description

Get a texture-buffer.

## -parameters

### -param ppTextureBuffer [out]

Type: <b><a href="/windows/desktop/api/d3d10/nn-d3d10-id3d10shaderresourceview">ID3D10ShaderResourceView</a>**</b>

The address of a pointer to a shader-resource-view interface for accessing a texture buffer. See <a href="/windows/desktop/api/d3d10/nn-d3d10-id3d10shaderresourceview">ID3D10ShaderResourceView Interface</a>.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

Returns one of the following <a href="/windows/desktop/direct3d10/d3d10-graphics-reference-returnvalues">Direct3D 10 Return Codes</a>.

## -see-also

<a href="/windows/desktop/api/d3d10effect/nn-d3d10effect-id3d10effectconstantbuffer">ID3D10EffectConstantBuffer Interface</a>