---
UID: NN:d3d11.ID3D11ShaderResourceView
title: ID3D11ShaderResourceView (d3d11.h)
description: A shader-resource-view interface specifies the subresources a shader can access during rendering. Examples of shader resources include a constant buffer, a texture buffer, and a texture.
helpviewer_keywords: ["7665f23b-5b1b-14d0-93b2-1c24ed09a978","ID3D11ShaderResourceView","ID3D11ShaderResourceView interface [Direct3D 11]","ID3D11ShaderResourceView interface [Direct3D 11]","described","d3d11/ID3D11ShaderResourceView","direct3d11.id3d11shaderresourceview"]
old-location: direct3d11\id3d11shaderresourceview.htm
tech.root: direct3d11
ms.assetid: 289555d8-2a6e-454f-86bc-48fb2c8ea345
ms.date: 12/05/2018
ms.keywords: 7665f23b-5b1b-14d0-93b2-1c24ed09a978, ID3D11ShaderResourceView, ID3D11ShaderResourceView interface [Direct3D 11], ID3D11ShaderResourceView interface [Direct3D 11],described, d3d11/ID3D11ShaderResourceView, direct3d11.id3d11shaderresourceview
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
 - ID3D11ShaderResourceView
 - d3d11/ID3D11ShaderResourceView
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
 - ID3D11ShaderResourceView
---

# ID3D11ShaderResourceView interface


## -description

A shader-resource-view interface specifies the subresources a shader can access during rendering. Examples of shader resources include a constant buffer, a texture buffer, and a texture.

## -inheritance

The <b>ID3D11ShaderResourceView</b> interface inherits from <a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11view">ID3D11View</a>. <b>ID3D11ShaderResourceView</b> also has these types of members:

## -remarks

To create a shader-resource view, call <a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11device-createshaderresourceview">ID3D11Device::CreateShaderResourceView</a>.

A shader-resource view is required when binding a resource to a shader stage; the binding occurs by calling <a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-gssetshaderresources">ID3D11DeviceContext::GSSetShaderResources</a>, <a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-vssetshaderresources">ID3D11DeviceContext::VSSetShaderResources</a> or <a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11devicecontext-pssetshaderresources">ID3D11DeviceContext::PSSetShaderResources</a>.

## -see-also

<a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11view">ID3D11View</a>



<a href="/windows/desktop/direct3d11/d3d11-graphics-reference-resource-interfaces">Resource Interfaces</a>
