---
UID: NN:d3d10shader.ID3D10ShaderReflection
title: ID3D10ShaderReflection (d3d10shader.h)
description: A shader-reflection interface accesses shader information. (ID3D10ShaderReflection)
helpviewer_keywords: ["ID3D10ShaderReflection","ID3D10ShaderReflection interface [Direct3D 10]","ID3D10ShaderReflection interface [Direct3D 10]","described","d3d10shader/ID3D10ShaderReflection","direct3d10.id3d10shaderreflection","fd699fe1-b903-c976-14c4-3b0023611424"]
old-location: direct3d10\id3d10shaderreflection.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\id3d10shaderreflection.htm
ms.date: 12/05/2018
ms.keywords: ID3D10ShaderReflection, ID3D10ShaderReflection interface [Direct3D 10], ID3D10ShaderReflection interface [Direct3D 10],described, d3d10shader/ID3D10ShaderReflection, direct3d10.id3d10shaderreflection, fd699fe1-b903-c976-14c4-3b0023611424
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
 - ID3D10ShaderReflection
 - d3d10shader/ID3D10ShaderReflection
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
 - ID3D10ShaderReflection
---

# ID3D10ShaderReflection interface


## -description

A shader-reflection interface accesses shader information.

## -inheritance

The <b>ID3D10ShaderReflection</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ID3D10ShaderReflection</b> also has these types of members:

## -remarks

Create the interface by calling <a href="/windows/desktop/direct3d10/d3dx10reflectshader">D3DX10ReflectShader</a>. Since it is a COM interface, creating the interface increases a reference count and the interface must be released when it is no longer needed. The remaining shader-reflection interfaces are not COM interfaces.

## -see-also

<a href="/windows/desktop/direct3d10/d3d10-graphics-reference-d3d10-shader-interfaces">Shader Interfaces</a>
