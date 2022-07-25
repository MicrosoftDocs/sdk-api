---
UID: NF:mfmediaengine.IMFMediaEngine.SetAutoPlay
title: IMFMediaEngine::SetAutoPlay (mfmediaengine.h)
description: Specifies whether the Media Engine automatically begins playback.
helpviewer_keywords: ["IMFMediaEngine interface [Media Foundation]","SetAutoPlay method","IMFMediaEngine.SetAutoPlay","IMFMediaEngine::SetAutoPlay","SetAutoPlay","SetAutoPlay method [Media Foundation]","SetAutoPlay method [Media Foundation]","IMFMediaEngine interface","mf.imfmediaengine_setautoplay","mfmediaengine/IMFMediaEngine::SetAutoPlay"]
old-location: mf\imfmediaengine_setautoplay.htm
tech.root: mf
ms.assetid: 867FE1D2-39AE-4A44-99DD-98A8ABD234A2
ms.date: 12/05/2018
ms.keywords: IMFMediaEngine interface [Media Foundation],SetAutoPlay method, IMFMediaEngine.SetAutoPlay, IMFMediaEngine::SetAutoPlay, SetAutoPlay, SetAutoPlay method [Media Foundation], SetAutoPlay method [Media Foundation],IMFMediaEngine interface, mf.imfmediaengine_setautoplay, mfmediaengine/IMFMediaEngine::SetAutoPlay
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
 - IMFMediaEngine::SetAutoPlay
 - mfmediaengine/IMFMediaEngine::SetAutoPlay
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
 - IMFMediaEngine.SetAutoPlay
---

# IMFMediaEngine::SetAutoPlay


## -description

Specifies whether the Media Engine automatically begins playback.

## -parameters

### -param AutoPlay [in]

If <b>TRUE</b>, the Media Engine automatically begins playback after it loads a media source. Otherwise, playback does not begin until the application calls <a href="/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengine-play">IMFMediaEngine::Play</a>.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

This method corresponds to setting the <b>autoplay</b> attribute of the <b>HTMLMediaElement</b> interface in HTML5.

## -see-also

<a href="/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediaengine">IMFMediaEngine</a>