---
UID: NN:d3d11_3.ID3D11ShaderResourceView1
title: ID3D11ShaderResourceView1 (d3d11_3.h)
description: A shader-resource-view interface represents the subresources a shader can access during rendering. Examples of shader resources include a constant buffer, a texture buffer, and a texture.
helpviewer_keywords: ["ID3D11ShaderResourceView1","ID3D11ShaderResourceView1 interface [Direct3D 11]","ID3D11ShaderResourceView1 interface [Direct3D 11]","described","d3d11_3/ID3D11ShaderResourceView1","direct3d11.id3d11shaderresourceview1"]
old-location: direct3d11\id3d11shaderresourceview1.htm
tech.root: direct3d11
ms.assetid: 5AF5DCAC-2C3A-45A7-A165-3FBE3E0D5CAB
ms.date: 12/05/2018
ms.keywords: ID3D11ShaderResourceView1, ID3D11ShaderResourceView1 interface [Direct3D 11], ID3D11ShaderResourceView1 interface [Direct3D 11],described, d3d11_3/ID3D11ShaderResourceView1, direct3d11.id3d11shaderresourceview1
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
 - ID3D11ShaderResourceView1
 - d3d11_3/ID3D11ShaderResourceView1
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
 - ID3D11ShaderResourceView1
---

# ID3D11ShaderResourceView1 interface


## -description

A shader-resource-view interface represents the subresources a shader can access during rendering. Examples of shader resources include a constant buffer, a texture buffer, and a texture.

## -inheritance

The <b>ID3D11ShaderResourceView1</b> interface inherits from <a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11shaderresourceview">ID3D11ShaderResourceView</a>. <b>ID3D11ShaderResourceView1</b> also has these types of members:

## -remarks

To create a shader-resource view, call <a href="/windows/desktop/api/d3d11_3/nf-d3d11_3-id3d11device3-createshaderresourceview1">ID3D11Device3::CreateShaderResourceView1</a>.

A shader-resource view is required when binding a resource to a shader stage; the binding occurs by calling <a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-gssetshaderresources">ID3D11DeviceContext::GSSetShaderResources</a>, <a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-vssetshaderresources">ID3D11DeviceContext::VSSetShaderResources</a> or <a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-pssetshaderresources">ID3D11DeviceContext::PSSetShaderResources</a>.

## -see-also

<a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11shaderresourceview">ID3D11ShaderResourceView</a>



<a href="/windows/desktop/direct3d11/d3d11-graphics-reference-resource-interfaces">Resource Interfaces</a>
