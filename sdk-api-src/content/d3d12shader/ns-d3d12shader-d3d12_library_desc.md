---
UID: NS:d3d12shader._D3D12_LIBRARY_DESC
title: D3D12_LIBRARY_DESC (d3d12shader.h)
description: Describes a library. (D3D12_LIBRARY_DESC)
helpviewer_keywords: ["D3D12_LIBRARY_DESC","D3D12_LIBRARY_DESC structure","d3d12shader/D3D12_LIBRARY_DESC","direct3d12.d3d12_library_desc"]
old-location: direct3d12\d3d12_library_desc.htm
tech.root: direct3d12
ms.assetid: 99CB0B61-8494-4591-A3CB-B6DAD19C79ED
ms.date: 12/05/2018
ms.keywords: D3D12_LIBRARY_DESC, D3D12_LIBRARY_DESC structure, d3d12shader/D3D12_LIBRARY_DESC, direct3d12.d3d12_library_desc
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
req.typenames: D3D12_LIBRARY_DESC
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _D3D12_LIBRARY_DESC
 - d3d12shader/_D3D12_LIBRARY_DESC
 - D3D12_LIBRARY_DESC
 - d3d12shader/D3D12_LIBRARY_DESC
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - d3d12shader.h
api_name:
 - D3D12_LIBRARY_DESC
---

# D3D12_LIBRARY_DESC structure


## -description

Describes a library.

## -struct-fields

### -field Creator

The name of the originator of the library.

### -field Flags

A combination of <a href="/windows/desktop/direct3dhlsl/d3dcompile-constants">D3DCOMPILE Constants</a> that are combined by using a bitwise OR operation. The resulting value specifies how the compiler compiles.

### -field FunctionCount

The number of functions exported from the library.

## -remarks

This structure is returned by <a href="/windows/desktop/api/d3d12shader/nf-d3d12shader-id3d12libraryreflection-getdesc">ID3D12LibraryReflection::GetDesc</a>.

## -see-also

<a href="/windows/desktop/api/d3d12shader/nf-d3d12shader-id3d12libraryreflection-getdesc">ID3D12LibraryReflection::GetDesc</a>



<a href="/windows/desktop/direct3d12/d3d12-graphics-reference-shader-structures">Shader Structures</a>
