---
UID: NS:mfplay.MFP_PLAYBACK_ENDED_EVENT
title: MFP_PLAYBACK_ENDED_EVENT (mfplay.h)
description: Event structure for the MFP_EVENT_TYPE_PLAYBACK_ENDED event.helpviewer_keywords: ["MFP_PLAYBACK_ENDED_EVENT","MFP_PLAYBACK_ENDED_EVENT structure [Media Foundation]","mf.mfp_playback_ended_event","mfplay/MFP_PLAYBACK_ENDED_EVENT"]
old-location: mf\mfp_playback_ended_event.htm
tech.root: medfound
ms.assetid: 08cea881-dce9-4170-9b44-9943b014d300
ms.date: 12/05/2018
ms.keywords: MFP_PLAYBACK_ENDED_EVENT, MFP_PLAYBACK_ENDED_EVENT structure [Media Foundation], mf.mfp_playback_ended_event, mfplay/MFP_PLAYBACK_ENDED_EVENT
f1_keywords:
- mfplay/MFP_PLAYBACK_ENDED_EVENT
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
- HeaderDef
api_location:
- mfplay.h
api_name:
- MFP_PLAYBACK_ENDED_EVENT
targetos: Windows
req.typenames: MFP_PLAYBACK_ENDED_EVENT
req.redist: 
ms.custom: 19H1
---

# MFP_PLAYBACK_ENDED_EVENT structure


## -description



<div class="alert"><b>Important</b>  Deprecated. This API may be removed from future releases of Windows. Applications should use the <a href="https://docs.microsoft.com/windows/desktop/medfound/media-session">Media Session</a> for playback.</div>
<div> </div>


Event structure for the <b>MFP_EVENT_TYPE_PLAYBACK_ENDED</b> event. This event is sent when the current media item finishes playing.


## -struct-fields




### -field header


<a href="https://docs.microsoft.com/windows/desktop/api/mfplay/ns-mfplay-mfp_event_header">MFP_EVENT_HEADER</a> structure that contains data common to all <a href="https://docs.microsoft.com/windows/desktop/api/mfplay/nn-mfplay-imfpmediaplayer">IMFPMediaPlayer</a> events.


### -field pMediaItem

Pointer to the <a href="https://docs.microsoft.com/windows/desktop/api/mfplay/nn-mfplay-imfpmediaitem">IMFPMediaItem</a> interface of the media item that has just ended.


## -remarks



To get a pointer to this structure, cast the <i>pEventHeader</i>parameter of the <a href="https://docs.microsoft.com/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayercallback-onmediaplayerevent">IMFPMediaPlayerCallback::OnMediaPlayerEvent</a>  method.  You can use the <a href="https://docs.microsoft.com/windows/desktop/api/mfplay/nf-mfplay-mfp_get_playback_ended_event">MFP_GET_PLAYBACK_ENDED_EVENT</a> macro for this purpose.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/mfplay/nn-mfplay-imfpmediaplayercallback">IMFPMediaPlayerCallback</a>



<a href="https://docs.microsoft.com/windows/desktop/medfound/media-foundation-structures">Media Foundation Structures</a>



<a href="https://docs.microsoft.com/windows/desktop/medfound/using-mfplay-for-audio-video-playback">Using MFPlay for Audio/Video Playback</a>
 

 

