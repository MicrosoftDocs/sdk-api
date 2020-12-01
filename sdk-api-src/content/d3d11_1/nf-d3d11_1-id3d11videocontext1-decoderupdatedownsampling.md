---
UID: NF:d3d11_1.ID3D11VideoContext1.DecoderUpdateDownsampling
title: ID3D11VideoContext1::DecoderUpdateDownsampling (d3d11_1.h)
description: Updates the decoder downsampling parameters.
helpviewer_keywords: ["DecoderUpdateDownsampling","DecoderUpdateDownsampling method [Media Foundation]","DecoderUpdateDownsampling method [Media Foundation]","ID3D11VideoContext1 interface","ID3D11VideoContext1 interface [Media Foundation]","DecoderUpdateDownsampling method","ID3D11VideoContext1.DecoderUpdateDownsampling","ID3D11VideoContext1::DecoderUpdateDownsampling","d3d11_1/ID3D11VideoContext1::DecoderUpdateDownsampling","mf.id3d11videocontext1_decoderupdatedownsampling"]
old-location: mf\id3d11videocontext1_decoderupdatedownsampling.htm
tech.root: mf
ms.assetid: A55D652B-9295-42E4-9A83-CAC467BEE68E
ms.date: 12/05/2018
ms.keywords: DecoderUpdateDownsampling, DecoderUpdateDownsampling method [Media Foundation], DecoderUpdateDownsampling method [Media Foundation],ID3D11VideoContext1 interface, ID3D11VideoContext1 interface [Media Foundation],DecoderUpdateDownsampling method, ID3D11VideoContext1.DecoderUpdateDownsampling, ID3D11VideoContext1::DecoderUpdateDownsampling, d3d11_1/ID3D11VideoContext1::DecoderUpdateDownsampling, mf.id3d11videocontext1_decoderupdatedownsampling
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
 - ID3D11VideoContext1::DecoderUpdateDownsampling
 - d3d11_1/ID3D11VideoContext1::DecoderUpdateDownsampling
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
 - ID3D11VideoContext1.DecoderUpdateDownsampling
---

# ID3D11VideoContext1::DecoderUpdateDownsampling


## -description

Updates the decoder downsampling parameters.

## -parameters

### -param pDecoder [in]

Type: <b>ID3D11VideoDecoder*</b>

A pointer to the <a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11videodecoder">ID3D11VideoDecoder</a> interface.

### -param pOutputDesc [in]

Type: <b>const <a href="/windows/desktop/api/d3d11_1/ns-d3d11_1-d3d11_video_sample_desc">D3D11_VIDEO_SAMPLE_DESC</a>*</b>

The resolution, format, and colorspace of the output/display frames.  This is the destination resolution and format of the downsample operation.

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

This method can only be called after decode downsampling is enabled by calling <a href="/windows/desktop/api/d3d11_1/nf-d3d11_1-id3d11videocontext1-decoderenabledownsampling">DecoderEnableDownsampling</a>. This method is only supported if the <a href="/windows/desktop/api/d3d11_1/ne-d3d11_1-d3d11_video_decoder_caps">D3D11_VIDEO_DECODER_CAPS_DOWNSAMPLE_DYNAMIC</a> capability is reported.

## -see-also

<a href="/windows/desktop/api/d3d11_1/nn-d3d11_1-id3d11videocontext1">ID3D11VideoContext1</a>