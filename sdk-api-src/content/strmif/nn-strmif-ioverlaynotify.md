---
UID: NN:strmif.IOverlayNotify
title: IOverlayNotify (strmif.h)
author: windows-sdk-content
description: The IOverlayNotify interface provides an upstream filter, such as a decoder, with notifications of changes to the rendering window.
old-location: dshow\ioverlaynotify.htm
tech.root: DirectShow
ms.assetid: 77dcee49-35ef-4664-b0e6-3044352d543c
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IOverlayNotify, IOverlayNotify interface [DirectShow], IOverlayNotify interface [DirectShow],described, IOverlayNotifyInterface, dshow.ioverlaynotify, strmif/IOverlayNotify
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
 - IOverlayNotify
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IOverlayNotify interface


## -description



The <code>IOverlayNotify</code> interface provides an upstream filter, such as a decoder, with notifications of changes to the rendering window. This includes notifications of changes to the palette, color key, and window position, and visible region (clipping) changes.

Most software video decoders let the video renderer draw the decompressed images they produce by passing the media samples to the <a href="https://docs.microsoft.com/windows/desktop/api/strmif/nn-strmif-imeminputpin">IMemInputPin</a> interface on the renderer's input pin.

However, some video decoding filters (typically hardware decompression boards) handle the drawing of the images themselves, perhaps by using a VGA connector. These filters do not need to use <a href="https://docs.microsoft.com/windows/desktop/api/strmif/nn-strmif-imeminputpin">IMemInputPin</a>, but can instead use the <a href="https://docs.microsoft.com/windows/desktop/api/strmif/nn-strmif-ioverlay">IOverlay</a> interface provided by the renderer input pin. Through this interface, the decoder can be notified when the window position or size changes, or when the current system palette changes in order to install and change color keys and palettes.

Decoders that do their own drawing should implement the <code>IOverlayNotify</code> and <a href="https://docs.microsoft.com/windows/desktop/api/strmif/nn-strmif-ioverlaynotify2">IOverlayNotify2</a> interfaces. The renderer uses this interface to notify the decoder whenever the window size or position changes, the system palette changes, or a different color key is used. The decoder should call the <a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-ioverlay-advise">IOverlay::Advise</a> method on the renderer's input pin, to set up the callback. Once the callback is established, the renderer calls the decoder's <code>IOverlayNotify</code> methods when the appropriate events occur. To cancel the callback, use the <a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-ioverlay-unadvise">IOverlay::Unadvise</a> method.

The video renderer is the only filter that calls the methods on this interface. This is done automatically by the default video renderer. If you are writing a replacement video renderer, you will need to use the methods on this interface if your filter supports <b>IOverlay</b> and this interface is passed to your filter in an <a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-ioverlay-advise">IOverlay::Advise</a> call.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IOverlayNotify</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IOverlayNotify</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IOverlayNotify</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-ioverlaynotify-onclipchange">OnClipChange</a>
</td>
<td align="left" width="63%">
Provides notification that the window's visible region has changed.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-ioverlaynotify-oncolorkeychange">OnColorKeyChange</a>
</td>
<td align="left" width="63%">
Provides notification that the chroma key has changed.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-ioverlaynotify-onpalettechange">OnPaletteChange</a>
</td>
<td align="left" width="63%">
Provides notification that the palette of the window has changed.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/strmif/nf-strmif-ioverlaynotify-onpositionchange">OnPositionChange</a>
</td>
<td align="left" width="63%">
Provides notification that the position has changed.

</td>
</tr>
</table> 

