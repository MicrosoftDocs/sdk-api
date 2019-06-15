---
UID: NN:mfplay.IMFPMediaPlayer
title: IMFPMediaPlayer (mfplay.h)
author: windows-sdk-content
description: Contains methods to play media files. (Deprecated.).
old-location: mf\imfpmediaplayer.htm
tech.root: medfound
ms.assetid: fa57d465-1ee9-4f7a-9be8-66a6d73f65e8
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IMFPMediaPlayer, IMFPMediaPlayer interface [Media Foundation], IMFPMediaPlayer interface [Media Foundation],described, mf.imfpmediaplayer, mfplay/IMFPMediaPlayer
ms.topic: interface
f1_keywords: ["mfplay/IMFPMediaPlayer"]
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
 - IMFPMediaPlayer
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMFPMediaPlayer interface


## -description



<div class="alert"><b>Important</b>  Deprecated. This API may be removed from future releases of Windows. Applications should use the <a href="https://docs.microsoft.com/windows/desktop/medfound/media-session">Media Session</a> for playback.</div>
<div> </div>


Contains methods to play media files.

The MFPlay player object exposes this interface. To get a pointer to this interface, call <a href="https://docs.microsoft.com/windows/desktop/api/mfplay/nf-mfplay-mfpcreatemediaplayer">MFPCreateMediaPlayer</a>.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMFPMediaPlayer</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IMFPMediaPlayer</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMFPMediaPlayer</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-clearmediaitem">ClearMediaItem</a>
</td>
<td align="left" width="63%">
Clears the current media item.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-createmediaitemfromobject">CreateMediaItemFromObject</a>
</td>
<td align="left" width="63%">
Creates a media item from an object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-createmediaitemfromurl">CreateMediaItemFromURL</a>
</td>
<td align="left" width="63%">
Creates a media item from a URL.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-framestep">FrameStep</a>
</td>
<td align="left" width="63%">
Steps forward one video frame.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-getaspectratiomode">GetAspectRatioMode</a>
</td>
<td align="left" width="63%">
Gets the current aspect-ratio correction mode. This mode controls whether the aspect ratio of the video is preserved during playback.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-getbalance">GetBalance</a>
</td>
<td align="left" width="63%">
Gets the current audio balance.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-getbordercolor">GetBorderColor</a>
</td>
<td align="left" width="63%">
Gets the current color of the video border.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-getduration">GetDuration</a>
</td>
<td align="left" width="63%">
Gets the playback duration of the current media item.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-getidealvideosize">GetIdealVideoSize</a>
</td>
<td align="left" width="63%">
Gets the range of video sizes that can be displayed without significantly degrading performance or image quality.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-getmediaitem">GetMediaItem</a>
</td>
<td align="left" width="63%">
Gets a pointer to the current media item.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-getmute">GetMute</a>
</td>
<td align="left" width="63%">
Queries whether the audio is muted.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-getnativevideosize">GetNativeVideoSize</a>
</td>
<td align="left" width="63%">
Gets the size and aspect ratio of the video.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-getposition">GetPosition</a>
</td>
<td align="left" width="63%">
Gets the current playback position.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-getrate">GetRate</a>
</td>
<td align="left" width="63%">
Gets the current playback rate.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-getstate">GetState</a>
</td>
<td align="left" width="63%">
Gets the current playback state.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-getsupportedrates">GetSupportedRates</a>
</td>
<td align="left" width="63%">
Gets the range of supported playback rates.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-getvideosourcerect">GetVideoSourceRect</a>
</td>
<td align="left" width="63%">
Gets the video source rectangle.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-getvideowindow">GetVideoWindow</a>
</td>
<td align="left" width="63%">
Gets the window where the video is displayed.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-getvolume">GetVolume</a>
</td>
<td align="left" width="63%">
Gets the current audio volume.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-inserteffect">InsertEffect</a>
</td>
<td align="left" width="63%">
Applies an audio or video effect to playback.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-pause">Pause</a>
</td>
<td align="left" width="63%">
Pauses playback.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-play">Play</a>
</td>
<td align="left" width="63%">
Starts playback.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-removealleffects">RemoveAllEffects</a>
</td>
<td align="left" width="63%">
Removes all effects that were added with the <a href="https://docs.microsoft.com/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-inserteffect">IMFPMediaPlayer::InsertEffect</a> method.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-removeeffect">RemoveEffect</a>
</td>
<td align="left" width="63%">
Removes an effect that was added with the <a href="https://docs.microsoft.com/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-inserteffect">IMFPMediaPlayer::InsertEffect</a> method.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-setaspectratiomode">SetAspectRatioMode</a>
</td>
<td align="left" width="63%">
Specifies whether the aspect ratio of the video is preserved during playback.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-setbalance">SetBalance</a>
</td>
<td align="left" width="63%">
Sets the audio balance.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-setbordercolor">SetBorderColor</a>
</td>
<td align="left" width="63%">
Sets the color for the video border.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-setmediaitem">SetMediaItem</a>
</td>
<td align="left" width="63%">
Queues a media item for playback.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-setmute">SetMute</a>
</td>
<td align="left" width="63%">
Mutes or unmutes the audio.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-setposition">SetPosition</a>
</td>
<td align="left" width="63%">
Sets the playback position.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-setrate">SetRate</a>
</td>
<td align="left" width="63%">
Sets the playback rate.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-setvideosourcerect">SetVideoSourceRect</a>
</td>
<td align="left" width="63%">
Sets the video source rectangle.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-setvolume">SetVolume</a>
</td>
<td align="left" width="63%">
Sets the audio volume.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-shutdown">Shutdown</a>
</td>
<td align="left" width="63%">
Shuts down the MFPlay player object and releases any resources that the object is using.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-stop">Stop</a>
</td>
<td align="left" width="63%">
Stops playback.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-updatevideo">UpdateVideo</a>
</td>
<td align="left" width="63%">
Updates the video frame. Call this method when your application receives a <b>WM_PAINT</b> or <b>WM_SIZE</b> message.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/medfound/media-foundation-interfaces">Media Foundation Interfaces</a>



<a href="https://docs.microsoft.com/windows/desktop/medfound/using-mfplay-for-audio-video-playback">Using MFPlay for Audio/Video Playback</a>
 

 

