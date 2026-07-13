---
UID: NS:d3d11shader._D3D11_LIBRARY_DESC
title: D3D11_LIBRARY_DESC (d3d11shader.h)
description: Describes a library. (D3D11_LIBRARY_DESC)
helpviewer_keywords: ["D3D11_LIBRARY_DESC","D3D11_LIBRARY_DESC structure [Direct3D 11]","d3d11shader/D3D11_LIBRARY_DESC","direct3d11.d3d11_library_desc"]
old-location: direct3d11\d3d11_library_desc.htm
tech.root: direct3d11
ms.assetid: A4AC9733-DB17-4855-AEB0-3DA7819F6627
ms.date: 12/05/2018
ms.keywords: D3D11_LIBRARY_DESC, D3D11_LIBRARY_DESC structure [Direct3D 11], d3d11shader/D3D11_LIBRARY_DESC, direct3d11.d3d11_library_desc
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: D3D11_LIBRARY_DESC
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _D3D11_LIBRARY_DESC
 - d3d11shader/_D3D11_LIBRARY_DESC
 - D3D11_LIBRARY_DESC
 - d3d11shader/D3D11_LIBRARY_DESC
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - D3D11Shader.h
api_name:
 - D3D11_LIBRARY_DESC
---

# D3D11_LIBRARY_DESC structure


## -description

Describes a library.

## -struct-fields

### -field Creator

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">LPCSTR</a></b>

The name of the originator of the library.

### -field Flags

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

A combination of <a href="/windows/desktop/direct3dhlsl/d3dcompile-constants">D3DCOMPILE Constants</a> that are combined by using a bitwise OR operation. The resulting value specifies how the compiler compiles.

### -field FunctionCount

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

The number of functions exported from the library.

## -see-also

<a href="/windows/desktop/api/d3d11shader/nf-d3d11shader-id3d11libraryreflection-getdesc">ID3D11LibraryReflection::GetDesc</a>



<a href="/windows/desktop/direct3d11/d3d11-graphics-reference-shader-structures">Shader Structures</a>
