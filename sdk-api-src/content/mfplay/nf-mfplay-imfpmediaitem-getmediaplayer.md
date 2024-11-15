---
UID: NF:mfplay.IMFPMediaItem.GetMediaPlayer
title: IMFPMediaItem::GetMediaPlayer (mfplay.h)
description: Gets a pointer to the MFPlay player object that created the media item.
helpviewer_keywords: ["GetMediaPlayer","GetMediaPlayer method [Media Foundation]","GetMediaPlayer method [Media Foundation]","IMFPMediaItem interface","IMFPMediaItem interface [Media Foundation]","GetMediaPlayer method","IMFPMediaItem.GetMediaPlayer","IMFPMediaItem::GetMediaPlayer","mf.imfpmediaitem_getmediaplayer","mfplay/IMFPMediaItem::GetMediaPlayer"]
old-location: mf\imfpmediaitem_getmediaplayer.htm
tech.root: mfarchive
archived: true
ms.assetid: 6d6f822a-d599-437e-a73a-2242d4d3fe3a
ms.date: 12/05/2018
ms.keywords: GetMediaPlayer, GetMediaPlayer method [Media Foundation], GetMediaPlayer method [Media Foundation],IMFPMediaItem interface, IMFPMediaItem interface [Media Foundation],GetMediaPlayer method, IMFPMediaItem.GetMediaPlayer, IMFPMediaItem::GetMediaPlayer, mf.imfpmediaitem_getmediaplayer, mfplay/IMFPMediaItem::GetMediaPlayer
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
 - IMFPMediaItem::GetMediaPlayer
 - mfplay/IMFPMediaItem::GetMediaPlayer
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
 - IMFPMediaItem.GetMediaPlayer
---

# IMFPMediaItem::GetMediaPlayer


## -description

\[The feature associated with this page, MFPlay, is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer) and  [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer** and **IMFMediaEngine** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]


Gets a pointer to the MFPlay player object that created the media item.

## -parameters

### -param ppMediaPlayer [out]

Receives a pointer to the player object's <a href="/windows/desktop/api/mfplay/nn-mfplay-imfpmediaplayer">IMFPMediaPlayer</a> interface. The caller must release the interface.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/mfplay/nn-mfplay-imfpmediaitem">IMFPMediaItem</a>



<a href="/windows/desktop/medfound/using-mfplay-for-audio-video-playback">Using MFPlay for Audio/Video Playback</a>