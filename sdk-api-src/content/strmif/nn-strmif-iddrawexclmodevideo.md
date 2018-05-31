---
UID: NN:strmif.IDDrawExclModeVideo
title: IDDrawExclModeVideo
author: windows-sdk-content
description: The IDDrawExclModeVideo interface enables video playback in DirectDraw exclusive full-screen mode.
old-location: dshow\iddrawexclmodevideo.htm
old-project: DirectShow
ms.assetid: 6a846a07-f513-49e7-85e8-192a5c211515
ms.author: windowssdkdev
ms.date: 05/29/2018
ms.keywords: IDDrawExclModeVideo, IDDrawExclModeVideo interface [DirectShow], IDDrawExclModeVideo interface [DirectShow],described, IDDrawExclModeVideoInterface, dshow.iddrawexclmodevideo, strmif/IDDrawExclModeVideo
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: strmif.h
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
req.typenames: DVD_RELATIVE_BUTTON
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Strmiids.lib
-	Strmiids.dll
api_name:
-	IDDrawExclModeVideo
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
req.product: Windows XP with SP1
---

# IDDrawExclModeVideo interface


## -description



The <code>IDDrawExclModeVideo</code> interface enables video playback in DirectDraw exclusive full-screen mode. The <a href="https://msdn.microsoft.com/e80938b7-31f0-467b-a3fa-c4511d14758d">Overlay Mixer Filter</a> implements this interface. Game applications can use DirectDraw in exclusive full-screen mode and continue playing video. For example, the video can be in the background and graphics can be used on top of it. The application passes in a DirectDraw object and primary surface, and these are passed to the Overlay Mixer filter in the filter graph.

The DVD graph builder object uses <code>IDDrawExclModeVideo</code> to play DVD content while in DirectDraw exclusive full-screen mode. This interface can also be used alone to play MPEG-1 or AVI videos in games.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDDrawExclModeVideo</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IDDrawExclModeVideo</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IDDrawExclModeVideo</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b664fbcc-de14-42ca-95d0-97719e381605">GetDDrawObject</a>
</td>
<td align="left" width="63%">
Retrieves the DirectDraw object being used by the Overlay Mixer.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0fb29af3-5f6f-4502-8785-72c64f72fec4">GetDDrawSurface</a>
</td>
<td align="left" width="63%">
Retrieves the DirectDraw surface being used by the Overlay Mixer.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/cc6b3f73-bfb4-4a71-b3e9-53345abd1430">GetNativeVideoProps</a>
</td>
<td align="left" width="63%">
Retrieves the width, height, and aspect ratio of the Overlay Mixer's primary stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f8f885fe-d1a2-4635-9f30-d57ac0eb905e">SetCallbackInterface</a>
</td>
<td align="left" width="63%">
Specifies the callback interface to the Overlay Mixer so that the calling application can be notified about adjustments to the display during video playback.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/fce1b5df-c3df-475c-adde-392c25d05e4c">SetDDrawObject</a>
</td>
<td align="left" width="63%">
Sets the DirectDraw object to be used in subsequent drawing.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a897c147-044d-44e2-9029-bd62c74483d2">SetDDrawSurface</a>
</td>
<td align="left" width="63%">
Sets the DirectDraw surface to be used in subsequent drawing.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e5c2eda5-4276-4906-8098-37bba3fd4e5a">SetDrawParameters</a>
</td>
<td align="left" width="63%">
Specifies which part of the original video will appear at which position of the screen.

</td>
</tr>
</table> 

