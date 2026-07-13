---
UID: NF:mfplay.IMFPMediaPlayer.GetMute
title: IMFPMediaPlayer::GetMute (mfplay.h)
description: Queries whether the audio is muted. (IMFPMediaPlayer.GetMute)
helpviewer_keywords: ["GetMute","GetMute method [Media Foundation]","GetMute method [Media Foundation]","IMFPMediaPlayer interface","IMFPMediaPlayer interface [Media Foundation]","GetMute method","IMFPMediaPlayer.GetMute","IMFPMediaPlayer::GetMute","mf.imfpmediaplayer_getmute","mfplay/IMFPMediaPlayer::GetMute"]
old-location: mf\imfpmediaplayer_getmute.htm
tech.root: mfarchive
archived: true
ms.assetid: 2a628608-37ea-48f3-aed4-0344d47ede9f
ms.date: 12/05/2018
ms.keywords: GetMute, GetMute method [Media Foundation], GetMute method [Media Foundation],IMFPMediaPlayer interface, IMFPMediaPlayer interface [Media Foundation],GetMute method, IMFPMediaPlayer.GetMute, IMFPMediaPlayer::GetMute, mf.imfpmediaplayer_getmute, mfplay/IMFPMediaPlayer::GetMute
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
 - IMFPMediaPlayer::GetMute
 - mfplay/IMFPMediaPlayer::GetMute
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
 - IMFPMediaPlayer.GetMute
---

# IMFPMediaPlayer::GetMute


## -description

\[The feature associated with this page, MFPlay, is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer) and  [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer** and **IMFMediaEngine** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]


Queries whether the audio is muted.

## -parameters

### -param pfMute [out]

Receives the value <b>TRUE</b> if the audio is muted, or <b>FALSE</b> otherwise.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/mfplay/nn-mfplay-imfpmediaplayer">IMFPMediaPlayer</a>



<a href="/windows/desktop/medfound/using-mfplay-for-audio-video-playback">Using MFPlay for Audio/Video Playback</a>
