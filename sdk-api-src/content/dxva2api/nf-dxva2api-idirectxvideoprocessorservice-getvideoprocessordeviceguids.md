---
UID: NF:dxva2api.IDirectXVideoProcessorService.GetVideoProcessorDeviceGuids
title: IDirectXVideoProcessorService::GetVideoProcessorDeviceGuids (dxva2api.h)
description: Gets an array of GUIDs which identify the video processors supported by the graphics hardware.
helpviewer_keywords: ["26b52407-7c75-4731-aff3-41376aa9ac3a","GetVideoProcessorDeviceGuids","GetVideoProcessorDeviceGuids method [Media Foundation]","GetVideoProcessorDeviceGuids method [Media Foundation]","IDirectXVideoProcessorService interface","IDirectXVideoProcessorService interface [Media Foundation]","GetVideoProcessorDeviceGuids method","IDirectXVideoProcessorService.GetVideoProcessorDeviceGuids","IDirectXVideoProcessorService::GetVideoProcessorDeviceGuids","dxva2api/IDirectXVideoProcessorService::GetVideoProcessorDeviceGuids","mf.idirectxvideoprocessorservice_getvideoprocessordeviceguids"]
old-location: mf\idirectxvideoprocessorservice_getvideoprocessordeviceguids.htm
tech.root: mf
ms.assetid: 26b52407-7c75-4731-aff3-41376aa9ac3a
ms.date: 12/05/2018
ms.keywords: 26b52407-7c75-4731-aff3-41376aa9ac3a, GetVideoProcessorDeviceGuids, GetVideoProcessorDeviceGuids method [Media Foundation], GetVideoProcessorDeviceGuids method [Media Foundation],IDirectXVideoProcessorService interface, IDirectXVideoProcessorService interface [Media Foundation],GetVideoProcessorDeviceGuids method, IDirectXVideoProcessorService.GetVideoProcessorDeviceGuids, IDirectXVideoProcessorService::GetVideoProcessorDeviceGuids, dxva2api/IDirectXVideoProcessorService::GetVideoProcessorDeviceGuids, mf.idirectxvideoprocessorservice_getvideoprocessordeviceguids
req.header: dxva2api.h
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IDirectXVideoProcessorService::GetVideoProcessorDeviceGuids
 - dxva2api/IDirectXVideoProcessorService::GetVideoProcessorDeviceGuids
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - dxva2api.h
api_name:
 - IDirectXVideoProcessorService.GetVideoProcessorDeviceGuids
---

# IDirectXVideoProcessorService::GetVideoProcessorDeviceGuids


## -description

Gets an array of GUIDs which identify the video processors supported by the graphics hardware.

## -parameters

### -param pVideoDesc [in]

Pointer to a <a href="/windows/desktop/api/dxva2api/ns-dxva2api-dxva2_videodesc">DXVA2_VideoDesc</a> structure that describes the video content.

### -param pCount [out]

Receives the number of GUIDs.

### -param pGuids [out]

Receives an array of GUIDs. The size of the array is retrieved in the <i>pCount</i> parameter. The method allocates the memory for the array. The caller must free the memory by calling <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree">CoTaskMemFree</a>.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

The following video processor GUIDs are predefined.

<table>
<tr>
<th>GUID</th>
<th>Description</th>
</tr>
<tr>
<td><b>DXVA2_VideoProcBobDevice</b></td>
<td>Bob deinterlace device. This device uses a "bob" algorithm to deinterlace the video. Bob algorithms create missing field lines by interpolating the lines in a single field.</td>
</tr>
<tr>
<td><b>DXVA2_VideoProcProgressiveDevice</b></td>
<td>Progressive video device. This device is available for progressive video, which does not require a deinterlace algorithm.</td>
</tr>
<tr>
<td><b>DXVA2_VideoProcSoftwareDevice</b></td>
<td>Reference (software) device.</td>
</tr>
</table>
 

The graphics device may define additional vendor-specific GUIDs. The driver provides the list of GUIDs in descending quality order. The mode with the highest quality is first in the list. To get the capabilities of each mode, call <a href="/windows/desktop/api/dxva2api/nf-dxva2api-idirectxvideoprocessorservice-getvideoprocessorcaps">IDirectXVideoProcessorService::GetVideoProcessorCaps</a> and pass in the GUID for the mode.


#### Examples


```cpp

    // Initialize the video descriptor.

    g_VideoDesc.SampleWidth                         = VIDEO_MAIN_WIDTH;
    g_VideoDesc.SampleHeight                        = VIDEO_MAIN_HEIGHT;
    g_VideoDesc.SampleFormat.VideoChromaSubsampling = DXVA2_VideoChromaSubsampling_MPEG2;
    g_VideoDesc.SampleFormat.NominalRange           = DXVA2_NominalRange_16_235;
    g_VideoDesc.SampleFormat.VideoTransferMatrix    = EX_COLOR_INFO[g_ExColorInfo][0];
    g_VideoDesc.SampleFormat.VideoLighting          = DXVA2_VideoLighting_dim;
    g_VideoDesc.SampleFormat.VideoPrimaries         = DXVA2_VideoPrimaries_BT709;
    g_VideoDesc.SampleFormat.VideoTransferFunction  = DXVA2_VideoTransFunc_709;
    g_VideoDesc.SampleFormat.SampleFormat           = DXVA2_SampleProgressiveFrame;
    g_VideoDesc.Format                              = VIDEO_MAIN_FORMAT;
    g_VideoDesc.InputSampleFreq.Numerator           = VIDEO_FPS;
    g_VideoDesc.InputSampleFreq.Denominator         = 1;
    g_VideoDesc.OutputFrameFreq.Numerator           = VIDEO_FPS;
    g_VideoDesc.OutputFrameFreq.Denominator         = 1;

    // Query the video processor GUID.

    UINT count;
    GUID* guids = NULL;

    hr = g_pDXVAVPS->GetVideoProcessorDeviceGuids(&g_VideoDesc, &count, &guids);

```

## -see-also

<a href="/windows/desktop/medfound/dxva-video-processing">DXVA Video Processing</a>



<a href="/windows/desktop/api/dxva2api/nn-dxva2api-idirectxvideoprocessorservice">IDirectXVideoProcessorService</a>