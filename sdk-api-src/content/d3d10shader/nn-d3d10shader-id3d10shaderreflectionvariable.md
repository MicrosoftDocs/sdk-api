---
UID: NN:d3d10shader.ID3D10ShaderReflectionVariable
title: ID3D10ShaderReflectionVariable (d3d10shader.h)
description: This shader-reflection interface provides access to a variable. (ID3D10ShaderReflectionVariable)
helpviewer_keywords: ["ID3D10ShaderReflectionVariable","ID3D10ShaderReflectionVariable interface [Direct3D 10]","ID3D10ShaderReflectionVariable interface [Direct3D 10]","described","d3d10shader/ID3D10ShaderReflectionVariable","direct3d10.id3d10shaderreflectionvariable","e8b67520-bfa7-7e41-f594-a51d5ad0301e"]
old-location: direct3d10\id3d10shaderreflectionvariable.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10shaderreflectionvariable.htm
ms.date: 12/05/2018
ms.keywords: ID3D10ShaderReflectionVariable, ID3D10ShaderReflectionVariable interface [Direct3D 10], ID3D10ShaderReflectionVariable interface [Direct3D 10],described, d3d10shader/ID3D10ShaderReflectionVariable, direct3d10.id3d10shaderreflectionvariable, e8b67520-bfa7-7e41-f594-a51d5ad0301e
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
 - ID3D10ShaderReflectionVariable
 - d3d10shader/ID3D10ShaderReflectionVariable
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
 - ID3D10ShaderReflectionVariable
---

# ID3D10ShaderReflectionVariable interface


## -description

This shader-reflection interface provides access to a variable.

## -inheritance

The <b>ID3D10ShaderReflectionVariable</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ID3D10ShaderReflectionVariable</b> also has these types of members:
<ul>
<li><a href="/">Methods</a></li>
</ul>

## -remarks

To get a shader-reflection-variable interface, call a method like <a href="/windows/desktop/api/d3d10shader/nf-d3d10shader-id3d10shaderreflectionconstantbuffer-getvariablebyindex">ID3D10ShaderReflectionConstantBuffer::GetVariableByIndex</a>.

## -see-also

<a href="/windows/desktop/direct3d10/d3d10-graphics-reference-d3d10-shader-interfaces">Shader Interfaces</a>
