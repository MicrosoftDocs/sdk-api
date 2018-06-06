---
UID: NN:amvideo.IFullScreenVideoEx
title: IFullScreenVideoEx
author: windows-sdk-content
description: The IFullScreenVideoEx interface is implemented on the Full Screen Renderer filter, which provides full-screen video rendering on older hardware.
old-location: dshow\ifullscreenvideoex.htm
old-project: DirectShow
ms.assetid: 4c9de58f-6ceb-4cf5-b1a5-d3e345e08190
ms.author: windowssdkdev
ms.date: 05/29/2018
ms.keywords: IFullScreenVideoEx, IFullScreenVideoEx interface [DirectShow], IFullScreenVideoEx interface [DirectShow],described, IFullScreenVideoInterface, amvideo/IFullScreenVideoEx, dshow.ifullscreenvideoex
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: amvideo.h
req.include-header: Dshow.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
req.typenames: AMVAUncompDataInfo, *LPAMVAUncompDataInfo
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmiids.lib
 - Strmiids.dll
api_name:
 - IFullScreenVideoEx
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
---

# IFullScreenVideoEx interface


## -description



The <code>IFullScreenVideoEx</code> interface is implemented on the <a href="https://msdn.microsoft.com/59332096-bdfe-4208-b99a-1f434652f287">Full Screen Renderer</a> filter, which provides full-screen video rendering on older hardware. Newer video cards can stretch the video efficiently enough that the Full Screen Renderer is not required. Therefore, both the filter and this interface are now deprecated.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IFullScreenVideoEx</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IFullScreenVideoEx</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IFullScreenVideoEx</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/70d4e124-083b-4729-8f39-778e815ea23b">CountModes</a>
</td>
<td align="left" width="63%">
Retrieves the number of display modes that the Full Screen Renderer supports.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/60d1246b-8719-4f41-9088-2672f51dd6a9">GetAcceleratorTable</a>
</td>
<td align="left" width="63%">
Retrieves the accelerator table currently being used to translate keyboard messages. (Not supported.)

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0757da34-cfc5-4a40-9ad0-03bd016ad828">GetCaption</a>
</td>
<td align="left" width="63%">
Retrieves the caption associated with the full-screen window.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f45e1736-8130-483b-9f90-614c4b6970db">GetClipFactor</a>
</td>
<td align="left" width="63%">
Retrieves the clip factor, which determines how much of the video the Full Screen Renderer is allowed to clip.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/036914da-4223-4601-9e4a-4c7840b7dd22">GetCurrentMode</a>
</td>
<td align="left" width="63%">
Retrieves the current display mode.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c1a83ad9-be4b-4adf-a316-d5dfb3df05ef">GetMessageDrain</a>
</td>
<td align="left" width="63%">
Retrieves the window that receives mouse and keyboard messages.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c1a4aea8-8c48-4073-80ed-060db5adb514">GetModeInfo</a>
</td>
<td align="left" width="63%">
Retrieves information about a specified display mode.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/18825029-2035-46b3-a6a5-9edd8e0437c6">GetMonitor</a>
</td>
<td align="left" width="63%">
Queries which monitor the Full Screen Renderer is using. (Not supported.)

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b2839876-40b1-4b41-a3a4-99e5cbdd9ef1">HideOnDeactivate</a>
</td>
<td align="left" width="63%">
Specifies the behavior when the user switches to another application.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0196215f-4efe-418a-acf3-445b8224a2ab">IsHideOnDeactivate</a>
</td>
<td align="left" width="63%">
Indicates the behavior when the user switches to another application.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3f3b55d9-b504-42a3-b60a-65073d1e1447">IsKeepPixelAspectRatio</a>
</td>
<td align="left" width="63%">
Queries whether the pixel aspect ratio is maintained. (Not supported.)

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9b05d6c6-522c-46b8-90b5-c4650cee5f6b">IsModeAvailable</a>
</td>
<td align="left" width="63%">
Queries whether a specified display mode is available.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/97d8b9f8-4dbf-4b49-b32f-4513c9e5186e">IsModeEnabled</a>
</td>
<td align="left" width="63%">
Queries whether a specified display mode is enabled.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f2c57560-7ffa-4bd4-8d0c-a048dafa35bc">KeepPixelAspectRatio</a>
</td>
<td align="left" width="63%">
Specifies whether to maintain the pixel aspect ratio. (Not supported.)

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/aff393e8-e0a5-418d-8706-3fde96dbcfd9">SetAcceleratorTable</a>
</td>
<td align="left" width="63%">
Specifies an accelerator table that will be used to translate keyboard messages. (Not supported.)

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6f520ab4-867f-4001-8f2f-25f0d8efe454">SetCaption</a>
</td>
<td align="left" width="63%">
Sets the caption associated with the full-screen window.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3e2cefd3-491f-4ba4-a234-047fe4e6c6cc">SetClipFactor</a>
</td>
<td align="left" width="63%">
Specifies the clip factor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1821703c-0da1-4b3e-a921-a66770b8ee0d">SetDefault</a>
</td>
<td align="left" width="63%">
Saves the current settings.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f05c1b3e-3ebc-4753-b3ca-e52907c59121">SetEnabled</a>
</td>
<td align="left" width="63%">
Enables or disables a specified display mode.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d0c24da9-c33f-48a7-b644-a7671acca20f">SetMessageDrain</a>
</td>
<td align="left" width="63%">
Specifies a window to receive mouse and keyboard messages from the video window.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f2db1009-ce5b-4ebe-becb-bed3d1187335">SetMonitor</a>
</td>
<td align="left" width="63%">
Specifies which monitor to use. (Not supported.)

</td>
</tr>
</table> 

