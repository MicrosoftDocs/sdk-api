---
UID: NN:evr.IMFVideoDisplayControl
title: IMFVideoDisplayControl
author: windows-sdk-content
description: Controls how the Enhanced Video Renderer (EVR) displays video.
old-location: mf\imfvideodisplaycontrol.htm
tech.root: medfound
ms.assetid: db9b4663-9240-484f-8c47-cb1f5daa238d
ms.author: windowssdkdev
ms.date: 10/15/2018
ms.keywords: IMFVideoDisplayControl, IMFVideoDisplayControl interface [Media Foundation], IMFVideoDisplayControl interface [Media Foundation],described, db9b4663-9240-484f-8c47-cb1f5daa238d, evr/IMFVideoDisplayControl, mf.imfvideodisplaycontrol
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMFVideoDisplayControl interface


## -description


Controls how the <a href="https://msdn.microsoft.com/1c985558-d25d-4f51-978a-58c05943dab9">Enhanced Video Renderer</a> (EVR) displays video.

The EVR presenter implements this interface. To get a pointer to the interface, call <a href="https://msdn.microsoft.com/4287dd1f-1718-4231-bc62-b58e0e61d688">IMFGetService::GetService</a>. The service identifier is GUID MR_VIDEO_RENDER_SERVICE. Call <b>GetService</b> on any of the following objects:
<ul>
<li>The <a href="https://msdn.microsoft.com/dac99908-be90-415d-8837-2f97d573feb5">Media Session</a>, if the topology contains an instance of the EVR.
            </li>
<li>The EVR media sink.
            </li>
<li>The DirectShow EVR filter.
            </li>
<li>The EVR presenter.
            </li>
</ul>If you implement a custom presenter for the EVR, the presenter can optionally expose this interface as a service.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMFVideoDisplayControl</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IMFVideoDisplayControl</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/b5e81f80-e5c9-4ecf-8f10-d52a0533f086">GetAspectRatioMode</a>
</td>
<td align="left" width="63%">
Queries how the EVR handles the aspect ratio of the source video.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1b65b793-d06d-4d7f-a19f-0068dd7f2e44">GetBorderColor</a>
</td>
<td align="left" width="63%">
Retrieves the border color for the video.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/25ec4c23-04dd-4e18-9cc1-de9e57271e8f">GetCurrentImage</a>
</td>
<td align="left" width="63%">
Retrieves a copy of the current image being displayed by the video renderer.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ee564655-be8a-46f7-9682-acf3b38d056a">GetFullscreen</a>
</td>
<td align="left" width="63%">
Queries whether the EVR is currently in full-screen mode.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c580778b-fe7c-4c62-9bcd-8a5fde370b9d">GetIdealVideoSize</a>
</td>
<td align="left" width="63%">
Gets the range of sizes that the EVR can display without significantly degrading performance or image quality.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/12630035-dd07-44bd-98f7-79974c9cc58b">GetNativeVideoSize</a>
</td>
<td align="left" width="63%">
Gets the size and aspect ratio of the video, prior to any stretching by the video renderer.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9a5bd1d6-e604-4798-af29-ad0c1931b651">GetRenderingPrefs</a>
</td>
<td align="left" width="63%">
Gets various video rendering settings.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/59c2e914-cc15-4534-976c-a760ff97f6ae">GetVideoPosition</a>
</td>
<td align="left" width="63%">
Gets the source and destination rectangles for the video.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0b2b6b61-a2c5-4efd-ac40-962b0c2ae9c5">GetVideoWindow</a>
</td>
<td align="left" width="63%">
Gets the clipping window for the video.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c8051883-2a48-4ca4-a7d2-c90d0d451cd2">RepaintVideo</a>
</td>
<td align="left" width="63%">
Gets the current video frame.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/dd49a110-1c11-4eca-9e7b-6021f3bdd397">SetAspectRatioMode</a>
</td>
<td align="left" width="63%">
Specifies how the EVR handles the aspect ratio of the source video.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4a3647a8-4789-4f18-979b-4a9ee1ce7b71">SetBorderColor</a>
</td>
<td align="left" width="63%">
Sets the border color for the video.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/95c85fb2-9267-477f-aa47-1c050ccc1bdd">SetFullscreen</a>
</td>
<td align="left" width="63%">
Sets or unsets full-screen rendering mode.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7603aaf8-1671-4b35-bee5-335f656de3c5">SetRenderingPrefs</a>
</td>
<td align="left" width="63%">
Sets various preferences related to video rendering.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5dc789b7-e206-4f1d-a0b2-12cb98ce4184">SetVideoPosition</a>
</td>
<td align="left" width="63%">
Sets the source and destination rectangles for the video.
        

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/50bc345c-ee44-4174-9b1a-e406041096b5">SetVideoWindow</a>
</td>
<td align="left" width="63%">
Sets the clipping window for the video.
        

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/1c985558-d25d-4f51-978a-58c05943dab9">Enhanced Video Renderer</a>



<a href="https://msdn.microsoft.com/cdd67082-8153-4f48-abc5-278be82ae082">How to Play Media Files with Media Foundation</a>



<a href="https://msdn.microsoft.com/3e367190-4c88-430e-adbf-9837e1bf0d2b">Media Foundation Interfaces</a>



<a href="https://msdn.microsoft.com/09501d67-effb-41ce-a7b7-d2415acdf3ac">Using the Video Display Controls</a>
 

 

