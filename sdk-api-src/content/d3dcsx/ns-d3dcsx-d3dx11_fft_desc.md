---
UID: NS:d3dcsx.D3DX11_FFT_DESC
title: D3DX11_FFT_DESC (d3dcsx.h)
description: Describes an FFT.
helpviewer_keywords: ["68cda090-9f5e-c349-40c7-a6e3b2bd2960","D3DX11_FFT_DESC","D3DX11_FFT_DESC structure [Direct3D 11]","d3dcsx/D3DX11_FFT_DESC","direct3d11.d3dx11_fft_desc"]
old-location: direct3d11\d3dx11_fft_desc.htm
tech.root: direct3d11
ms.assetid: b410e7c4-3b16-4510-9555-fc8b22fd3e2c
ms.date: 12/05/2018
ms.keywords: 68cda090-9f5e-c349-40c7-a6e3b2bd2960, D3DX11_FFT_DESC, D3DX11_FFT_DESC structure [Direct3D 11], d3dcsx/D3DX11_FFT_DESC, direct3d11.d3dx11_fft_desc
req.header: d3dcsx.h
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
req.typenames: D3DX11_FFT_DESC
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D3DX11_FFT_DESC
 - d3dcsx/D3DX11_FFT_DESC
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - d3dcsx.h
api_name:
 - D3DX11_FFT_DESC
---

# D3DX11_FFT_DESC structure


## -description

Describes an FFT.

## -struct-fields

### -field NumDimensions

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Number of dimension in the FFT.

### -field ElementLengths

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a>[D3DX11_FFT_MAX_DIMENSIONS]</b>

Length of each dimension in the FFT.

### -field DimensionMask

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Combination of <a href="/windows/desktop/api/d3dcsx/ne-d3dcsx-d3dx11_fft_dim_mask">D3DX11_FFT_DIM_MASK</a> flags indicating the  dimensions to transform.

### -field Type

Type: <b><a href="/windows/desktop/api/d3dcsx/ne-d3dcsx-d3dx11_fft_data_type">D3DX11_FFT_DATA_TYPE</a></b>


<a href="/windows/desktop/api/d3dcsx/ne-d3dcsx-d3dx11_fft_data_type">D3DX11_FFT_DATA_TYPE</a> flag indicating the type of data being transformed.

## -see-also

<a href="/windows/desktop/direct3d11/d3d11-graphics-reference-d3dcsx11-structures">D3DCSX 11 Structures</a>