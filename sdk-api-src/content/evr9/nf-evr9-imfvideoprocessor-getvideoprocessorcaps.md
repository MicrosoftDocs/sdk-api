---
UID: NF:evr9.IMFVideoProcessor.GetVideoProcessorCaps
title: IMFVideoProcessor::GetVideoProcessorCaps (evr9.h)
description: Retrieves the capabilities of a video processor mode.
helpviewer_keywords: ["9a02aed2-8225-4416-ae54-7ed51c67a149","GetVideoProcessorCaps","GetVideoProcessorCaps method [Media Foundation]","GetVideoProcessorCaps method [Media Foundation]","IMFVideoProcessor interface","IMFVideoProcessor interface [Media Foundation]","GetVideoProcessorCaps method","IMFVideoProcessor.GetVideoProcessorCaps","IMFVideoProcessor::GetVideoProcessorCaps","evr9/IMFVideoProcessor::GetVideoProcessorCaps","mf.imfvideoprocessor_getvideoprocessorcaps"]
old-location: mf\imfvideoprocessor_getvideoprocessorcaps.htm
tech.root: mf
ms.assetid: 9a02aed2-8225-4416-ae54-7ed51c67a149
ms.date: 12/05/2018
ms.keywords: 9a02aed2-8225-4416-ae54-7ed51c67a149, GetVideoProcessorCaps, GetVideoProcessorCaps method [Media Foundation], GetVideoProcessorCaps method [Media Foundation],IMFVideoProcessor interface, IMFVideoProcessor interface [Media Foundation],GetVideoProcessorCaps method, IMFVideoProcessor.GetVideoProcessorCaps, IMFVideoProcessor::GetVideoProcessorCaps, evr9/IMFVideoProcessor::GetVideoProcessorCaps, mf.imfvideoprocessor_getvideoprocessorcaps
req.header: evr9.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Strmiids.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IMFVideoProcessor::GetVideoProcessorCaps
 - evr9/IMFVideoProcessor::GetVideoProcessorCaps
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - strmiids.lib
 - strmiids.dll
api_name:
 - IMFVideoProcessor.GetVideoProcessorCaps
---

# IMFVideoProcessor::GetVideoProcessorCaps


## -description

Retrieves the capabilities of a video processor mode.

## -parameters

### -param lpVideoProcessorMode [in]

Pointer to a GUID that identifies the video processor mode. To get a list of available modes, call <a href="/windows/desktop/api/evr9/nf-evr9-imfvideoprocessor-getavailablevideoprocessormodes">IMFVideoProcessor::GetAvailableVideoProcessorModes</a>.

### -param lpVideoProcessorCaps [out]

Pointer to a <a href="/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videoprocessorcaps">DXVA2_VideoProcessorCaps</a> structure that receives the capabilities.

## -returns

The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MF_E_TRANSFORM_TYPE_NOT_SET</b></dt>
</dl>
</td>
<td width="60%">
The media type for the reference stream is not set.

</td>
</tr>
</table>

## -remarks

Before calling this method, you must set the media type for the reference stream.

## -see-also

<a href="/windows/desktop/medfound/enhanced-video-renderer">Enhanced Video Renderer</a>



<a href="/windows/desktop/api/evr9/nn-evr9-imfvideoprocessor">IMFVideoProcessor</a>