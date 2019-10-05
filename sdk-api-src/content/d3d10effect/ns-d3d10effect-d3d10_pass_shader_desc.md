---
UID: NS:d3d10effect._D3D10_PASS_SHADER_DESC
title: D3D10_PASS_SHADER_DESC (d3d10effect.h)
author: windows-sdk-content
description: Describes an effect variable that contains a shader.
old-location: direct3d10\d3d10_pass_shader_desc.htm
tech.root: direct3d10
ms.assetid: VS|directx_sdk|~\d3d10_pass_shader_desc.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: D3D10_PASS_SHADER_DESC, D3D10_PASS_SHADER_DESC structure [Direct3D 10], d3d10effect/D3D10_PASS_SHADER_DESC, d6701cbf-a851-873f-5e5e-7ef5dd77bdb1, direct3d10.d3d10_pass_shader_desc
ms.topic: struct
f1_keywords: 
 - "d3d10effect/D3D10_PASS_SHADER_DESC"
dev_langs:
 - c++
req.header: d3d10effect.h
req.include-header: D3D10.h
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - d3d10effect.h
api_name:
 - D3D10_PASS_SHADER_DESC
targetos: Windows
req.typenames: D3D10_PASS_SHADER_DESC
req.redist: 
ms.custom: 19H1
---

# D3D10_PASS_SHADER_DESC structure


## -description


Describes an effect variable that contains a shader.


## -struct-fields




### -field pShaderVariable

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/d3d10effect/nn-d3d10effect-id3d10effectshadervariable">ID3D10EffectShaderVariable</a>*</b>

A pointer to the variable that the shader came from. If it is an inline shader assignment, the returned interface will be an anonymous shader variable, which is not retrievable any other way.  Its name in the variable description will be "$Anonymous". If there is no assignment of this type in the pass block, this will point to a shader variable that returns false when IsValid is called.


### -field ShaderIndex

Type: <b><a href="https://docs.microsoft.com/windows/desktop/WinProg/windows-data-types">UINT</a></b>

A zero-based array index; otherwise 0.


## -remarks



To get a shader description, call a method like <a href="https://docs.microsoft.com/windows/desktop/api/d3d10effect/nf-d3d10effect-id3d10effectpass-getvertexshaderdesc">ID3D10EffectPass::GetVertexShaderDesc</a>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/direct3d10/d3d10-graphics-reference-effect-structures">Effect Structures (Direct3D 10)</a>
 

 

