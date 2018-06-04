---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# IMFCapturePreviewSink interface


## -description


Controls the preview sink. The preview sink enables the application to preview audio and video from the camera.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMFCapturePreviewSink</b> interface inherits from <a href="https://msdn.microsoft.com/FBC85FEC-9CD1-45C8-8A2A-04E7BEC483DE">IMFCaptureSink</a>. <b>IMFCapturePreviewSink</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMFCapturePreviewSink</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6EFC9DFF-4029-46F0-9357-983FE528D4FE">GetMirrorState</a>
</td>
<td align="left" width="63%">
Gets the current mirroring state of the video preview stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5C750060-762B-42EE-92AD-8497B83E5D51">GetRotation</a>
</td>
<td align="left" width="63%">
Gets the rotation of the video preview stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/98D6F026-408F-4C22-B4A3-68C1B0EFD1E9">SetCustomSink</a>
</td>
<td align="left" width="63%">
Sets a custom media sink for preview.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/F7F04E29-E7AD-46BD-AAF9-5B7BA68822EE">SetMirrorState</a>
</td>
<td align="left" width="63%">
Enables or disables mirroring of the video preview stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/98D3EFC4-841D-41EC-BC5C-E67029663864">SetRenderHandle</a>
</td>
<td align="left" width="63%">
Specifies a window for preview.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/AC50EB86-A39D-4ACA-9582-A8DB0232E056">SetRenderSurface</a>
</td>
<td align="left" width="63%">
Specifies a DirectComposition visual for preview.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/84C53A34-B2FB-4D13-9A45-5172E9E3CEE8">SetRotation</a>
</td>
<td align="left" width="63%">
Rotates the video preview stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0E14E3E4-25C7-4FCA-B220-20E346E66933">SetSampleCallback</a>
</td>
<td align="left" width="63%">
Sets a callback to receive the preview data for one stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/B541D209-BB03-4FCF-834C-82002037C357">UpdateVideo</a>
</td>
<td align="left" width="63%">
Updates the video frame.

</td>
</tr>
</table> 


## -remarks



To start preview, call <a href="https://msdn.microsoft.com/C5BCF990-E7F9-48E9-B082-79953F5ED27C">IMFCaptureEngine::StartPreview</a>.




## -see-also




<a href="https://msdn.microsoft.com/FBC85FEC-9CD1-45C8-8A2A-04E7BEC483DE">IMFCaptureSink</a>



<a href="https://msdn.microsoft.com/3e367190-4c88-430e-adbf-9837e1bf0d2b">Media Foundation Interfaces</a>
 

 

