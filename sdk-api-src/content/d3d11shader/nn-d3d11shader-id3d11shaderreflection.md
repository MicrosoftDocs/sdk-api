---
UID: NN:d3d11shader.ID3D11ShaderReflection
title: ID3D11ShaderReflection (d3d11shader.h)
description: A shader-reflection interface accesses shader information. (ID3D11ShaderReflection)
helpviewer_keywords: ["83fba8f9-987e-26d3-4909-fd45ac6e9df2","ID3D11ShaderReflection","ID3D11ShaderReflection interface [Direct3D 11]","ID3D11ShaderReflection interface [Direct3D 11]","described","d3d11shader/ID3D11ShaderReflection","direct3d11.id3d11shaderreflection"]
old-location: direct3d11\id3d11shaderreflection.htm
tech.root: direct3d11
ms.assetid: a28cca72-7f2d-416a-bfa9-4d1f71fc98d5
ms.date: 12/05/2018
ms.keywords: 83fba8f9-987e-26d3-4909-fd45ac6e9df2, ID3D11ShaderReflection, ID3D11ShaderReflection interface [Direct3D 11], ID3D11ShaderReflection interface [Direct3D 11],described, d3d11shader/ID3D11ShaderReflection, direct3d11.id3d11shaderreflection
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
 - ID3D11ShaderReflection
 - d3d11shader/ID3D11ShaderReflection
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
 - ID3D11ShaderReflection
---

# ID3D11ShaderReflection interface


## -description

A shader-reflection interface accesses shader information.

## -inheritance

The <b>ID3D11ShaderReflection</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ID3D11ShaderReflection</b> also has these types of members:

## -remarks

An <b>ID3D11ShaderReflection</b> interface can be retrieved for a shader by using  <a href="/windows/desktop/direct3dhlsl/d3dreflect">D3DReflect</a>.  The following code illustrates retrieving a <b>ID3D11ShaderReflection</b>  from a shader.
          


```
pd3dDevice->CreatePixelShader( pPixelShaderBuffer->GetBufferPointer(),
                               pPixelShaderBuffer->GetBufferSize(), g_pPSClassLinkage, &g_pPixelShader );

ID3D11ShaderReflection* pReflector = NULL; 
D3DReflect( pPixelShaderBuffer->GetBufferPointer(), pPixelShaderBuffer->GetBufferSize(), 
            IID_ID3D11ShaderReflection, (void**) &pReflector);
```

## -see-also

<a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>



<a href="/windows/desktop/direct3d11/d3d11-graphics-reference-d3d11-shader-interfaces">Shader Interfaces</a>
