---
UID: NF:mfplay.IMFPMediaPlayer.Play
title: IMFPMediaPlayer::Play (mfplay.h)
description: Starts playback. (IMFPMediaPlayer.Play)
helpviewer_keywords: ["IMFPMediaPlayer interface [Media Foundation]","Play method","IMFPMediaPlayer.Play","IMFPMediaPlayer::Play","Play","Play method [Media Foundation]","Play method [Media Foundation]","IMFPMediaPlayer interface","mf.imfpmediaplayer_play","mfplay/IMFPMediaPlayer::Play"]
old-location: mf\imfpmediaplayer_play.htm
tech.root: mfarchive
archived: true
ms.assetid: 24d6e8a0-d910-46f9-8172-dfcb68c4f364
ms.date: 12/05/2018
ms.keywords: IMFPMediaPlayer interface [Media Foundation],Play method, IMFPMediaPlayer.Play, IMFPMediaPlayer::Play, Play, Play method [Media Foundation], Play method [Media Foundation],IMFPMediaPlayer interface, mf.imfpmediaplayer_play, mfplay/IMFPMediaPlayer::Play
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
 - IMFPMediaPlayer::Play
 - mfplay/IMFPMediaPlayer::Play
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
 - IMFPMediaPlayer.Play
---

# IMFPMediaPlayer::Play


## -description

\[The feature associated with this page, MFPlay, is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer) and  [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer** and **IMFMediaEngine** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]


Starts playback.



## -returns

The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MF_E_SHUTDOWN</b></dt>
</dl>
</td>
<td width="60%">
The object's <a href="/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-shutdown">Shutdown</a> method was called.

</td>
</tr>
</table>

## -remarks

This method completes asynchronously.  When the operation completes, the application's <a href="/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayercallback-onmediaplayerevent">IMFPMediaPlayerCallback::OnMediaPlayerEvent</a> callback method is invoked. The event type is <b>MFP_EVENT_TYPE_PLAY</b>.

## -see-also

<a href="/windows/desktop/api/mfplay/nn-mfplay-imfpmediaplayer">IMFPMediaPlayer</a>



<a href="/windows/desktop/medfound/using-mfplay-for-audio-video-playback">Using MFPlay for Audio/Video Playback</a>
