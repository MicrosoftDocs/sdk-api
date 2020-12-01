---
UID: NN:evr9.IMFVideoProcessor
title: IMFVideoProcessor (evr9.h)
description: Controls video processing in the Enhanced Video Renderer (EVR).
helpviewer_keywords: ["0a63c4f8-eb32-4f0c-b69b-0c16243f2f21","IMFVideoProcessor","IMFVideoProcessor interface [Media Foundation]","IMFVideoProcessor interface [Media Foundation]","described","evr9/IMFVideoProcessor","mf.imfvideoprocessor"]
old-location: mf\imfvideoprocessor.htm
tech.root: mf
ms.assetid: 0a63c4f8-eb32-4f0c-b69b-0c16243f2f21
ms.date: 12/05/2018
ms.keywords: 0a63c4f8-eb32-4f0c-b69b-0c16243f2f21, IMFVideoProcessor, IMFVideoProcessor interface [Media Foundation], IMFVideoProcessor interface [Media Foundation],described, evr9/IMFVideoProcessor, mf.imfvideoprocessor
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
 - IMFVideoProcessor
 - evr9/IMFVideoProcessor
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
 - IMFVideoProcessor
---

# IMFVideoProcessor interface


## -description

Controls video processing in the <a href="/windows/desktop/medfound/enhanced-video-renderer">Enhanced Video Renderer</a> (EVR). The operations controlled through this interface include color adjustment (ProcAmp), noise filters, and detail filters.

The EVR mixer implements this interface. To get a pointer to the interface, call <a href="/windows/desktop/api/mfidl/nf-mfidl-imfgetservice-getservice">IMFGetService::GetService</a>. The service identifier is GUID MR_VIDEO_MIXER_SERVICE. Call <b>GetService</b> on any of the following objects:
<ul>
<li>The media sesson (if the topology contains an instance of the EVR).
            </li>
<li>The EVR media sink.
            </li>
<li>The DirectShow EVR filter.
            </li>
<li>The EVR mixer.
            </li>
</ul>If you implement a custom mixer for the EVR, the mixer can optionally expose this interface as a service.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMFVideoProcessor</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IMFVideoProcessor</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMFVideoProcessor</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/evr9/nf-evr9-imfvideoprocessor-getavailablevideoprocessormodes">GetAvailableVideoProcessorModes</a>
</td>
<td align="left" width="63%">
Retrieves the video processor modes that the video driver supports.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/evr9/nf-evr9-imfvideoprocessor-getbackgroundcolor">GetBackgroundColor</a>
</td>
<td align="left" width="63%">
Retrieves the background color that is used for the composition rectangle.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/evr9/nf-evr9-imfvideoprocessor-getfilteringrange">GetFilteringRange</a>
</td>
<td align="left" width="63%">
Retrieves the range of values for a specified image filter setting.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/evr9/nf-evr9-imfvideoprocessor-getfilteringvalue">GetFilteringValue</a>
</td>
<td align="left" width="63%">
Retrieves the current setting for an image filter.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/evr9/nf-evr9-imfvideoprocessor-getprocamprange">GetProcAmpRange</a>
</td>
<td align="left" width="63%">
Retrieves the range of values for a ProcAmp setting.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/evr9/nf-evr9-imfvideoprocessor-getprocampvalues">GetProcAmpValues</a>
</td>
<td align="left" width="63%">
Retrieves the current settings for one or more ProcAmp settings.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/evr9/nf-evr9-imfvideoprocessor-getvideoprocessorcaps">GetVideoProcessorCaps</a>
</td>
<td align="left" width="63%">
Retrieves the capabilities of a video processor mode.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/evr9/nf-evr9-imfvideoprocessor-getvideoprocessormode">GetVideoProcessorMode</a>
</td>
<td align="left" width="63%">
Retrieves the application's preferred video processor mode.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/evr9/nf-evr9-imfvideoprocessor-setbackgroundcolor">SetBackgroundColor</a>
</td>
<td align="left" width="63%">
Sets the background color for the composition rectangle.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/evr9/nf-evr9-imfvideoprocessor-setfilteringvalue">SetFilteringValue</a>
</td>
<td align="left" width="63%">
Sets a parameter for an image filter.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/evr9/nf-evr9-imfvideoprocessor-setprocampvalues">SetProcAmpValues</a>
</td>
<td align="left" width="63%">
Sets one or more ProcAmp settings.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/evr9/nf-evr9-imfvideoprocessor-setvideoprocessormode">SetVideoProcessorMode</a>
</td>
<td align="left" width="63%">
Sets the preferred video processor mode.

</td>
</tr>
</table>

## -remarks

This interface provides access to functionality that is implemented by the graphics driver. The driver provides one or more video processor <i>modes</i>, which are identified by GUID. Each mode has its own set of capabilities. The list of available modes might change depending on the media type of the video.

To use this interface, perform the following steps:

<ol>
<li>
Initialize the media types on the EVR input streams. (If you are using the Media Session, this occurs after the topology is resolved. Wait for the Media Session to send the <a href="/windows/desktop/medfound/mesessiontopologystatus">MESessionTopologyStatus</a> event with a status value of MF_TOPOSTATUS_READY.)

</li>
<li>
Call <a href="/windows/desktop/api/evr9/nf-evr9-imfvideoprocessor-getavailablevideoprocessormodes">IMFVideoProcessor::GetAvailableVideoProcessorModes</a> to get the list of video processor modes that are available.

</li>
<li>
Call <a href="/windows/desktop/api/evr9/nf-evr9-imfvideoprocessor-getvideoprocessorcaps">IMFVideoProcessor::GetVideoProcessorCaps</a> to find the capabilities of each video processor mode.

</li>
<li>
Call <a href="/windows/desktop/api/evr9/nf-evr9-imfvideoprocessor-setvideoprocessormode">IMFVideoProcessor::SetVideoProcessorMode</a> to select a mode. If you skip this step, the EVR automatically selects a video processor mode when streaming begins. In that case, wait for playback to start before continuing to step 5.

</li>
<li>
Call <a href="/windows/desktop/api/evr9/nf-evr9-imfvideoprocessor-getprocamprange">IMFVideoProcessor::GetProcAmpRange</a> and <a href="/windows/desktop/api/evr9/nf-evr9-imfvideoprocessor-getfilteringrange">IMFVideoProcessor::GetFilteringRange</a> to find the range of values for the various ProcAmp and image filter settings.

</li>
<li>
Call <a href="/windows/desktop/api/evr9/nf-evr9-imfvideoprocessor-setprocampvalues">IMFVideoProcessor::SetProcAmpValues</a> and <a href="/windows/desktop/api/evr9/nf-evr9-imfvideoprocessor-setfilteringvalue">IMFVideoProcessor::SetFilteringValue</a> to change the ProcAmp and image filter settings.

</li>
</ol>

## -see-also

<a href="/windows/desktop/medfound/enhanced-video-renderer">Enhanced Video Renderer</a>



<a href="/windows/desktop/medfound/media-foundation-interfaces">Media Foundation Interfaces</a>