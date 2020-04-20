---
UID: NF:mfplay.IMFPMediaPlayer.Stop
title: IMFPMediaPlayer::Stop (mfplay.h)
description: Stops playback.helpviewer_keywords: ["IMFPMediaPlayer interface [Media Foundation]","Stop method","IMFPMediaPlayer.Stop","IMFPMediaPlayer::Stop","Stop","Stop method [Media Foundation]","Stop method [Media Foundation]","IMFPMediaPlayer interface","mf.imfpmediaplayer_stop","mfplay/IMFPMediaPlayer::Stop"]
old-location: mf\imfpmediaplayer_stop.htm
tech.root: medfound
ms.assetid: 1cfa41c7-209e-4c18-a204-563ede29c7c6
ms.date: 12/05/2018
ms.keywords: IMFPMediaPlayer interface [Media Foundation],Stop method, IMFPMediaPlayer.Stop, IMFPMediaPlayer::Stop, Stop, Stop method [Media Foundation], Stop method [Media Foundation],IMFPMediaPlayer interface, mf.imfpmediaplayer_stop, mfplay/IMFPMediaPlayer::Stop
f1_keywords:
- mfplay/IMFPMediaPlayer.Stop
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- mfplay.h
api_name:
- IMFPMediaPlayer.Stop
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMFPMediaPlayer::Stop


## -description



<div class="alert"><b>Important</b>  Deprecated. This API may be removed from future releases of Windows. Applications should use the <a href="https://docs.microsoft.com/windows/desktop/medfound/media-session">Media Session</a> for playback.</div>
<div> </div>


Stops playback.


## -parameters






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
The object's <a href="https://docs.microsoft.com/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-shutdown">Shutdown</a> method was called.

</td>
</tr>
</table>
 




## -remarks



This method completes asynchronously.  When the operation completes, the application's <a href="https://docs.microsoft.com/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayercallback-onmediaplayerevent">IMFPMediaPlayerCallback::OnMediaPlayerEvent</a> callback method is invoked. The event type is <b>MFP_EVENT_TYPE_STOP</b>.

The current media item is still valid. After playback stops, the playback position resets to the beginning of the current media item. 




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/mfplay/nn-mfplay-imfpmediaplayer">IMFPMediaPlayer</a>



<a href="https://docs.microsoft.com/windows/desktop/medfound/using-mfplay-for-audio-video-playback">Using MFPlay for Audio/Video Playback</a>
 

 

