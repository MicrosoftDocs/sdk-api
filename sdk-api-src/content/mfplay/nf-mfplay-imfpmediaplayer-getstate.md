---
UID: NF:mfplay.IMFPMediaPlayer.GetState
title: IMFPMediaPlayer::GetState (mfplay.h)
description: Gets the current playback state of the MFPlay player object.
helpviewer_keywords: ["GetState","GetState method [Media Foundation]","GetState method [Media Foundation]","IMFPMediaPlayer interface","IMFPMediaPlayer interface [Media Foundation]","GetState method","IMFPMediaPlayer.GetState","IMFPMediaPlayer::GetState","mf.imfpmediaplayer_getstate","mfplay/IMFPMediaPlayer::GetState"]
old-location: mf\imfpmediaplayer_getstate.htm
tech.root: mfarchive
archived: true
ms.assetid: 072c5e93-b3ce-469c-8235-3e9c63bd77e3
ms.date: 12/05/2018
ms.keywords: GetState, GetState method [Media Foundation], GetState method [Media Foundation],IMFPMediaPlayer interface, IMFPMediaPlayer interface [Media Foundation],GetState method, IMFPMediaPlayer.GetState, IMFPMediaPlayer::GetState, mf.imfpmediaplayer_getstate, mfplay/IMFPMediaPlayer::GetState
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
 - IMFPMediaPlayer::GetState
 - mfplay/IMFPMediaPlayer::GetState
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
 - IMFPMediaPlayer.GetState
---

# IMFPMediaPlayer::GetState


## -description

\[The feature associated with this page, MFPlay, is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer) and  [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer** and **IMFMediaEngine** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]


Gets the current playback state of the MFPlay player object.

## -parameters

### -param peState [out]

Receives the playback state, as a member of the <a href="/windows/desktop/api/mfplay/ne-mfplay-mfp_mediaplayer_state">MFP_MEDIAPLAYER_STATE</a> enumeration.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

This method can be called after the player object has been shut down.

Many of the <a href="/windows/desktop/api/mfplay/nn-mfplay-imfpmediaplayer">IMFPMediaPlayer</a> methods complete asynchronously. While an asynchronous operation is pending, the current state is not updated until the operation completes. When the operation completes, the application receives an event callback, and the new state is given in the <a href="/windows/desktop/api/mfplay/ns-mfplay-mfp_event_header">MFP_EVENT_HEADER</a> structure that is passed to the callback.

## -see-also

<a href="/windows/desktop/api/mfplay/nn-mfplay-imfpmediaplayer">IMFPMediaPlayer</a>



<a href="/windows/desktop/medfound/using-mfplay-for-audio-video-playback">Using MFPlay for Audio/Video Playback</a>