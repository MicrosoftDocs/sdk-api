---
UID: NF:d3dcompiler.D3DGetBlobPart
title: D3DGetBlobPart function (d3dcompiler.h)
description: Retrieves a specific part from a compilation result.
helpviewer_keywords: ["D3DGetBlobPart","D3DGetBlobPart function [HLSL]","d3dcompiler/D3DGetBlobPart","direct3dhlsl.d3dgetblobpart"]
old-location: direct3dhlsl\d3dgetblobpart.htm
tech.root: direct3dhlsl
ms.assetid: cf9cea53-e7a3-4473-bfdf-0cdeb8370974
ms.date: 12/05/2018
ms.keywords: D3DGetBlobPart, D3DGetBlobPart function [HLSL], d3dcompiler/D3DGetBlobPart, direct3dhlsl.d3dgetblobpart
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
 - D3DGetBlobPart
 - d3dcompiler/D3DGetBlobPart
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
 - D3DGetBlobPart
---

# D3DGetBlobPart function


## -description

Retrieves a specific part from a compilation result.

## -parameters

### -param pSrcData [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">LPCVOID</a></b>

A pointer to uncompiled shader data; either ASCII HLSL code or a compiled effect.

### -param SrcDataSize [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">SIZE_T</a></b>

Length of uncompiled shader data that <i>pSrcData</i> points to.

### -param Part [in]

Type: <b><a href="/windows/desktop/direct3dhlsl/d3d-blob-part">D3D_BLOB_PART</a></b>

A <a href="/windows/desktop/direct3dhlsl/d3d-blob-part">D3D_BLOB_PART</a>-typed value that specifies the part of the buffer to retrieve.

### -param Flags [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Flags that indicate how to retrieve the blob part. Currently, no flags are defined.

### -param ppPart [out]

Type: <b><a href="/previous-versions/windows/desktop/legacy/ff728743(v=vs.85)">ID3DBlob</a>**</b>

The address of a pointer to the <a href="/previous-versions/windows/desktop/legacy/ff728743(v=vs.85)">ID3DBlob</a> interface that is used to retrieve the specified part of the buffer.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

Returns one of the <a href="/windows/desktop/direct3d11/d3d11-graphics-reference-returnvalues">Direct3D 11 return codes</a>.

## -remarks

<b>D3DGetBlobPart</b> retrieves the part of a blob (arbitrary length data buffer) that contains the type of data that the  <i>Part</i> parameter specifies.

## -see-also

<a href="/windows/desktop/direct3dhlsl/dx-graphics-d3dcompiler-reference-functions">Functions</a>