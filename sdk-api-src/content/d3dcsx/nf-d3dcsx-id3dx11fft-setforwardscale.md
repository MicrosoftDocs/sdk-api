---
UID: NF:d3dcsx.ID3DX11FFT.SetForwardScale
title: ID3DX11FFT::SetForwardScale (d3dcsx.h)
description: Sets the scale used for forward transforms.
helpviewer_keywords: ["ID3DX11FFT interface [Direct3D 11]","SetForwardScale method","ID3DX11FFT.SetForwardScale","ID3DX11FFT::SetForwardScale","SetForwardScale","SetForwardScale method [Direct3D 11]","SetForwardScale method [Direct3D 11]","ID3DX11FFT interface","ceddf377-cf6d-2efb-3b7d-dcf4a17d5886","d3dcsx/ID3DX11FFT::SetForwardScale","direct3d11.id3dx11fft_setforwardscale"]
old-location: direct3d11\id3dx11fft_setforwardscale.htm
tech.root: direct3d11
ms.assetid: afca03bb-459f-42ff-bc88-7487b1bc250d
ms.date: 12/05/2018
ms.keywords: ID3DX11FFT interface [Direct3D 11],SetForwardScale method, ID3DX11FFT.SetForwardScale, ID3DX11FFT::SetForwardScale, SetForwardScale, SetForwardScale method [Direct3D 11], SetForwardScale method [Direct3D 11],ID3DX11FFT interface, ceddf377-cf6d-2efb-3b7d-dcf4a17d5886, d3dcsx/ID3DX11FFT::SetForwardScale, direct3d11.id3dx11fft_setforwardscale
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
 - ID3DX11FFT::SetForwardScale
 - d3dcsx/ID3DX11FFT::SetForwardScale
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
 - ID3DX11FFT.SetForwardScale
---

# ID3DX11FFT::SetForwardScale


## -description

Sets the scale used for forward transforms.

## -parameters

### -param ForwardScale [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">FLOAT</a></b>

The scale to use for forward transforms.  Setting <i>ForwardScale</i> to 0 causes the default values of 1 to be used.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

Returns one of the return codes described in the topic <a href="/windows/desktop/direct3d11/d3d11-graphics-reference-returnvalues">Direct3D 11 Return Codes</a>.

## -remarks

<b>SetForwardScale</b> sets the scale used by <a href="/windows/desktop/api/d3dcsx/nf-d3dcsx-id3dx11fft-forwardtransform">ID3DX11FFT::ForwardTransform</a>.

## -see-also

<a href="/windows/desktop/api/d3dcsx/nn-d3dcsx-id3dx11fft">ID3DX11FFT</a>