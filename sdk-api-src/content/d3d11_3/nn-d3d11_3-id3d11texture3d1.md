---
UID: NN:d3d11_3.ID3D11Texture3D1
title: ID3D11Texture3D1 (d3d11_3.h)
description: A 3D texture interface represents texel data, which is structured memory.
helpviewer_keywords: ["ID3D11Texture3D1","ID3D11Texture3D1 interface [Direct3D 11]","ID3D11Texture3D1 interface [Direct3D 11]","described","d3d11_3/ID3D11Texture3D1","direct3d11.id3d11texture3d1"]
old-location: direct3d11\id3d11texture3d1.htm
tech.root: direct3d11
ms.assetid: 8ADF6845-BC62-4FCC-946E-7DE676C250B0
ms.date: 12/05/2018
ms.keywords: ID3D11Texture3D1, ID3D11Texture3D1 interface [Direct3D 11], ID3D11Texture3D1 interface [Direct3D 11],described, d3d11_3/ID3D11Texture3D1, direct3d11.id3d11texture3d1
req.header: d3d11_3.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2016 [desktop apps \| UWP apps]
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
 - ID3D11Texture3D1
 - d3d11_3/ID3D11Texture3D1
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
 - ID3D11Texture3D1
---

# ID3D11Texture3D1 interface


## -description

A 3D texture interface represents texel data, which is structured memory.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ID3D11Texture3D1</b> interface inherits from <a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11texture3d">ID3D11Texture3D</a>. <b>ID3D11Texture3D1</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -remarks

To create an empty Texture3D resource, call <a href="/windows/desktop/api/d3d11_3/nf-d3d11_3-id3d11device3-createtexture3d1">ID3D11Device3::CreateTexture3D1</a>. For info about how to create a 2D texture, which is similar to creating a 3D texture, see <a href="/windows/desktop/direct3d11/overviews-direct3d-11-resources-textures-create">How to: Create a Texture</a>. 

Textures can't be bound directly to the pipeline; instead, a view must be created and bound. Using a view, texture data can be interpreted at run time within certain restrictions. To use the texture as a render-target or depth-stencil resource, call <a href="/windows/desktop/api/d3d11_3/nf-d3d11_3-id3d11device3-createrendertargetview1">ID3D11Device3::CreateRenderTargetView1</a>, and <a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11device-createdepthstencilview">ID3D11Device::CreateDepthStencilView</a>, respectively. To use the texture as an input to a shader, call <a href="/windows/desktop/api/d3d11_3/nf-d3d11_3-id3d11device3-createshaderresourceview1">ID3D11Device3::CreateShaderResourceView1</a>.

## -see-also

<a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11texture3d">ID3D11Texture3D</a>



<a href="/windows/desktop/direct3d11/d3d11-graphics-reference-resource-interfaces">Resource Interfaces</a>
