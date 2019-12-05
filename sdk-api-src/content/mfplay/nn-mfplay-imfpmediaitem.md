---
UID: NN:mfplay.IMFPMediaItem
title: IMFPMediaItem (mfplay.h)
description: Represents a media item. (Deprecated.).
old-location: mf\imfpmediaitem.htm
tech.root: medfound
ms.assetid: 2839d256-bdaf-40cf-9f9d-46f9e2ce59e8
ms.date: 12/05/2018
ms.keywords: IMFPMediaItem, IMFPMediaItem interface [Media Foundation], IMFPMediaItem interface [Media Foundation],described, mf.imfpmediaitem, mfplay/IMFPMediaItem
ms.topic: interface
f1_keywords:
- mfplay/IMFPMediaItem
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
- IMFPMediaItem
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMFPMediaItem interface


## -description



<div class="alert"><b>Note</b>  Deprecated. This API may be removed from future releases of Windows. Applications should use the <a href="https://docs.microsoft.com/windows/desktop/medfound/media-session">Media Session</a> for playback.</div>
<div> </div>


Represents a media item. A <i>media item</i> is an abstraction for a source of media data, such as a video file. Use this interface to get information about the source, or to change certain playback settings, such as the start and stop times. To get a pointer to this interface, call one of the following methods:
<ul>
<li>
<a href="https://docs.microsoft.com/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-createmediaitemfromobject">IMFPMediaPlayer::CreateMediaItemFromObject</a>
</li>
<li>
<a href="https://docs.microsoft.com/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-createmediaitemfromurl">IMFPMediaPlayer::CreateMediaItemFromURL</a>
</li>
</ul>

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IMFPMediaItem</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IMFPMediaItem</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IMFPMediaItem</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfplay/nf-mfplay-imfpmediaitem-getcharacteristics">GetCharacteristics</a>
</td>
<td align="left" width="63%">
Gets various flags that describe the media item.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfplay/nf-mfplay-imfpmediaitem-getduration">GetDuration</a>
</td>
<td align="left" width="63%">
Gets the duration of the media item.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfplay/nf-mfplay-imfpmediaitem-getmediaplayer">GetMediaPlayer</a>
</td>
<td align="left" width="63%">
Retrieves a pointer to the MFPlay player object that created the media item.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfplay/nf-mfplay-imfpmediaitem-getmetadata">GetMetadata</a>
</td>
<td align="left" width="63%">
Gets a property store that contains metadata for the source. 

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfplay/nf-mfplay-imfpmediaitem-getnumberofstreams">GetNumberOfStreams</a>
</td>
<td align="left" width="63%">
Gets the number of streams (audio, video, and other) in the media item.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfplay/nf-mfplay-imfpmediaitem-getobject">GetObject</a>
</td>
<td align="left" width="63%">
Gets the object that was used to create the media item.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfplay/nf-mfplay-imfpmediaitem-getpresentationattribute">GetPresentationAttribute</a>
</td>
<td align="left" width="63%">
Queries the media item for a presentation attribute.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfplay/nf-mfplay-imfpmediaitem-getstartstopposition">GetStartStopPosition</a>
</td>
<td align="left" width="63%">
Gets the start and stop times for the media item.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfplay/nf-mfplay-imfpmediaitem-getstreamattribute">GetStreamAttribute</a>
</td>
<td align="left" width="63%">
Queries the media item for a stream attribute.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfplay/nf-mfplay-imfpmediaitem-getstreamselection">GetStreamSelection</a>
</td>
<td align="left" width="63%">
Queries whether a stream is selected to play.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfplay/nf-mfplay-imfpmediaitem-geturl">GetURL</a>
</td>
<td align="left" width="63%">
Gets the URL that was used to create the media item.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfplay/nf-mfplay-imfpmediaitem-getuserdata">GetUserData</a>
</td>
<td align="left" width="63%">
Gets the application-defined value stored in the media item.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfplay/nf-mfplay-imfpmediaitem-hasaudio">HasAudio</a>
</td>
<td align="left" width="63%">
Queries whether the media item contains an audio stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfplay/nf-mfplay-imfpmediaitem-hasvideo">HasVideo</a>
</td>
<td align="left" width="63%">
Queries whether the media item contains a video stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfplay/nf-mfplay-imfpmediaitem-isprotected">IsProtected</a>
</td>
<td align="left" width="63%">
Queries whether the media item contains protected content.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfplay/nf-mfplay-imfpmediaitem-setstartstopposition">SetStartStopPosition</a>
</td>
<td align="left" width="63%">
Sets the start and stop times for the media item.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfplay/nf-mfplay-imfpmediaitem-setstreamselection">SetStreamSelection</a>
</td>
<td align="left" width="63%">
Selects or deselects a stream.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfplay/nf-mfplay-imfpmediaitem-setstreamsink">SetStreamSink</a>
</td>
<td align="left" width="63%">
Sets a media sink for the media item.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/mfplay/nf-mfplay-imfpmediaitem-setuserdata">SetUserData</a>
</td>
<td align="left" width="63%">
Sets an application-defined value that is stored in the media item.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/medfound/media-foundation-interfaces">Media Foundation Interfaces</a>



<a href="https://docs.microsoft.com/windows/desktop/medfound/using-mfplay-for-audio-video-playback">Using MFPlay for Audio/Video Playback</a>
 

 

