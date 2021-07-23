---
UID: NF:mfmediaengine.IMFMediaEngine.SetCurrentTime
title: IMFMediaEngine::SetCurrentTime (mfmediaengine.h)
description: Seeks to a new playback position.
helpviewer_keywords: ["IMFMediaEngine interface [Media Foundation]","SetCurrentTime method","IMFMediaEngine.SetCurrentTime","IMFMediaEngine::SetCurrentTime","SetCurrentTime","SetCurrentTime method [Media Foundation]","SetCurrentTime method [Media Foundation]","IMFMediaEngine interface","mf.imfmediaengine_setcurrenttime","mfmediaengine/IMFMediaEngine::SetCurrentTime"]
old-location: mf\imfmediaengine_setcurrenttime.htm
tech.root: mf
ms.assetid: C64BCBA0-097E-4035-BFEE-F9EC949B109A
ms.date: 12/05/2018
ms.keywords: IMFMediaEngine interface [Media Foundation],SetCurrentTime method, IMFMediaEngine.SetCurrentTime, IMFMediaEngine::SetCurrentTime, SetCurrentTime, SetCurrentTime method [Media Foundation], SetCurrentTime method [Media Foundation],IMFMediaEngine interface, mf.imfmediaengine_setcurrenttime, mfmediaengine/IMFMediaEngine::SetCurrentTime
req.header: mfmediaengine.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps \| UWP apps]
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
 - IMFMediaEngine::SetCurrentTime
 - mfmediaengine/IMFMediaEngine::SetCurrentTime
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfmediaengine.h
api_name:
 - IMFMediaEngine.SetCurrentTime
---

# IMFMediaEngine::SetCurrentTime


## -description

Seeks to a new playback position.

## -parameters

### -param seekTime [in]

The new playback position, in seconds.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

This method corresponds to setting the <b>currentTime</b> attribute of the <b>HTMLMediaElement</b> interface in HTML5.

The method completes asynchronously. When the seek operation starts, the Media Engine sends an <b>MF_MEDIA_ENGINE_EVENT_SEEKING</b> event. When the seek operation completes, the Media Engine sends an <b>MF_MEDIA_ENGINE_EVENT_SEEKED</b> event. See <a href="/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaenginenotify-eventnotify">IMFMediaEventNotify::EventNotify</a>.

## -see-also

<a href="/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediaengine">IMFMediaEngine</a>