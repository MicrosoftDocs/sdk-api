---
UID: NS:mfplay.MFP_MF_EVENT
title: MFP_MF_EVENT (mfplay.h)
description: Event structure for the MFP_EVENT_TYPE_MF event.
helpviewer_keywords: ["MFP_MF_EVENT","MFP_MF_EVENT structure [Media Foundation]","mf.mfp_mf_event","mfplay/MFP_MF_EVENT"]
old-location: mf\mfp_mf_event.htm
tech.root: mfarchive
archived: true
ms.assetid: 61dec86d-919c-4b1b-ab2a-527d062ae0f8
ms.date: 12/05/2018
ms.keywords: MFP_MF_EVENT, MFP_MF_EVENT structure [Media Foundation], mf.mfp_mf_event, mfplay/MFP_MF_EVENT
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
req.typenames: MFP_MF_EVENT
req.redist: 
ms.custom: 19H1
f1_keywords:
 - MFP_MF_EVENT
 - mfplay/MFP_MF_EVENT
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - mfplay.h
api_name:
 - MFP_MF_EVENT
---

# MFP_MF_EVENT structure


## -description

\[The feature associated with this page, MFPlay, is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer) and  [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer** and **IMFMediaEngine** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]


Event structure for the <b>MFP_EVENT_TYPE_MF</b> event. The MFPlay player object uses this event to forward certain events from the Media Foundation pipeline to the application.

## -struct-fields

### -field header

<a href="/windows/desktop/api/mfplay/ns-mfplay-mfp_event_header">MFP_EVENT_HEADER</a> structure that contains data common to all <a href="/windows/desktop/api/mfplay/nn-mfplay-imfpmediaplayer">IMFPMediaPlayer</a> events.

### -field MFEventType

Media Foundation event type. Currently, the MFPlay player object forwards the following pipeline events to the application:

<table>
<tr>
<th>Event</th>
<th>Description</th>
</tr>
<tr>
<td>
<a href="/windows/desktop/medfound/mebufferingstarted">MEBufferingStarted</a>
</td>
<td>The source has started buffering data.</td>
</tr>
<tr>
<td>
<a href="/windows/desktop/medfound/mebufferingstopped">MEBufferingStopped</a>
</td>
<td>The source has stopped buffering data.</td>
</tr>
<tr>
<td>
<a href="/windows/desktop/medfound/meextendedtype">MEExtendedType</a>
</td>
<td>Custom event type.</td>
</tr>
<tr>
<td>
<a href="/windows/desktop/medfound/mereconnectend">MEReconnectEnd</a>
</td>
<td>The source has completed an attempt to reconnect to the server.</td>
</tr>
<tr>
<td>
<a href="/windows/desktop/medfound/mereconnectstart">MEReconnectStart</a>
</td>
<td>The source is attempting to reconnect to the server.</td>
</tr>
<tr>
<td>
<a href="/windows/desktop/medfound/merendererevent">MERendererEvent</a>
</td>
<td>Event sent by a renderer, such as the <a href="/windows/desktop/medfound/enhanced-video-renderer">Enhanced Video Renderer</a> (EVR).</td>
</tr>
<tr>
<td>
<a href="/windows/desktop/medfound/mestreamsinkformatchanged">MEStreamSinkFormatChanged</a>
</td>
<td>A stream format has changed.</td>
</tr>
</table>

### -field pMFMediaEvent

Pointer to the <a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaevent">IMFMediaEvent</a> interface of the Media Foundation event.

### -field pMediaItem

Pointer to the <a href="/windows/desktop/api/mfplay/nn-mfplay-imfpmediaitem">IMFPMediaItem</a> interface of the current media item.

## -remarks

To get a pointer to this structure, cast the <i>pEventHeader</i> parameter of the <a href="/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayercallback-onmediaplayerevent">IMFPMediaPlayerCallback::OnMediaPlayerEvent</a> method. You can use the <a href="/windows/desktop/api/mfplay/nf-mfplay-mfp_get_mf_event">MFP_GET_MF_EVENT</a> macro for this purpose.

If <b>MFEventType</b> is <a href="/windows/desktop/medfound/mestreamsinkformatchanged">MEStreamSinkFormatChanged</a>, the following property may be stored in the event property store, which can be accessed through the <b>header.pPropertyStore</b> member.

<table>
<tr>
<th>Property</th>
<th>Description</th>
</tr>
<tr>
<td>
<a href="/previous-versions/windows/desktop/legacy/dd375565(v=vs.85)">MFP_PKEY_StreamIndex</a>
</td>
<td>The index of the stream whose format changed. </td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/mfplay/nn-mfplay-imfpmediaplayercallback">IMFPMediaPlayerCallback</a>



<a href="/windows/desktop/medfound/media-foundation-structures">Media Foundation Structures</a>



<a href="/windows/desktop/medfound/using-mfplay-for-audio-video-playback">Using MFPlay for Audio/Video Playback</a>