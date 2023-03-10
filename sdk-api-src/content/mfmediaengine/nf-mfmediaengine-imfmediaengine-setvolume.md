---
UID: NF:mfmediaengine.IMFMediaEngine.SetVolume
title: IMFMediaEngine::SetVolume (mfmediaengine.h)
description: Sets the audio volume level.
helpviewer_keywords: ["IMFMediaEngine interface [Media Foundation]","SetVolume method","IMFMediaEngine.SetVolume","IMFMediaEngine::SetVolume","SetVolume","SetVolume method [Media Foundation]","SetVolume method [Media Foundation]","IMFMediaEngine interface","mf.imfmediaengine_setvolume","mfmediaengine/IMFMediaEngine::SetVolume"]
old-location: mf\imfmediaengine_setvolume.htm
tech.root: mf
ms.assetid: 010EE05C-3F81-404E-8AFB-7C57CA55A8AE
ms.date: 12/05/2018
ms.keywords: IMFMediaEngine interface [Media Foundation],SetVolume method, IMFMediaEngine.SetVolume, IMFMediaEngine::SetVolume, SetVolume, SetVolume method [Media Foundation], SetVolume method [Media Foundation],IMFMediaEngine interface, mf.imfmediaengine_setvolume, mfmediaengine/IMFMediaEngine::SetVolume
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
 - IMFMediaEngine::SetVolume
 - mfmediaengine/IMFMediaEngine::SetVolume
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
 - IMFMediaEngine.SetVolume
---

# IMFMediaEngine::SetVolume


## -description

Sets the audio volume level.

## -parameters

### -param Volume [in]

The volume level. Volume is expressed as an attenuation level, where 0.0 indicates silence and 1.0 indicates full volume (no attenuation).

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

When the audio balance changes, the Media Engine sends an <b>MF_MEDIA_ENGINE_EVENT_VOLUMECHANGE</b> event. See <a href="/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaenginenotify-eventnotify">IMFMediaEventNotify::EventNotify</a>.

## -see-also

<a href="/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediaengine">IMFMediaEngine</a>