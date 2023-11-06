---
UID: NF:strmif.IAMExtTransport.put_MediaState
title: IAMExtTransport::put_MediaState (strmif.h)
description: The put_MediaState method sets the current state of the media.
helpviewer_keywords: ["IAMExtTransport interface [DirectShow]","put_MediaState method","IAMExtTransport.put_MediaState","IAMExtTransport::put_MediaState","IAMExtTransportput_MediaState","dshow.iamexttransport_put_mediastate","put_MediaState","put_MediaState method [DirectShow]","put_MediaState method [DirectShow]","IAMExtTransport interface","strmif/IAMExtTransport::put_MediaState"]
old-location: dshow\iamexttransport_put_mediastate.htm
tech.root: dshow
ms.assetid: e5a4638e-3246-44dd-a7f8-52d0da12fc9c
ms.date: 4/26/2023
ms.keywords: IAMExtTransport interface [DirectShow],put_MediaState method, IAMExtTransport.put_MediaState, IAMExtTransport::put_MediaState, IAMExtTransportput_MediaState, dshow.iamexttransport_put_mediastate, put_MediaState, put_MediaState method [DirectShow], put_MediaState method [DirectShow],IAMExtTransport interface, strmif/IAMExtTransport::put_MediaState
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
 - IAMExtTransport::put_MediaState
 - strmif/IAMExtTransport::put_MediaState
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
 - IAMExtTransport.put_MediaState
---

# IAMExtTransport::put_MediaState


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>put_MediaState</code> method sets the current state of the media.

## -parameters

### -param State [in]

Specifies the media state as a <b>long</b> integer. Use one of the following:

<table>
<tr>
<th>Value
                </th>
<th>Description
                </th>
</tr>
<tr>
<td>ED_MEDIA_SPIN_DOWN</td>
<td>For disk media: Stop spinning. For tape media: Unthread the tape.</td>
</tr>
<tr>
<td>ED_MEDIA_SPIN_UP</td>
<td>For disk media: Start spinning. For tape media: Thread the tape.</td>
</tr>
<tr>
<td>ED_MEDIA_UNLOAD</td>
<td>Eject the media from the drive.</td>
</tr>
</table>
 

These constants are for disk and tape media. Other devices might need to define new constants.

## -returns

When this method succeeds, it returns S_OK. Otherwise it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-iamexttransport">IAMExtTransport Interface</a>



<a href="/windows/desktop/api/strmif/nf-strmif-iamexttransport-get_mediastate">IAMExtTransport::get_MediaState</a>