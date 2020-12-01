---
UID: NF:d3dcsx.ID3DX11FFT.AttachBuffersAndPrecompute
title: ID3DX11FFT::AttachBuffersAndPrecompute (d3dcsx.h)
description: Attaches buffers to an FFT context and performs any required precomputations.
helpviewer_keywords: ["AttachBuffersAndPrecompute","AttachBuffersAndPrecompute method [Direct3D 11]","AttachBuffersAndPrecompute method [Direct3D 11]","ID3DX11FFT interface","ID3DX11FFT interface [Direct3D 11]","AttachBuffersAndPrecompute method","ID3DX11FFT.AttachBuffersAndPrecompute","ID3DX11FFT::AttachBuffersAndPrecompute","d035d5bc-194b-3f37-2b54-5d5f4ae0fbc8","d3dcsx/ID3DX11FFT::AttachBuffersAndPrecompute","direct3d11.id3dx11fft_attachbuffersandprecompute"]
old-location: direct3d11\id3dx11fft_attachbuffersandprecompute.htm
tech.root: direct3d11
ms.assetid: 50c714fc-91fb-4a7d-a430-40ff221a1a14
ms.date: 12/05/2018
ms.keywords: AttachBuffersAndPrecompute, AttachBuffersAndPrecompute method [Direct3D 11], AttachBuffersAndPrecompute method [Direct3D 11],ID3DX11FFT interface, ID3DX11FFT interface [Direct3D 11],AttachBuffersAndPrecompute method, ID3DX11FFT.AttachBuffersAndPrecompute, ID3DX11FFT::AttachBuffersAndPrecompute, d035d5bc-194b-3f37-2b54-5d5f4ae0fbc8, d3dcsx/ID3DX11FFT::AttachBuffersAndPrecompute, direct3d11.id3dx11fft_attachbuffersandprecompute
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
 - ID3DX11FFT::AttachBuffersAndPrecompute
 - d3dcsx/ID3DX11FFT::AttachBuffersAndPrecompute
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - d3dcsx.lib
 - d3dcsx.dll
api_name:
 - ID3DX11FFT.AttachBuffersAndPrecompute
---

# ID3DX11FFT::AttachBuffersAndPrecompute


## -description

Attaches buffers to an FFT context and performs any required precomputations.

## -parameters

### -param NumTempBuffers [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Number of buffers in <i>ppTempBuffers</i>.

### -param ppTempBuffers [in]

Type: <b><a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11unorderedaccessview">ID3D11UnorderedAccessView</a>*</b>

A pointer to an array of <a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11unorderedaccessview">ID3D11UnorderedAccessView</a> pointers for the temporary buffers to attach. The FFT object might use these temporary buffers for its algorithm.

### -param NumPrecomputeBuffers [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">UINT</a></b>

Number of buffers in <i>ppPrecomputeBuffers</i>.

### -param ppPrecomputeBufferSizes [in]

Type: <b><a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11unorderedaccessview">ID3D11UnorderedAccessView</a>*</b>

A pointer to an array of <a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11unorderedaccessview">ID3D11UnorderedAccessView</a> pointers for the precompute buffers to attach. The FFT object might store precomputed data  in these buffers.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

Returns one of the return codes described in the topic <a href="/windows/desktop/direct3d11/d3d11-graphics-reference-returnvalues">Direct3D 11 Return Codes</a>.

## -remarks

The <a href="/windows/desktop/api/d3dcsx/ns-d3dcsx-d3dx11_fft_buffer_info">D3DX11_FFT_BUFFER_INFO</a> structure is initialized by a call to one of the create-FFT functions 
      (for example, <a href="/windows/desktop/api/d3dcsx/nf-d3dcsx-d3dx11createfft">D3DX11CreateFFT</a>). For more create-FFT functions, see <a href="/windows/desktop/direct3d11/d3d11-graphics-reference-d3dcsx11-functions">D3DCSX 11 Functions</a>.

Use the info in <a href="/windows/desktop/api/d3dcsx/ns-d3dcsx-d3dx11_fft_buffer_info">D3DX11_FFT_BUFFER_INFO</a> to allocate raw buffers of the specified (or larger) sizes and then call the <b>AttachBuffersAndPrecompute</b> to register the buffers with the FFT object.

Although you can share temporary buffers between multiple
      device contexts, we recommend not to concurrently execute multiple FFT objects that share temporary buffers.

Some FFT algorithms benefit from precomputing sin and cos. The FFT object might store precomputed data  in the user-supplied precompute buffers.

## -see-also

<a href="/windows/desktop/api/d3dcsx/nn-d3dcsx-id3dx11fft">ID3DX11FFT</a>