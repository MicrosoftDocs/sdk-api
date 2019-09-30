---
UID: NN:evr.IMFVideoDisplayControl
title: IMFVideoDisplayControl (evr.h)
author: windows-sdk-content
description: Controls how the Enhanced Video Renderer (EVR) displays video.
old-location: mf\imfvideodisplaycontrol.htm
tech.root: medfound
ms.assetid: db9b4663-9240-484f-8c47-cb1f5daa238d
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IMFVideoDisplayControl, IMFVideoDisplayControl interface [Media Foundation], IMFVideoDisplayControl interface [Media Foundation],described, db9b4663-9240-484f-8c47-cb1f5daa238d, evr/IMFVideoDisplayControl, mf.imfvideodisplaycontrol
ms.topic: interface
f1_keywords: 
 - "evr/IMFVideoDisplayControl"
req.header: evr.h
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - strmiids.lib
 - strmiids.dll
api_name:
 - IMFVideoDisplayControl
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMFVideoDisplayControl interface


## -description


Controls how the <a href="https://docs.microsoft.com/windows/desktop/medfound/enhanced-video-renderer">Enhanced Video Renderer</a> (EVR) displays video.

The EVR presenter implements this interface. To get a pointer to the interface, call <a href="https://docs.microsoft.com/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice">IMFGetService::GetService</a>. The service identifier is GUID MR_VIDEO_RENDER_SERVICE. Call <b>GetService</b> on any of the following objects:
<ul>
<li>The <a href="https://docs.microsoft.com/windows/desktop/medfound/media-session">Media Session</a>, if the topology contains an instance of the EVR.
            </li>
<li>The EVR media sink.
            </li>
<li>The DirectShow EVR filter.
            </li>
<li>The EVR presenter.
            </li>
</ul>If you implement a custom presenter for the EVR, the presenter can optionally expose this interface as a service.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMFVideoDisplayControl</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IMFVideoDisplayControl</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMFVideoDisplayControl</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/evr/nf-evr-imfvideodisplaycontrol-getaspectratiomode">GetAspectRatioMode</a>
</td>
<td align="left" width="63%">
Queries how the EVR handles the aspect ratio of the source video.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/evr/nf-evr-imfvideodisplaycontrol-getbordercolor">GetBorderColor</a>
</td>
<td align="left" width="63%">
Retrieves the border color for the video.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/evr/nf-evr-imfvideodisplaycontrol-getcurrentimage">GetCurrentImage</a>
</td>
<td align="left" width="63%">
Retrieves a copy of the current image being displayed by the video renderer.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/evr/nf-evr-imfvideodisplaycontrol-getfullscreen">GetFullscreen</a>
</td>
<td align="left" width="63%">
Queries whether the EVR is currently in full-screen mode.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/evr/nf-evr-imfvideodisplaycontrol-getidealvideosize">GetIdealVideoSize</a>
</td>
<td align="left" width="63%">
Gets the range of sizes that the EVR can display without significantly degrading performance or image quality.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/evr/nf-evr-imfvideodisplaycontrol-getnativevideosize">GetNativeVideoSize</a>
</td>
<td align="left" width="63%">
Gets the size and aspect ratio of the video, prior to any stretching by the video renderer.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/evr/nf-evr-imfvideodisplaycontrol-getrenderingprefs">GetRenderingPrefs</a>
</td>
<td align="left" width="63%">
Gets various video rendering settings.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/evr/nf-evr-imfvideodisplaycontrol-getvideoposition">GetVideoPosition</a>
</td>
<td align="left" width="63%">
Gets the source and destination rectangles for the video.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/evr/nf-evr-imfvideodisplaycontrol-getvideowindow">GetVideoWindow</a>
</td>
<td align="left" width="63%">
Gets the clipping window for the video.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/evr/nf-evr-imfvideodisplaycontrol-repaintvideo">RepaintVideo</a>
</td>
<td align="left" width="63%">
Gets the current video frame.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/evr/nf-evr-imfvideodisplaycontrol-setaspectratiomode">SetAspectRatioMode</a>
</td>
<td align="left" width="63%">
Specifies how the EVR handles the aspect ratio of the source video.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/evr/nf-evr-imfvideodisplaycontrol-setbordercolor">SetBorderColor</a>
</td>
<td align="left" width="63%">
Sets the border color for the video.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/evr/nf-evr-imfvideodisplaycontrol-setfullscreen">SetFullscreen</a>
</td>
<td align="left" width="63%">
Sets or unsets full-screen rendering mode.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/evr/nf-evr-imfvideodisplaycontrol-setrenderingprefs">SetRenderingPrefs</a>
</td>
<td align="left" width="63%">
Sets various preferences related to video rendering.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/evr/nf-evr-imfvideodisplaycontrol-setvideoposition">SetVideoPosition</a>
</td>
<td align="left" width="63%">
Sets the source and destination rectangles for the video.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/evr/nf-evr-imfvideodisplaycontrol-setvideowindow">SetVideoWindow</a>
</td>
<td align="left" width="63%">
Sets the clipping window for the video.
        

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/medfound/enhanced-video-renderer">Enhanced Video Renderer</a>



<a href="https://docs.microsoft.com/windows/desktop/medfound/how-to-play-unprotected-media-files">How to Play Media Files with Media Foundation</a>



<a href="https://docs.microsoft.com/windows/desktop/medfound/media-foundation-interfaces">Media Foundation Interfaces</a>



<a href="https://docs.microsoft.com/windows/desktop/medfound/using-the-video-display-controls">Using the Video Display Controls</a>
 

 

