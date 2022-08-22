---
UID: NF:mfmediaengine.IMFMediaEngine.Play
title: IMFMediaEngine::Play (mfmediaengine.h)
description: Starts playback. (IMFMediaEngine.Play)
helpviewer_keywords: ["IMFMediaEngine interface [Media Foundation]","Play method","IMFMediaEngine.Play","IMFMediaEngine::Play","Play","Play method [Media Foundation]","Play method [Media Foundation]","IMFMediaEngine interface","mf.imfmediaengine_play","mfmediaengine/IMFMediaEngine::Play"]
old-location: mf\imfmediaengine_play.htm
tech.root: mf
ms.assetid: 2D6083F5-734A-4350-8E54-56C79038389D
ms.date: 12/05/2018
ms.keywords: IMFMediaEngine interface [Media Foundation],Play method, IMFMediaEngine.Play, IMFMediaEngine::Play, Play, Play method [Media Foundation], Play method [Media Foundation],IMFMediaEngine interface, mf.imfmediaengine_play, mfmediaengine/IMFMediaEngine::Play
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
 - IMFMediaEngine::Play
 - mfmediaengine/IMFMediaEngine::Play
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
 - IMFMediaEngine.Play
---

# IMFMediaEngine::Play


## -description

Starts playback.



## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

This method corresponds to the <b>play</b> method of the <b>HTMLMediaElement</b> interface in HTML5.

The method completes asynchronously. When the operation starts, the Media Engine sends an <b>MF_MEDIA_ENGINE_EVENT_PLAY</b> event. When playback is under way, the Media Engine sends an <b>MF_MEDIA_ENGINE_EVENT_PLAYING</b> event. See <a href="/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaenginenotify-eventnotify">IMFMediaEventNotify::EventNotify</a>.

## -see-also

<a href="/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediaengine">IMFMediaEngine</a>
