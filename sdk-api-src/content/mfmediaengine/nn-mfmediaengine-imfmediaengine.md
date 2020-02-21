---
UID: NN:mfmediaengine.IMFMediaEngine
title: IMFMediaEngine (mfmediaengine.h)
description: Enables an application to play audio or video files.
old-location: mf\imfmediaengine.htm
tech.root: medfound
ms.assetid: A0023F18-2D28-4F0D-9B00-B8FB11567034
ms.date: 12/05/2018
ms.keywords: IMFMediaEngine, IMFMediaEngine interface [Media Foundation], IMFMediaEngine interface [Media Foundation],described, mf.imfmediaengine, mfmediaengine/IMFMediaEngine
f1_keywords:
- mfmediaengine/IMFMediaEngine
dev_langs:
- c++
req.header: mfmediaengine.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps \| UWP apps]
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
- mfmediaengine.h
api_name:
- IMFMediaEngine
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMFMediaEngine interface


## -description


Enables an application to play audio or video files.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMFMediaEngine</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IMFMediaEngine</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMFMediaEngine</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengine-canplaytype">CanPlayType</a>
</td>
<td align="left" width="63%">
Queries how likely it is that the Media Engine can play a specified type of media resource.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengine-getautoplay">GetAutoPlay</a>
</td>
<td align="left" width="63%">
Queries whether the Media Engine automatically begins playback.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengine-getbuffered">GetBuffered</a>
</td>
<td align="left" width="63%">
Queries how much resource data the media engine has buffered.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengine-getcurrentsource">GetCurrentSource</a>
</td>
<td align="left" width="63%">
Gets the URL of the current media resource, or an empty string if no media resource is present.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengine-getcurrenttime">GetCurrentTime</a>
</td>
<td align="left" width="63%">
Gets the current playback position.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengine-getdefaultplaybackrate">GetDefaultPlaybackRate</a>
</td>
<td align="left" width="63%">
Gets the default playback rate.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengine-getduration">GetDuration</a>
</td>
<td align="left" width="63%">
Gets the duration of the media resource.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengine-geterror">GetError</a>
</td>
<td align="left" width="63%">
Gets the most recent error status.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengine-getloop">GetLoop</a>
</td>
<td align="left" width="63%">
Queries whether the Media Engine will loop playback.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengine-getmuted">GetMuted</a>
</td>
<td align="left" width="63%">
Queries whether the audio is muted.



</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengine-getnativevideosize">GetNativeVideoSize</a>
</td>
<td align="left" width="63%">
Gets the size of the video frame, adjusted for aspect ratio.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengine-getnetworkstate">GetNetworkState</a>
</td>
<td align="left" width="63%">
Gets the current network state of the media engine.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengine-getplaybackrate">GetPlaybackRate</a>
</td>
<td align="left" width="63%">
Gets the current playback rate.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengine-getplayed">GetPlayed</a>
</td>
<td align="left" width="63%">
Gets the time ranges that have been rendered.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengine-getpreload">GetPreload</a>
</td>
<td align="left" width="63%">
Gets the preload flag.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengine-getreadystate">GetReadyState</a>
</td>
<td align="left" width="63%">
Gets the ready state, which indicates whether the current media resource can be rendered.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengine-getseekable">GetSeekable</a>
</td>
<td align="left" width="63%">
Gets the time ranges to which the Media Engine can currently seek.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengine-getstarttime">GetStartTime</a>
</td>
<td align="left" width="63%">
Gets the initial playback position.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengine-getvideoaspectratio">GetVideoAspectRatio</a>
</td>
<td align="left" width="63%">
Gets the picture aspect ratio of the video stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengine-getvolume">GetVolume</a>
</td>
<td align="left" width="63%">
Gets the audio volume level.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengine-hasaudio">HasAudio</a>
</td>
<td align="left" width="63%">
Queries whether the current media resource contains an audio stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengine-hasvideo">HasVideo</a>
</td>
<td align="left" width="63%">
Queries whether the current media resource contains a video stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengine-isended">IsEnded</a>
</td>
<td align="left" width="63%">
Queries whether playback has ended.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengine-ispaused">IsPaused</a>
</td>
<td align="left" width="63%">
Queries whether playback is currently paused.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengine-isseeking">IsSeeking</a>
</td>
<td align="left" width="63%">
Queries whether the Media Engine is currently seeking to a new playback position.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengine-load">Load</a>
</td>
<td align="left" width="63%">
Loads the current media source.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengine-onvideostreamtick">OnVideoStreamTick</a>
</td>
<td align="left" width="63%">
Queries the Media Engine to find out whether a new video frame is ready.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengine-pause">Pause</a>
</td>
<td align="left" width="63%">
Pauses playback.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengine-play">Play</a>
</td>
<td align="left" width="63%">
Starts playback.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengine-setautoplay">SetAutoPlay</a>
</td>
<td align="left" width="63%">
Specifies whether the Media Engine automatically begins playback.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengine-setcurrenttime">SetCurrentTime</a>
</td>
<td align="left" width="63%">
Seeks to a new playback position.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengine-setdefaultplaybackrate">SetDefaultPlaybackRate</a>
</td>
<td align="left" width="63%">
Sets the default playback rate.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengine-seterrorcode">SetErrorCode</a>
</td>
<td align="left" width="63%">
Sets the current error code.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengine-setloop">SetLoop</a>
</td>
<td align="left" width="63%">
Specifies whether the Media Engine loops playback.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengine-setmuted">SetMuted</a>
</td>
<td align="left" width="63%">
Mutes or unmutes the audio.



</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengine-setplaybackrate">SetPlaybackRate</a>
</td>
<td align="left" width="63%">
Sets the current playback rate.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengine-setpreload">SetPreload</a>
</td>
<td align="left" width="63%">
Sets the preload flag.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengine-setsource">SetSource</a>
</td>
<td align="left" width="63%">
Sets the URL of a media resource.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengine-setsourceelements">SetSourceElements</a>
</td>
<td align="left" width="63%">
Sets a list of media sources.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengine-setvolume">SetVolume</a>
</td>
<td align="left" width="63%">
Sets the audio volume level.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengine-shutdown">Shutdown</a>
</td>
<td align="left" width="63%">
Shuts down the Media Engine and releases the resources it is using.



</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengine-transfervideoframe">TransferVideoFrame</a>
</td>
<td align="left" width="63%">
Copies the current video frame to a DXGI surface or WIC bitmap.

</td>
</tr>
</table> 


## -remarks



The Media Engine implements this interface. To create an instance of the Media Engine, call <a href="https://docs.microsoft.com/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengineclassfactory-createinstance">IMFMediaEngineClassFactory::CreateInstance</a>.

This interface is extended with <a href="https://docs.microsoft.com/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediaengineex">IMFMediaEngineEx</a>.




## -see-also




<a href="https://code.msdn.microsoft.com/windowsapps/media-engine-playback-ce1c82f0">Media Engine Sample</a>



<a href="https://docs.microsoft.com/windows/desktop/medfound/media-foundation-interfaces">Media Foundation Interfaces</a>
 

 

