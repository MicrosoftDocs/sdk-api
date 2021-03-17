---
UID: NF:d3d11_1.ID3D11VideoDevice1.CheckVideoDecoderDownsampling
title: ID3D11VideoDevice1::CheckVideoDecoderDownsampling (d3d11_1.h)
description: Indicates whether the video decoder supports downsampling with the specified input format, and whether real-time downsampling is supported.
helpviewer_keywords: ["CheckVideoDecoderDownsampling","CheckVideoDecoderDownsampling method [Media Foundation]","CheckVideoDecoderDownsampling method [Media Foundation]","ID3D11VideoDevice1 interface","ID3D11VideoDevice1 interface [Media Foundation]","CheckVideoDecoderDownsampling method","ID3D11VideoDevice1.CheckVideoDecoderDownsampling","ID3D11VideoDevice1::CheckVideoDecoderDownsampling","d3d11_1/ID3D11VideoDevice1::CheckVideoDecoderDownsampling","mf.id3d11videodevice1_checkvideodecoderdownsampling"]
old-location: mf\id3d11videodevice1_checkvideodecoderdownsampling.htm
tech.root: mf
ms.assetid: EB05C2F7-AC7A-42BD-A661-5101641A920C
ms.date: 12/05/2018
ms.keywords: CheckVideoDecoderDownsampling, CheckVideoDecoderDownsampling method [Media Foundation], CheckVideoDecoderDownsampling method [Media Foundation],ID3D11VideoDevice1 interface, ID3D11VideoDevice1 interface [Media Foundation],CheckVideoDecoderDownsampling method, ID3D11VideoDevice1.CheckVideoDecoderDownsampling, ID3D11VideoDevice1::CheckVideoDecoderDownsampling, d3d11_1/ID3D11VideoDevice1::CheckVideoDecoderDownsampling, mf.id3d11videodevice1_checkvideodecoderdownsampling
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
 - ID3D11VideoDevice1::CheckVideoDecoderDownsampling
 - d3d11_1/ID3D11VideoDevice1::CheckVideoDecoderDownsampling
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
 - ID3D11VideoDevice1.CheckVideoDecoderDownsampling
---

# ID3D11VideoDevice1::CheckVideoDecoderDownsampling


## -description

Indicates whether the video decoder supports downsampling with the specified input format, and whether real-time downsampling is supported.

## -parameters

### -param pInputDesc [in]

Type: <b>const <a href="/windows/desktop/api/d3d11/ns-d3d11-d3d11_video_decoder_desc">D3D11_VIDEO_DECODER_DESC</a>*</b>

An object describing the decoding profile, the resolution, and format of the input stream.  This is the resolution and format to be downsampled.

### -param InputColorSpace [in]

Type: <b><a href="/windows/desktop/api/dxgicommon/ne-dxgicommon-dxgi_color_space_type">DXGI_COLOR_SPACE_TYPE</a></b>

A  <a href="/windows/desktop/api/dxgicommon/ne-dxgicommon-dxgi_color_space_type">DXGI_COLOR_SPACE_TYPE</a> value that specifies the colorspace of the reference frame data.

### -param pInputConfig [in]

Type: <b>const <a href="/windows/desktop/api/d3d11/ns-d3d11-d3d11_video_decoder_config">D3D11_VIDEO_DECODER_CONFIG</a>*</b>

The configuration data associated with the decode profile.

### -param pFrameRate [in]

Type: <b>const <a href="/windows/desktop/api/dxgicommon/ns-dxgicommon-dxgi_rational">DXGI_RATIONAL</a>*</b>

The frame rate of the video content. This is used by the driver to determine whether the video can be decoded in real-time.

### -param pOutputDesc [in]

Type: <b>const <a href="/windows/desktop/api/d3d11_1/ns-d3d11_1-d3d11_video_sample_desc">D3D11_VIDEO_SAMPLE_DESC</a>*</b>

An object describing the resolution, format, and colorspace of the output frames.  This is the destination resolution and format of the downsample operation.

### -param pSupported [out]

Type: <b>BOOL*</b>

Pointer to a boolean value set by the driver that indicates if downsampling is supported with the specified input data. True if the driver supports the requested downsampling;  otherwise, false.

### -param pRealTimeHint [out]

Type: <b>BOOL*</b>

Pointer to a boolean value set by the driver that indicates if real-time decoding is supported with the specified input data. True if the driver supports the requested real-time decoding;  otherwise, false. Note that the returned value is based on the current configuration of the video decoder and does not guarantee that real-time decoding will be supported for future downsampling operations.

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