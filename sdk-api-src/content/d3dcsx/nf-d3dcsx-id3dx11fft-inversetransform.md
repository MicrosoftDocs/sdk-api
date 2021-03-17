---
UID: NF:d3dcsx.ID3DX11FFT.InverseTransform
title: ID3DX11FFT::InverseTransform (d3dcsx.h)
description: Performs an inverse FFT.
helpviewer_keywords: ["9e07e88b-a097-403f-b882-754a12668d07","ID3DX11FFT interface [Direct3D 11]","InverseTransform method","ID3DX11FFT.InverseTransform","ID3DX11FFT::InverseTransform","InverseTransform","InverseTransform method [Direct3D 11]","InverseTransform method [Direct3D 11]","ID3DX11FFT interface","d3dcsx/ID3DX11FFT::InverseTransform","direct3d11.id3dx11fft_inversetransform"]
old-location: direct3d11\id3dx11fft_inversetransform.htm
tech.root: direct3d11
ms.assetid: e4fe7a35-b039-4977-ba68-9869c5cc4383
ms.date: 12/05/2018
ms.keywords: 9e07e88b-a097-403f-b882-754a12668d07, ID3DX11FFT interface [Direct3D 11],InverseTransform method, ID3DX11FFT.InverseTransform, ID3DX11FFT::InverseTransform, InverseTransform, InverseTransform method [Direct3D 11], InverseTransform method [Direct3D 11],ID3DX11FFT interface, d3dcsx/ID3DX11FFT::InverseTransform, direct3d11.id3dx11fft_inversetransform
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
 - ID3DX11FFT::InverseTransform
 - d3dcsx/ID3DX11FFT::InverseTransform
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
 - ID3DX11FFT.InverseTransform
---

# ID3DX11FFT::InverseTransform


## -description

Performs an inverse FFT.

## -parameters

### -param pInputBuffer [in]

Type: <b>const <a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11unorderedaccessview">ID3D11UnorderedAccessView</a>*</b>

Pointer to <a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11unorderedaccessview">ID3D11UnorderedAccessView</a> onto the input buffer.

### -param ppOutputBuffer [in, out]

Type: <b><a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11unorderedaccessview">ID3D11UnorderedAccessView</a>**</b>

Pointer to a <a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11unorderedaccessview">ID3D11UnorderedAccessView</a> pointer.  If *<i>ppOutput</i> is <b>NULL</b>, then the computation will switch
          between temp buffers; in addition, the last buffer written to is stored at *<i>ppOutput</i>.
          Otherwise, *<i>ppOutput</i> is used as the output buffer (which might incur an extra copy).

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

Returns one of the return codes described in the topic <a href="/windows/desktop/direct3d11/d3d11-graphics-reference-returnvalues">Direct3D 11 Return Codes</a>.

## -see-also

<a href="/windows/desktop/api/d3dcsx/nn-d3dcsx-id3dx11fft">ID3DX11FFT</a>