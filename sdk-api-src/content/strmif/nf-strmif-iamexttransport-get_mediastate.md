---
UID: NF:strmif.IAMExtTransport.get_MediaState
title: IAMExtTransport::get_MediaState (strmif.h)
description: The get_MediaState method retrieves the current state of the media.
helpviewer_keywords: ["IAMExtTransport interface [DirectShow]","get_MediaState method","IAMExtTransport.get_MediaState","IAMExtTransport::get_MediaState","IAMExtTransportget_MediaState","dshow.iamexttransport_get_mediastate","get_MediaState","get_MediaState method [DirectShow]","get_MediaState method [DirectShow]","IAMExtTransport interface","strmif/IAMExtTransport::get_MediaState"]
old-location: dshow\iamexttransport_get_mediastate.htm
tech.root: dshow
ms.assetid: 806356c7-796e-459f-8d5f-82c6b744bf07
ms.date: 4/26/2023
ms.keywords: IAMExtTransport interface [DirectShow],get_MediaState method, IAMExtTransport.get_MediaState, IAMExtTransport::get_MediaState, IAMExtTransportget_MediaState, dshow.iamexttransport_get_mediastate, get_MediaState, get_MediaState method [DirectShow], get_MediaState method [DirectShow],IAMExtTransport interface, strmif/IAMExtTransport::get_MediaState
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
 - IAMExtTransport::get_MediaState
 - strmif/IAMExtTransport::get_MediaState
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
 - IAMExtTransport.get_MediaState
---

# IAMExtTransport::get_MediaState


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>get_MediaState</code> method retrieves the current state of the media.



This method is not implemented.

## -parameters

### -param pState [out]

Pointer to a <b>long</b> integer that receives one of the following values.

<table>
<tr>
<th>Value
                </th>
<th>Description
                </th>
</tr>
<tr>
<td>ED_MEDIA_SPIN_DOWN</td>
<td>For disk media: Stopped spinning. For tape media: Tape is unthreaded.</td>
</tr>
<tr>
<td>ED_MEDIA_SPIN_UP</td>
<td>For disk media: Started spinning, but not at full speed. For tape media: Threading the tape.</td>
</tr>
<tr>
<td>ED_MEDIA_UNLOAD</td>
<td>Media is ejected from the drive.</td>
</tr>
</table>

## -returns

When this method succeeds, it returns S_OK. Otherwise it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-iamexttransport">IAMExtTransport Interface</a>