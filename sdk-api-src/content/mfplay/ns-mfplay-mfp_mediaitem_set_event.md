---
UID: NS:mfplay.MFP_MEDIAITEM_SET_EVENT
title: MFP_MEDIAITEM_SET_EVENT (mfplay.h)
description: Event structure for the MFP_EVENT_TYPE_MEDIAITEM_SET event.
helpviewer_keywords: ["MFP_MEDIAITEM_SET_EVENT","MFP_MEDIAITEM_SET_EVENT structure [Media Foundation]","mf.mfp_mediaitem_set_event","mfplay/MFP_MEDIAITEM_SET_EVENT"]
old-location: mf\mfp_mediaitem_set_event.htm
tech.root: mfarchive
archived: true
ms.assetid: 51ff492f-8199-4e1a-8d8b-d86bbb3c98dc
ms.date: 12/05/2018
ms.keywords: MFP_MEDIAITEM_SET_EVENT, MFP_MEDIAITEM_SET_EVENT structure [Media Foundation], mf.mfp_mediaitem_set_event, mfplay/MFP_MEDIAITEM_SET_EVENT
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
req.typenames: MFP_MEDIAITEM_SET_EVENT
req.redist: 
ms.custom: 19H1
f1_keywords:
 - MFP_MEDIAITEM_SET_EVENT
 - mfplay/MFP_MEDIAITEM_SET_EVENT
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
 - MFP_MEDIAITEM_SET_EVENT
---

# MFP_MEDIAITEM_SET_EVENT structure


## -description

\[The feature associated with this page, MFPlay, is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer) and  [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer** and **IMFMediaEngine** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]


Event structure for the <b>MFP_EVENT_TYPE_MEDIAITEM_SET</b> event. This event is sent when the <a href="/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-setmediaitem">IMFPMediaPlayer::SetMediaItem</a> method completes.

## -struct-fields

### -field header

<a href="/windows/desktop/api/mfplay/ns-mfplay-mfp_event_header">MFP_EVENT_HEADER</a> structure that contains data common to all <a href="/windows/desktop/api/mfplay/nn-mfplay-imfpmediaplayer">IMFPMediaPlayer</a> events.

### -field pMediaItem

A pointer to the <a href="/windows/desktop/api/mfplay/nn-mfplay-imfpmediaitem">IMFPMediaItem</a> interface of the media item that was queued for playback.

## -remarks

To get a pointer to this structure, cast the <i>pEventHeader</i> parameter of the <a href="/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayercallback-onmediaplayerevent">IMFPMediaPlayerCallback::OnMediaPlayerEvent</a>  method.  You can use the <a href="/windows/desktop/api/mfplay/nf-mfplay-mfp_get_mediaitem_set_event">MFP_GET_MEDIAITEM_SET_EVENT</a> macro for this purpose.

If one or more streams could not be connected to a media sink, the event property store contains the <a href="/windows/desktop/medfound/mfp-pkey-streamrenderingresults">MFP_PKEY_StreamRenderingResults</a> property. The value of the property is an array of <b>HRESULT</b> values, indicating which streams were connected successfully.  The event property store can be accessed through the <b>header.pPropertyStore</b> member.

## -see-also

<a href="/windows/desktop/api/mfplay/nn-mfplay-imfpmediaplayercallback">IMFPMediaPlayerCallback</a>



<a href="/windows/desktop/medfound/media-foundation-structures">Media Foundation Structures</a>



<a href="/windows/desktop/medfound/using-mfplay-for-audio-video-playback">Using MFPlay for Audio/Video Playback</a>