---
UID: NS:mfplay.MFP_MEDIAITEM_CREATED_EVENT
title: MFP_MEDIAITEM_CREATED_EVENT (mfplay.h)
description: Event structure for the MFP_EVENT_TYPE_MEDIAITEM_CREATED event.
helpviewer_keywords: ["MFP_MEDIAITEM_CREATED_EVENT","MFP_MEDIAITEM_CREATED_EVENT structure [Media Foundation]","mf.mfp_mediaitem_created_event","mfplay/MFP_MEDIAITEM_CREATED_EVENT"]
old-location: mf\mfp_mediaitem_created_event.htm
tech.root: mf
ms.assetid: 68e4076f-c03c-4780-9731-67eb6e78ec8b
ms.date: 12/05/2018
ms.keywords: MFP_MEDIAITEM_CREATED_EVENT, MFP_MEDIAITEM_CREATED_EVENT structure [Media Foundation], mf.mfp_mediaitem_created_event, mfplay/MFP_MEDIAITEM_CREATED_EVENT
f1_keywords:
- mfplay/MFP_MEDIAITEM_CREATED_EVENT
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
- MFP_MEDIAITEM_CREATED_EVENT
targetos: Windows
req.typenames: MFP_MEDIAITEM_CREATED_EVENT
req.redist: 
ms.custom: 19H1
---

# MFP_MEDIAITEM_CREATED_EVENT structure


## -description



<div class="alert"><b>Important</b>  Deprecated. This API may be removed from future releases of Windows. Applications should use the <a href="https://docs.microsoft.com/windows/desktop/medfound/media-session">Media Session</a> for playback.</div>
<div> </div>


Event structure for the <b>MFP_EVENT_TYPE_MEDIAITEM_CREATED</b> event. This event is sent when the <a href="https://docs.microsoft.com/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-createmediaitemfromurl">IMFPMediaPlayer::CreateMediaItemFromURL</a> or  <a href="https://docs.microsoft.com/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-createmediaitemfromobject">IMFPMediaPlayer::CreateMediaItemFromObject</a> method completes.


## -struct-fields




### -field header


<a href="https://docs.microsoft.com/windows/desktop/api/mfplay/ns-mfplay-mfp_event_header">MFP_EVENT_HEADER</a> structure that contains data common to all <a href="https://docs.microsoft.com/windows/desktop/api/mfplay/nn-mfplay-imfpmediaplayer">IMFPMediaPlayer</a> events.


### -field pMediaItem

Pointer to the <a href="https://docs.microsoft.com/windows/desktop/api/mfplay/nn-mfplay-imfpmediaitem">IMFPMediaItem</a> interface of the new media item. If creating the media item failed, this member is <b>NULL</b>.


### -field dwUserData

Application-defined user data for the media item. This value is specified when the application calls <a href="https://docs.microsoft.com/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-createmediaitemfromurl">CreateMediaItemFromURL</a> or  <a href="https://docs.microsoft.com/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayer-createmediaitemfromobject">CreateMediaItemFromObject</a>.


## -remarks



To get a pointer to this structure, cast the <i>pEventHeader</i>parameter of the <a href="https://docs.microsoft.com/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayercallback-onmediaplayerevent">IMFPMediaPlayerCallback::OnMediaPlayerEvent</a>  method.  You can use the <a href="https://docs.microsoft.com/windows/desktop/api/mfplay/nf-mfplay-mfp_get_mediaitem_created_event">MFP_GET_MEDIAITEM_CREATED_EVENT</a> macro for this purpose.

Media items are created asynchronously. If multiple items are created, the operations can complete in any order, not necessarily in the same order as the method calls. You can use  the <b>dwUserData</b> member to identify the items, if you have simultaneous requests pending. 




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/mfplay/nn-mfplay-imfpmediaplayercallback">IMFPMediaPlayerCallback</a>



<a href="https://docs.microsoft.com/windows/desktop/medfound/media-foundation-structures">Media Foundation Structures</a>



<a href="https://docs.microsoft.com/windows/desktop/medfound/using-mfplay-for-audio-video-playback">Using MFPlay for Audio/Video Playback</a>
 

 

