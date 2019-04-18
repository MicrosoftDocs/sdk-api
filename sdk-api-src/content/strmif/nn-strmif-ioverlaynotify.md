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

Most software video decoders let the video renderer draw the decompressed images they produce by passing the media samples to the <a href="https://msdn.microsoft.com/a4407c6f-6bb5-4274-920b-8bf7d76268bc">IMemInputPin</a> interface on the renderer's input pin.

However, some video decoding filters (typically hardware decompression boards) handle the drawing of the images themselves, perhaps by using a VGA connector. These filters do not need to use <a href="https://msdn.microsoft.com/a4407c6f-6bb5-4274-920b-8bf7d76268bc">IMemInputPin</a>, but can instead use the <a href="https://msdn.microsoft.com/2d49888a-7046-4779-9634-d181fa582584">IOverlay</a> interface provided by the renderer input pin. Through this interface, the decoder can be notified when the window position or size changes, or when the current system palette changes in order to install and change color keys and palettes.

Decoders that do their own drawing should implement the <code>IOverlayNotify</code> and <a href="https://msdn.microsoft.com/439b3939-84da-48f5-b2a5-47f68fedef06">IOverlayNotify2</a> interfaces. The renderer uses this interface to notify the decoder whenever the window size or position changes, the system palette changes, or a different color key is used. The decoder should call the <a href="https://msdn.microsoft.com/02db2233-b185-47a9-9655-409991a74d4e">IOverlay::Advise</a> method on the renderer's input pin, to set up the callback. Once the callback is established, the renderer calls the decoder's <code>IOverlayNotify</code> methods when the appropriate events occur. To cancel the callback, use the <a href="https://msdn.microsoft.com/da987152-d5cd-42c5-848a-6d70ad25ca33">IOverlay::Unadvise</a> method.

The video renderer is the only filter that calls the methods on this interface. This is done automatically by the default video renderer. If you are writing a replacement video renderer, you will need to use the methods on this interface if your filter supports <b>IOverlay</b> and this interface is passed to your filter in an <a href="https://msdn.microsoft.com/02db2233-b185-47a9-9655-409991a74d4e">IOverlay::Advise</a> call.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IOverlayNotify</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IOverlayNotify</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/d5bed27f-2918-4c1f-9340-a0d5714d911b">OnClipChange</a>
</td>
<td align="left" width="63%">
Provides notification that the window's visible region has changed.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a1e7fc88-a50a-4832-9b29-21b94184f1c7">OnColorKeyChange</a>
</td>
<td align="left" width="63%">
Provides notification that the chroma key has changed.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/128e3834-d561-46d3-b32b-5bfd290f0995">OnPaletteChange</a>
</td>
<td align="left" width="63%">
Provides notification that the palette of the window has changed.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a5d110a6-5056-4fc1-9589-c2cc66566322">OnPositionChange</a>
</td>
<td align="left" width="63%">
Provides notification that the position has changed.

</td>
</tr>
</table> 

