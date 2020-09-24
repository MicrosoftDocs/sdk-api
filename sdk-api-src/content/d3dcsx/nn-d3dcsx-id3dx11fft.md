---
UID: NN:d3dcsx.ID3DX11FFT
title: ID3DX11FFT (d3dcsx.h)
description: Encapsulates forward and inverse FFTs.
helpviewer_keywords: ["6baaded3-822f-0135-c977-9d5552c9ac99","ID3DX11FFT","ID3DX11FFT interface [Direct3D 11]","ID3DX11FFT interface [Direct3D 11]","described","d3dcsx/ID3DX11FFT","direct3d11.id3dx11fft"]
old-location: direct3d11\id3dx11fft.htm
tech.root: direct3d11
ms.assetid: 6979aea4-5121-4a65-85f6-4b5753083715
ms.date: 12/05/2018
ms.keywords: 6baaded3-822f-0135-c977-9d5552c9ac99, ID3DX11FFT, ID3DX11FFT interface [Direct3D 11], ID3DX11FFT interface [Direct3D 11],described, d3dcsx/ID3DX11FFT, direct3d11.id3dx11fft
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
 - ID3DX11FFT
 - d3dcsx/ID3DX11FFT
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
 - ID3DX11FFT
---

# ID3DX11FFT interface


## -description

Encapsulates forward and inverse FFTs.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ID3DX11FFT</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ID3DX11FFT</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ID3DX11FFT</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/d3dcsx/nf-d3dcsx-id3dx11fft-attachbuffersandprecompute">AttachBuffersAndPrecompute</a>
</td>
<td align="left" width="63%">
Attaches buffers to an FFT context and performs any required precomputations.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/d3dcsx/nf-d3dcsx-id3dx11fft-forwardtransform">ForwardTransform</a>
</td>
<td align="left" width="63%">
Performs a forward FFT.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/d3dcsx/nf-d3dcsx-id3dx11fft-getforwardscale">GetForwardScale</a>
</td>
<td align="left" width="63%">
Gets the scale for forward transforms.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/d3dcsx/nf-d3dcsx-id3dx11fft-getinversescale">GetInverseScale</a>
</td>
<td align="left" width="63%">
Get the scale for inverse transforms.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/d3dcsx/nf-d3dcsx-id3dx11fft-inversetransform">InverseTransform</a>
</td>
<td align="left" width="63%">
Performs an inverse FFT.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/d3dcsx/nf-d3dcsx-id3dx11fft-setforwardscale">SetForwardScale</a>
</td>
<td align="left" width="63%">
Sets the scale used for forward transforms.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/d3dcsx/nf-d3dcsx-id3dx11fft-setinversescale">SetInverseScale</a>
</td>
<td align="left" width="63%">
Sets the scale used for inverse transforms.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/direct3d11/d3d11-graphics-reference-d3dcsx11-interfaces">D3DCSX 11 Interfaces</a>