---
UID: NF:mfplay.IMFPMediaPlayer.Pause
title: IMFPMediaPlayer::Pause (mfplay.h)
description: Pauses playback. (IMFPMediaPlayer.Pause)
helpviewer_keywords: ["IMFPMediaPlayer interface [Media Foundation]","Pause method","IMFPMediaPlayer.Pause","IMFPMediaPlayer::Pause","Pause","Pause method [Media Foundation]","Pause method [Media Foundation]","IMFPMediaPlayer interface","mf.imfpmediaplayer_pause","mfplay/IMFPMediaPlayer::Pause"]
old-location: mf\imfpmediaplayer_pause.htm
tech.root: mf
ms.assetid: f6bf6896-6ed6-4135-a01d-f875bfdc72f4
ms.date: 12/05/2018
ms.keywords: IMFPMediaPlayer interface [Media Foundation],Pause method, IMFPMediaPlayer.Pause, IMFPMediaPlayer::Pause, Pause, Pause method [Media Foundation], Pause method [Media Foundation],IMFPMediaPlayer interface, mf.imfpmediaplayer_pause, mfplay/IMFPMediaPlayer::Pause
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
 - IMFPMediaPlayer::Pause
 - mfplay/IMFPMediaPlayer::Pause
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
 - IMFPMediaPlayer.Pause
---

# IMFPMediaPlayer::Pause


## -description

<div class="alert"><b>Important</b>  Deprecated. This API may be removed from future releases of Windows. Applications should use the <a href="/windows/desktop/medfound/media-session">Media Session</a> for playback.</div>
<div> </div>


Pauses playback. While playback is paused, the most recent video frame is displayed, and audio is silent.



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
<dt><b><b>S_OK</b></b></dt>
</dl>
</td>
<td width="60%">
The method succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><b>MF_E_SHUTDOWN</b></b></dt>
</dl>
</td>
<td width="60%">
The object's <a href="/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-shutdown">Shutdown</a> method was called.

</td>
</tr>
</table>

## -remarks

This method completes asynchronously.  When the operation completes, the application's <a href="/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayercallback-onmediaplayerevent">IMFPMediaPlayerCallback::OnMediaPlayerEvent</a> callback method is invoked. The event type is <b>MFP_EVENT_TYPE_PAUSE</b>.

## -see-also

<a href="/windows/desktop/api/mfplay/nn-mfplay-imfpmediaplayer">IMFPMediaPlayer</a>



<a href="/windows/desktop/medfound/using-mfplay-for-audio-video-playback">Using MFPlay for Audio/Video Playback</a>
