---
UID: NN:strmif.IDDrawExclModeVideo
title: IDDrawExclModeVideo (strmif.h)

description: The IDDrawExclModeVideo interface enables video playback in DirectDraw exclusive full-screen mode.
old-location: dshow\iddrawexclmodevideo.htm
tech.root: DirectShow
ms.assetid: 6a846a07-f513-49e7-85e8-192a5c211515

ms.date: 12/05/2018
ms.keywords: IDDrawExclModeVideo, IDDrawExclModeVideo interface [DirectShow], IDDrawExclModeVideo interface [DirectShow],described, IDDrawExclModeVideoInterface, dshow.iddrawexclmodevideo, strmif/IDDrawExclModeVideo
ms.topic: interface
f1_keywords: 
 - "strmif/IDDrawExclModeVideo"
dev_langs:
 - c++
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
 - IDDrawExclModeVideo
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDDrawExclModeVideo interface


## -description



The <code>IDDrawExclModeVideo</code> interface enables video playback in DirectDraw exclusive full-screen mode. The <a href="https://docs.microsoft.com/windows/desktop/DirectShow/overlay-mixer-filter">Overlay Mixer Filter</a> implements this interface. Game applications can use DirectDraw in exclusive full-screen mode and continue playing video. For example, the video can be in the background and graphics can be used on top of it. The application passes in a DirectDraw object and primary surface, and these are passed to the Overlay Mixer filter in the filter graph.

The DVD graph builder object uses <code>IDDrawExclModeVideo</code> to play DVD content while in DirectDraw exclusive full-screen mode. This interface can also be used alone to play MPEG-1 or AVI videos in games.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDDrawExclModeVideo</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IDDrawExclModeVideo</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-iddrawexclmodevideo-getddrawobject">GetDDrawObject</a>
</td>
<td align="left" width="63%">
Retrieves the DirectDraw object being used by the Overlay Mixer.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-iddrawexclmodevideo-getddrawsurface">GetDDrawSurface</a>
</td>
<td align="left" width="63%">
Retrieves the DirectDraw surface being used by the Overlay Mixer.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-iddrawexclmodevideo-getnativevideoprops">GetNativeVideoProps</a>
</td>
<td align="left" width="63%">
Retrieves the width, height, and aspect ratio of the Overlay Mixer's primary stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-iddrawexclmodevideo-setcallbackinterface">SetCallbackInterface</a>
</td>
<td align="left" width="63%">
Specifies the callback interface to the Overlay Mixer so that the calling application can be notified about adjustments to the display during video playback.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-iddrawexclmodevideo-setddrawobject">SetDDrawObject</a>
</td>
<td align="left" width="63%">
Sets the DirectDraw object to be used in subsequent drawing.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-iddrawexclmodevideo-setddrawsurface">SetDDrawSurface</a>
</td>
<td align="left" width="63%">
Sets the DirectDraw surface to be used in subsequent drawing.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-iddrawexclmodevideo-setdrawparameters">SetDrawParameters</a>
</td>
<td align="left" width="63%">
Specifies which part of the original video will appear at which position of the screen.

</td>
</tr>
</table> 

