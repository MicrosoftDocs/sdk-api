---
UID: NF:mfplay.IMFPMediaPlayer.ClearMediaItem
title: IMFPMediaPlayer::ClearMediaItem (mfplay.h)
description: Clears the current media item.
helpviewer_keywords: ["ClearMediaItem","ClearMediaItem method [Media Foundation]","ClearMediaItem method [Media Foundation]","IMFPMediaPlayer interface","IMFPMediaPlayer interface [Media Foundation]","ClearMediaItem method","IMFPMediaPlayer.ClearMediaItem","IMFPMediaPlayer::ClearMediaItem","mf.imfpmediaplayer_clearmediaitem","mfplay/IMFPMediaPlayer::ClearMediaItem"]
old-location: mf\imfpmediaplayer_clearmediaitem.htm
tech.root: mfarchive
archived: true
ms.assetid: 2c2b23ab-b282-445f-a5a0-4291ee6f22ba
ms.date: 12/05/2018
ms.keywords: ClearMediaItem, ClearMediaItem method [Media Foundation], ClearMediaItem method [Media Foundation],IMFPMediaPlayer interface, IMFPMediaPlayer interface [Media Foundation],ClearMediaItem method, IMFPMediaPlayer.ClearMediaItem, IMFPMediaPlayer::ClearMediaItem, mf.imfpmediaplayer_clearmediaitem, mfplay/IMFPMediaPlayer::ClearMediaItem
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
 - IMFPMediaPlayer::ClearMediaItem
 - mfplay/IMFPMediaPlayer::ClearMediaItem
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
 - IMFPMediaPlayer.ClearMediaItem
---

# IMFPMediaPlayer::ClearMediaItem


## -description

\[The feature associated with this page, MFPlay, is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer) and  [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer** and **IMFMediaEngine** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]


Clears the current media item.
<div class="alert"><b>Note</b>  This method is currently not implemented.</div><div> </div>



## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

This method stops playback and releases the player object's references to the current media item.

This method completes asynchronously.  When the operation completes, the application's <a href="/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayercallback-onmediaplayerevent">IMFPMediaPlayerCallback::OnMediaPlayerEvent</a> callback method is invoked. The event type is <b>MFP_EVENT_TYPE_MEDIAITEM_CLEARED</b>.

## -see-also

<a href="/windows/desktop/api/mfplay/nn-mfplay-imfpmediaplayer">IMFPMediaPlayer</a>



<a href="/windows/desktop/medfound/using-mfplay-for-audio-video-playback">Using MFPlay for Audio/Video Playback</a>
