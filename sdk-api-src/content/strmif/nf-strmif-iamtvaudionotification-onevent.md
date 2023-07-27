---
UID: NF:strmif.IAMTVAudioNotification.OnEvent
title: IAMTVAudioNotification::OnEvent (strmif.h)
description: Note  The IAMTVAudioNotification interface is deprecated. The OnEvent method handles events from a TV tuner card controlled by the IAMTVAudio interface.
helpviewer_keywords: ["IAMTVAudioNotification interface [DirectShow]","OnEvent method","IAMTVAudioNotification.OnEvent","IAMTVAudioNotification::OnEvent","IAMTVAudioNotificationOnEvent","OnEvent","OnEvent method [DirectShow]","OnEvent method [DirectShow]","IAMTVAudioNotification interface","dshow.iamtvaudionotification_onevent","strmif/IAMTVAudioNotification::OnEvent"]
old-location: dshow\iamtvaudionotification_onevent.htm
tech.root: dshow
ms.assetid: 5282cbbf-5501-42eb-95ba-bf7b32792d56
ms.date: 4/26/2023
ms.keywords: IAMTVAudioNotification interface [DirectShow],OnEvent method, IAMTVAudioNotification.OnEvent, IAMTVAudioNotification::OnEvent, IAMTVAudioNotificationOnEvent, OnEvent, OnEvent method [DirectShow], OnEvent method [DirectShow],IAMTVAudioNotification interface, dshow.iamtvaudionotification_onevent, strmif/IAMTVAudioNotification::OnEvent
req.header: strmif.h
req.include-header: Dshow.h
req.target-type: Windows
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IAMTVAudioNotification::OnEvent
 - strmif/IAMTVAudioNotification::OnEvent
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmif.h
api_name:
 - IAMTVAudioNotification.OnEvent
---

# IAMTVAudioNotification::OnEvent


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

<div class="alert"><b>Note</b>  The <b>IAMTVAudioNotification</b> interface is deprecated.</div>
<div> </div>
The <code>OnEvent</code> method handles events from a TV tuner card controlled by the <a href="/windows/desktop/api/strmif/nn-strmif-iamtvaudio">IAMTVAudio</a> interface.

## -parameters

### -param Event [in]

Flag identifying the type of event. The only value currently defined is AMTVAUDIO_EVENT_CHANGED.

## -returns

Returns an <b>HRESULT</b> value that depends on the implementation of the interface.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-iamtvaudionotification">IAMTVAudioNotification Interface</a>