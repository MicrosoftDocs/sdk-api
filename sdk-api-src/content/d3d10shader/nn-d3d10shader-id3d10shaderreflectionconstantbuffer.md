---
UID: NN:d3d10shader.ID3D10ShaderReflectionConstantBuffer
title: ID3D10ShaderReflectionConstantBuffer (d3d10shader.h)
description: This shader-reflection interface provides access to a constant buffer. (ID3D10ShaderReflectionConstantBuffer)
helpviewer_keywords: ["ID3D10ShaderReflectionConstantBuffer","ID3D10ShaderReflectionConstantBuffer interface [Direct3D 10]","ID3D10ShaderReflectionConstantBuffer interface [Direct3D 10]","described","d3d10shader/ID3D10ShaderReflectionConstantBuffer","direct3d10.id3d10shaderreflectionconstantbuffer","fdeec4a2-cda3-d87b-9d10-c899b8675fd1"]
old-location: direct3d10\id3d10shaderreflectionconstantbuffer.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10shaderreflectionconstantbuffer.htm
ms.date: 12/05/2018
ms.keywords: ID3D10ShaderReflectionConstantBuffer, ID3D10ShaderReflectionConstantBuffer interface [Direct3D 10], ID3D10ShaderReflectionConstantBuffer interface [Direct3D 10],described, d3d10shader/ID3D10ShaderReflectionConstantBuffer, direct3d10.id3d10shaderreflectionconstantbuffer, fdeec4a2-cda3-d87b-9d10-c899b8675fd1
req.header: d3d10shader.h
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
 - ID3D10ShaderReflectionConstantBuffer
 - d3d10shader/ID3D10ShaderReflectionConstantBuffer
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
 - ID3D10ShaderReflectionConstantBuffer
---

# ID3D10ShaderReflectionConstantBuffer interface


## -description

This shader-reflection interface provides access to a constant buffer.

## -inheritance

The <b>ID3D10ShaderReflectionConstantBuffer</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ID3D10ShaderReflectionConstantBuffer</b> also has these types of members:
<ul>
<li><a href="/">Methods</a></li>
</ul>

## -remarks

To create a constant-buffer interface, call <a href="/windows/desktop/api/d3d10shader/nf-d3d10shader-id3d10shaderreflection-getconstantbufferbyindex">ID3D10ShaderReflection::GetConstantBufferByIndex</a> or <a href="/windows/desktop/api/d3d10shader/nf-d3d10shader-id3d10shaderreflection-getconstantbufferbyname">ID3D10ShaderReflection::GetConstantBufferByName</a>. This is not a COM interface; therefore, you do not need to worry about reference counts or releasing the interface when you are done with it.

## -see-also

<a href="/windows/desktop/direct3d10/d3d10-graphics-reference-d3d10-shader-interfaces">Shader Interfaces</a>
