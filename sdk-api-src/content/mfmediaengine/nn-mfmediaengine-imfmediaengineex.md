---
UID: NN:mfmediaengine.IMFMediaEngineEx
title: IMFMediaEngineEx (mfmediaengine.h)
description: Extends the IMFMediaEngine interface.
old-location: mf\imfmediaengineex.htm
tech.root: medfound
ms.assetid: EE3591FD-4FE8-4F20-A4E2-52C896229571
ms.date: 12/05/2018
ms.keywords: IMFMediaEngineEx, IMFMediaEngineEx interface [Media Foundation], IMFMediaEngineEx interface [Media Foundation],described, mf.imfmediaengineex, mfmediaengine/IMFMediaEngineEx
ms.topic: interface
f1_keywords:
- mfmediaengine/IMFMediaEngineEx
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
- IMFMediaEngineEx
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMFMediaEngineEx interface


## -description


Extends the <a href="https://docs.microsoft.com/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediaengine">IMFMediaEngine</a> interface.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMFMediaEngineEx</b> interface inherits from <a href="https://docs.microsoft.com/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediaengine">IMFMediaEngine</a>. <b>IMFMediaEngineEx</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMFMediaEngineEx</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengineex-applystreamselections">ApplyStreamSelections</a>
</td>
<td align="left" width="63%">
Applies the stream selections from previous calls to <a href="https://docs.microsoft.com/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengineex-setstreamselection">SetStreamSelection</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengineex-canceltimelinemarkertimer">CancelTimelineMarkerTimer</a>
</td>
<td align="left" width="63%">
Cancels the next pending timeline marker.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengineex-enablehorizontalmirrormode">EnableHorizontalMirrorMode</a>
</td>
<td align="left" width="63%">
Enables or disables mirroring of the video.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengineex-enabletimeupdatetimer">EnableTimeUpdateTimer</a>
</td>
<td align="left" width="63%">
Enables or disables the time update timer.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengineex-enablewindowlessswapchainmode">EnableWindowlessSwapchainMode</a>
</td>
<td align="left" width="63%">
Enables or disables windowless swap-chain mode.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengineex-framestep">FrameStep</a>
</td>
<td align="left" width="63%">
Steps forward or backward one frame.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengineex-getaudioendpointrole">GetAudioEndpointRole</a>
</td>
<td align="left" width="63%">
Gets the audio device endpoint role used for the next  call to <a href="https://docs.microsoft.com/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengine-setsource">SetSource</a> or <a href="https://docs.microsoft.com/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengine-load">Load</a>. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengineex-getaudiostreamcategory">GetAudioStreamCategory</a>
</td>
<td align="left" width="63%">
Gets the audio stream category used for the next call to <a href="https://docs.microsoft.com/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengine-setsource">SetSource</a> or <a href="https://docs.microsoft.com/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengine-load">Load</a>. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengineex-getbalance">GetBalance</a>
</td>
<td align="left" width="63%">
Gets the audio balance.



</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengineex-getnumberofstreams">GetNumberOfStreams</a>
</td>
<td align="left" width="63%">
Gets the number of streams in the media resource.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengineex-getpresentationattribute">GetPresentationAttribute</a>
</td>
<td align="left" width="63%">
Gets a presentation attribute from the media resource.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengineex-getrealtimemode">GetRealTimeMode</a>
</td>
<td align="left" width="63%">
Gets the real time mode used for the next call to <a href="https://docs.microsoft.com/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengine-setsource">SetSource</a> or <a href="https://docs.microsoft.com/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengine-load">Load</a>. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengineex-getresourcecharacteristics">GetResourceCharacteristics</a>
</td>
<td align="left" width="63%">
Gets various flags that describe the media resource.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengineex-getstatistics">GetStatistics</a>
</td>
<td align="left" width="63%">
Gets a playback statistic from the Media Engine.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengineex-getstereo3dframepackingmode">GetStereo3DFramePackingMode</a>
</td>
<td align="left" width="63%">
For stereoscopic 3D video, gets the layout of the two views within a video frame.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengineex-getstereo3drendermode">GetStereo3DRenderMode</a>
</td>
<td align="left" width="63%">
For stereoscopic 3D video, queries how the Media Engine renders the 3D video content.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengineex-getstreamattribute">GetStreamAttribute</a>
</td>
<td align="left" width="63%">
Gets a stream-level attribute from the media resource.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengineex-getstreamselection">GetStreamSelection</a>
</td>
<td align="left" width="63%">
Queries whether a stream is selected to play.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengineex-gettimelinemarkertimer">GetTimelineMarkerTimer</a>
</td>
<td align="left" width="63%">
Gets the time of the next timeline marker, if any.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengineex-getvideoswapchainhandle">GetVideoSwapchainHandle</a>
</td>
<td align="left" width="63%">
Gets a handle to the windowless swap chain.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengineex-insertaudioeffect">InsertAudioEffect</a>
</td>
<td align="left" width="63%">
Inserts an audio effect.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengineex-insertvideoeffect">InsertVideoEffect</a>
</td>
<td align="left" width="63%">
Inserts a video effect.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengineex-isplaybackratesupported">IsPlaybackRateSupported</a>
</td>
<td align="left" width="63%">
Queries whether the Media Engine can play at a specified playback rate.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengineex-isprotected">IsProtected</a>
</td>
<td align="left" width="63%">
Queries whether the media resource contains protected content.



</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengineex-isstereo3d">IsStereo3D</a>
</td>
<td align="left" width="63%">
Queries whether the media resource contains stereoscopic 3D video.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengineex-removealleffects">RemoveAllEffects</a>
</td>
<td align="left" width="63%">
Removes all audio and video effects.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengineex-setaudioendpointrole">SetAudioEndpointRole</a>
</td>
<td align="left" width="63%">
Sets the audio device endpoint used for the next call to <a href="https://docs.microsoft.com/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengine-setsource">SetSource</a> or <a href="https://docs.microsoft.com/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengine-load">Load</a>. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengineex-setaudiostreamcategory">SetAudioStreamCategory</a>
</td>
<td align="left" width="63%">
Sets the audio stream category for the next call to  <a href="https://docs.microsoft.com/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengine-setsource">SetSource</a> or <a href="https://docs.microsoft.com/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengine-load">Load</a>. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengineex-setbalance">SetBalance</a>
</td>
<td align="left" width="63%">
Sets the audio balance.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengineex-setcurrenttimeex">SetCurrentTimeEx</a>
</td>
<td align="left" width="63%">
Seeks to a new playback position using the  specified <a href="https://docs.microsoft.com/windows/desktop/api/mfmediaengine/ne-mfmediaengine-mf_media_engine_seek_mode">MF_MEDIA_ENGINE_SEEK_MODE</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengineex-setrealtimemode">SetRealTimeMode</a>
</td>
<td align="left" width="63%">
Sets the real time mode used for the next call to  <a href="https://docs.microsoft.com/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengine-setsource">SetSource</a> or <a href="https://docs.microsoft.com/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengine-load">Load</a>. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengineex-setsourcefrombytestream">SetSourceFromByteStream</a>
</td>
<td align="left" width="63%">
Opens a media resource from a byte stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengineex-setstereo3dframepackingmode">SetStereo3DFramePackingMode</a>
</td>
<td align="left" width="63%">
For stereoscopic 3D video, sets the layout of the two views within a video frame.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengineex-setstereo3drendermode">SetStereo3DRenderMode</a>
</td>
<td align="left" width="63%">
For stereoscopic 3D video, specifies how the Media Engine renders the 3D video content.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengineex-setstreamselection">SetStreamSelection</a>
</td>
<td align="left" width="63%">
Selects or deselects a stream for playback.



</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengineex-settimelinemarkertimer">SetTimelineMarkerTimer</a>
</td>
<td align="left" width="63%">
Specifies a presentation time when the Media Engine will send a marker event.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengineex-updatevideostream">UpdateVideoStream</a>
</td>
<td align="left" width="63%">
Updates the source rectangle, destination rectangle, and border color for the video.

</td>
</tr>
</table> 


## -remarks



The <a href="https://docs.microsoft.com/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediaengine">IMFMediaEngine</a> interface contains methods that map to the HTML5 media elements. The <b>IMFMediaEngineEx</b> provides additional functionality that does not correspond directly to HTML5.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediaengine">IMFMediaEngine</a>



<a href="http://go.microsoft.com/fwlink/p/?linkid=241429">Media Engine Sample</a>



<a href="https://docs.microsoft.com/windows/desktop/medfound/media-foundation-interfaces">Media Foundation Interfaces</a>
 

 

