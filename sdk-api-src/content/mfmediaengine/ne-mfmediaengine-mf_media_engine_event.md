---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# MF_MEDIA_ENGINE_EVENT enumeration


## -description


Defines event codes for the Media Engine. 


## -enum-fields




### -field MF_MEDIA_ENGINE_EVENT_LOADSTART

The Media Engine has started to load the source. See <a href="https://msdn.microsoft.com/5ACE8143-DC14-495C-A644-A2076FB1980F">IMFMediaEngine::Load</a>.


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
<td>A member of the <a href="https://msdn.microsoft.com/CFA5C2AF-C804-47B4-B76A-907F26CF3DFC">MF_MEDIA_ENGINE_ERR</a> enumeration.</td>
</tr>
<tr>
<td><i>param2</i></td>
<td>An <b>HRESULT</b> error code, or zero.</td>
</tr>
</table>
 


### -field MF_MEDIA_ENGINE_EVENT_EMPTIED

The Media Engine has switched to the <b>MF_MEDIA_ENGINE_NETWORK_EMPTY</b> state. This can occur when the <a href="https://msdn.microsoft.com/5ACE8143-DC14-495C-A644-A2076FB1980F">IMFMediaEngine::Load</a> method is called, or if an error occurs during the <b>Load</b> method. See <a href="https://msdn.microsoft.com/7CCA902A-51E9-4B6D-B16C-643177BE1BC9">IMFMediaEngine::GetNetworkState</a>.


### -field MF_MEDIA_ENGINE_EVENT_STALLED

The <a href="https://msdn.microsoft.com/5ACE8143-DC14-495C-A644-A2076FB1980F">Load</a> algorithm is stalled, waiting for data.


### -field MF_MEDIA_ENGINE_EVENT_PLAY

The Media Engine is switching to the playing state. See <a href="https://msdn.microsoft.com/2D6083F5-734A-4350-8E54-56C79038389D">IMFMediaEngine::Play</a>.


### -field MF_MEDIA_ENGINE_EVENT_PAUSE

The media engine has paused. See <a href="https://msdn.microsoft.com/5C1FEBDA-18B5-4BF4-9AF4-FF6DBCDD880D">IMFMediaEngine::Pause</a>.


### -field MF_MEDIA_ENGINE_EVENT_LOADEDMETADATA

The Media Engine has loaded enough source data to determine the duration and dimensions  of the source.


### -field MF_MEDIA_ENGINE_EVENT_LOADEDDATA

The Media Engine has loaded enough data to render some content (for example, a video frame).


### -field MF_MEDIA_ENGINE_EVENT_WAITING

Playback has stopped because the next frame is not available.


### -field MF_MEDIA_ENGINE_EVENT_PLAYING

Playback has started. See <a href="https://msdn.microsoft.com/2D6083F5-734A-4350-8E54-56C79038389D">IMFMediaEngine::Play</a>.


### -field MF_MEDIA_ENGINE_EVENT_CANPLAY

Playback can start, but the Media Engine might need to stop to buffer more data.


### -field MF_MEDIA_ENGINE_EVENT_CANPLAYTHROUGH

The Media Engine can probably play through to the end of the resource, without stopping to buffer data.


### -field MF_MEDIA_ENGINE_EVENT_SEEKING

The Media Engine has started seeking to a new playback position. See <a href="https://msdn.microsoft.com/C64BCBA0-097E-4035-BFEE-F9EC949B109A">IMFMediaEngine::SetCurrentTime</a>.


### -field MF_MEDIA_ENGINE_EVENT_SEEKED

The Media Engine has seeked to a new playback position. See <a href="https://msdn.microsoft.com/C64BCBA0-097E-4035-BFEE-F9EC949B109A">IMFMediaEngine::SetCurrentTime</a>.


### -field MF_MEDIA_ENGINE_EVENT_TIMEUPDATE

The playback position has changed. See <a href="https://msdn.microsoft.com/49FA2383-8AEC-4DDF-8998-25987EEC8223">IMFMediaEngine::GetCurrentTime</a>.


### -field MF_MEDIA_ENGINE_EVENT_ENDED

Playback has reached the end of the source. This event is not sent if the <a href="https://msdn.microsoft.com/EBAB4E73-164D-4AE5-87A4-0D37C10071E9">GetLoop</a>is <b>TRUE</b>.


### -field MF_MEDIA_ENGINE_EVENT_RATECHANGE

The playback rate has changed. See <a href="https://msdn.microsoft.com/648BF1CC-BFAC-4874-808B-F8B46E3E9989">IMFMediaEngine::SetPlaybackRate</a>.


### -field MF_MEDIA_ENGINE_EVENT_DURATIONCHANGE

The duration of the media source has changed. See <a href="https://msdn.microsoft.com/831f023b-c06f-4099-9f4c-df38f3d1382f">IMFMediaEngine::GetDuration</a>.


### -field MF_MEDIA_ENGINE_EVENT_VOLUMECHANGE

The audio volume changed. See <a href="https://msdn.microsoft.com/010EE05C-3F81-404E-8AFB-7C57CA55A8AE">IMFMediaEngine::SetVolume</a>.


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

The playback position reached a timeline marker. See <a href="https://msdn.microsoft.com/2FD65E4A-C70A-4CB4-9038-3A8B791E251C">IMFMediaEngineEx::SetTimelineMarkerTimer</a>.


### -field MF_MEDIA_ENGINE_EVENT_BALANCECHANGE

The audio balance changed. See <a href="https://msdn.microsoft.com/11187826-B873-4182-A77B-FD9CCECFBAE5">IMFMediaEngineEx::SetBalance</a>.


### -field MF_MEDIA_ENGINE_EVENT_DOWNLOADCOMPLETE

The Media Engine has finished downloading the source data.


### -field MF_MEDIA_ENGINE_EVENT_BUFFERINGSTARTED

The media source has started to buffer data.


### -field MF_MEDIA_ENGINE_EVENT_BUFFERINGENDED

The media source has stopped buffering data.


### -field MF_MEDIA_ENGINE_EVENT_FRAMESTEPCOMPLETED

The <a href="https://msdn.microsoft.com/090B5B6F-E4D1-43D7-AD09-BA3008B48104">IMFMediaEngineEx::FrameStep</a> method completed.


### -field MF_MEDIA_ENGINE_EVENT_NOTIFYSTABLESTATE

The Media Engine's <a href="https://msdn.microsoft.com/5ACE8143-DC14-495C-A644-A2076FB1980F">Load</a> algorithm is waiting to start.

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
 

If Media Engine is created with the <b>MF_MEDIA_ENGINE_WAITFORSTABLE_STATE</b> flag, the Media Engine sends the <b>MF_MEDIA_ENGINE_EVENT_NOTIFYSTABLESTATE</b> event at the start of the <a href="https://msdn.microsoft.com/5ACE8143-DC14-495C-A644-A2076FB1980F">Load</a> algorithm. The <i>param1</i> parameter is a handle to a waitable event. The <b>Load</b> thread waits for the application to signal the event by calling <a href="https://msdn.microsoft.com/b474eef1-5df9-4729-b940-0c5f201c5f31">SetEvent</a>.

If the Media Engine is not created with the <b>MF_MEDIA_ENGINE_WAITFORSTABLE_STATE</b>, it does not send this event, and the <a href="https://msdn.microsoft.com/5ACE8143-DC14-495C-A644-A2076FB1980F">Load</a> thread does not wait to be signalled.


### -field MF_MEDIA_ENGINE_EVENT_FIRSTFRAMEREADY

The first frame of the media source is ready to render.


### -field MF_MEDIA_ENGINE_EVENT_TRACKSCHANGE

Raised when a new track is added or removed.

Supported in Windows 8.1 and later.


### -field MF_MEDIA_ENGINE_EVENT_OPMINFO

Raised when there is new information about the <a href="https://msdn.microsoft.com/daae615b-37c4-4044-91c6-693357e0016a">Output Protection Manager</a>  (OPM). 

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



The application receives Media Engine events through the <a href="https://msdn.microsoft.com/F6B9E025-53C4-4459-9EC4-EA228065FAD3">IMFMediaEngineNotify::EventNotify</a> method. The <b>EventNotify</b> method includes two event parameters, <i>param1</i> and <i>param2</i>. The meaning of the parameters depends on the event code. If the event description does not list any parameters, ignore the values of <i>param1</i> and <i>param2</i>.

Values below 1000 correspond to events defined in HTML 5 for media elements.




## -see-also




<a href="https://msdn.microsoft.com/F6B9E025-53C4-4459-9EC4-EA228065FAD3">IMFMediaEngineNotify::EventNotify</a>



<a href="https://msdn.microsoft.com/f26a730f-18c4-4247-acaf-af1dfad19086">Media Foundation Enumerations</a>
 

 

