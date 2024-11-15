---
UID: NF:mfplay.IMFPMediaItem.HasVideo
title: IMFPMediaItem::HasVideo (mfplay.h)
description: Queries whether the media item contains a video stream.
helpviewer_keywords: ["HasVideo","HasVideo method [Media Foundation]","HasVideo method [Media Foundation]","IMFPMediaItem interface","IMFPMediaItem interface [Media Foundation]","HasVideo method","IMFPMediaItem.HasVideo","IMFPMediaItem::HasVideo","mf.imfpmediaitem_hasvideo","mfplay/IMFPMediaItem::HasVideo"]
old-location: mf\imfpmediaitem_hasvideo.htm
tech.root: mfarchive
archived: true
ms.assetid: 6dc8a85c-25e4-4da7-965d-c8882514fc7d
ms.date: 12/05/2018
ms.keywords: HasVideo, HasVideo method [Media Foundation], HasVideo method [Media Foundation],IMFPMediaItem interface, IMFPMediaItem interface [Media Foundation],HasVideo method, IMFPMediaItem.HasVideo, IMFPMediaItem::HasVideo, mf.imfpmediaitem_hasvideo, mfplay/IMFPMediaItem::HasVideo
req.header: mfplay.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IMFPMediaItem::HasVideo
 - mfplay/IMFPMediaItem::HasVideo
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfplay.h
api_name:
 - IMFPMediaItem.HasVideo
---

# IMFPMediaItem::HasVideo


## -description

\[The feature associated with this page, MFPlay, is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer) and  [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer** and **IMFMediaEngine** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]


Queries whether the media item contains a video stream.

## -parameters

### -param pfHasVideo [out]

Receives the value <b>TRUE</b> if the media item contains at least one video stream, or <b>FALSE</b> otherwise.

### -param pfSelected [out]

Receives the value <b>TRUE</b> if at least one video stream is selected, or <b>FALSE</b> otherwise.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

To select or deselect streams before playback starts, call <a href="/windows/desktop/api/mfplay/nf-mfplay-imfpmediaitem-setstreamselection">IMFPMediaItem::SetStreamSelection</a>.

## -see-also

<a href="/windows/desktop/api/mfplay/nn-mfplay-imfpmediaitem">IMFPMediaItem</a>



<a href="/windows/desktop/medfound/using-mfplay-for-audio-video-playback">Using MFPlay for Audio/Video Playback</a>