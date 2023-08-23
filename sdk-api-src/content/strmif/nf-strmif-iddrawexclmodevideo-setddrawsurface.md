---
UID: NF:strmif.IDDrawExclModeVideo.SetDDrawSurface
title: IDDrawExclModeVideo::SetDDrawSurface (strmif.h)
description: The SetDDrawSurface method specifies the DirectDraw surface to be used in subsequent drawing.
helpviewer_keywords: ["IDDrawExclModeVideo interface [DirectShow]","SetDDrawSurface method","IDDrawExclModeVideo.SetDDrawSurface","IDDrawExclModeVideo::SetDDrawSurface","IDDrawExclModeVideoSetDDrawSurface","SetDDrawSurface","SetDDrawSurface method [DirectShow]","SetDDrawSurface method [DirectShow]","IDDrawExclModeVideo interface","dshow.iddrawexclmodevideo_setddrawsurface","strmif/IDDrawExclModeVideo::SetDDrawSurface"]
old-location: dshow\iddrawexclmodevideo_setddrawsurface.htm
tech.root: dshow
ms.assetid: a897c147-044d-44e2-9029-bd62c74483d2
ms.date: 4/26/2023
ms.keywords: IDDrawExclModeVideo interface [DirectShow],SetDDrawSurface method, IDDrawExclModeVideo.SetDDrawSurface, IDDrawExclModeVideo::SetDDrawSurface, IDDrawExclModeVideoSetDDrawSurface, SetDDrawSurface, SetDDrawSurface method [DirectShow], SetDDrawSurface method [DirectShow],IDDrawExclModeVideo interface, dshow.iddrawexclmodevideo_setddrawsurface, strmif/IDDrawExclModeVideo::SetDDrawSurface
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
 - IDDrawExclModeVideo::SetDDrawSurface
 - strmif/IDDrawExclModeVideo::SetDDrawSurface
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
 - IDDrawExclModeVideo.SetDDrawSurface
---

# IDDrawExclModeVideo::SetDDrawSurface


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>SetDDrawSurface</code> method specifies the DirectDraw surface to be used in subsequent drawing.

## -parameters

### -param pDDrawSurface [in]

Pointer to the <b>IDirectDrawSurface</b> interface on the surface to use.

## -returns

Returns an <b>HRESULT</b> value that depends on the implementation of the interface.

The current DirectShow implementation return values include the following.

<table>
<tr>
<th>Return value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt>S_OK</dt>
</dl>
</td>
<td width="60%">
Success.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>E_INVALIDARG</dt>
</dl>
</td>
<td width="60%">
Argument is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>A DirectDraw error code</dt>
</dl>
</td>
<td width="60%">
A DirectDraw error is encountered when trying to set the specified surface on the Overlay Mixer.

</td>
</tr>
</table>

## -remarks

A game application can use this to share its DirectDraw surface with the <a href="/windows/desktop/DirectShow/overlay-mixer-filter">Overlay Mixer</a> filter so that the video can be drawn in a specified surface. This surface must be associated with the object specified in <a href="/windows/desktop/api/strmif/nf-strmif-iddrawexclmodevideo-setddrawobject">IDDrawExclModeVideo::SetDDrawObject</a>.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-iddrawexclmodevideo">IDDrawExclModeVideo Interface</a>