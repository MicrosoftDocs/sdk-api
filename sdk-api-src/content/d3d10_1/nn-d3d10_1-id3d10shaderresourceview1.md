---
UID: NN:d3d10_1.ID3D10ShaderResourceView1
title: ID3D10ShaderResourceView1 (d3d10_1.h)
description: A shader-resource-view interface specifies the subresources a shader can access during rendering. Examples of shader resources include a constant buffer, a texture buffer, a texture or a sampler. (ID3D10ShaderResourceView1)
helpviewer_keywords: ["42bd4307-40a4-6b0e-192f-643d483668e8","ID3D10ShaderResourceView1","ID3D10ShaderResourceView1 interface [Direct3D 10]","ID3D10ShaderResourceView1 interface [Direct3D 10]","described","d3d10_1/ID3D10ShaderResourceView1","direct3d10.id3d10shaderresourceview1"]
old-location: direct3d10\id3d10shaderresourceview1.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10shaderresourceview1.htm
ms.date: 12/05/2018
ms.keywords: 42bd4307-40a4-6b0e-192f-643d483668e8, ID3D10ShaderResourceView1, ID3D10ShaderResourceView1 interface [Direct3D 10], ID3D10ShaderResourceView1 interface [Direct3D 10],described, d3d10_1/ID3D10ShaderResourceView1, direct3d10.id3d10shaderresourceview1
req.header: d3d10_1.h
req.include-header: D3D10Shader.h
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
req.lib: D3D10.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ID3D10ShaderResourceView1
 - d3d10_1/ID3D10ShaderResourceView1
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3D10.lib
 - D3D10.dll
api_name:
 - ID3D10ShaderResourceView1
---

# ID3D10ShaderResourceView1 interface


## -description

A shader-resource-view interface specifies the <a href="/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-types">subresources</a> a shader can access during rendering. Examples of shader resources include a constant buffer, a texture buffer, a texture or a sampler.

## -inheritance

The <b>ID3D10ShaderResourceView1</b> interface inherits from <a href="/windows/desktop/api/d3d10/nn-d3d10-id3d10shaderresourceview">ID3D10ShaderResourceView</a>. <b>ID3D10ShaderResourceView1</b> also has these types of members:

## -remarks

To create a shader-resource view, call <a href="/windows/desktop/api/d3d10_1/nf-d3d10_1-id3d10device1-createshaderresourceview1">ID3D10Device1::CreateShaderResourceView1</a>.

A shader-resource view is required when binding a resource to a shader stage; the binding occurs by calling <a href="/windows/desktop/api/d3d10/nf-d3d10-id3d10device-gssetshaderresources">ID3D10Device::GSSetShaderResources</a>, <a href="/windows/desktop/api/d3d10/nf-d3d10-id3d10device-vssetshaderresources">ID3D10Device::VSSetShaderResources</a> or <a href="/windows/desktop/api/d3d10/nf-d3d10-id3d10device-pssetshaderresources">ID3D10Device::PSSetShaderResources</a>.

This method requires Windows Vista Service Pack 1.

## -see-also

<a href="/windows/desktop/api/d3d10/nn-d3d10-id3d10shaderresourceview">ID3D10ShaderResourceView</a>



<a href="/windows/desktop/direct3d10/d3d10-graphics-reference-resource-interfaces">Resource Interfaces</a>
