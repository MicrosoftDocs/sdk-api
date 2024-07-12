---
UID: NF:mfplay.IMFPMediaPlayer.GetRate
title: IMFPMediaPlayer::GetRate (mfplay.h)
description: Gets the current playback rate. (IMFPMediaPlayer.GetRate)
helpviewer_keywords: ["GetRate","GetRate method [Media Foundation]","GetRate method [Media Foundation]","IMFPMediaPlayer interface","IMFPMediaPlayer interface [Media Foundation]","GetRate method","IMFPMediaPlayer.GetRate","IMFPMediaPlayer::GetRate","mf.imfpmediaplayer_getrate","mfplay/IMFPMediaPlayer::GetRate"]
old-location: mf\imfpmediaplayer_getrate.htm
tech.root: mfarchive
archived: true
ms.assetid: 51257361-0362-43c4-8aca-81fd49be8482
ms.date: 12/05/2018
ms.keywords: GetRate, GetRate method [Media Foundation], GetRate method [Media Foundation],IMFPMediaPlayer interface, IMFPMediaPlayer interface [Media Foundation],GetRate method, IMFPMediaPlayer.GetRate, IMFPMediaPlayer::GetRate, mf.imfpmediaplayer_getrate, mfplay/IMFPMediaPlayer::GetRate
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
 - IMFPMediaPlayer::GetRate
 - mfplay/IMFPMediaPlayer::GetRate
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
 - IMFPMediaPlayer.GetRate
---

# IMFPMediaPlayer::GetRate


## -description

\[The feature associated with this page, MFPlay, is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer) and  [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer** and **IMFMediaEngine** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]


Gets the current playback rate.

## -parameters

### -param pflRate [out]

Receives the playback rate. The playback rate is expressed as a ratio of the current rate to the normal rate. For example, 1.0 indicates normal playback, 0.5 indicates half speed, and 2.0 indicates twice speed. Positive values indicate forward playback, and negative values indicate reverse playback.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/mfplay/nn-mfplay-imfpmediaplayer">IMFPMediaPlayer</a>



<a href="/windows/desktop/medfound/using-mfplay-for-audio-video-playback">Using MFPlay for Audio/Video Playback</a>
