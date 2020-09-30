---
UID: NF:strmif.IAMTVAudioNotification.OnEvent
title: IAMTVAudioNotification::OnEvent (strmif.h)
description: Note  The IAMTVAudioNotification interface is deprecated. The OnEvent method handles events from a TV tuner card controlled by the IAMTVAudio interface.
helpviewer_keywords: ["IAMTVAudioNotification interface [DirectShow]","OnEvent method","IAMTVAudioNotification.OnEvent","IAMTVAudioNotification::OnEvent","IAMTVAudioNotificationOnEvent","OnEvent","OnEvent method [DirectShow]","OnEvent method [DirectShow]","IAMTVAudioNotification interface","dshow.iamtvaudionotification_onevent","strmif/IAMTVAudioNotification::OnEvent"]
old-location: dshow\iamtvaudionotification_onevent.htm
tech.root: dshow
ms.assetid: 5282cbbf-5501-42eb-95ba-bf7b32792d56
ms.date: 12/05/2018
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