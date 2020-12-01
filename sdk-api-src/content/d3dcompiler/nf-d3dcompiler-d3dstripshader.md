---
UID: NF:d3dcompiler.D3DStripShader
title: D3DStripShader function (d3dcompiler.h)
description: Removes unwanted blobs from a compilation result.
helpviewer_keywords: ["3320d273-7542-f3d8-0828-2c357608a8c8","D3DStripShader","D3DStripShader function [HLSL]","d3dcompiler/D3DStripShader","direct3dhlsl.d3dstripshader"]
old-location: direct3dhlsl\d3dstripshader.htm
tech.root: direct3dhlsl
ms.assetid: VS|directx_sdk|~\d3dstripshader.htm
ms.date: 12/05/2018
ms.keywords: 3320d273-7542-f3d8-0828-2c357608a8c8, D3DStripShader, D3DStripShader function [HLSL], d3dcompiler/D3DStripShader, direct3dhlsl.d3dstripshader
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
req.lib: D3dcompiler_47.lib
req.dll: D3dcompiler_47.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D3DStripShader
 - d3dcompiler/D3DStripShader
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - d3dcompiler_47.dll
api_name:
 - D3DStripShader
---

# D3DStripShader function


## -description

Removes unwanted blobs from a compilation result.

## -parameters

### -param pShaderBytecode [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">LPCVOID</a></b>

A pointer to source data as compiled HLSL code.

### -param BytecodeLength [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">SIZE_T</a></b>

Length of <i>pSrcData</i>.

### -param uStripFlags [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Strip flag options, represented by <a href="/windows/desktop/direct3dhlsl/d3dcompiler-strip-flags">D3DCOMPILER_STRIP_FLAGS</a>.

### -param ppStrippedBlob [out]

Type: <b><a href="/previous-versions/windows/desktop/legacy/ff728743(v=vs.85)">ID3DBlob</a>**</b>

A pointer to a variable that receives a pointer to the <a href="/previous-versions/windows/desktop/legacy/ff728743(v=vs.85)">ID3DBlob</a> interface that you can use to access the unwanted stripped out shader code.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

Returns one of the <a href="/windows/desktop/direct3d11/d3d11-graphics-reference-returnvalues">Direct3D 11 return codes</a>.

## -see-also

<a href="/windows/desktop/direct3dhlsl/dx-graphics-d3dcompiler-reference-functions">Functions</a>