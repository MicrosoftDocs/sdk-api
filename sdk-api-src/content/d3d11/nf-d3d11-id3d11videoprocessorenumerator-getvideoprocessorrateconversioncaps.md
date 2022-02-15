---
UID: NF:d3d11.ID3D11VideoProcessorEnumerator.GetVideoProcessorRateConversionCaps
title: ID3D11VideoProcessorEnumerator::GetVideoProcessorRateConversionCaps (d3d11.h)
description: Returns a group of video processor capabilities that are associated with frame-rate conversion, including deinterlacing and inverse telecine.
helpviewer_keywords: ["GetVideoProcessorRateConversionCaps","GetVideoProcessorRateConversionCaps method [Media Foundation]","GetVideoProcessorRateConversionCaps method [Media Foundation]","ID3D11VideoProcessorEnumerator interface","ID3D11VideoProcessorEnumerator interface [Media Foundation]","GetVideoProcessorRateConversionCaps method","ID3D11VideoProcessorEnumerator.GetVideoProcessorRateConversionCaps","ID3D11VideoProcessorEnumerator::GetVideoProcessorRateConversionCaps","d3d11/ID3D11VideoProcessorEnumerator::GetVideoProcessorRateConversionCaps","mf.id3d11videoprocessorenumerator_getvideoprocessorrateconversioncaps"]
old-location: mf\id3d11videoprocessorenumerator_getvideoprocessorrateconversioncaps.htm
tech.root: mf
ms.assetid: 2DB74CB9-C6B3-477A-9EF9-6E2EC1DE37D6
ms.date: 12/05/2018
ms.keywords: GetVideoProcessorRateConversionCaps, GetVideoProcessorRateConversionCaps method [Media Foundation], GetVideoProcessorRateConversionCaps method [Media Foundation],ID3D11VideoProcessorEnumerator interface, ID3D11VideoProcessorEnumerator interface [Media Foundation],GetVideoProcessorRateConversionCaps method, ID3D11VideoProcessorEnumerator.GetVideoProcessorRateConversionCaps, ID3D11VideoProcessorEnumerator::GetVideoProcessorRateConversionCaps, d3d11/ID3D11VideoProcessorEnumerator::GetVideoProcessorRateConversionCaps, mf.id3d11videoprocessorenumerator_getvideoprocessorrateconversioncaps
req.header: d3d11.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps \| UWP apps]
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
 - ID3D11VideoProcessorEnumerator::GetVideoProcessorRateConversionCaps
 - d3d11/ID3D11VideoProcessorEnumerator::GetVideoProcessorRateConversionCaps
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - d3d11.h
api_name:
 - ID3D11VideoProcessorEnumerator.GetVideoProcessorRateConversionCaps
---

# ID3D11VideoProcessorEnumerator::GetVideoProcessorRateConversionCaps


## -description

Returns a group of video processor capabilities that are associated with frame-rate conversion, including deinterlacing and inverse telecine.

## -parameters

### -param TypeIndex [in]

The zero-based index of the group to retrieve. To get the maximum index, call <a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11videoprocessorenumerator-getvideoprocessorcaps">ID3D11VideoProcessorEnumerator::GetVideoProcessorCaps</a> and check the <b>RateConversionCapsCount</b> member of the <a href="/windows/desktop/api/d3d11/ns-d3d11-d3d11_video_processor_caps">D3D11_VIDEO_PROCESSOR_CAPS</a> structure.

### -param pCaps [out]

A pointer to a <a href="/windows/desktop/api/d3d11/ns-d3d11-d3d11_video_processor_rate_conversion_caps">D3D11_VIDEO_PROCESSOR_RATE_CONVERSION_CAPS</a> structure that receives the frame-rate conversion capabilities.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

The capabilities defined in the <a href="/windows/desktop/api/d3d11/ns-d3d11-d3d11_video_processor_rate_conversion_caps">D3D11_VIDEO_PROCESSOR_RATE_CONVERSION_CAPS</a> structure are interdependent. Therefore, the driver can support multiple, distinct groups of these capabilities.

## -see-also

<a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11videoprocessorenumerator">ID3D11VideoProcessorEnumerator</a>