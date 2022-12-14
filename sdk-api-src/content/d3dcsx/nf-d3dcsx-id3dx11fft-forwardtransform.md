---
UID: NF:d3dcsx.ID3DX11FFT.ForwardTransform
title: ID3DX11FFT::ForwardTransform (d3dcsx.h)
description: Performs a forward FFT.
helpviewer_keywords: ["ForwardTransform","ForwardTransform method [Direct3D 11]","ForwardTransform method [Direct3D 11]","ID3DX11FFT interface","ID3DX11FFT interface [Direct3D 11]","ForwardTransform method","ID3DX11FFT.ForwardTransform","ID3DX11FFT::ForwardTransform","d3dcsx/ID3DX11FFT::ForwardTransform","direct3d11.id3dx11fft_forwardtransform","fbd555b1-86f3-8e92-7c5e-ed1c088e2207"]
old-location: direct3d11\id3dx11fft_forwardtransform.htm
tech.root: direct3d11
ms.assetid: da10b166-9561-4c04-b6b8-92b2daec30d7
ms.date: 12/05/2018
ms.keywords: ForwardTransform, ForwardTransform method [Direct3D 11], ForwardTransform method [Direct3D 11],ID3DX11FFT interface, ID3DX11FFT interface [Direct3D 11],ForwardTransform method, ID3DX11FFT.ForwardTransform, ID3DX11FFT::ForwardTransform, d3dcsx/ID3DX11FFT::ForwardTransform, direct3d11.id3dx11fft_forwardtransform, fbd555b1-86f3-8e92-7c5e-ed1c088e2207
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
 - ID3DX11FFT::ForwardTransform
 - d3dcsx/ID3DX11FFT::ForwardTransform
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
 - ID3DX11FFT.ForwardTransform
---

# ID3DX11FFT::ForwardTransform


## -description

Performs a forward FFT.

## -parameters

### -param pInputBuffer [in]

Type: <b>const <a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11unorderedaccessview">ID3D11UnorderedAccessView</a>*</b>

Pointer to <a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11unorderedaccessview">ID3D11UnorderedAccessView</a> onto the input buffer.

### -param ppOutputBuffer [in, out]

Type: <b><a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11unorderedaccessview">ID3D11UnorderedAccessView</a>**</b>

Pointer to a <a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11unorderedaccessview">ID3D11UnorderedAccessView</a> pointer.  If *<i>ppOutputBuffer</i> is <b>NULL</b>, the computation will switch
          between temp buffers; in addition, the last buffer written to is stored at *<i>ppOutputBuffer</i>.
          Otherwise, *<i>ppOutputBuffer</i> is used as the output buffer (which might incur an extra copy).

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

Returns one of the return codes described in the topic <a href="/windows/desktop/direct3d11/d3d11-graphics-reference-returnvalues">Direct3D 11 Return Codes</a>.

## -remarks

<b>ForwardTransform</b> can be called after buffers have been attached to the context using <a href="/windows/desktop/api/d3dcsx/nf-d3dcsx-id3dx11fft-attachbuffersandprecompute">ID3DX11FFT::AttachBuffersAndPrecompute</a>. The combination of <i>pInputBuffer</i> and *<i>ppOutputBuffer</i> can be one of the temp buffers.

The format of complex data is interleaved components (for example, (Real0, Imag0), 
      (Real1, Imag1) ... , and so on). Data is stored in row major order.

## -see-also

<a href="/windows/desktop/api/d3dcsx/nn-d3dcsx-id3dx11fft">ID3DX11FFT</a>