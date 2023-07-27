---
UID: NF:strmif.IAMTunerNotification.OnEvent
title: IAMTunerNotification::OnEvent (strmif.h)
description: Note  The IAMTunerNotification interface is deprecated. The OnEvent method handles events from the TV tuner card.
helpviewer_keywords: ["IAMTunerNotification interface [DirectShow]","OnEvent method","IAMTunerNotification.OnEvent","IAMTunerNotification::OnEvent","IAMTunerNotificationOnEvent","OnEvent","OnEvent method [DirectShow]","OnEvent method [DirectShow]","IAMTunerNotification interface","dshow.iamtunernotification_onevent","strmif/IAMTunerNotification::OnEvent"]
old-location: dshow\iamtunernotification_onevent.htm
tech.root: dshow
ms.assetid: ac28a445-dfa0-4e88-861d-3364106c2b20
ms.date: 4/26/2023
ms.keywords: IAMTunerNotification interface [DirectShow],OnEvent method, IAMTunerNotification.OnEvent, IAMTunerNotification::OnEvent, IAMTunerNotificationOnEvent, OnEvent, OnEvent method [DirectShow], OnEvent method [DirectShow],IAMTunerNotification interface, dshow.iamtunernotification_onevent, strmif/IAMTunerNotification::OnEvent
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
 - IAMTunerNotification::OnEvent
 - strmif/IAMTunerNotification::OnEvent
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
 - IAMTunerNotification.OnEvent
---

# IAMTunerNotification::OnEvent


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

<div class="alert"><b>Note</b>  The <b>IAMTunerNotification</b> interface is deprecated.</div>
<div> </div>
The <code>OnEvent</code> method handles events from the TV tuner card.

## -parameters

### -param Event [in]

Flag identifying the type of event. Currently, the only value defined is AMTUNER_EVENT_CHANGED.

## -returns

Returns an <b>HRESULT</b> value that depends on the implementation of the interface.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-iamtunernotification">IAMTunerNotification Interface</a>