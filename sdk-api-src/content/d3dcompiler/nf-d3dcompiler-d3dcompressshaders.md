---
UID: NF:d3dcompiler.D3DCompressShaders
title: D3DCompressShaders function (d3dcompiler.h)
description: Compresses a set of shaders into a more compact form.
helpviewer_keywords: ["D3DCompressShaders","D3DCompressShaders function [HLSL]","d3dcompiler/D3DCompressShaders","direct3dhlsl.d3dcompressshaders"]
old-location: direct3dhlsl\d3dcompressshaders.htm
tech.root: direct3dhlsl
ms.assetid: e53a0d36-3cd4-4327-8969-6a864b38a15b
ms.date: 12/05/2018
ms.keywords: D3DCompressShaders, D3DCompressShaders function [HLSL], d3dcompiler/D3DCompressShaders, direct3dhlsl.d3dcompressshaders
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
 - D3DCompressShaders
 - d3dcompiler/D3DCompressShaders
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
 - D3DCompressShaders
---

# D3DCompressShaders function


## -description

<div class="alert"><b>Note</b>  You can use this API to develop your Windows Store apps, but you can't use it in apps that you submit to the Windows Store.</div><div> </div>Compresses a set of shaders into a more compact form.

## -parameters

### -param uNumShaders [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

The number of shaders to compress.

### -param pShaderData [in]

Type: [D3D_SHADER_DATA](./ns-d3dcompiler-d3d_shader_data.md)*</b>

An array of [D3D_SHADER_DATA](./ns-d3dcompiler-d3d_shader_data.md) structures that describe the set of shaders to compress.

### -param uFlags [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Flags that indicate how to compress the shaders. Currently, only the  D3D_COMPRESS_SHADER_KEEP_ALL_PARTS (0x00000001) flag is defined.

### -param ppCompressedData [out]

Type: <b><a href="/previous-versions/windows/desktop/legacy/ff728743(v=vs.85)">ID3DBlob</a>**</b>

The address of a pointer to the <a href="/previous-versions/windows/desktop/legacy/ff728743(v=vs.85)">ID3DBlob</a> interface that is used to retrieve the compressed shader data.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

Returns one of the <a href="/windows/desktop/direct3d11/d3d11-graphics-reference-returnvalues">Direct3D 11 return codes</a>.

## -see-also

<a href="/windows/desktop/direct3dhlsl/dx-graphics-d3dcompiler-reference-functions">Functions</a>