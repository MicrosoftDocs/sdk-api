---
UID: NS:d3dcsx.D3DX11_FFT_BUFFER_INFO
title: D3DX11_FFT_BUFFER_INFO (d3dcsx.h)
description: Describes buffer requirements for an FFT.
helpviewer_keywords: ["D3DX11_FFT_BUFFER_INFO","D3DX11_FFT_BUFFER_INFO structure [Direct3D 11]","d3dcsx/D3DX11_FFT_BUFFER_INFO","direct3d11.d3dx11_fft_buffer_info","f06d9ab2-6da1-c0ae-f9cc-c42662b380f5"]
old-location: direct3d11\d3dx11_fft_buffer_info.htm
tech.root: direct3d11
ms.assetid: 18db9e61-f1bc-4c70-8b2c-37305d9ac479
ms.date: 12/05/2018
ms.keywords: D3DX11_FFT_BUFFER_INFO, D3DX11_FFT_BUFFER_INFO structure [Direct3D 11], d3dcsx/D3DX11_FFT_BUFFER_INFO, direct3d11.d3dx11_fft_buffer_info, f06d9ab2-6da1-c0ae-f9cc-c42662b380f5
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
req.typenames: D3DX11_FFT_BUFFER_INFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D3DX11_FFT_BUFFER_INFO
 - d3dcsx/D3DX11_FFT_BUFFER_INFO
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
 - D3DX11_FFT_BUFFER_INFO
---

# D3DX11_FFT_BUFFER_INFO structure


## -description

Describes buffer requirements for an FFT.

## -struct-fields

### -field NumTempBufferSizes

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Number of temporary buffers needed. 
            Allowed range is 0 to <b>D3DX11_FFT_MAX_TEMP_BUFFERS</b>.

### -field TempBufferFloatSizes

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a>[D3DX11_FFT_MAX_TEMP_BUFFERS]</b>

Minimum sizes (in FLOATs) of temporary buffers.

### -field NumPrecomputeBufferSizes

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Number of precompute buffers required.  
            Allowed range is 0 to <b>D3DX11_FFT_MAX_PRECOMPUTE_BUFFERS</b>.

### -field PrecomputeBufferFloatSizes

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a>[D3DX11_FFT_MAX_PRECOMPUTE_BUFFERS]</b>

Minimum sizes (in FLOATs) for precompute buffers.

## -remarks

The <b>D3DX11_FFT_BUFFER_INFO</b> structure is initialized by a call to one of the create-FFT functions
          (for example, <a href="/windows/desktop/api/d3dcsx/nf-d3dcsx-d3dx11createfft">D3DX11CreateFFT</a>).
          For more create-FFT functions, see <a href="/windows/desktop/direct3d11/d3d11-graphics-reference-d3dcsx11-functions">D3DCSX 11 Functions</a>.
        

Use the info in <b>D3DX11_FFT_BUFFER_INFO</b> to allocate raw buffers of the specified (or larger) sizes and then call the <a href="/windows/desktop/api/d3dcsx/nf-d3dcsx-id3dx11fft-attachbuffersandprecompute">ID3DX11FFT::AttachBuffersAndPrecompute</a> method to register the buffers with the FFT object.
        

Some FFT algorithms benefit from precomputing sin and cos. The FFT object might store precomputed data in the user-supplied buffers.

## -see-also

<a href="/windows/desktop/direct3d11/d3d11-graphics-reference-d3dcsx11-structures">D3DCSX 11 Structures</a>