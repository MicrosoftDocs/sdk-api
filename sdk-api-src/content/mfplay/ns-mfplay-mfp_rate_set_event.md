---
UID: NS:mfplay.MFP_RATE_SET_EVENT
title: MFP_RATE_SET_EVENT (mfplay.h)
description: Event structure for the MFP_EVENT_TYPE_RATE_SET event.
helpviewer_keywords: ["MFP_RATE_SET_EVENT","MFP_RATE_SET_EVENT structure [Media Foundation]","mf.mfp_rate_set_event","mfplay/MFP_RATE_SET_EVENT"]
old-location: mf\mfp_rate_set_event.htm
tech.root: mf
ms.assetid: 19e3bcb0-340a-46dc-bfda-62890ec9a8ae
ms.date: 12/05/2018
ms.keywords: MFP_RATE_SET_EVENT, MFP_RATE_SET_EVENT structure [Media Foundation], mf.mfp_rate_set_event, mfplay/MFP_RATE_SET_EVENT
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
req.typenames: MFP_RATE_SET_EVENT
req.redist: 
ms.custom: 19H1
f1_keywords:
 - MFP_RATE_SET_EVENT
 - mfplay/MFP_RATE_SET_EVENT
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
 - MFP_RATE_SET_EVENT
---

# MFP_RATE_SET_EVENT structure


## -description

<div class="alert"><b>Important</b>  Deprecated. This API may be removed from future releases of Windows. Applications should use the <a href="/windows/desktop/medfound/media-session">Media Session</a> for playback.</div>
<div> </div>


Event structure for the MFP_EVENT_TYPE_RATE_SET event. This event is sent when the <a href="/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-setrate">IMFPMediaPlayer::SetRate</a> method completes.

## -struct-fields

### -field header

<a href="/windows/desktop/api/mfplay/ns-mfplay-mfp_event_header">MFP_EVENT_HEADER</a> structure that contains data common to all <a href="/windows/desktop/api/mfplay/nn-mfplay-imfpmediaplayer">IMFPMediaPlayer</a> events.

### -field pMediaItem

Pointer to the <a href="/windows/desktop/api/mfplay/nn-mfplay-imfpmediaitem">IMFPMediaItem</a> interface of the current media item.

### -field flRate

New playback rate. This value can differ from the requested rate.

## -remarks

To get a pointer to this structure, cast the <i>pEventHeader</i>parameter of the <a href="/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayercallback-onmediaplayerevent">IMFPMediaPlayerCallback::OnMediaPlayerEvent</a>  method.  You can use the <a href="/windows/desktop/api/mfplay/nf-mfplay-mfp_get_rate_set_event">MFP_GET_RATE_SET_EVENT</a> macro for this purpose.

## -see-also

<a href="/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-setrate">IMFPMediaPlayer::SetRate</a>



<a href="/windows/desktop/api/mfplay/nn-mfplay-imfpmediaplayercallback">IMFPMediaPlayerCallback</a>



<a href="/windows/desktop/medfound/media-foundation-structures">Media Foundation Structures</a>



<a href="/windows/desktop/medfound/using-mfplay-for-audio-video-playback">Using MFPlay for Audio/Video Playback</a>