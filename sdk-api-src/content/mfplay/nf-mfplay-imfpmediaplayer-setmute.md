---
UID: NF:mfplay.IMFPMediaPlayer.SetMute
title: IMFPMediaPlayer::SetMute (mfplay.h)
description: Mutes or unmutes the audio. (IMFPMediaPlayer.SetMute)
helpviewer_keywords: ["IMFPMediaPlayer interface [Media Foundation]","SetMute method","IMFPMediaPlayer.SetMute","IMFPMediaPlayer::SetMute","SetMute","SetMute method [Media Foundation]","SetMute method [Media Foundation]","IMFPMediaPlayer interface","mf.imfpmediaplayer_setmute","mfplay/IMFPMediaPlayer::SetMute"]
old-location: mf\imfpmediaplayer_setmute.htm
tech.root: mfarchive
archived: true
ms.assetid: 81e2fb76-a125-4665-9aa5-8971410ee554
ms.date: 12/05/2018
ms.keywords: IMFPMediaPlayer interface [Media Foundation],SetMute method, IMFPMediaPlayer.SetMute, IMFPMediaPlayer::SetMute, SetMute, SetMute method [Media Foundation], SetMute method [Media Foundation],IMFPMediaPlayer interface, mf.imfpmediaplayer_setmute, mfplay/IMFPMediaPlayer::SetMute
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
 - IMFPMediaPlayer::SetMute
 - mfplay/IMFPMediaPlayer::SetMute
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
 - IMFPMediaPlayer.SetMute
---

# IMFPMediaPlayer::SetMute


## -description

\[The feature associated with this page, MFPlay, is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer) and  [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer** and **IMFMediaEngine** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]


Mutes or unmutes the audio.

## -parameters

### -param fMute

Specify <b>TRUE</b> to mute the audio, or <b>FALSE</b> to unmute the audio.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

If you call this method before playback starts, the setting is applied after playback starts.

This method does not mute the entire audio session to which the player belongs. It mutes only the streams from the current media item. Other streams in the audio session are not affected. For more information, see <a href="/windows/desktop/medfound/managing-the-audio-session">Managing the Audio Session</a>.

## -see-also

<a href="/windows/desktop/api/mfplay/nn-mfplay-imfpmediaplayer">IMFPMediaPlayer</a>



<a href="/windows/desktop/medfound/using-mfplay-for-audio-video-playback">Using MFPlay for Audio/Video Playback</a>
