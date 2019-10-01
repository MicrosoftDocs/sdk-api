---
UID: NE:mfmediaengine.MF_MEDIA_ENGINE_EVENT
title: MF_MEDIA_ENGINE_EVENT (mfmediaengine.h)
author: windows-sdk-content
description: Defines event codes for the Media Engine.
old-location: mf\mf_media_engine_event.htm
tech.root: medfound
ms.assetid: 05790FF8-0720-474B-AFF1-362E7A1B7C34
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: MF_MEDIA_ENGINE_EVENT, MF_MEDIA_ENGINE_EVENT enumeration [Media Foundation], MF_MEDIA_ENGINE_EVENT_ABORT, MF_MEDIA_ENGINE_EVENT_BALANCECHANGE, MF_MEDIA_ENGINE_EVENT_BUFFERINGENDED, MF_MEDIA_ENGINE_EVENT_BUFFERINGSTARTED, MF_MEDIA_ENGINE_EVENT_CANPLAY, MF_MEDIA_ENGINE_EVENT_CANPLAYTHROUGH, MF_MEDIA_ENGINE_EVENT_DOWNLOADCOMPLETE, MF_MEDIA_ENGINE_EVENT_DURATIONCHANGE, MF_MEDIA_ENGINE_EVENT_EMPTIED, MF_MEDIA_ENGINE_EVENT_ENDED, MF_MEDIA_ENGINE_EVENT_ERROR, MF_MEDIA_ENGINE_EVENT_FIRSTFRAMEREADY, MF_MEDIA_ENGINE_EVENT_FORMATCHANGE, MF_MEDIA_ENGINE_EVENT_FRAMESTEPCOMPLETED, MF_MEDIA_ENGINE_EVENT_LOADEDDATA, MF_MEDIA_ENGINE_EVENT_LOADEDMETADATA, MF_MEDIA_ENGINE_EVENT_LOADSTART, MF_MEDIA_ENGINE_EVENT_NOTIFYSTABLESTATE, MF_MEDIA_ENGINE_EVENT_OPMINFO, MF_MEDIA_ENGINE_EVENT_PAUSE, MF_MEDIA_ENGINE_EVENT_PLAY, MF_MEDIA_ENGINE_EVENT_PLAYING, MF_MEDIA_ENGINE_EVENT_PROGRESS, MF_MEDIA_ENGINE_EVENT_PURGEQUEUEDEVENTS, MF_MEDIA_ENGINE_EVENT_RATECHANGE, MF_MEDIA_ENGINE_EVENT_SEEKED, MF_MEDIA_ENGINE_EVENT_SEEKING, MF_MEDIA_ENGINE_EVENT_STALLED, MF_MEDIA_ENGINE_EVENT_STREAMRENDERINGERROR, MF_MEDIA_ENGINE_EVENT_SUSPEND, MF_MEDIA_ENGINE_EVENT_TIMELINE_MARKER, MF_MEDIA_ENGINE_EVENT_TIMEUPDATE, MF_MEDIA_ENGINE_EVENT_TRACKSCHANGE, MF_MEDIA_ENGINE_EVENT_VOLUMECHANGE, MF_MEDIA_ENGINE_EVENT_WAITING, mf.mf_media_engine_event, mfmediaengine/MF_MEDIA_ENGINE_EVENT, mfmediaengine/MF_MEDIA_ENGINE_EVENT_ABORT, mfmediaengine/MF_MEDIA_ENGINE_EVENT_BALANCECHANGE, mfmediaengine/MF_MEDIA_ENGINE_EVENT_BUFFERINGENDED, mfmediaengine/MF_MEDIA_ENGINE_EVENT_BUFFERINGSTARTED, mfmediaengine/MF_MEDIA_ENGINE_EVENT_CANPLAY, mfmediaengine/MF_MEDIA_ENGINE_EVENT_CANPLAYTHROUGH, mfmediaengine/MF_MEDIA_ENGINE_EVENT_DOWNLOADCOMPLETE, mfmediaengine/MF_MEDIA_ENGINE_EVENT_DURATIONCHANGE, mfmediaengine/MF_MEDIA_ENGINE_EVENT_EMPTIED, mfmediaengine/MF_MEDIA_ENGINE_EVENT_ENDED, mfmediaengine/MF_MEDIA_ENGINE_EVENT_ERROR, mfmediaengine/MF_MEDIA_ENGINE_EVENT_FIRSTFRAMEREADY, mfmediaengine/MF_MEDIA_ENGINE_EVENT_FORMATCHANGE, mfmediaengine/MF_MEDIA_ENGINE_EVENT_FRAMESTEPCOMPLETED, mfmediaengine/MF_MEDIA_ENGINE_EVENT_LOADEDDATA, mfmediaengine/MF_MEDIA_ENGINE_EVENT_LOADEDMETADATA, mfmediaengine/MF_MEDIA_ENGINE_EVENT_LOADSTART, mfmediaengine/MF_MEDIA_ENGINE_EVENT_NOTIFYSTABLESTATE, mfmediaengine/MF_MEDIA_ENGINE_EVENT_OPMINFO, mfmediaengine/MF_MEDIA_ENGINE_EVENT_PAUSE, mfmediaengine/MF_MEDIA_ENGINE_EVENT_PLAY, mfmediaengine/MF_MEDIA_ENGINE_EVENT_PLAYING, mfmediaengine/MF_MEDIA_ENGINE_EVENT_PROGRESS, mfmediaengine/MF_MEDIA_ENGINE_EVENT_PURGEQUEUEDEVENTS, mfmediaengine/MF_MEDIA_ENGINE_EVENT_RATECHANGE, mfmediaengine/MF_MEDIA_ENGINE_EVENT_SEEKED, mfmediaengine/MF_MEDIA_ENGINE_EVENT_SEEKING, mfmediaengine/MF_MEDIA_ENGINE_EVENT_STALLED, mfmediaengine/MF_MEDIA_ENGINE_EVENT_STREAMRENDERINGERROR, mfmediaengine/MF_MEDIA_ENGINE_EVENT_SUSPEND, mfmediaengine/MF_MEDIA_ENGINE_EVENT_TIMELINE_MARKER, mfmediaengine/MF_MEDIA_ENGINE_EVENT_TIMEUPDATE, mfmediaengine/MF_MEDIA_ENGINE_EVENT_TRACKSCHANGE, mfmediaengine/MF_MEDIA_ENGINE_EVENT_VOLUMECHANGE, mfmediaengine/MF_MEDIA_ENGINE_EVENT_WAITING
ms.topic: enum
f1_keywords: 
 - "mfmediaengine/MF_MEDIA_ENGINE_EVENT"
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
 - HeaderDef
api_location:
 - mfmediaengine.h
api_name:
 - MF_MEDIA_ENGINE_EVENT
targetos: Windows
req.typenames: MF_MEDIA_ENGINE_EVENT
req.redist: 
ms.custom: 19H1
---

# MF_MEDIA_ENGINE_EVENT enumeration


## -description


Defines event codes for the Media Engine. 


## -enum-fields




### -field MF_MEDIA_ENGINE_EVENT_LOADSTART

The Media Engine has started to load the source. See <a href="https://docs.microsoft.com/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengine-load">IMFMediaEngine::Load</a>.


### -field MF_MEDIA_ENGINE_EVENT_PROGRESS

The Media Engine is loading the source.


### -field MF_MEDIA_ENGINE_EVENT_SUSPEND

The Media Engine has suspended a load operation.


### -field MF_MEDIA_ENGINE_EVENT_ABORT

The Media Engine cancelled a load operation that was in progress. 


### -field MF_MEDIA_ENGINE_EVENT_ERROR

An error occurred.

<table>
<tr>
<th>Event Parameter</th>
<th>Description</th>
</tr>
<tr>
<td><i>param1</i></td>
<td>A member of the <a href="https://docs.microsoft.com/windows/desktop/api/mfmediaengine/ne-mfmediaengine-mf_media_engine_err">MF_MEDIA_ENGINE_ERR</a> enumeration.</td>
</tr>
<tr>
<td><i>param2</i></td>
<td>An <b>HRESULT</b> error code, or zero.</td>
</tr>
</table>
 


### -field MF_MEDIA_ENGINE_EVENT_EMPTIED

The Media Engine has switched to the <b>MF_MEDIA_ENGINE_NETWORK_EMPTY</b> state. This can occur when the <a href="https://docs.microsoft.com/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengine-load">IMFMediaEngine::Load</a> method is called, or if an error occurs during the <b>Load</b> method. See <a href="https://docs.microsoft.com/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengine-getnetworkstate">IMFMediaEngine::GetNetworkState</a>.


### -field MF_MEDIA_ENGINE_EVENT_STALLED

The <a href="https://docs.microsoft.com/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengine-load">Load</a> algorithm is stalled, waiting for data.


### -field MF_MEDIA_ENGINE_EVENT_PLAY

The Media Engine is switching to the playing state. See <a href="https://docs.microsoft.com/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengine-play">IMFMediaEngine::Play</a>.


### -field MF_MEDIA_ENGINE_EVENT_PAUSE

The media engine has paused. See <a href="https://docs.microsoft.com/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengine-pause">IMFMediaEngine::Pause</a>.


### -field MF_MEDIA_ENGINE_EVENT_LOADEDMETADATA

The Media Engine has loaded enough source data to determine the duration and dimensions  of the source.


### -field MF_MEDIA_ENGINE_EVENT_LOADEDDATA

The Media Engine has loaded enough data to render some content (for example, a video frame).


### -field MF_MEDIA_ENGINE_EVENT_WAITING

Playback has stopped because the next frame is not available.


### -field MF_MEDIA_ENGINE_EVENT_PLAYING

Playback has started. See <a href="https://docs.microsoft.com/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengine-play">IMFMediaEngine::Play</a>.


### -field MF_MEDIA_ENGINE_EVENT_CANPLAY

Playback can start, but the Media Engine might need to stop to buffer more data.


### -field MF_MEDIA_ENGINE_EVENT_CANPLAYTHROUGH

The Media Engine can probably play through to the end of the resource, without stopping to buffer data.


### -field MF_MEDIA_ENGINE_EVENT_SEEKING

The Media Engine has started seeking to a new playback position. See <a href="https://docs.microsoft.com/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengine-setcurrenttime">IMFMediaEngine::SetCurrentTime</a>.


### -field MF_MEDIA_ENGINE_EVENT_SEEKED

The Media Engine has seeked to a new playback position. See <a href="https://docs.microsoft.com/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengine-setcurrenttime">IMFMediaEngine::SetCurrentTime</a>.


### -field MF_MEDIA_ENGINE_EVENT_TIMEUPDATE

The playback position has changed. See <a href="https://docs.microsoft.com/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengine-getcurrenttime">IMFMediaEngine::GetCurrentTime</a>.


### -field MF_MEDIA_ENGINE_EVENT_ENDED

Playback has reached the end of the source. This event is not sent if the <a href="https://docs.microsoft.com/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengine-getloop">GetLoop</a>is <b>TRUE</b>.


### -field MF_MEDIA_ENGINE_EVENT_RATECHANGE

The playback rate has changed. See <a href="https://docs.microsoft.com/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengine-setplaybackrate">IMFMediaEngine::SetPlaybackRate</a>.


### -field MF_MEDIA_ENGINE_EVENT_DURATIONCHANGE

The duration of the media source has changed. See <a href="https://docs.microsoft.com/windows/desktop/api/mfplay/nf-mfplay-imfpmediaitem-getduration">IMFMediaEngine::GetDuration</a>.


### -field MF_MEDIA_ENGINE_EVENT_VOLUMECHANGE

The audio volume changed. See <a href="https://docs.microsoft.com/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengine-setvolume">IMFMediaEngine::SetVolume</a>.


### -field MF_MEDIA_ENGINE_EVENT_FORMATCHANGE

The output format of the media source has changed.

<table>
<tr>
<th>Event Parameter</th>
<th>Description</th>
</tr>
<tr>
<td><i>param1</i></td>
<td>Zero if the video format changed, 1 if the audio format changed.</td>
</tr>
<tr>
<td><i>param2</i></td>
<td>Zero.</td>
</tr>
</table>
 


### -field MF_MEDIA_ENGINE_EVENT_PURGEQUEUEDEVENTS

The Media Engine flushed any pending events from its 	queue.


### -field MF_MEDIA_ENGINE_EVENT_TIMELINE_MARKER

The playback position reached a timeline marker. See <a href="https://docs.microsoft.com/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengineex-settimelinemarkertimer">IMFMediaEngineEx::SetTimelineMarkerTimer</a>.


### -field MF_MEDIA_ENGINE_EVENT_BALANCECHANGE

The audio balance changed. See <a href="https://docs.microsoft.com/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengineex-setbalance">IMFMediaEngineEx::SetBalance</a>.


### -field MF_MEDIA_ENGINE_EVENT_DOWNLOADCOMPLETE

The Media Engine has finished downloading the source data.


### -field MF_MEDIA_ENGINE_EVENT_BUFFERINGSTARTED

The media source has started to buffer data.


### -field MF_MEDIA_ENGINE_EVENT_BUFFERINGENDED

The media source has stopped buffering data.


### -field MF_MEDIA_ENGINE_EVENT_FRAMESTEPCOMPLETED

The <a href="https://docs.microsoft.com/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengineex-framestep">IMFMediaEngineEx::FrameStep</a> method completed.


### -field MF_MEDIA_ENGINE_EVENT_NOTIFYSTABLESTATE

The Media Engine's <a href="https://docs.microsoft.com/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengine-load">Load</a> algorithm is waiting to start.

<table>
<tr>
<th>Event Parameter</th>
<th>Description</th>
</tr>
<tr>
<td><i>param1</i></td>
<td>A handle to a waitable event, of type <b>HANDLE</b>.</td>
</tr>
<tr>
<td><i>param2</i></td>
<td>Zero.</td>
</tr>
</table>
 

If Media Engine is created with the <b>MF_MEDIA_ENGINE_WAITFORSTABLE_STATE</b> flag, the Media Engine sends the <b>MF_MEDIA_ENGINE_EVENT_NOTIFYSTABLESTATE</b> event at the start of the <a href="https://docs.microsoft.com/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengine-load">Load</a> algorithm. The <i>param1</i> parameter is a handle to a waitable event. The <b>Load</b> thread waits for the application to signal the event by calling <a href="https://docs.microsoft.com/windows/desktop/api/synchapi/nf-synchapi-setevent">SetEvent</a>.

If the Media Engine is not created with the <b>MF_MEDIA_ENGINE_WAITFORSTABLE_STATE</b>, it does not send this event, and the <a href="https://docs.microsoft.com/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengine-load">Load</a> thread does not wait to be signalled.


### -field MF_MEDIA_ENGINE_EVENT_FIRSTFRAMEREADY

The first frame of the media source is ready to render.


### -field MF_MEDIA_ENGINE_EVENT_TRACKSCHANGE

Raised when a new track is added or removed.

Supported in Windows 8.1 and later.


### -field MF_MEDIA_ENGINE_EVENT_OPMINFO

Raised when there is new information about the <a href="https://docs.microsoft.com/windows/desktop/medfound/output-protection-manager">Output Protection Manager</a>  (OPM). 

This event will be raised when an OPM failure occurs, but ITA allows fallback without the OPM. In this case, constriction can be applied. 

This event will not be raised when there is an OPM failure and the fallback also fails. For example, if ITA blocks playback entirely when OPM cannot be established.

Supported in Windows 8.1 and later.


### -field MF_MEDIA_ENGINE_EVENT_RESOURCELOST


### -field MF_MEDIA_ENGINE_EVENT_DELAYLOADEVENT_CHANGED


### -field MF_MEDIA_ENGINE_EVENT_STREAMRENDERINGERROR

Raised when one of the component streams of a media stream fails. This event is only raised if the media stream contains other component streams that did not fail.


### -field MF_MEDIA_ENGINE_EVENT_SUPPORTEDRATES_CHANGED


### -field MF_MEDIA_ENGINE_EVENT_AUDIOENDPOINTCHANGE




## -remarks



The application receives Media Engine events through the <a href="https://docs.microsoft.com/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaenginenotify-eventnotify">IMFMediaEngineNotify::EventNotify</a> method. The <b>EventNotify</b> method includes two event parameters, <i>param1</i> and <i>param2</i>. The meaning of the parameters depends on the event code. If the event description does not list any parameters, ignore the values of <i>param1</i> and <i>param2</i>.

Values below 1000 correspond to events defined in HTML 5 for media elements.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaenginenotify-eventnotify">IMFMediaEngineNotify::EventNotify</a>



<a href="https://docs.microsoft.com/windows/desktop/medfound/media-foundation-enumerations">Media Foundation Enumerations</a>
 

 

