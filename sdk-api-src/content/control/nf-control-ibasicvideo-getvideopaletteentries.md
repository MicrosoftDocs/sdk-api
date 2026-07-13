---
UID: NF:control.IBasicVideo.GetVideoPaletteEntries
title: IBasicVideo::GetVideoPaletteEntries (control.h)
description: The GetVideoPaletteEntries method retrieves the palette colors for the video.
helpviewer_keywords: ["GetVideoPaletteEntries","GetVideoPaletteEntries method [DirectShow]","GetVideoPaletteEntries method [DirectShow]","IBasicVideo interface","IBasicVideo interface [DirectShow]","GetVideoPaletteEntries method","IBasicVideo.GetVideoPaletteEntries","IBasicVideo::GetVideoPaletteEntries","IBasicVideoGetVideoPaletteEntries","control/IBasicVideo::GetVideoPaletteEntries","dshow.ibasicvideo_getvideopaletteentries"]
old-location: dshow\ibasicvideo_getvideopaletteentries.htm
tech.root: dshow
ms.assetid: 9a022bc5-56f5-41c0-940f-f9074791a353
ms.date: 4/26/2023
ms.keywords: GetVideoPaletteEntries, GetVideoPaletteEntries method [DirectShow], GetVideoPaletteEntries method [DirectShow],IBasicVideo interface, IBasicVideo interface [DirectShow],GetVideoPaletteEntries method, IBasicVideo.GetVideoPaletteEntries, IBasicVideo::GetVideoPaletteEntries, IBasicVideoGetVideoPaletteEntries, control/IBasicVideo::GetVideoPaletteEntries, dshow.ibasicvideo_getvideopaletteentries
req.header: control.h
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
 - IBasicVideo::GetVideoPaletteEntries
 - control/IBasicVideo::GetVideoPaletteEntries
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
 - IBasicVideo.GetVideoPaletteEntries
---

# IBasicVideo::GetVideoPaletteEntries


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>GetVideoPaletteEntries</code> method retrieves the palette colors for the video.

## -parameters

### -param StartIndex [in]

Start index for the palette.

### -param Entries [in]

Number of palette entries to retrieve.

### -param pRetrieved [out]

Pointer to a variable that receives the number of entries returned in <i>pPallette</i>.

### -param pPalette [out]

Pointer to an array of <a href="/previous-versions/dd162769(v=vs.85)">PALETTEENTRY</a> structures of size <i>Entries</i>. Cast the pointer to a long pointer type. The method fills the array.

## -returns

Returns an <b>HRESULT</b> value. Possible values include the following.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Success.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
<b>NULL</b> pointer argument.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VFW_E_NO_PALETTE_AVAILABLE</b></dt>
</dl>
</td>
<td width="60%">
No palette is available.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VFW_E_NOT_CONNECTED</b></dt>
</dl>
</td>
<td width="60%">
The Video Renderer's input pin is not connected.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/control/nn-control-ibasicvideo">IBasicVideo Interface</a>