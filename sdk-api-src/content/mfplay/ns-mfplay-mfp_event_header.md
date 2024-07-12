---
UID: NS:mfplay.MFP_EVENT_HEADER
title: MFP_EVENT_HEADER (mfplay.h)
description: Contains information that is common to every type of MFPlay event.
helpviewer_keywords: ["MFP_EVENT_HEADER","MFP_EVENT_HEADER structure [Media Foundation]","mf.mfp_event_header","mfplay/MFP_EVENT_HEADER"]
old-location: mf\mfp_event_header.htm
tech.root: mfarchive
archived: true
ms.assetid: ed9d3790-845a-4392-b755-6a5ce6e20de5
ms.date: 12/05/2018
ms.keywords: MFP_EVENT_HEADER, MFP_EVENT_HEADER structure [Media Foundation], mf.mfp_event_header, mfplay/MFP_EVENT_HEADER
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
req.typenames: MFP_EVENT_HEADER
req.redist: 
ms.custom: 19H1
f1_keywords:
 - MFP_EVENT_HEADER
 - mfplay/MFP_EVENT_HEADER
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
 - MFP_EVENT_HEADER
---

# MFP_EVENT_HEADER structure


## -description

\[The feature associated with this page, MFPlay, is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer) and  [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer** and **IMFMediaEngine** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]


Contains information that is common to  every type of MFPlay event.

## -struct-fields

### -field eEventType

The type of event, specified as a member of the <a href="/windows/desktop/api/mfplay/ne-mfplay-mfp_event_type">MFP_EVENT_TYPE</a> enumeration.

### -field hrEvent

Error or success code for the operation that caused the event.

### -field pMediaPlayer

Pointer to the <a href="/windows/desktop/api/mfplay/nn-mfplay-imfpmediaplayer">IMFPMediaPlayer</a> interface of the MFPlay player object that sent the event.

### -field eState

The new state of the MFPlay player object, specified as a member of the <a href="/windows/desktop/api/mfplay/ne-mfplay-mfp_mediaplayer_state">MFP_MEDIAPLAYER_STATE</a> enumeration.

### -field pPropertyStore

A pointer to the <b>IPropertyStore</b> interface of  a property store object. The property store is used to hold additional event data for some event types. This member might be <b>NULL</b>.

## -see-also

<a href="/windows/desktop/api/mfplay/nn-mfplay-imfpmediaplayercallback">IMFPMediaPlayerCallback</a>



<a href="/windows/desktop/medfound/media-foundation-structures">Media Foundation Structures</a>



<a href="/windows/desktop/medfound/using-mfplay-for-audio-video-playback">Using MFPlay for Audio/Video Playback</a>