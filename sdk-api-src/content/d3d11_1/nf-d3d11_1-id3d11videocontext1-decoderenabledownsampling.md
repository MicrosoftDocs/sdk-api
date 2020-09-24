---
UID: NF:d3d11_1.ID3D11VideoContext1.DecoderEnableDownsampling
title: ID3D11VideoContext1::DecoderEnableDownsampling (d3d11_1.h)
description: Indicates that decoder downsampling will be used and that the driver should allocate the appropriate reference frames.
helpviewer_keywords: ["DecoderEnableDownsampling","DecoderEnableDownsampling method [Media Foundation]","DecoderEnableDownsampling method [Media Foundation]","ID3D11VideoContext1 interface","ID3D11VideoContext1 interface [Media Foundation]","DecoderEnableDownsampling method","ID3D11VideoContext1.DecoderEnableDownsampling","ID3D11VideoContext1::DecoderEnableDownsampling","d3d11_1/ID3D11VideoContext1::DecoderEnableDownsampling","mf.id3d11videocontext1_decoderenabledownsampling"]
old-location: mf\id3d11videocontext1_decoderenabledownsampling.htm
tech.root: mf
ms.assetid: 0BE7E6EC-E090-4A13-9D18-108BDBBC211A
ms.date: 12/05/2018
ms.keywords: DecoderEnableDownsampling, DecoderEnableDownsampling method [Media Foundation], DecoderEnableDownsampling method [Media Foundation],ID3D11VideoContext1 interface, ID3D11VideoContext1 interface [Media Foundation],DecoderEnableDownsampling method, ID3D11VideoContext1.DecoderEnableDownsampling, ID3D11VideoContext1::DecoderEnableDownsampling, d3d11_1/ID3D11VideoContext1::DecoderEnableDownsampling, mf.id3d11videocontext1_decoderenabledownsampling
req.header: d3d11_1.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10 [desktop apps only]
req.target-min-winversvr: Windows Server 2016 [desktop apps only]
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
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ID3D11VideoContext1::DecoderEnableDownsampling
 - d3d11_1/ID3D11VideoContext1::DecoderEnableDownsampling
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - d3d11_1.h
api_name:
 - ID3D11VideoContext1.DecoderEnableDownsampling
---

# ID3D11VideoContext1::DecoderEnableDownsampling


## -description

Indicates that decoder downsampling will be used and that the driver should allocate the appropriate reference frames.

## -parameters

### -param pDecoder [in]

Type: <b>ID3D11VideoDecoder*</b>

A pointer to the <a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11videodecoder">ID3D11VideoDecoder</a> interface.

### -param InputColorSpace [in]

Type: <b>DXGI_COLOR_SPACE_TYPE</b>

The color space information of the reference frame data.

### -param pOutputDesc [in]

Type: <b>const <a href="/windows/desktop/api/d3d11_1/ns-d3d11_1-d3d11_video_sample_desc">D3D11_VIDEO_SAMPLE_DESC</a>*</b>

The resolution, format, and colorspace of the output/display frames.  This is the destination resolution and format of the downsample operation.

### -param ReferenceFrameCount [in]

Type: <b>UINT</b>

The number of reference frames to be used in the operation.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

This method returns one of the following error codes.

<table>
<tr>
<td>S_OK</td>
<td>The operation completed successfully.</td>
</tr>
<tr>
<td>E_INVALIDARG</td>
<td>An invalid parameter was passed or this function was called using an invalid calling pattern.</td>
</tr>
<tr>
<td>E_OUTOFMEMORY</td>
<td>There is insufficient memory to complete the operation.</td>
</tr>
</table>

## -remarks

This function can only be called once for a specific <a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11videodecoder">ID3D11VideoDecoder</a> interface. This method must be called prior to the first call to <a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11videocontext-decoderbeginframe">DecoderBeginFrame</a>. To update the downsampling parameters, use <a href="/windows/desktop/api/d3d11_1/nf-d3d11_1-id3d11videocontext1-decoderupdatedownsampling">DecoderUpdateDownsampling</a>.

## -see-also

<a href="/windows/desktop/api/d3d11_1/nn-d3d11_1-id3d11videocontext1">ID3D11VideoContext1</a>