---
UID: NF:strmif.IAMTVAudio.RegisterNotificationCallBack
title: IAMTVAudio::RegisterNotificationCallBack (strmif.h)
description: The RegisterNotificationCallBack method enables an object that implements the IAMTunerNotification interface to receive event notifications when the tuner changes state.
helpviewer_keywords: ["IAMTVAudio interface [DirectShow]","RegisterNotificationCallBack method","IAMTVAudio.RegisterNotificationCallBack","IAMTVAudio::RegisterNotificationCallBack","IAMTVAudioRegisterNotificationCallBack","RegisterNotificationCallBack","RegisterNotificationCallBack method [DirectShow]","RegisterNotificationCallBack method [DirectShow]","IAMTVAudio interface","dshow.iamtvaudio_registernotificationcallback","strmif/IAMTVAudio::RegisterNotificationCallBack"]
old-location: dshow\iamtvaudio_registernotificationcallback.htm
tech.root: dshow
ms.assetid: dfd8d0b3-e90f-4f77-9a26-0a4db03041ee
ms.date: 4/26/2023
ms.keywords: IAMTVAudio interface [DirectShow],RegisterNotificationCallBack method, IAMTVAudio.RegisterNotificationCallBack, IAMTVAudio::RegisterNotificationCallBack, IAMTVAudioRegisterNotificationCallBack, RegisterNotificationCallBack, RegisterNotificationCallBack method [DirectShow], RegisterNotificationCallBack method [DirectShow],IAMTVAudio interface, dshow.iamtvaudio_registernotificationcallback, strmif/IAMTVAudio::RegisterNotificationCallBack
req.header: strmif.h
req.include-header: Dshow.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Strmiids.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IAMTVAudio::RegisterNotificationCallBack
 - strmif/IAMTVAudio::RegisterNotificationCallBack
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmiids.lib
 - Strmiids.dll
api_name:
 - IAMTVAudio.RegisterNotificationCallBack
---

# IAMTVAudio::RegisterNotificationCallBack


## -description

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer), [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine), and [Audio/Video Capture in Media Foundation](/windows/win32/medfound/audio-video-capture-in-media-foundation). Those features have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer**, **IMFMediaEngine** and **Audio/Video Capture in Media Foundation** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The <code>RegisterNotificationCallBack</code> method enables an object that implements the <a href="/windows/desktop/api/strmif/nn-strmif-iamtunernotification">IAMTunerNotification</a> interface to receive event notifications when the tuner changes state.



This method is not implemented.

## -parameters

### -param pNotify [in]

Pointer to the <a href="/windows/desktop/api/strmif/nn-strmif-iamtunernotification">IAMTunerNotification</a> interface that will receive the event notifications.

### -param lEvents [in]

Flag indicating that an event has occurred.

## -returns

Returns E_NOTIMPL.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/strmif/nn-strmif-iamtvaudio">IAMTVAudio Interface</a>