---
UID: NF:mfplay.IMFPMediaPlayer.Shutdown
title: IMFPMediaPlayer::Shutdown (mfplay.h)
description: Shuts down the MFPlay player object and releases any resources the object is using.
helpviewer_keywords: ["IMFPMediaPlayer interface [Media Foundation]","Shutdown method","IMFPMediaPlayer.Shutdown","IMFPMediaPlayer::Shutdown","Shutdown","Shutdown method [Media Foundation]","Shutdown method [Media Foundation]","IMFPMediaPlayer interface","mf.imfpmediaplayer_shutdown","mfplay/IMFPMediaPlayer::Shutdown"]
old-location: mf\imfpmediaplayer_shutdown.htm
tech.root: mfarchive
archived: true
ms.assetid: c56b07b5-f595-4933-9af6-868fc8938849
ms.date: 12/05/2018
ms.keywords: IMFPMediaPlayer interface [Media Foundation],Shutdown method, IMFPMediaPlayer.Shutdown, IMFPMediaPlayer::Shutdown, Shutdown, Shutdown method [Media Foundation], Shutdown method [Media Foundation],IMFPMediaPlayer interface, mf.imfpmediaplayer_shutdown, mfplay/IMFPMediaPlayer::Shutdown
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
 - IMFPMediaPlayer::Shutdown
 - mfplay/IMFPMediaPlayer::Shutdown
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
 - IMFPMediaPlayer.Shutdown
---

# IMFPMediaPlayer::Shutdown


## -description

\[The feature associated with this page, MFPlay, is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer) and  [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer** and **IMFMediaEngine** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]


Shuts down the MFPlay player object and releases any resources the object is using.



## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

After this method is called, most <a href="/windows/desktop/api/mfplay/nn-mfplay-imfpmediaplayer">IMFPMediaPlayer</a> methods return <b>MF_E_SHUTDOWN</b>. Also, any media items created from this instance of the player object are invalidated and most <a href="/windows/desktop/api/mfplay/nn-mfplay-imfpmediaitem">IMFPMediaItem</a> methods also return <b>MF_E_SHUTDOWN</b>.

The player object automatically shuts itself down when its reference count reaches zero. You can use the <b>Shutdown</b> method to shut down the player before all of the references have been released.

## -see-also

<a href="/windows/desktop/api/mfplay/nn-mfplay-imfpmediaplayer">IMFPMediaPlayer</a>



<a href="/windows/desktop/medfound/using-mfplay-for-audio-video-playback">Using MFPlay for Audio/Video Playback</a>
