---
UID: NS:mfplay.MFP_ERROR_EVENT
title: MFP_ERROR_EVENT (mfplay.h)
description: Event structure for the MFP_EVENT_TYPE_ERROR event.
helpviewer_keywords: ["MFP_ERROR_EVENT","MFP_ERROR_EVENT structure [Media Foundation]","mf.mfp_error_event","mfplay/MFP_ERROR_EVENT"]
old-location: mf\mfp_error_event.htm
tech.root: mf
ms.assetid: 0ccfdefa-4913-4a02-bb91-14df1c185ddf
ms.date: 12/05/2018
ms.keywords: MFP_ERROR_EVENT, MFP_ERROR_EVENT structure [Media Foundation], mf.mfp_error_event, mfplay/MFP_ERROR_EVENT
f1_keywords:
- mfplay/MFP_ERROR_EVENT
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
- MFP_ERROR_EVENT
targetos: Windows
req.typenames: MFP_ERROR_EVENT
req.redist: 
ms.custom: 19H1
---

# MFP_ERROR_EVENT structure


## -description



<div class="alert"><b>Important</b>  Deprecated. This API may be removed from future releases of Windows. Applications should use the <a href="https://docs.microsoft.com/windows/desktop/medfound/media-session">Media Session</a> for playback.</div>
<div> </div>


Event structure for the <b>MFP_EVENT_TYPE_ERROR</b> event. This event is sent if an error occurs during playback.  


## -struct-fields




### -field header


<a href="https://docs.microsoft.com/windows/desktop/api/mfplay/ns-mfplay-mfp_event_header">MFP_EVENT_HEADER</a> structure that contains data common to all <a href="https://docs.microsoft.com/windows/desktop/api/mfplay/nn-mfplay-imfpmediaplayer">IMFPMediaPlayer</a> events. The <b>hrEvent</b> member of the structure contains the error code. 


## -remarks



To get a pointer to this structure, cast the <i>pEventHeader</i>parameter of the <a href="https://docs.microsoft.com/windows/desktop/api/mfplay/nf-mfplay-imfpmediaplayercallback-onmediaplayerevent">IMFPMediaPlayerCallback::OnMediaPlayerEvent</a>  method.  You can use the <a href="https://docs.microsoft.com/windows/desktop/api/mfplay/nf-mfplay-mfp_get_error_event">MFP_GET_ERROR_EVENT</a> macro for this purpose.

This event is not used to signal the failure of an asynchronous <a href="https://docs.microsoft.com/windows/desktop/api/mfplay/nn-mfplay-imfpmediaplayer">IMFPMediaPlayer</a> method. If an asynchronous method fails, the error is reported in the standard event listed for that method. The <b>MFP_EVENT_TYPE_ERROR</b> event is used for errors that happen outside the context of an asynchronous method call.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/mfplay/nn-mfplay-imfpmediaplayercallback">IMFPMediaPlayerCallback</a>



<a href="https://docs.microsoft.com/windows/desktop/medfound/media-foundation-structures">Media Foundation Structures</a>



<a href="https://docs.microsoft.com/windows/desktop/medfound/using-mfplay-for-audio-video-playback">Using MFPlay for Audio/Video Playback</a>
 

 

