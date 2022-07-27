---
UID: NF:d3dcsx.D3DX11CreateFFT3DReal
title: D3DX11CreateFFT3DReal function (d3dcsx.h)
description: Creates an ID3DX11FFT COM interface object. (D3DX11CreateFFT3DReal)
helpviewer_keywords: ["965f86f8-f5c0-6a29-55ee-93b995644cf2","D3DX11CreateFFT3DReal","D3DX11CreateFFT3DReal function [Direct3D 11]","d3dcsx/D3DX11CreateFFT3DReal","direct3d11.d3dx11createfft3dreal"]
old-location: direct3d11\d3dx11createfft3dreal.htm
tech.root: direct3d11
ms.assetid: c9194109-3755-4e63-969d-c01a96198d2b
ms.date: 12/05/2018
ms.keywords: 965f86f8-f5c0-6a29-55ee-93b995644cf2, D3DX11CreateFFT3DReal, D3DX11CreateFFT3DReal function [Direct3D 11], d3dcsx/D3DX11CreateFFT3DReal, direct3d11.d3dx11createfft3dreal
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
req.lib: D3dcsx.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - D3DX11CreateFFT3DReal
 - d3dcsx/D3DX11CreateFFT3DReal
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - LibDef
api_location:
 - d3dcsx.lib
 - d3dcsx.dll
api_name:
 - D3DX11CreateFFT3DReal
---

# D3DX11CreateFFT3DReal function


## -description

Creates an <a href="/windows/desktop/api/d3dcsx/nn-d3dcsx-id3dx11fft">ID3DX11FFT</a> COM interface object.

## -parameters

### -param pDeviceContext

Type: <b><a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11devicecontext">ID3D11DeviceContext</a>*</b>

A pointer to the <a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11devicecontext">ID3D11DeviceContext</a> interface to use for the FFT.

### -param X

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Length of the first dimension of the FFT.

### -param Y

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Length of the second dimension of the FFT.

### -param Z

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Length of the third dimension of the FFT.

### -param Flags

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Flags that affect the behavior of the FFT, can be 0 or a combination of flags from <a href="/windows/desktop/api/d3dcsx/ne-d3dcsx-d3dx11_fft_create_flag">D3DX11_FFT_CREATE_FLAG</a>.

### -param pBufferInfo [out]

Type: <b><a href="/windows/desktop/api/d3dcsx/ns-d3dcsx-d3dx11_fft_buffer_info">D3DX11_FFT_BUFFER_INFO</a>*</b>

A pointer to a <a href="/windows/desktop/api/d3dcsx/ns-d3dcsx-d3dx11_fft_buffer_info">D3DX11_FFT_BUFFER_INFO</a> structure that receives the buffer requirements to execute the FFT algorithms. Use this info to allocate raw buffers of the specified (or larger) sizes and then call the <a href="/windows/desktop/api/d3dcsx/nf-d3dcsx-id3dx11fft-attachbuffersandprecompute">ID3DX11FFT::AttachBuffersAndPrecompute</a> method to register the buffers with the FFT object.

### -param ppFFT [out]

Type: <b><a href="/windows/desktop/api/d3dcsx/nn-d3dcsx-id3dx11fft">ID3DX11FFT</a>**</b>

A pointer to a variable that receives a pointer to the <a href="/windows/desktop/api/d3dcsx/nn-d3dcsx-id3dx11fft">ID3DX11FFT</a> interface for the created FFT object.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

The return value is one of the values listed in <a href="/windows/desktop/direct3d11/d3d11-graphics-reference-returnvalues">Direct3D 11 Return Codes</a>.

## -see-also

<a href="/windows/desktop/direct3d11/d3d11-graphics-reference-d3dcsx11-functions">D3DCSX 11 Functions</a>
