---
UID: NN:strmif.IOverlay
title: IOverlay (strmif.h)

description: The IOverlay interface provides information so that a filter can write directly to video memory while placing the video in the correct window position.
old-location: dshow\ioverlay.htm
tech.root: DirectShow
ms.assetid: 2d49888a-7046-4779-9634-d181fa582584

ms.date: 12/05/2018
ms.keywords: IOverlay, IOverlay interface [DirectShow], IOverlay interface [DirectShow],described, IOverlayInterface, dshow.ioverlay, strmif/IOverlay
ms.topic: interface
f1_keywords: 
 - "strmif/IOverlay"
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
 - IOverlay
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IOverlay interface


## -description



The <code>IOverlay</code> interface provides information so that a filter can write directly to video memory while placing the video in the correct window position. It is implemented on the input pin of the video renderer and communicates with an upstream filter (typically a video decompressor) by calling that filter's <a href="https://docs.microsoft.com/windows/desktop/api/strmif/nn-strmif-ioverlaynotify">IOverlayNotify</a> methods to notify it of changes to the video window.

This interface has no relationship to the DirectDraw® overlay capability. The Microsoft video renderer draws data it receives through the <a href="https://docs.microsoft.com/windows/desktop/api/strmif/nn-strmif-imeminputpin">IMemInputPin</a> interface, using DirectDraw overlays when available. This interface, used in place of <b>IMemInputPin</b>, is intended to provide notification support for any upstream filter that bypasses the renderer's drawing capabilities, but needs notifications of other display properties.

See the <a href="https://docs.microsoft.com/windows/desktop/api/strmif/nn-strmif-ioverlaynotify">IOverlayNotify</a> reference page for more information on how the <code>IOverlay</code> and <b>IOverlayNotify</b> interfaces work together.

See the <a href="https://docs.microsoft.com/windows/desktop/api/strmif/nn-strmif-ioverlaynotify2">IOverlayNotify2</a> interface for more information on asynchronous notifications of changes to the rendering window.

This interface is implemented on the Microsoft® DirectShow® video renderer filter. It can also be implemented on replacement video renderer filters if desired. If doing so, implement this interface so that filters writing directly to the frame buffer or trying to position an overlay know where to display their video. To implement this interface, the renderer must be prepared to use methods on the <a href="https://docs.microsoft.com/windows/desktop/api/strmif/nn-strmif-ioverlaynotify">IOverlayNotify</a> interface or the <a href="https://docs.microsoft.com/windows/desktop/api/strmif/nn-strmif-ioverlaynotify2">IOverlayNotify2</a> interface of the filter doing the drawing, with notifications of video property changes.

The window-based renderer in DirectShow supports both <a href="https://docs.microsoft.com/windows/desktop/api/strmif/nn-strmif-imeminputpin">IMemInputPin</a> and <b>IOverlay</b> interfaces. These two interfaces are mutually exclusive. A filter chooses to use the <b>IOverlay</b> transport by providing a media type during connection that has a subtype of MEDIASUBTYPE_Overlay. After connection, it will be able to get and use successfully the <code>IOverlay</code> interface. If it connects with any other video formats (such as MEDIASUBTYPE_RGB8), trying to call through <code>IOverlay</code> returns VFW_E_NOT_OVERLAY_CONNECTION.

Use the methods on this function from an upstream filter that must control video overlay properties and intends to handle the displaying of the video data itself. This typically is used by hardware video decoders that have an alternate connection to the video hardware.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IOverlay</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IOverlay</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IOverlay</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-ioverlay-advise">Advise</a>
</td>
<td align="left" width="63%">
Sets up an advise link for the overlay events.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-ioverlay-getcliplist">GetClipList</a>
</td>
<td align="left" width="63%">
Retrieves the clipping list.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-ioverlay-getcolorkey">GetColorKey</a>
</td>
<td align="left" width="63%">
Returns the identifier of the currently active color key.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-ioverlay-getdefaultcolorkey">GetDefaultColorKey</a>
</td>
<td align="left" width="63%">
Retrieves the default color key.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-ioverlay-getpalette">GetPalette</a>
</td>
<td align="left" width="63%">
Retrieves the current palette.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-ioverlay-getvideoposition">GetVideoPosition</a>
</td>
<td align="left" width="63%">
Retrieves the current video source and destination rectangles.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-ioverlay-getwindowhandle">GetWindowHandle</a>
</td>
<td align="left" width="63%">
Returns the window handle.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-ioverlay-setcolorkey">SetColorKey</a>
</td>
<td align="left" width="63%">
Changes the color key.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-ioverlay-setpalette">SetPalette</a>
</td>
<td align="left" width="63%">
Sets the palette.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-ioverlay-unadvise">Unadvise</a>
</td>
<td align="left" width="63%">
Terminates the advise link.

</td>
</tr>
</table> 

