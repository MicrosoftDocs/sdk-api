---
UID: NN:d3d11.ID3D11Texture3D
title: ID3D11Texture3D (d3d11.h)
description: A 3D texture interface accesses texel data, which is structured memory. (ID3D11Texture3D)
helpviewer_keywords: ["28ce947f-3bc9-9f8f-f8e7-667b8d30bf8e","ID3D11Texture3D","ID3D11Texture3D interface [Direct3D 11]","ID3D11Texture3D interface [Direct3D 11]","described","d3d11/ID3D11Texture3D","direct3d11.id3d11texture3d"]
old-location: direct3d11\id3d11texture3d.htm
tech.root: direct3d11
ms.assetid: 178d4ac4-c71f-40cb-bcaf-45ca96b36350
ms.date: 12/05/2018
ms.keywords: 28ce947f-3bc9-9f8f-f8e7-667b8d30bf8e, ID3D11Texture3D, ID3D11Texture3D interface [Direct3D 11], ID3D11Texture3D interface [Direct3D 11],described, d3d11/ID3D11Texture3D, direct3d11.id3d11texture3d
req.header: d3d11.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: D3D11.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ID3D11Texture3D
 - d3d11/ID3D11Texture3D
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3D11.lib
 - D3D11.dll
api_name:
 - ID3D11Texture3D
---

# ID3D11Texture3D interface


## -description

A 3D texture interface accesses texel data, which is structured memory.

## -inheritance

The <b>ID3D11Texture3D</b> interface inherits from <a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11resource">ID3D11Resource</a>. <b>ID3D11Texture3D</b> also has these types of members:

## -remarks

To create an empty Texture3D resource, call <a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11device-createtexture3d">ID3D11Device::CreateTexture3D</a>. For info about how to create a 2D texture, which is similar to creating a 3D texture, see <a href="/windows/desktop/direct3d11/overviews-direct3d-11-resources-textures-create">How to: Create a Texture</a>. 

Textures cannot be bound directly to the pipeline; instead, a view must be created and bound. Using a view, texture data can be interpreted at run time within certain restrictions. To use the texture as a render target or depth-stencil resource, call <a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11device-createrendertargetview">ID3D11Device::CreateRenderTargetView</a>, and <a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11device-createdepthstencilview">ID3D11Device::CreateDepthStencilView</a>, respectively. To use the texture as an input to a shader, create a  by calling <a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11device-createshaderresourceview">ID3D11Device::CreateShaderResourceView</a>.

## -see-also

<a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11resource">ID3D11Resource</a>



<a href="/windows/desktop/direct3d11/d3d11-graphics-reference-resource-interfaces">Resource Interfaces</a>
