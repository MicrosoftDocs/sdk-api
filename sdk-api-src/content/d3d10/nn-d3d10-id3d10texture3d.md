---
UID: NN:d3d10.ID3D10Texture3D
title: ID3D10Texture3D (d3d10.h)
description: A 3D texture interface accesses texel data, which is structured memory. (ID3D10Texture3D)
helpviewer_keywords: ["ID3D10Texture3D","ID3D10Texture3D interface [Direct3D 10]","ID3D10Texture3D interface [Direct3D 10]","described","a0af960d-1977-383c-0ee3-09972ece4699","d3d10/ID3D10Texture3D","direct3d10.id3d10texture3d"]
old-location: direct3d10\id3d10texture3d.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10texture3d.htm
ms.date: 12/05/2018
ms.keywords: ID3D10Texture3D, ID3D10Texture3D interface [Direct3D 10], ID3D10Texture3D interface [Direct3D 10],described, a0af960d-1977-383c-0ee3-09972ece4699, d3d10/ID3D10Texture3D, direct3d10.id3d10texture3d
req.header: d3d10.h
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
req.lib: D3D10.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ID3D10Texture3D
 - d3d10/ID3D10Texture3D
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
 - ID3D10Texture3D
---

# ID3D10Texture3D interface


## -description

A <a href="/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-types">3D texture</a> interface accesses texel data, which is structured memory.

## -inheritance

The <b>ID3D10Texture3D</b> interface inherits from <a href="/windows/desktop/api/d3d10/nn-d3d10-id3d10resource">ID3D10Resource</a>. <b>ID3D10Texture3D</b> also has these types of members:

## -remarks

To create an empty Texture3D resource, call <a href="/windows/desktop/api/d3d10/nf-d3d10-id3d10device-createtexture3d">ID3D10Device::CreateTexture3D</a>. For more details on creating and loading textures, see <a href="/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-creating-textures">Creating Texture Resources</a>.

Textures cannot be bound directly to the <a href="/windows/desktop/direct3d10/d3d10-graphics-programming-guide-pipeline-stages">pipeline</a>; instead, a <a href="/windows/desktop/direct3d10/d3d10-graphics-programming-guide-resources-access-views">view</a> must be created and bound. Using a view, texture data can be interpreted at run time within certain restrictions. To use the texture as a render target or depth-stencil resource, call <a href="/windows/desktop/api/d3d10/nf-d3d10-id3d10device-createrendertargetview">ID3D10Device::CreateRenderTargetView</a>, and <a href="/windows/desktop/api/d3d10/nf-d3d10-id3d10device-createdepthstencilview">ID3D10Device::CreateDepthStencilView</a>, respectively. To use the texture as an input to a shader, create a  by calling <a href="/windows/desktop/api/d3d10/nf-d3d10-id3d10device-createshaderresourceview">ID3D10Device::CreateShaderResourceView</a>.

## -see-also

<a href="/windows/desktop/api/d3d10/nn-d3d10-id3d10resource">ID3D10Resource</a>



<a href="/windows/desktop/direct3d10/d3d10-graphics-reference-resource-interfaces">Resource Interfaces</a>
