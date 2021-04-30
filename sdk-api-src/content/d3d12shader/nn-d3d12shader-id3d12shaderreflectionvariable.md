---
UID: NN:d3d12shader.ID3D12ShaderReflectionVariable
title: ID3D12ShaderReflectionVariable (d3d12shader.h)
description: This shader-reflection interface provides access to a variable.
helpviewer_keywords: ["ID3D12ShaderReflectionVariable","ID3D12ShaderReflectionVariable interface","ID3D12ShaderReflectionVariable interface","described","d3d12shader/ID3D12ShaderReflectionVariable","direct3d12.id3d12shaderreflectionvariable"]
old-location: direct3d12\id3d12shaderreflectionvariable.htm
tech.root: direct3d12
ms.assetid: E4CF0C77-2792-46DC-B38F-22C0ACBFD615
ms.date: 12/05/2018
ms.keywords: ID3D12ShaderReflectionVariable, ID3D12ShaderReflectionVariable interface, ID3D12ShaderReflectionVariable interface,described, d3d12shader/ID3D12ShaderReflectionVariable, direct3d12.id3d12shaderreflectionvariable
req.header: d3d12shader.h
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
 - ID3D12ShaderReflectionVariable
 - d3d12shader/ID3D12ShaderReflectionVariable
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - d3d12shader.h
api_name:
 - ID3D12ShaderReflectionVariable
---

# ID3D12ShaderReflectionVariable interface


## -description

This shader-reflection interface provides access to a variable.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ID3D12ShaderReflectionVariable</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ID3D12ShaderReflectionVariable</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -remarks

To get a shader-reflection-variable interface, call a method like <a href="/windows/desktop/api/d3d12shader/nf-d3d12shader-id3d12shaderreflection-getvariablebyname">ID3D12ShaderReflection::GetVariableByName</a>. This isn't a COM interface, so you don't need to worry about reference counts or releasing the interface when you're done with it.

## -see-also

<a href="/windows/desktop/direct3d12/d3d12-graphics-reference-shader-interfaces">Shader Interfaces</a>
