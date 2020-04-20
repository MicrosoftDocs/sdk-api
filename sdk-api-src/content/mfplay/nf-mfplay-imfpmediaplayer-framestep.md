---
UID: NF:mfplay.IMFPMediaPlayer.FrameStep
title: IMFPMediaPlayer::FrameStep (mfplay.h)
description: Steps forward one video frame.helpviewer_keywords: ["FrameStep","FrameStep method [Media Foundation]","FrameStep method [Media Foundation]","IMFPMediaPlayer interface","IMFPMediaPlayer interface [Media Foundation]","FrameStep method","IMFPMediaPlayer.FrameStep","IMFPMediaPlayer::FrameStep","mf.imfpmediaplayer_framestep","mfplay/IMFPMediaPlayer::FrameStep"]
old-location: mf\imfpmediaplayer_framestep.htm
tech.root: medfound
ms.assetid: b7965965-2fbc-4494-9368-7d9699e4092a
ms.date: 12/05/2018
ms.keywords: FrameStep, FrameStep method [Media Foundation], FrameStep method [Media Foundation],IMFPMediaPlayer interface, IMFPMediaPlayer interface [Media Foundation],FrameStep method, IMFPMediaPlayer.FrameStep, IMFPMediaPlayer::FrameStep, mf.imfpmediaplayer_framestep, mfplay/IMFPMediaPlayer::FrameStep
f1_keywords:
- mfplay/IMFPMediaPlayer.FrameStep
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
- IMFPMediaPlayer.FrameStep
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMFPMediaPlayer::FrameStep


## -description



<div class="alert"><b>Important</b>  Deprecated. This API may be removed from future releases of Windows. Applications should use the <a href="https://docs.microsoft.com/windows/desktop/medfound/media-session">Media Session</a> for playback.</div>
<div> </div>


Steps forward one video frame.


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
<dt><b>MF_E_INVALIDREQUEST</b></dt>
</dl>
</td>
<td width="60%">
Cannot frame step. Reasons for this error code include:

<ul>
<li>There is no media item queued for playback.</li>
<li>The current media item does not contain video.</li>
</ul>
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
<tr>
<td width="40%">
<dl>
<dt><b>MF_E_UNSUPPORTED_RATE</b></dt>
</dl>
</td>
<td width="60%">
The media source does not support frame stepping, or the current playback rate is negative.

</td>
</tr>
</table>
 




## -remarks



This method completes asynchronously.  When the operation completes, the application's <a href="https://docs.microsoft.com/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayercallback-onmediaplayerevent">IMFPMediaPlayerCallback::OnMediaPlayerEvent</a> callback method is invoked. The event type is <b>MFP_EVENT_TYPE_FRAME_STEP</b>.

The player object does not support frame stepping during reverse playback (that is, while the playback rate is negative).




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/mfplay/nn-mfplay-imfpmediaplayer">IMFPMediaPlayer</a>



<a href="https://docs.microsoft.com/windows/desktop/medfound/using-mfplay-for-audio-video-playback">Using MFPlay for Audio/Video Playback</a>
 

 

