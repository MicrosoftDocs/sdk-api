---
UID: NF:mfplay.IMFPMediaPlayer.GetVolume
title: IMFPMediaPlayer::GetVolume (mfplay.h)
description: Gets the current audio volume.
helpviewer_keywords: ["GetVolume","GetVolume method [Media Foundation]","GetVolume method [Media Foundation]","IMFPMediaPlayer interface","IMFPMediaPlayer interface [Media Foundation]","GetVolume method","IMFPMediaPlayer.GetVolume","IMFPMediaPlayer::GetVolume","mf.imfpmediaplayer_getvolume","mfplay/IMFPMediaPlayer::GetVolume"]
old-location: mf\imfpmediaplayer_getvolume.htm
tech.root: mfarchive
archived: true
ms.assetid: 08bf0bb3-4ee2-4229-9f41-64924c6122c9
ms.date: 12/05/2018
ms.keywords: GetVolume, GetVolume method [Media Foundation], GetVolume method [Media Foundation],IMFPMediaPlayer interface, IMFPMediaPlayer interface [Media Foundation],GetVolume method, IMFPMediaPlayer.GetVolume, IMFPMediaPlayer::GetVolume, mf.imfpmediaplayer_getvolume, mfplay/IMFPMediaPlayer::GetVolume
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
 - IMFPMediaPlayer::GetVolume
 - mfplay/IMFPMediaPlayer::GetVolume
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
 - IMFPMediaPlayer.GetVolume
---

# IMFPMediaPlayer::GetVolume


## -description

\[The feature associated with this page, MFPlay, is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer) and  [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer** and **IMFMediaEngine** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]


Gets the current audio volume.

## -parameters

### -param pflVolume [out]

Receives the audio volume. Volume is expressed as an attenuation level, where 0.0 indicates silence and 1.0 indicates full volume (no attenuation).

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/mfplay/nn-mfplay-imfpmediaplayer">IMFPMediaPlayer</a>



<a href="/windows/desktop/medfound/using-mfplay-for-audio-video-playback">Using MFPlay for Audio/Video Playback</a>