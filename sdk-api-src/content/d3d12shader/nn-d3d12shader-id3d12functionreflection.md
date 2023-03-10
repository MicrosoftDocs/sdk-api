---
UID: NN:d3d12shader.ID3D12FunctionReflection
title: ID3D12FunctionReflection (d3d12shader.h)
description: A function-reflection interface accesses function info. (ID3D12FunctionReflection)
helpviewer_keywords: ["ID3D12FunctionReflection","ID3D12FunctionReflection interface","ID3D12FunctionReflection interface","described","d3d12shader/ID3D12FunctionReflection","direct3d12.id3d12functionreflection"]
old-location: direct3d12\id3d12functionreflection.htm
tech.root: direct3d12
ms.assetid: F0BF4AA9-66D7-4A33-A51C-B03C1D61F537
ms.date: 12/05/2018
ms.keywords: ID3D12FunctionReflection, ID3D12FunctionReflection interface, ID3D12FunctionReflection interface,described, d3d12shader/ID3D12FunctionReflection, direct3d12.id3d12functionreflection
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
 - ID3D12FunctionReflection
 - d3d12shader/ID3D12FunctionReflection
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
 - ID3D12FunctionReflection
---

# ID3D12FunctionReflection interface


## -description

A function-reflection interface accesses function info. 
          <div class="alert"><b>Note</b>  This interface is part of the HLSL shader linking technology that you can use on all Direct3D 12 platforms to create precompiled HLSL functions, package them into libraries, and link them into full shaders at run time.
          </div>
<div> </div>

## -inheritance

The <b>ID3D12FunctionReflection</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ID3D12FunctionReflection</b> also has these types of members:
<ul>
<li><a href="/">Methods</a></li>
</ul>

## -remarks

To get a function-reflection interface, call <a href="/windows/desktop/api/d3d12shader/nf-d3d12shader-id3d12libraryreflection-getfunctionbyindex">ID3D12LibraryReflection::GetFunctionByIndex</a>. This isn't a COM interface, so you don't need to worry about reference counts or releasing the interface when you're done with it.
      

<div class="alert"><b>Note</b>  <b>ID3D12FunctionReflection</b> requires the D3dcompiler_47.dll or a later version of the DLL.
      </div>
<div> </div>

## -see-also

<a href="/windows/desktop/direct3d12/d3d12-graphics-reference-shader-interfaces">Shader Interfaces</a>
