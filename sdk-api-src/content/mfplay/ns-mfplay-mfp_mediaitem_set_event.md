---
UID: NS:mfplay.MFP_MEDIAITEM_SET_EVENT
title: MFP_MEDIAITEM_SET_EVENT (mfplay.h)
author: windows-sdk-content
description: Event structure for the MFP_EVENT_TYPE_MEDIAITEM_SET event.
old-location: mf\mfp_mediaitem_set_event.htm
tech.root: medfound
ms.assetid: 51ff492f-8199-4e1a-8d8b-d86bbb3c98dc
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: MFP_MEDIAITEM_SET_EVENT, MFP_MEDIAITEM_SET_EVENT structure [Media Foundation], mf.mfp_mediaitem_set_event, mfplay/MFP_MEDIAITEM_SET_EVENT
ms.topic: struct
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
 - MFP_MEDIAITEM_SET_EVENT
product: Windows
targetos: Windows
req.typenames: MFP_MEDIAITEM_SET_EVENT
req.redist: 
ms.custom: 19H1
---

# MFP_MEDIAITEM_SET_EVENT structure


## -description



<div class="alert"><b>Important</b>  Deprecated. This API may be removed from future releases of Windows. Applications should use the <a href="https://docs.microsoft.com/windows/desktop/medfound/media-session">Media Session</a> for playback.</div>
<div> </div>


Event structure for the <b>MFP_EVENT_TYPE_MEDIAITEM_SET</b> event. This event is sent when the <a href="https://docs.microsoft.com/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-setmediaitem">IMFPMediaPlayer::SetMediaItem</a> method completes.


## -struct-fields




### -field header


<a href="https://docs.microsoft.com/windows/desktop/api/mfplay/ns-mfplay-mfp_event_header">MFP_EVENT_HEADER</a> structure that contains data common to all <a href="https://docs.microsoft.com/windows/desktop/api/mfplay/nn-mfplay-imfpmediaplayer">IMFPMediaPlayer</a> events.


### -field pMediaItem

A pointer to the <a href="https://docs.microsoft.com/windows/desktop/api/mfplay/nn-mfplay-imfpmediaitem">IMFPMediaItem</a> interface of the media item that was queued for playback.


## -remarks



To get a pointer to this structure, cast the <i>pEventHeader</i>parameter of the <a href="https://docs.microsoft.com/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayercallback-onmediaplayerevent">IMFPMediaPlayerCallback::OnMediaPlayerEvent</a>  method.  You can use the <a href="https://docs.microsoft.com/windows/desktop/api/mfplay/nf-mfplay-mfp_get_mediaitem_set_event">MFP_GET_MEDIAITEM_SET_EVENT</a> macro for this purpose.

If one or more streams could not be connected to a media sink, the event property store contains the <a href="https://docs.microsoft.com/windows/desktop/medfound/mfp-pkey-streamrenderingresults">MFP_PKEY_StreamRenderingResults</a> property. The value of the property is an array of <b>HRESULT</b> values, indicating which streams were connected successfully.  The event property store can be accessed through the <b>header.pPropertyStore</b> member.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/mfplay/nn-mfplay-imfpmediaplayercallback">IMFPMediaPlayerCallback</a>



<a href="https://docs.microsoft.com/windows/desktop/medfound/media-foundation-structures">Media Foundation Structures</a>



<a href="https://docs.microsoft.com/windows/desktop/medfound/using-mfplay-for-audio-video-playback">Using MFPlay for Audio/Video Playback</a>
 

 

