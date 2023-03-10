---
UID: NF:d3dcompiler.D3DDecompressShaders
title: D3DDecompressShaders function (d3dcompiler.h)
description: Decompresses one or more shaders from a compressed set.
helpviewer_keywords: ["D3DDecompressShaders","D3DDecompressShaders function [HLSL]","d3dcompiler/D3DDecompressShaders","direct3dhlsl.d3ddecompressshaders"]
old-location: direct3dhlsl\d3ddecompressshaders.htm
tech.root: direct3dhlsl
ms.assetid: 9b62026f-0658-405c-8f45-ee921213148a
ms.date: 12/05/2018
ms.keywords: D3DDecompressShaders, D3DDecompressShaders function [HLSL], d3dcompiler/D3DDecompressShaders, direct3dhlsl.d3ddecompressshaders
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
 - D3DDecompressShaders
 - d3dcompiler/D3DDecompressShaders
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
 - D3DDecompressShaders
---

# D3DDecompressShaders function


## -description

<div class="alert"><b>Note</b>  You can use this API to develop your Windows Store apps, but you can't use it in apps that you submit to the Windows Store.</div><div> </div>Decompresses one or more shaders from a compressed set.

## -parameters

### -param pSrcData [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">LPCVOID</a></b>

A pointer to uncompiled shader data; either ASCII HLSL code or a compiled effect.

### -param SrcDataSize [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">SIZE_T</a></b>

Length of uncompiled shader data that <i>pSrcData</i> points to.

### -param uNumShaders [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

The number of shaders to decompress.

### -param uStartIndex [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

The index of the first shader to decompress.

### -param pIndices [in, optional]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a>*</b>

An array of indexes that represent the shaders to decompress.

### -param uFlags [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Flags that indicate how to decompress. Currently, no flags are defined.

### -param ppShaders [out]

Type: <b><a href="/previous-versions/windows/desktop/legacy/ff728743(v=vs.85)">ID3DBlob</a>**</b>

The address of a pointer to the <a href="/previous-versions/windows/desktop/legacy/ff728743(v=vs.85)">ID3DBlob</a> interface that is used to retrieve the decompressed shader data.

### -param pTotalShaders [out, optional]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a>*</b>

A pointer to a variable that receives the total number of shaders that  <b>D3DDecompressShaders</b> decompressed.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

Returns one of the <a href="/windows/desktop/direct3d11/d3d11-graphics-reference-returnvalues">Direct3D 11 return codes</a>.

## -see-also

<a href="/windows/desktop/direct3dhlsl/dx-graphics-d3dcompiler-reference-functions">Functions</a>