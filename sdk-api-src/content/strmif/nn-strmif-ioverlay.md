---
UID: NN:strmif.IOverlay
title: IOverlay (strmif.h)
author: windows-sdk-content
description: The IOverlay interface provides information so that a filter can write directly to video memory while placing the video in the correct window position.
old-location: dshow\ioverlay.htm
tech.root: DirectShow
ms.assetid: 2d49888a-7046-4779-9634-d181fa582584
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IOverlay, IOverlay interface [DirectShow], IOverlay interface [DirectShow],described, IOverlayInterface, dshow.ioverlay, strmif/IOverlay
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
 - IOverlay
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IOverlay interface


## -description



The <code>IOverlay</code> interface provides information so that a filter can write directly to video memory while placing the video in the correct window position. It is implemented on the input pin of the video renderer and communicates with an upstream filter (typically a video decompressor) by calling that filter's <a href="https://msdn.microsoft.com/77dcee49-35ef-4664-b0e6-3044352d543c">IOverlayNotify</a> methods to notify it of changes to the video window.

This interface has no relationship to the DirectDraw® overlay capability. The Microsoft video renderer draws data it receives through the <a href="https://msdn.microsoft.com/a4407c6f-6bb5-4274-920b-8bf7d76268bc">IMemInputPin</a> interface, using DirectDraw overlays when available. This interface, used in place of <b>IMemInputPin</b>, is intended to provide notification support for any upstream filter that bypasses the renderer's drawing capabilities, but needs notifications of other display properties.

See the <a href="https://msdn.microsoft.com/77dcee49-35ef-4664-b0e6-3044352d543c">IOverlayNotify</a> reference page for more information on how the <code>IOverlay</code> and <b>IOverlayNotify</b> interfaces work together.

See the <a href="https://msdn.microsoft.com/439b3939-84da-48f5-b2a5-47f68fedef06">IOverlayNotify2</a> interface for more information on asynchronous notifications of changes to the rendering window.

This interface is implemented on the Microsoft® DirectShow® video renderer filter. It can also be implemented on replacement video renderer filters if desired. If doing so, implement this interface so that filters writing directly to the frame buffer or trying to position an overlay know where to display their video. To implement this interface, the renderer must be prepared to use methods on the <a href="https://msdn.microsoft.com/77dcee49-35ef-4664-b0e6-3044352d543c">IOverlayNotify</a> interface or the <a href="https://msdn.microsoft.com/439b3939-84da-48f5-b2a5-47f68fedef06">IOverlayNotify2</a> interface of the filter doing the drawing, with notifications of video property changes.

The window-based renderer in DirectShow supports both <a href="https://msdn.microsoft.com/a4407c6f-6bb5-4274-920b-8bf7d76268bc">IMemInputPin</a> and <b>IOverlay</b> interfaces. These two interfaces are mutually exclusive. A filter chooses to use the <b>IOverlay</b> transport by providing a media type during connection that has a subtype of MEDIASUBTYPE_Overlay. After connection, it will be able to get and use successfully the <code>IOverlay</code> interface. If it connects with any other video formats (such as MEDIASUBTYPE_RGB8), trying to call through <code>IOverlay</code> returns VFW_E_NOT_OVERLAY_CONNECTION.

Use the methods on this function from an upstream filter that must control video overlay properties and intends to handle the displaying of the video data itself. This typically is used by hardware video decoders that have an alternate connection to the video hardware.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IOverlay</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IOverlay</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/02db2233-b185-47a9-9655-409991a74d4e">Advise</a>
</td>
<td align="left" width="63%">
Sets up an advise link for the overlay events.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3133bcae-0a08-45e9-b70a-07ea6ffef8ee">GetClipList</a>
</td>
<td align="left" width="63%">
Retrieves the clipping list.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/fc9e414e-be53-46e7-b329-23f17fc23725">GetColorKey</a>
</td>
<td align="left" width="63%">
Returns the identifier of the currently active color key.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d3aec72f-472e-44fa-bbd8-81e64732e5bc">GetDefaultColorKey</a>
</td>
<td align="left" width="63%">
Retrieves the default color key.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/993c80fb-fa67-4dd6-815b-8e15d2f7f495">GetPalette</a>
</td>
<td align="left" width="63%">
Retrieves the current palette.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a140cc63-29a1-4c81-8393-7f4342c7b7cc">GetVideoPosition</a>
</td>
<td align="left" width="63%">
Retrieves the current video source and destination rectangles.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f2d4cc53-ab0a-4c15-9818-3f312a13d4e1">GetWindowHandle</a>
</td>
<td align="left" width="63%">
Returns the window handle.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/dacbaf03-348f-403d-9c2c-aed8ec344879">SetColorKey</a>
</td>
<td align="left" width="63%">
Changes the color key.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/572f77ab-08a8-453a-993b-724da967bcde">SetPalette</a>
</td>
<td align="left" width="63%">
Sets the palette.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/da987152-d5cd-42c5-848a-6d70ad25ca33">Unadvise</a>
</td>
<td align="left" width="63%">
Terminates the advise link.

</td>
</tr>
</table> 

