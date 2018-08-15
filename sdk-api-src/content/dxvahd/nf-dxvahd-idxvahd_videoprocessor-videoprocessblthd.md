---
UID: NF:dxvahd.IDXVAHD_VideoProcessor.VideoProcessBltHD
title: IDXVAHD_VideoProcessor::VideoProcessBltHD
author: windows-sdk-content
description: Performs a video processing blit on one or more input samples and writes the result to a Microsoft Direct3D surface.
old-location: mf\idxvahd_videoprocessor_videoprocessblthd.htm
old-project: medfound
ms.assetid: 59c4deee-4ef2-4aba-8188-989904055e70
ms.author: windowssdkdev
ms.date: 08/07/2018
ms.keywords: IDXVAHD_VideoProcessor interface [Media Foundation],VideoProcessBltHD method, IDXVAHD_VideoProcessor.VideoProcessBltHD, IDXVAHD_VideoProcessor::VideoProcessBltHD, VideoProcessBltHD, VideoProcessBltHD method [Media Foundation], VideoProcessBltHD method [Media Foundation],IDXVAHD_VideoProcessor interface, dxvahd/IDXVAHD_VideoProcessor::VideoProcessBltHD, mf.idxvahd_videoprocessor_videoprocessblthd
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: dxvahd.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: DXVAHD_SURFACE_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - dxvahd.h
api_name:
 - IDXVAHD_VideoProcessor.VideoProcessBltHD
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IDXVAHD_VideoProcessor::VideoProcessBltHD


## -description


Performs a video processing blit on one or more input samples and writes the result to a Microsoft Direct3D surface.


## -parameters




### -param pOutputSurface [in]

A pointer to the <b>IDirect3DSurface9</b> interface of a Direct3D surface. The output of the video processing operation will be written to this surface. The following surface types can be used:

<ul>
<li>A video surface of type <b>DXVAHD_SURFACE_TYPE_VIDEO_OUTPUT</b>. See <a href="https://msdn.microsoft.com/c467a077-104c-443d-896b-d69441aa5160">IDXVAHD_Device::CreateVideoSurface</a>. </li>
<li>A render-target surface or texture surface created with D3DUSAGE_RENDERTARGET usage.</li>
<li>A swap chain.</li>
<li>A swap chain with overlay support (<b>D3DSWAPEFFECT_OVERLAY</b>).</li>
</ul>

### -param OutputFrame [in]

Frame number of the output video frame, indexed from zero.


### -param StreamCount [in]

Number of input streams to process. 


### -param pStreams [in]

Pointer to an array of <a href="https://msdn.microsoft.com/95d74c87-5884-4004-926f-108e9bbb012d">DXVAHD_STREAM_DATA</a> structures that contain information about the input streams. The caller allocates the array and fills in each structure. The number of elements in the array is given in the <i>StreamCount</i> parameter.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The maximum value of <i>StreamCount</i> is given in the <b>MaxStreamStates</b> member of the <a href="https://msdn.microsoft.com/340669d4-2a84-4030-83c3-a61469fdfd61">DXVAHD_VPDEVCAPS</a> structure. The maximum numbr of streams that can be enabled at one time is given in the <b>MaxInputStreams</b> member of that structure.




## -see-also




<a href="https://msdn.microsoft.com/38ebec28-c4fc-4e72-ac87-1e41707d1908">DXVA-HD</a>



<a href="https://msdn.microsoft.com/cbfacff5-1cbb-4296-8242-c06b43fc95af">IDXVAHD_VideoProcessor</a>
 

 

