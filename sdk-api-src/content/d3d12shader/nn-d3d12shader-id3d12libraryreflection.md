---
UID: NN:d3d12shader.ID3D12LibraryReflection
title: ID3D12LibraryReflection (d3d12shader.h)
description: A library-reflection interface accesses library info. (ID3D12LibraryReflection)
helpviewer_keywords: ["ID3D12LibraryReflection","ID3D12LibraryReflection interface","ID3D12LibraryReflection interface","described","d3d12shader/ID3D12LibraryReflection","direct3d12.id3d12libraryreflection"]
old-location: direct3d12\id3d12libraryreflection.htm
tech.root: direct3d12
ms.assetid: CE6AEA77-A6A0-46A5-BDBC-AE4907AAC820
ms.date: 12/05/2018
ms.keywords: ID3D12LibraryReflection, ID3D12LibraryReflection interface, ID3D12LibraryReflection interface,described, d3d12shader/ID3D12LibraryReflection, direct3d12.id3d12libraryreflection
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
 - ID3D12LibraryReflection
 - d3d12shader/ID3D12LibraryReflection
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
 - ID3D12LibraryReflection
---

# ID3D12LibraryReflection interface


## -description

A library-reflection interface accesses library info.
          <div class="alert"><b>Note</b>  This interface is part of the HLSL shader linking technology that you can use on all Direct3D 12 platforms to create precompiled HLSL functions, package them into libraries, and link them into full shaders at run time.
          </div>
<div> </div>

## -inheritance

The <b>ID3D12LibraryReflection</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ID3D12LibraryReflection</b> also has these types of members:

## -remarks

To get a library-reflection interface, call <a href="/windows/desktop/api/d3dcompiler/nf-d3dcompiler-d3dreflectlibrary">D3DReflectLibrary</a>.
      

<div class="alert"><b>Note</b>  <b>ID3D12LibraryReflection</b> requires the D3dcompiler_47.dll or a later version of the DLL.
      </div>
<div> </div>

## -see-also

<a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>



<a href="/windows/desktop/direct3d12/d3d12-graphics-reference-shader-interfaces">Shader Interfaces</a>
