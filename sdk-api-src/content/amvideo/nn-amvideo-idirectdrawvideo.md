---
UID: NN:amvideo.IDirectDrawVideo
title: IDirectDrawVideo (amvideo.h)
description: The IDirectDrawVideo interface queries the Video Renderer filter about DirectDraw surfaces and hardware capabilities.Applications can use this interface to control what DirectDraw features the Video Renderer will take advantage of.
old-location: dshow\idirectdrawvideo.htm
tech.root: DirectShow
ms.assetid: b918bf3b-b91b-40fb-abb8-4115a4f254bb
ms.date: 12/05/2018
ms.keywords: IDirectDrawVideo, IDirectDrawVideo interface [DirectShow], IDirectDrawVideo interface [DirectShow],described, IDirectDrawVideoInterface, amvideo/IDirectDrawVideo, dshow.idirectdrawvideo
ms.topic: interface
f1_keywords:
- amvideo/IDirectDrawVideo
dev_langs:
- c++
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
- IDirectDrawVideo
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDirectDrawVideo interface


## -description



The <code>IDirectDrawVideo</code> interface queries the <a href="https://docs.microsoft.com/windows/desktop/DirectShow/video-renderer-filter">Video Renderer</a> filter about DirectDraw surfaces and hardware capabilities.

Applications can use this interface to control what DirectDraw features the Video Renderer will take advantage of. For example, if you are positive that you don't want the Video Renderer to use a hardware overlay you can disable its use via the <a href="https://docs.microsoft.com/windows/desktop/api/amvideo/nf-amvideo-idirectdrawvideo-setswitches">SetSwitches</a> method.

<div class="alert"><b>Note</b>  You can't use this interface to force the Video Renderer to use a particular DirectDraw feature; you can only stop it from using that feature.</div>
<div> </div>
There is some duplication in this interface with the <b>IDirectDraw</b> interface; however, this interface enables simple access to that information without calling the DirectDraw provider directly.

The Video Renderer does not load DirectDraw until it is connected, and likewise DirectDraw is unloaded only when the renderer is disconnected. When the renderer has allocated the DirectDraw surfaces it will use for video playback, an application can obtain a <b>DDSURFACEDESC</b> structure describing it. By passing in a pointer to a <b>DDSURFACEDESC</b> structure, the renderer will fill in the structure with the details of the current surface. If DirectDraw has not been loaded, the renderer will return E_FAIL. If the renderer is using DCI (the predecessor to DirectDraw), the <b>DDSURFACEDESC</b> structure is not filled in but the call will return S_FALSE. The only type of DCI surfaces the renderer uses are primary surfaces.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDirectDrawVideo</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IDirectDrawVideo</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IDirectDrawVideo</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/amvideo/nf-amvideo-idirectdrawvideo-canuseoverlaystretch">CanUseOverlayStretch</a>
</td>
<td align="left" width="63%">
Determines whether the renderer will check overlay restrictions.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/amvideo/nf-amvideo-idirectdrawvideo-canusescanline">CanUseScanLine</a>
</td>
<td align="left" width="63%">
Determines whether the renderer will check the current scan line when drawing.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/amvideo/nf-amvideo-idirectdrawvideo-getcaps">GetCaps</a>
</td>
<td align="left" width="63%">
Retrieves a DirectDraw-defined DDCAPS structure containing the hardware capabilities.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/amvideo/nf-amvideo-idirectdrawvideo-getdirectdraw">GetDirectDraw</a>
</td>
<td align="left" width="63%">
Retrieves the <b>IDirectDraw</b> interface.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/amvideo/nf-amvideo-idirectdrawvideo-getemulatedcaps">GetEmulatedCaps</a>
</td>
<td align="left" width="63%">
Retrieves a DirectDraw-defined DDCAPS structure containing the emulated capabilities.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/amvideo/nf-amvideo-idirectdrawvideo-getfourcccodes">GetFourCCCodes</a>
</td>
<td align="left" width="63%">
Retrieves the multimedia format type <b>FOURCC DWORD</b>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/amvideo/nf-amvideo-idirectdrawvideo-getsurfacedesc">GetSurfaceDesc</a>
</td>
<td align="left" width="63%">
Retrieves a description of the DirectDraw surface in use.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/amvideo/nf-amvideo-idirectdrawvideo-getsurfacetype">GetSurfaceType</a>
</td>
<td align="left" width="63%">
Retrieves the actual surface type.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/amvideo/nf-amvideo-idirectdrawvideo-getswitches">GetSwitches</a>
</td>
<td align="left" width="63%">
Retrieves the surface types that the renderer is allowed to use.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/amvideo/nf-amvideo-idirectdrawvideo-setdefault">SetDefault</a>
</td>
<td align="left" width="63%">
Makes the current property settings the global default.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/amvideo/nf-amvideo-idirectdrawvideo-setdirectdraw">SetDirectDraw</a>
</td>
<td align="left" width="63%">
Passes the <b>IDirectDraw</b> interface to a loaded driver.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/amvideo/nf-amvideo-idirectdrawvideo-setswitches">SetSwitches</a>
</td>
<td align="left" width="63%">
Sets the surface types that the renderer is allowed to use.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/amvideo/nf-amvideo-idirectdrawvideo-useoverlaystretch">UseOverlayStretch</a>
</td>
<td align="left" width="63%">
Determines whether the renderer should check overlay stretch limitations.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/amvideo/nf-amvideo-idirectdrawvideo-usescanline">UseScanLine</a>
</td>
<td align="left" width="63%">
Determines whether the renderer should check the current scan line when drawing a video.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/amvideo/nf-amvideo-idirectdrawvideo-usewhenfullscreen">UseWhenFullScreen</a>
</td>
<td align="left" width="63%">
Determines whether DirectShow should change display mode when going to full-screen mode.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/amvideo/nf-amvideo-idirectdrawvideo-willusefullscreen">WillUseFullScreen</a>
</td>
<td align="left" width="63%">
Determines whether DirectShow will change display mode when going to full-screen mode.

</td>
</tr>
</table> 

