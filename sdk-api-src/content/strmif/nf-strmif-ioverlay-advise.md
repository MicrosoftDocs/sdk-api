---
UID: NF:strmif.IOverlay.Advise
title: IOverlay::Advise (strmif.h)
description: The Advise method sets up an advise link for the overlay events specified by the dwInterests parameter.
helpviewer_keywords: ["Advise","Advise method [DirectShow]","Advise method [DirectShow]","IOverlay interface","IOverlay interface [DirectShow]","Advise method","IOverlay.Advise","IOverlay::Advise","IOverlayAdvise","dshow.ioverlay_advise","strmif/IOverlay::Advise"]
old-location: dshow\ioverlay_advise.htm
tech.root: dshow
ms.assetid: 02db2233-b185-47a9-9655-409991a74d4e
ms.date: 4/26/2023
ms.keywords: Advise, Advise method [DirectShow], Advise method [DirectShow],IOverlay interface, IOverlay interface [DirectShow],Advise method, IOverlay.Advise, IOverlay::Advise, IOverlayAdvise, dshow.ioverlay_advise, strmif/IOverlay::Advise
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IOverlay::Advise
 - strmif/IOverlay::Advise
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmiids.lib
 - Strmiids.dll
api_name:
 - IOverlay.Advise
---

# IOverlay::Advise


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>Advise</code> method sets up an advise link for the overlay events specified by the <i>dwInterests</i> parameter.

## -parameters

### -param pOverlayNotify [in]

Pointer to the notification interface.

### -param dwInterests [in]

Callbacks of interest, which can be any subset of the following events.

<table>
<tr>
<th>Event
                </th>
<th>Description
                </th>
</tr>
<tr>
<td>ADVISE_NONE</td>
<td>No changes.</td>
</tr>
<tr>
<td>ADVISE_CLIPPING</td>
<td>Change in clipping region (synchronized with the window).</td>
</tr>
<tr>
<td>ADVISE_PALETTE</td>
<td>Change in palette.</td>
</tr>
<tr>
<td>ADVISE_COLORKEY</td>
<td>Change of chroma key value.</td>
</tr>
<tr>
<td>ADVISE_POSITION</td>
<td>Change in position of video window (not synchronized with the window).</td>
</tr>
<tr>
<td>ADVISE_DISPLAY_CHANGE</td>
<td>Called on <a href="/windows/desktop/gdi/wm-displaychange">WM_DISPLAYCHANGE</a>. The <b>WM_DISPLAYCHANGE</b> message is sent to all windows when the display resolution has changed.</td>
</tr>
<tr>
<td>ADVISE_ALL2</td>
<td>All of the above.</td>
</tr>
</table>

## -returns

Returns S_OK if successful. If the method fails, it returns an <b>HRESULT</b> error code.

## -remarks

This method sets up an advise link for the <a href="/windows/desktop/api/strmif/nn-strmif-ioverlaynotify">IOverlayNotify</a> interface to receive notifications. If one of these events occurs, the appropriate entry point in the <i>pOverlayNotify</i> parameter passed in is called (<a href="/windows/desktop/api/strmif/nf-strmif-ioverlaynotify-onclipchange">IOverlayNotify::OnClipChange</a>, <a href="/windows/desktop/api/strmif/nf-strmif-ioverlaynotify-oncolorkeychange">IOverlayNotify::OnColorKeyChange</a>, <a href="/windows/desktop/api/strmif/nf-strmif-ioverlaynotify-onpalettechange">IOverlayNotify::OnPaletteChange</a>, or <a href="/windows/desktop/api/strmif/nf-strmif-ioverlaynotify-onpositionchange">IOverlayNotify::OnPositionChange</a>).

Only one advise link can be set on any given <a href="/windows/desktop/api/strmif/nn-strmif-ioverlay">IOverlay</a> interface. Trying to set another notification interface on second and subsequent calls returns VFW_E_ADVISE_ALREADY_SET. You can cancel an advise link by using <a href="/windows/desktop/api/strmif/nf-strmif-ioverlay-unadvise">IOverlay::Unadvise</a>.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-ioverlay">IOverlay Interface</a>