---
UID: NN:dxvahd.IDXVAHD_VideoProcessor
title: IDXVAHD_VideoProcessor (dxvahd.h)
author: windows-sdk-content
description: Represents a Microsoft DirectX Video Acceleration High Definition (DXVA-HD) video processor.
old-location: mf\idxvahd_videoprocessor.htm
tech.root: medfound
ms.assetid: cbfacff5-1cbb-4296-8242-c06b43fc95af
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IDXVAHD_VideoProcessor, IDXVAHD_VideoProcessor interface [Media Foundation], IDXVAHD_VideoProcessor interface [Media Foundation],described, dxvahd/IDXVAHD_VideoProcessor, mf.idxvahd_videoprocessor
ms.topic: interface
f1_keywords: ["dxvahd/IDXVAHD_VideoProcessor"]
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - dxvahd.h
api_name:
 - IDXVAHD_VideoProcessor
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDXVAHD_VideoProcessor interface


## -description


Represents a Microsoft DirectX Video Acceleration High Definition (DXVA-HD) video processor. 

To get a pointer to this interface, call the <a href="https://docs.microsoft.com/windows/desktop/api/dxvahd/nf-dxvahd-idxvahd_device-createvideoprocessor">IDXVAHD_Device::CreateVideoProcessor</a> method.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDXVAHD_VideoProcessor</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IDXVAHD_VideoProcessor</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IDXVAHD_VideoProcessor</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dxvahd/nf-dxvahd-idxvahd_videoprocessor-getvideoprocessbltstate">GetVideoProcessBltState</a>
</td>
<td align="left" width="63%">
Gets the value of a state parameter for a DXVA-HD blit operation.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dxvahd/nf-dxvahd-idxvahd_videoprocessor-getvideoprocessstreamstate">GetVideoProcessStreamState</a>
</td>
<td align="left" width="63%">
Gets the value of a state parameter for a DXVA-HD input stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dxvahd/nf-dxvahd-idxvahd_videoprocessor-setvideoprocessbltstate">SetVideoProcessBltState</a>
</td>
<td align="left" width="63%">
Sets a state parameter for a DXVA-HD blit operation.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dxvahd/nf-dxvahd-idxvahd_videoprocessor-setvideoprocessstreamstate">SetVideoProcessStreamState</a>
</td>
<td align="left" width="63%">
Sets a state parameter for a DXVA-HD input stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dxvahd/nf-dxvahd-idxvahd_videoprocessor-videoprocessblthd">VideoProcessBltHD</a>
</td>
<td align="left" width="63%">
Performs a video processing blit on one or more input samples and writes the result to a Microsoft Direct3D surface.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/medfound/dxva-hd">DXVA-HD</a>



<a href="https://docs.microsoft.com/windows/desktop/medfound/direct3d-video-interfaces">Direct3D Video Interfaces</a>



<a href="https://docs.microsoft.com/windows/desktop/medfound/media-foundation-interfaces">Media Foundation Interfaces</a>
 

 

