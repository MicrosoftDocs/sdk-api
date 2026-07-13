---
UID: NN:d3d11shader.ID3D11Module
title: ID3D11Module (d3d11shader.h)
description: A module interface creates an instance of a module that is used for resource rebinding.
helpviewer_keywords: ["ID3D11Module","ID3D11Module interface [Direct3D 11]","ID3D11Module interface [Direct3D 11]","described","d3d11shader/ID3D11Module","direct3d11.id3d11module"]
old-location: direct3d11\id3d11module.htm
tech.root: direct3d11
ms.assetid: 5915DACB-1D3A-496C-96C6-77D85CC6560B
ms.date: 12/05/2018
ms.keywords: ID3D11Module, ID3D11Module interface [Direct3D 11], ID3D11Module interface [Direct3D 11],described, d3d11shader/ID3D11Module, direct3d11.id3d11module
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
 - ID3D11Module
 - d3d11shader/ID3D11Module
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
 - ID3D11Module
---

# ID3D11Module interface


## -description

A module interface creates an instance of a module that is used for resource rebinding. <div class="alert"><b>Note</b>  This interface is part of the HLSL shader linking technology that you can use on all Direct3D 11 platforms to create precompiled HLSL functions, package them into libraries, and link them into full shaders at run time.
          </div>
<div> </div>

## -inheritance

The <b>ID3D11Module</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ID3D11Module</b> also has these types of members:

## -remarks

To get a module interface, call <a href="/windows/desktop/api/d3dcompiler/nf-d3dcompiler-d3dloadmodule">D3DLoadModule</a>.
      

<div class="alert"><b>Note</b>  <b>ID3D11Module</b> requires the D3dcompiler_47.dll or a later version of the DLL.
      </div>
<div> </div>

## -see-also

<a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>



<a href="/windows/desktop/direct3d11/d3d11-graphics-reference-d3d11-shader-interfaces">Shader Interfaces</a>
