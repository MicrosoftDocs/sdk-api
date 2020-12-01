---
UID: NF:d3d11_1.ID3D11VideoDevice1.RecommendVideoDecoderDownsampleParameters
title: ID3D11VideoDevice1::RecommendVideoDecoderDownsampleParameters (d3d11_1.h)
description: Allows the driver to recommend optimal output downsample parameters from the input parameters.
helpviewer_keywords: ["ID3D11VideoDevice1 interface [Media Foundation]","RecommendVideoDecoderDownsampleParameters method","ID3D11VideoDevice1.RecommendVideoDecoderDownsampleParameters","ID3D11VideoDevice1::RecommendVideoDecoderDownsampleParameters","RecommendVideoDecoderDownsampleParameters","RecommendVideoDecoderDownsampleParameters method [Media Foundation]","RecommendVideoDecoderDownsampleParameters method [Media Foundation]","ID3D11VideoDevice1 interface","d3d11_1/ID3D11VideoDevice1::RecommendVideoDecoderDownsampleParameters","mf.id3d11videodevice1_recommendvideodecoderdownsampleparameters"]
old-location: mf\id3d11videodevice1_recommendvideodecoderdownsampleparameters.htm
tech.root: mf
ms.assetid: DD1C1273-C069-4C46-933F-3450F9DDAFBD
ms.date: 12/05/2018
ms.keywords: ID3D11VideoDevice1 interface [Media Foundation],RecommendVideoDecoderDownsampleParameters method, ID3D11VideoDevice1.RecommendVideoDecoderDownsampleParameters, ID3D11VideoDevice1::RecommendVideoDecoderDownsampleParameters, RecommendVideoDecoderDownsampleParameters, RecommendVideoDecoderDownsampleParameters method [Media Foundation], RecommendVideoDecoderDownsampleParameters method [Media Foundation],ID3D11VideoDevice1 interface, d3d11_1/ID3D11VideoDevice1::RecommendVideoDecoderDownsampleParameters, mf.id3d11videodevice1_recommendvideodecoderdownsampleparameters
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
 - ID3D11VideoDevice1::RecommendVideoDecoderDownsampleParameters
 - d3d11_1/ID3D11VideoDevice1::RecommendVideoDecoderDownsampleParameters
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
 - ID3D11VideoDevice1.RecommendVideoDecoderDownsampleParameters
---

# ID3D11VideoDevice1::RecommendVideoDecoderDownsampleParameters


## -description

Allows the driver to recommend optimal output downsample parameters from the input parameters.

## -parameters

### -param pInputDesc [in]

Type: <b>const <a href="/windows/desktop/api/d3d11/ns-d3d11-d3d11_video_decoder_desc">D3D11_VIDEO_DECODER_DESC</a>*</b>

A <a href="/windows/desktop/api/d3d11/ns-d3d11-d3d11_video_decoder_desc">D3D11_VIDEO_DECODER_DESC</a> object describing the decoding profile, the resolution, and format of the input stream.  This is the resolution and format to be downsampled.

### -param InputColorSpace [in]

Type: <b><a href="/windows/desktop/api/dxgicommon/ne-dxgicommon-dxgi_color_space_type">DXGI_COLOR_SPACE_TYPE</a></b>

A  <a href="/windows/desktop/api/dxgicommon/ne-dxgicommon-dxgi_color_space_type">DXGI_COLOR_SPACE_TYPE</a> value that specifies the colorspace of the reference frame data.

### -param pInputConfig [in]

Type: <b>const <a href="/windows/desktop/api/d3d11/ns-d3d11-d3d11_video_decoder_config">D3D11_VIDEO_DECODER_CONFIG</a>*</b>

The configuration data associated with the decode profile.

### -param pFrameRate [in]

Type: <b>const <a href="/windows/desktop/api/dxgicommon/ns-dxgicommon-dxgi_rational">DXGI_RATIONAL</a>*</b>

The frame rate of the video content. This is used by the driver to determine whether the video can be decoded in real-time.

### -param pRecommendedOutputDesc [out]

Type: <b><a href="/windows/desktop/api/d3d11_1/ns-d3d11_1-d3d11_video_sample_desc">D3D11_VIDEO_SAMPLE_DESC</a>*</b>

Pointer to a <a href="/windows/desktop/api/d3d11_1/ns-d3d11_1-d3d11_video_sample_desc">D3D11_VIDEO_SAMPLE_DESC</a> structure that the driver populates with the recommended output buffer parameters for a downsample operation. The driver will attempt to recommend parameters that can support real-time decoding. If it is unable to do so, the driver will recommend values that are as close to the real-time solution as possible.

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
</table>

## -remarks

You  should call <a href="/windows/desktop/api/d3d11_1/nf-d3d11_1-id3d11videodevice1-getvideodecodercaps">GetVideoDecoderCaps</a> to determine whether decoder downsampling is supported before checking support for a  specific configuration.

## -see-also

<a href="/windows/desktop/api/d3d11_1/nn-d3d11_1-id3d11videodevice1">ID3D11VideoDevice1</a>