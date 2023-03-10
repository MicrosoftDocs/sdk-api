---
UID: NN:d3d11shader.ID3D11Linker
title: ID3D11Linker (d3d11shader.h)
description: A linker interface is used to link a shader module.
helpviewer_keywords: ["ID3D11Linker","ID3D11Linker interface [Direct3D 11]","ID3D11Linker interface [Direct3D 11]","described","d3d11shader/ID3D11Linker","direct3d11.id3d11linker"]
old-location: direct3d11\id3d11linker.htm
tech.root: direct3d11
ms.assetid: 08967A5F-AAAE-4352-A8A9-C7B1ED16EF25
ms.date: 12/05/2018
ms.keywords: ID3D11Linker, ID3D11Linker interface [Direct3D 11], ID3D11Linker interface [Direct3D 11],described, d3d11shader/ID3D11Linker, direct3d11.id3d11linker
req.header: d3d11shader.h
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
req.lib: D3DCompiler.lib
req.dll: D3DCompiler_47.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ID3D11Linker
 - d3d11shader/ID3D11Linker
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
 - ID3D11Linker
---

# ID3D11Linker interface


## -description

A linker interface is used to link a shader module. <div class="alert"><b>Note</b>  This interface is part of the HLSL shader linking technology that you can use on all Direct3D 11 platforms to create precompiled HLSL functions, package them into libraries, and link them into full shaders at run time.
          </div>
<div> </div>

## -inheritance

The <b>ID3D11Linker</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ID3D11Linker</b> also has these types of members:

## -remarks

To get a linker interface, call <a href="/windows/desktop/api/d3dcompiler/nf-d3dcompiler-d3dcreatelinker">D3DCreateLinker</a>.
      

<div class="alert"><b>Note</b>  <b>ID3D11Linker</b> requires the D3dcompiler_47.dll or a later version of the DLL.
      </div>
<div> </div>

## -see-also

<a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>



<a href="/windows/desktop/direct3d11/d3d11-graphics-reference-d3d11-shader-interfaces">Shader Interfaces</a>
