---
UID: NF:d3d11.ID3D11VideoProcessorEnumerator.GetVideoProcessorCustomRate
title: ID3D11VideoProcessorEnumerator::GetVideoProcessorCustomRate (d3d11.h)
description: Gets a list of custom frame rates that a video processor supports.
helpviewer_keywords: ["GetVideoProcessorCustomRate","GetVideoProcessorCustomRate method [Media Foundation]","GetVideoProcessorCustomRate method [Media Foundation]","ID3D11VideoProcessorEnumerator interface","ID3D11VideoProcessorEnumerator interface [Media Foundation]","GetVideoProcessorCustomRate method","ID3D11VideoProcessorEnumerator.GetVideoProcessorCustomRate","ID3D11VideoProcessorEnumerator::GetVideoProcessorCustomRate","d3d11/ID3D11VideoProcessorEnumerator::GetVideoProcessorCustomRate","mf.id3d11videoprocessorenumerator_getvideoprocessorcustomrate"]
old-location: mf\id3d11videoprocessorenumerator_getvideoprocessorcustomrate.htm
tech.root: mf
ms.assetid: 0FA868E6-B0FB-433B-A183-72DDE39B207E
ms.date: 12/05/2018
ms.keywords: GetVideoProcessorCustomRate, GetVideoProcessorCustomRate method [Media Foundation], GetVideoProcessorCustomRate method [Media Foundation],ID3D11VideoProcessorEnumerator interface, ID3D11VideoProcessorEnumerator interface [Media Foundation],GetVideoProcessorCustomRate method, ID3D11VideoProcessorEnumerator.GetVideoProcessorCustomRate, ID3D11VideoProcessorEnumerator::GetVideoProcessorCustomRate, d3d11/ID3D11VideoProcessorEnumerator::GetVideoProcessorCustomRate, mf.id3d11videoprocessorenumerator_getvideoprocessorcustomrate
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
 - ID3D11VideoProcessorEnumerator::GetVideoProcessorCustomRate
 - d3d11/ID3D11VideoProcessorEnumerator::GetVideoProcessorCustomRate
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
 - ID3D11VideoProcessorEnumerator.GetVideoProcessorCustomRate
---

# ID3D11VideoProcessorEnumerator::GetVideoProcessorCustomRate


## -description

Gets a list of custom frame rates that a video processor supports.

## -parameters

### -param TypeIndex [in]

The zero-based index of the frame-rate capability group. To get the maxmum index, call <a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11videoprocessorenumerator-getvideoprocessorcaps">ID3D11VideoProcessorEnumerator::GetVideoProcessorCaps </a> and check the <b>RateConversionCapsCount</b> member of the <a href="/windows/desktop/api/d3d11/ns-d3d11-d3d11_video_processor_caps">D3D11_VIDEO_PROCESSOR_CAPS</a> structure.

### -param CustomRateIndex [in]

The zero-based index of the custom rate to retrieve. To get the maximum index, call <a href="/windows/desktop/api/d3d11/nf-d3d11-id3d11videoprocessorenumerator-getvideoprocessorrateconversioncaps">ID3D11VideoProcessorEnumerator::GetVideoProcessorRateConversionCaps</a> and check the <b>CustomRateCount</b> member of the <a href="/windows/desktop/api/d3d11/ns-d3d11-d3d11_video_processor_rate_conversion_caps">D3D11_VIDEO_PROCESSOR_RATE_CONVERSION_CAPS</a> structure.

This index value is always relative to the capability group specified in the <i>TypeIndex</i> parameter.

### -param pRate [out]

A pointer to a <a href="/windows/desktop/api/d3d11/ns-d3d11-d3d11_video_processor_custom_rate">D3D11_VIDEO_PROCESSOR_CUSTOM_RATE</a> structure that receives the custom rate.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/d3d11/nn-d3d11-id3d11videoprocessorenumerator">ID3D11VideoProcessorEnumerator</a>