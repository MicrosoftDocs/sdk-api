---
UID: NN:d3d11shader.ID3D11ShaderReflectionConstantBuffer
title: ID3D11ShaderReflectionConstantBuffer (d3d11shader.h)
description: This shader-reflection interface provides access to a constant buffer. (ID3D11ShaderReflectionConstantBuffer)
helpviewer_keywords: ["082bcb34-3d5a-3d3f-e3c1-0cf676c0b05b","ID3D11ShaderReflectionConstantBuffer","ID3D11ShaderReflectionConstantBuffer interface [Direct3D 11]","ID3D11ShaderReflectionConstantBuffer interface [Direct3D 11]","described","d3d11shader/ID3D11ShaderReflectionConstantBuffer","direct3d11.id3d11shaderreflectionconstantbuffer"]
old-location: direct3d11\id3d11shaderreflectionconstantbuffer.htm
tech.root: direct3d11
ms.assetid: 4b47ed8d-e814-4a7b-bc8e-25a8b71200ce
ms.date: 12/05/2018
ms.keywords: 082bcb34-3d5a-3d3f-e3c1-0cf676c0b05b, ID3D11ShaderReflectionConstantBuffer, ID3D11ShaderReflectionConstantBuffer interface [Direct3D 11], ID3D11ShaderReflectionConstantBuffer interface [Direct3D 11],described, d3d11shader/ID3D11ShaderReflectionConstantBuffer, direct3d11.id3d11shaderreflectionconstantbuffer
req.header: d3d11shader.h
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
req.lib: D3DCompiler.lib
req.dll: D3DCompiler_47.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ID3D11ShaderReflectionConstantBuffer
 - d3d11shader/ID3D11ShaderReflectionConstantBuffer
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D3DCompiler_47.dll
api_name:
 - ID3D11ShaderReflectionConstantBuffer
---

# ID3D11ShaderReflectionConstantBuffer interface


## -description

This shader-reflection interface provides access to a constant buffer.

## -inheritance

The <b>ID3D11ShaderReflectionConstantBuffer</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ID3D11ShaderReflectionConstantBuffer</b> also has these types of members:
<ul>
<li><a href="/">Methods</a></li>
</ul>

## -remarks

To create a constant-buffer interface, call <a href="/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11shaderreflection-getconstantbufferbyindex">ID3D11ShaderReflection::GetConstantBufferByIndex</a> or <a href="/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11shaderreflection-getconstantbufferbyname">ID3D11ShaderReflection::GetConstantBufferByName</a>. This isn't a COM interface, so you don't need to worry about reference counts or releasing the interface when you're done with it.

## -see-also

<a href="/windows/desktop/direct3d11/d3d11-graphics-reference-d3d11-shader-interfaces">Shader Interfaces</a>
