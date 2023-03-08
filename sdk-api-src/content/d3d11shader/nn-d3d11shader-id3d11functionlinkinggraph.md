---
UID: NN:d3d11shader.ID3D11FunctionLinkingGraph
title: ID3D11FunctionLinkingGraph (d3d11shader.h)
description: A function-linking-graph interface is used for constructing shaders that consist of a sequence of precompiled function calls that pass values to each other.
helpviewer_keywords: ["ID3D11FunctionLinkingGraph","ID3D11FunctionLinkingGraph interface [Direct3D 11]","ID3D11FunctionLinkingGraph interface [Direct3D 11]","described","d3d11shader/ID3D11FunctionLinkingGraph","direct3d11.id3d11functionlinkinggraph"]
old-location: direct3d11\id3d11functionlinkinggraph.htm
tech.root: direct3d11
ms.assetid: B1952085-CCD2-40F6-9A23-83B4F18FC30A
ms.date: 12/05/2018
ms.keywords: ID3D11FunctionLinkingGraph, ID3D11FunctionLinkingGraph interface [Direct3D 11], ID3D11FunctionLinkingGraph interface [Direct3D 11],described, d3d11shader/ID3D11FunctionLinkingGraph, direct3d11.id3d11functionlinkinggraph
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
 - ID3D11FunctionLinkingGraph
 - d3d11shader/ID3D11FunctionLinkingGraph
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
 - ID3D11FunctionLinkingGraph
---

# ID3D11FunctionLinkingGraph interface


## -description

A function-linking-graph interface is used for constructing shaders that consist of a sequence of precompiled function calls that pass values to each other. <div class="alert"><b>Note</b>  This interface is part of the HLSL shader linking technology that you can use on all Direct3D 11 platforms to create precompiled HLSL functions, package them into libraries, and link them into full shaders at run time.
</div>
<div> </div>

## -inheritance

The <b>ID3D11FunctionLinkingGraph</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ID3D11FunctionLinkingGraph</b> also has these types of members:

## -remarks

To get a function-linking-graph interface, call <a href="/windows/desktop/api/d3dcompiler/nf-d3dcompiler-d3dcreatefunctionlinkinggraph">D3DCreateFunctionLinkingGraph</a>. 

You can use the function-linking-graph (FLG) interface methods to construct shaders that consist of a sequence of precompiled function calls that pass values to each other. You don't need to write HLSL and then call the HLSL compiler. Instead, the shader structure is specified programmatically via a C++ API. FLG nodes represent input and output signatures and invocations of precompiled library functions. The order of registering the function-call nodes defines the sequence of invocations. You must specify the input signature node first and the output signature node last. FLG edges define how values are passed from one node to another. The data types of passed values must be the same; there is no implicit type conversion. Shape and swizzling rules follow the HLSL behavior. Values can only be passed forward in this sequence.

<div class="alert"><b>Note</b>  <b>ID3D11FunctionLinkingGraph</b> requires the D3dcompiler_47.dll or a later version of the DLL. </div>
<div> </div>

## -see-also

<a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>



<a href="/windows/desktop/direct3d11/d3d11-graphics-reference-d3d11-shader-interfaces">Shader Interfaces</a>
