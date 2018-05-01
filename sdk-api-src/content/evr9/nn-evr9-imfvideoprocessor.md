---
UID: NN:evr9.IMFVideoProcessor
title: IMFVideoProcessor
author: windows-driver-content
description: Controls video processing in the Enhanced Video Renderer (EVR).
old-location: mf\imfvideoprocessor.htm
old-project: medfound
ms.assetid: 0a63c4f8-eb32-4f0c-b69b-0c16243f2f21
ms.author: windowsdriverdev
ms.date: 4/23/2018
ms.keywords: 0a63c4f8-eb32-4f0c-b69b-0c16243f2f21, IMFVideoProcessor, IMFVideoProcessor interface [Media Foundation], IMFVideoProcessor interface [Media Foundation], described, evr9/IMFVideoProcessor, mf.imfvideoprocessor
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
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
req.typenames: MFVideoAlphaBitmapFlags
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	strmiids.lib
-	strmiids.dll
api_name:
-	IMFVideoProcessor
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
req.product: Windows Media Format 9 Series or later
---

# IMFVideoProcessor interface


## -description


Controls video processing in the <a href="https://msdn.microsoft.com/1c985558-d25d-4f51-978a-58c05943dab9">Enhanced Video Renderer</a> (EVR). The operations controlled through this interface include color adjustment (ProcAmp), noise filters, and detail filters.

The EVR mixer implements this interface. To get a pointer to the interface, call <a href="https://msdn.microsoft.com/4287dd1f-1718-4231-bc62-b58e0e61d688">IMFGetService::GetService</a>. The service identifier is GUID MR_VIDEO_MIXER_SERVICE. Call <b>GetService</b> on any of the following objects:
<ul>
<li>
              The media sesson (if the topology contains an instance of the EVR).
            </li>
<li>
              The EVR media sink.
            </li>
<li>
              The DirectShow EVR filter.
            </li>
<li>
              The EVR mixer.
            </li>
</ul>If you implement a custom mixer for the EVR, the mixer can optionally expose this interface as a service.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMFVideoProcessor</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IMFVideoProcessor</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/1004341d-d39b-4032-a027-39e35ecab635">GetAvailableVideoProcessorModes</a>
</td>
<td align="left" width="63%">
Retrieves the video processor modes that the video driver supports.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d9068346-f0b3-4361-a56b-2360ecc3b9d9">GetBackgroundColor</a>
</td>
<td align="left" width="63%">
Retrieves the background color that is used for the composition rectangle.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1e5f1635-51fe-4394-8a25-dcee3f55c711">GetFilteringRange</a>
</td>
<td align="left" width="63%">
Retrieves the range of values for a specified image filter setting.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1c8d6836-ca62-4d26-be4e-572dc6ff994d">GetFilteringValue</a>
</td>
<td align="left" width="63%">
Retrieves the current setting for an image filter.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/03894bfe-020a-4478-af6f-88521d4bbb6d">GetProcAmpRange</a>
</td>
<td align="left" width="63%">
Retrieves the range of values for a ProcAmp setting.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d1d6f6a4-fe3b-4acf-a004-d02ece41a302">GetProcAmpValues</a>
</td>
<td align="left" width="63%">
Retrieves the current settings for one or more ProcAmp settings.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/hh451674">GetVideoProcessorCaps</a>
</td>
<td align="left" width="63%">
Retrieves the capabilities of a video processor mode.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/df45c379-f525-4018-b2c2-88a52b13dff5">GetVideoProcessorMode</a>
</td>
<td align="left" width="63%">
Retrieves the application's preferred video processor mode.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/fb654dba-1f03-48a7-ac8e-fa0c82f29849">SetBackgroundColor</a>
</td>
<td align="left" width="63%">
Sets the background color for the composition rectangle.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/cb3c9516-2083-4c9d-b583-fc561f977ed5">SetFilteringValue</a>
</td>
<td align="left" width="63%">
Sets a parameter for an image filter.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/84a5e022-773c-483b-adb5-5883b25b716f">SetProcAmpValues</a>
</td>
<td align="left" width="63%">
Sets one or more ProcAmp settings.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4b353576-c8ee-4f73-9ee6-ba4545a6f4fc">SetVideoProcessorMode</a>
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
Initialize the media types on the EVR input streams. (If you are using the Media Session, this occurs after the topology is resolved. Wait for the Media Session to send the <a href="https://msdn.microsoft.com/b45fd598-ab1e-4b12-8d82-c88c96d1f770">MESessionTopologyStatus</a> event with a status value of MF_TOPOSTATUS_READY.)

</li>
<li>
Call <a href="https://msdn.microsoft.com/1004341d-d39b-4032-a027-39e35ecab635">IMFVideoProcessor::GetAvailableVideoProcessorModes</a> to get the list of video processor modes that are available.

</li>
<li>
Call <a href="https://msdn.microsoft.com/9a02aed2-8225-4416-ae54-7ed51c67a149">IMFVideoProcessor::GetVideoProcessorCaps</a> to find the capabilities of each video processor mode.

</li>
<li>
Call <a href="https://msdn.microsoft.com/4b353576-c8ee-4f73-9ee6-ba4545a6f4fc">IMFVideoProcessor::SetVideoProcessorMode</a> to select a mode. If you skip this step, the EVR automatically selects a video processor mode when streaming begins. In that case, wait for playback to start before continuing to step 5.

</li>
<li>
Call <a href="https://msdn.microsoft.com/03894bfe-020a-4478-af6f-88521d4bbb6d">IMFVideoProcessor::GetProcAmpRange</a> and <a href="https://msdn.microsoft.com/1e5f1635-51fe-4394-8a25-dcee3f55c711">IMFVideoProcessor::GetFilteringRange</a> to find the range of values for the various ProcAmp and image filter settings.

</li>
<li>
Call <a href="https://msdn.microsoft.com/84a5e022-773c-483b-adb5-5883b25b716f">IMFVideoProcessor::SetProcAmpValues</a> and <a href="https://msdn.microsoft.com/cb3c9516-2083-4c9d-b583-fc561f977ed5">IMFVideoProcessor::SetFilteringValue</a> to change the ProcAmp and image filter settings.

</li>
</ol>



## -see-also




<a href="https://msdn.microsoft.com/1c985558-d25d-4f51-978a-58c05943dab9">Enhanced Video Renderer</a>



<a href="https://msdn.microsoft.com/3e367190-4c88-430e-adbf-9837e1bf0d2b">Media Foundation Interfaces</a>
 

 

