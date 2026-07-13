---
UID: NF:d3d11_4.ID3D11VideoContext3.DecoderBeginFrame1
title: ID3D11VideoContext3::DecoderBeginFrame1
description: Starts a decoding operation to decode a video frame. (ID3D11VideoContext3::DecoderBeginFrame1)
tech.root: direct3d11
helpviewer_keywords: ["ID3D11VideoContext3::DecoderBeginFrame1"]
ms.date: 4/26/2019
ms.keywords: ID3D11VideoContext3::DecoderBeginFrame1
targetos: Windows
req.assembly: 
req.construct-type: function
req.ddi-compliance: 
req.dll: 
req.header: d3d11_4.h
req.idl: 
req.include-header: 
req.irql: 
req.kmdf-ver: 
req.lib: 
req.max-support: 
req.namespace: 
req.redist: 
req.target-min-winverclnt: Windows 10 Build 20348
req.target-min-winversvr: Windows 10 Build 20348
req.target-type: 
req.type-library: 
req.umdf-ver: 
req.unicode-ansi: 
f1_keywords:
 - ID3D11VideoContext3::DecoderBeginFrame1
 - d3d11_4/ID3D11VideoContext3::DecoderBeginFrame1
dev_langs:
 - c++
topic_type:
 - apiref
api_type:
 - COM
api_location:
 - d3d11_4.h
api_name:
 - ID3D11VideoContext3::DecoderBeginFrame1
---

## -description

Starts a decoding operation to decode a video frame.

## -parameters

### -param pDecoder

A pointer to the [ID3D11VideoDecoder](../d3d11/nn-d3d11-id3d11videodecoder.md) interface. To get this pointer, call [ID3D11VideoDevice::CreateVideoDecoder](../d3d11/nf-d3d11-id3d11videodevice-createvideodecoder.md)

### -param pView

A pointer to a [ID3D11VideoDecoderOutputView](../d3d11/nn-d3d11-id3d11videodecoderoutputview.md) interface. This interface describes the resource that will receive the decoded frame. To get this pointer, call [ID3D11VideoDevice::CreateVideoDecoderOutputView](../d3d11/nf-d3d11-id3d11videodevice-createvideodecoderoutputview.md
).

### -param ContentKeySize

The size of the content key that is specified in *pContentKey*. If *pContentKey* is NULL, set *ContentKeySize* to zero.

### -param pContentKey

An optional pointer to a content key that was used to encrypt the frame data. If no content key was used, set this parameter to NULL. If the caller provides a content key, the caller must use the session key to encrypt the content key.

### -param NumComponentHistograms

The number of components to record a histograms for.  Use [D3D11_FEATURE_VIDEO_DECODE_HISTOGRAM](ne-d3d11_4-d3d11_feature_video.md) to check for support.  Use zero when not recording histograms or when the feature is not supported.  Specifying fewer components than are in the format implies that those components do not have histogram recording enabled. The maximum number of components is defined as **D3D11_4_VIDEO_DECODER_MAX_HISTOGRAM_COMPONENTS**.

### -param pHistogramOffsets

An array of starting buffer offset locations within the *ppHistogramBuffers* parallel array.  Use [D3D11_VIDEO_DECODE_HISTOGRAM_COMPONENT](ne-d3d11_4-d3d11_video_decoder_histogram_component.md) to index the array.  If a component is not requested, specify an offset of zero.   The offsets must be 256-byte aligned.

### -param ppHistogramBuffers

An array of target buffers for hardware to write the components histogram.  Use [D3D11_VIDEO_DECODE_HISTOGRAM_COMPONENT](ne-d3d11_4-d3d11_video_decoder_histogram_component.md) to index the array.  Set this parameter to **nullptr** when the component histogram is disabled or unsupported

## -returns

Returns **S\_OK** if successful.

## -remarks

The following [D3D11_RESOURCE_MISC](../d3d11/ne-d3d11-d3d11_resource_misc_flag.md) flags are allowed when allocating resources for video decode histograms.

- D3D11_RESOURCE_MISC_SHARED
- D3D11_RESOURCE_MISC_DRAWINDIRECT_ARGS
- D3D11_RESOURCE_MISC_BUFFER_ALLOW_RAW_VIEWS
- D3D11_RESOURCE_MISC_BUFFER_STRUCTURED
- D3D11_RESOURCE_MISC_SHARED_KEYEDMUTEX
- D3D11_RESOURCE_MISC_SHARED_NTHANDLE
- D3D11_RESOURCE_MISC_RESTRICT_SHARED_RESOURCE
- D3D11_RESOURCE_MISC_RESTRICT_SHARED_RESOURCE_DRIVER

All other D3D11_RESOURCE_MISC flags are disallowed.

## -see-also
