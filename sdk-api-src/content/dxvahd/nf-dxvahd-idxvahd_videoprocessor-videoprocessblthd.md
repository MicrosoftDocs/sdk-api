---
UID: NF:dxvahd.IDXVAHD_VideoProcessor.VideoProcessBltHD
title: IDXVAHD_VideoProcessor::VideoProcessBltHD (dxvahd.h)
description: Performs a video processing blit on one or more input samples and writes the result to a Microsoft Direct3D surface.
helpviewer_keywords: ["IDXVAHD_VideoProcessor interface [Media Foundation]","VideoProcessBltHD method","IDXVAHD_VideoProcessor.VideoProcessBltHD","IDXVAHD_VideoProcessor::VideoProcessBltHD","VideoProcessBltHD","VideoProcessBltHD method [Media Foundation]","VideoProcessBltHD method [Media Foundation]","IDXVAHD_VideoProcessor interface","dxvahd/IDXVAHD_VideoProcessor::VideoProcessBltHD","mf.idxvahd_videoprocessor_videoprocessblthd"]
old-location: mf\idxvahd_videoprocessor_videoprocessblthd.htm
tech.root: mf
ms.assetid: 59c4deee-4ef2-4aba-8188-989904055e70
ms.date: 12/05/2018
ms.keywords: IDXVAHD_VideoProcessor interface [Media Foundation],VideoProcessBltHD method, IDXVAHD_VideoProcessor.VideoProcessBltHD, IDXVAHD_VideoProcessor::VideoProcessBltHD, VideoProcessBltHD, VideoProcessBltHD method [Media Foundation], VideoProcessBltHD method [Media Foundation],IDXVAHD_VideoProcessor interface, dxvahd/IDXVAHD_VideoProcessor::VideoProcessBltHD, mf.idxvahd_videoprocessor_videoprocessblthd
req.header: dxvahd.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
 - IDXVAHD_VideoProcessor::VideoProcessBltHD
 - dxvahd/IDXVAHD_VideoProcessor::VideoProcessBltHD
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - dxvahd.h
api_name:
 - IDXVAHD_VideoProcessor.VideoProcessBltHD
---

# IDXVAHD_VideoProcessor::VideoProcessBltHD


## -description

Performs a video processing blit on one or more input samples and writes the result to a Microsoft Direct3D surface.

## -parameters

### -param pOutputSurface [in]

A pointer to the <b>IDirect3DSurface9</b> interface of a Direct3D surface. The output of the video processing operation will be written to this surface. The following surface types can be used:

<ul>
<li>A video surface of type <b>DXVAHD_SURFACE_TYPE_VIDEO_OUTPUT</b>. See <a href="/windows/desktop/api/dxvahd/nf-dxvahd-idxvahd_device-createvideosurface">IDXVAHD_Device::CreateVideoSurface</a>. </li>
<li>A render-target surface or texture surface created with D3DUSAGE_RENDERTARGET usage.</li>
<li>A swap chain.</li>
<li>A swap chain with overlay support (<b>D3DSWAPEFFECT_OVERLAY</b>).</li>
</ul>

### -param OutputFrame [in]

Frame number of the output video frame, indexed from zero.

### -param StreamCount [in]

Number of input streams to process.

### -param pStreams [in]

Pointer to an array of <a href="/windows/desktop/api/dxvahd/ns-dxvahd-dxvahd_stream_data">DXVAHD_STREAM_DATA</a> structures that contain information about the input streams. The caller allocates the array and fills in each structure. The number of elements in the array is given in the <i>StreamCount</i> parameter.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

The maximum value of <i>StreamCount</i> is given in the <b>MaxStreamStates</b> member of the <a href="/windows/desktop/api/dxvahd/ns-dxvahd-dxvahd_vpdevcaps">DXVAHD_VPDEVCAPS</a> structure. The maximum number of streams that can be enabled at one time is given in the <b>MaxInputStreams</b> member of that structure.

## -see-also

<a href="/windows/desktop/medfound/dxva-hd">DXVA-HD</a>



<a href="/windows/desktop/api/dxvahd/nn-dxvahd-idxvahd_videoprocessor">IDXVAHD_VideoProcessor</a>