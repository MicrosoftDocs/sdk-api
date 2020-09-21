---
UID: NF:d3dcsx.ID3DX11FFT.SetInverseScale
title: ID3DX11FFT::SetInverseScale (d3dcsx.h)
description: Sets the scale used for inverse transforms.
helpviewer_keywords: ["ID3DX11FFT interface [Direct3D 11]","SetInverseScale method","ID3DX11FFT.SetInverseScale","ID3DX11FFT::SetInverseScale","SetInverseScale","SetInverseScale method [Direct3D 11]","SetInverseScale method [Direct3D 11]","ID3DX11FFT interface","d3dcsx/ID3DX11FFT::SetInverseScale","direct3d11.id3dx11fft_setinversescale","e2fd7d2b-bce2-191f-6387-e478c2a535fb"]
old-location: direct3d11\id3dx11fft_setinversescale.htm
tech.root: direct3d11
ms.assetid: db29b6f8-ee36-48b6-8e28-f4bbaa6b0a7f
ms.date: 12/05/2018
ms.keywords: ID3DX11FFT interface [Direct3D 11],SetInverseScale method, ID3DX11FFT.SetInverseScale, ID3DX11FFT::SetInverseScale, SetInverseScale, SetInverseScale method [Direct3D 11], SetInverseScale method [Direct3D 11],ID3DX11FFT interface, d3dcsx/ID3DX11FFT::SetInverseScale, direct3d11.id3dx11fft_setinversescale, e2fd7d2b-bce2-191f-6387-e478c2a535fb
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
 - ID3DX11FFT::SetInverseScale
 - d3dcsx/ID3DX11FFT::SetInverseScale
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
 - ID3DX11FFT.SetInverseScale
---

# ID3DX11FFT::SetInverseScale


## -description

Sets the scale used for inverse transforms.

## -parameters

### -param InverseScale [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">FLOAT</a></b>

Scale used for inverse transforms.  Setting <i>InverseScale</i> to 0 causes the default value of 1/N to be used, 
          where N is the product of the transformed dimension lengths.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

Returns one of the return codes described in the topic <a href="/windows/desktop/direct3d11/d3d11-graphics-reference-returnvalues">Direct3D 11 Return Codes</a>.

## -remarks

<b>SetInverseScale</b> sets the scale used by <a href="/windows/desktop/api/d3dcsx/nf-d3dcsx-id3dx11fft-inversetransform">ID3DX11FFT::InverseTransform</a>.

## -see-also

<a href="/windows/desktop/api/d3dcsx/nn-d3dcsx-id3dx11fft">ID3DX11FFT</a>