---
UID: NS:mfplay.MFP_EVENT_HEADER
title: MFP_EVENT_HEADER (mfplay.h)
description: Contains information that is common to every type of MFPlay event.
helpviewer_keywords: ["MFP_EVENT_HEADER","MFP_EVENT_HEADER structure [Media Foundation]","mf.mfp_event_header","mfplay/MFP_EVENT_HEADER"]
old-location: mf\mfp_event_header.htm
tech.root: mf
ms.assetid: ed9d3790-845a-4392-b755-6a5ce6e20de5
ms.date: 12/05/2018
ms.keywords: MFP_EVENT_HEADER, MFP_EVENT_HEADER structure [Media Foundation], mf.mfp_event_header, mfplay/MFP_EVENT_HEADER
f1_keywords:
- mfplay/MFP_EVENT_HEADER
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
- MFP_EVENT_HEADER
targetos: Windows
req.typenames: MFP_EVENT_HEADER
req.redist: 
ms.custom: 19H1
---

# MFP_EVENT_HEADER structure


## -description



<div class="alert"><b>Important</b>  Deprecated. This API may be removed from future releases of Windows. Applications should use the <a href="https://docs.microsoft.com/windows/desktop/medfound/media-session">Media Session</a> for playback.</div>
<div> </div>


Contains information that is common to  every type of MFPlay event.


## -struct-fields




### -field eEventType

The type of event, specified as a member of the <a href="https://docs.microsoft.com/windows/desktop/api/mfplay/ne-mfplay-mfp_event_type">MFP_EVENT_TYPE</a> enumeration.


### -field hrEvent

Error or success code for the operation that caused the event.


### -field pMediaPlayer

Pointer to the <a href="https://docs.microsoft.com/windows/desktop/api/mfplay/nn-mfplay-imfpmediaplayer">IMFPMediaPlayer</a> interface of the MFPlay player object that sent the event.


### -field eState

The new state of the MFPlay player object, specified as a member of the <a href="https://docs.microsoft.com/windows/desktop/api/mfplay/ne-mfplay-mfp_mediaplayer_state">MFP_MEDIAPLAYER_STATE</a> enumeration.


### -field pPropertyStore

A pointer to the <b>IPropertyStore</b> interface of  a property store object. The property store is used to hold additional event data for some event types. This member might be <b>NULL</b>.


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/mfplay/nn-mfplay-imfpmediaplayercallback">IMFPMediaPlayerCallback</a>



<a href="https://docs.microsoft.com/windows/desktop/medfound/media-foundation-structures">Media Foundation Structures</a>



<a href="https://docs.microsoft.com/windows/desktop/medfound/using-mfplay-for-audio-video-playback">Using MFPlay for Audio/Video Playback</a>
 

 

