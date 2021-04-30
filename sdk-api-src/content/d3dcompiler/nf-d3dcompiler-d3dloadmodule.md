---
UID: NF:d3dcompiler.D3DLoadModule
title: D3DLoadModule function (d3dcompiler.h)
description: Creates a shader module interface from source data for the shader module.
helpviewer_keywords: ["D3DLoadModule","D3DLoadModule function [HLSL]","d3dcompiler/D3DLoadModule","direct3dhlsl.d3dloadmodule"]
old-location: direct3dhlsl\d3dloadmodule.htm
tech.root: direct3dhlsl
ms.assetid: 698AADA6-0A88-44AD-9F15-F085BFE52CA1
ms.date: 12/05/2018
ms.keywords: D3DLoadModule, D3DLoadModule function [HLSL], d3dcompiler/D3DLoadModule, direct3dhlsl.d3dloadmodule
req.header: d3dcompiler.h
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
 - D3DLoadModule
 - d3dcompiler/D3DLoadModule
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - D3DCompiler_47.dll
api_name:
 - D3DLoadModule
---

# D3DLoadModule function


## -description

Creates a shader module interface from source data for the shader module. <div class="alert"><b>Note</b>  This function is part of the HLSL shader linking technology that you can use on all Direct3D 11 platforms to create precompiled HLSL functions, package them into libraries, and link them into full shaders at run time.
</div>
<div> </div>

## -parameters

### -param pSrcData [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">LPCVOID</a></b>

A pointer to the source data for the shader module.

### -param cbSrcDataSize [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">SIZE_T</a></b>

The size, in bytes, of the block of memory that <i>pSrcData</i> points to.

### -param ppModule [out]

Type: <b><a href="/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11module">ID3D11Module</a>**</b>

A pointer to a variable that receives a pointer to the <a href="/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11module">ID3D11Module</a> interface that is used for shader resource re-binding.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

Returns S_OK if successful; otherwise, returns one of the <a href="/windows/desktop/direct3d11/d3d11-graphics-reference-returnvalues">Direct3D 11 Return Codes</a>.

## -remarks

<div class="alert"><b>Note</b>  The D3dcompiler_47.dll or later version of the DLL contains the <b>D3DLoadModule</b> function.</div>
<div> </div>

## -see-also

<a href="/windows/desktop/direct3dhlsl/dx-graphics-d3dcompiler-reference-functions">Functions</a>



<a href="/windows/desktop/api/d3d11shader/nn-d3d11shader-id3d11module">ID3D11Module</a>