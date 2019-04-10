---
UID: NN:amvideo.IFullScreenVideoEx
title: IFullScreenVideoEx (amvideo.h)
author: windows-sdk-content
description: The IFullScreenVideoEx interface is implemented on the Full Screen Renderer filter, which provides full-screen video rendering on older hardware.
old-location: dshow\ifullscreenvideoex.htm
tech.root: DirectShow
ms.assetid: 4c9de58f-6ceb-4cf5-b1a5-d3e345e08190
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IFullScreenVideoEx, IFullScreenVideoEx interface [DirectShow], IFullScreenVideoEx interface [DirectShow],described, IFullScreenVideoInterface, amvideo/IFullScreenVideoEx, dshow.ifullscreenvideoex
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
req.lib: Strmiids.lib
req.dll: 
req.irql: 
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
req.typenames: 
req.redist: 
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
<a href="https://msdn.microsoft.com/en-us/library/Dd390057(v=VS.85).aspx">CountModes</a>
</td>
<td align="left" width="63%">
Retrieves the number of display modes that the Full Screen Renderer supports.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd390058(v=VS.85).aspx">GetAcceleratorTable</a>
</td>
<td align="left" width="63%">
Retrieves the accelerator table currently being used to translate keyboard messages. (Not supported.)

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd390059(v=VS.85).aspx">GetCaption</a>
</td>
<td align="left" width="63%">
Retrieves the caption associated with the full-screen window.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd390060(v=VS.85).aspx">GetClipFactor</a>
</td>
<td align="left" width="63%">
Retrieves the clip factor, which determines how much of the video the Full Screen Renderer is allowed to clip.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd390061(v=VS.85).aspx">GetCurrentMode</a>
</td>
<td align="left" width="63%">
Retrieves the current display mode.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd390062(v=VS.85).aspx">GetMessageDrain</a>
</td>
<td align="left" width="63%">
Retrieves the window that receives mouse and keyboard messages.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd390063(v=VS.85).aspx">GetModeInfo</a>
</td>
<td align="left" width="63%">
Retrieves information about a specified display mode.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd390064(v=VS.85).aspx">GetMonitor</a>
</td>
<td align="left" width="63%">
Queries which monitor the Full Screen Renderer is using. (Not supported.)

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd390065(v=VS.85).aspx">HideOnDeactivate</a>
</td>
<td align="left" width="63%">
Specifies the behavior when the user switches to another application.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd390066(v=VS.85).aspx">IsHideOnDeactivate</a>
</td>
<td align="left" width="63%">
Indicates the behavior when the user switches to another application.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd390067(v=VS.85).aspx">IsKeepPixelAspectRatio</a>
</td>
<td align="left" width="63%">
Queries whether the pixel aspect ratio is maintained. (Not supported.)

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd390068(v=VS.85).aspx">IsModeAvailable</a>
</td>
<td align="left" width="63%">
Queries whether a specified display mode is available.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd390069(v=VS.85).aspx">IsModeEnabled</a>
</td>
<td align="left" width="63%">
Queries whether a specified display mode is enabled.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd390070(v=VS.85).aspx">KeepPixelAspectRatio</a>
</td>
<td align="left" width="63%">
Specifies whether to maintain the pixel aspect ratio. (Not supported.)

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd390071(v=VS.85).aspx">SetAcceleratorTable</a>
</td>
<td align="left" width="63%">
Specifies an accelerator table that will be used to translate keyboard messages. (Not supported.)

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd390072(v=VS.85).aspx">SetCaption</a>
</td>
<td align="left" width="63%">
Sets the caption associated with the full-screen window.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd390073(v=VS.85).aspx">SetClipFactor</a>
</td>
<td align="left" width="63%">
Specifies the clip factor.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd390074(v=VS.85).aspx">SetDefault</a>
</td>
<td align="left" width="63%">
Saves the current settings.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd390075(v=VS.85).aspx">SetEnabled</a>
</td>
<td align="left" width="63%">
Enables or disables a specified display mode.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd390076(v=VS.85).aspx">SetMessageDrain</a>
</td>
<td align="left" width="63%">
Specifies a window to receive mouse and keyboard messages from the video window.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Dd390077(v=VS.85).aspx">SetMonitor</a>
</td>
<td align="left" width="63%">
Specifies which monitor to use. (Not supported.)

</td>
</tr>
</table> 

