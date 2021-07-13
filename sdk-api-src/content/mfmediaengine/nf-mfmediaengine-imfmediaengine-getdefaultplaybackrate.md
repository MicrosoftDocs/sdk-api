---
UID: NF:mfmediaengine.IMFMediaEngine.GetDefaultPlaybackRate
title: IMFMediaEngine::GetDefaultPlaybackRate (mfmediaengine.h)
description: Gets the default playback rate.
helpviewer_keywords: ["GetDefaultPlaybackRate","GetDefaultPlaybackRate method [Media Foundation]","GetDefaultPlaybackRate method [Media Foundation]","IMFMediaEngine interface","IMFMediaEngine interface [Media Foundation]","GetDefaultPlaybackRate method","IMFMediaEngine.GetDefaultPlaybackRate","IMFMediaEngine::GetDefaultPlaybackRate","mf.imfmediaengine_getdefaultplaybackrate","mfmediaengine/IMFMediaEngine::GetDefaultPlaybackRate"]
old-location: mf\imfmediaengine_getdefaultplaybackrate.htm
tech.root: mf
ms.assetid: FF7E9E76-B85E-40BB-88BD-5033FCE31177
ms.date: 12/05/2018
ms.keywords: GetDefaultPlaybackRate, GetDefaultPlaybackRate method [Media Foundation], GetDefaultPlaybackRate method [Media Foundation],IMFMediaEngine interface, IMFMediaEngine interface [Media Foundation],GetDefaultPlaybackRate method, IMFMediaEngine.GetDefaultPlaybackRate, IMFMediaEngine::GetDefaultPlaybackRate, mf.imfmediaengine_getdefaultplaybackrate, mfmediaengine/IMFMediaEngine::GetDefaultPlaybackRate
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
 - IMFMediaEngine::GetDefaultPlaybackRate
 - mfmediaengine/IMFMediaEngine::GetDefaultPlaybackRate
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
 - IMFMediaEngine.GetDefaultPlaybackRate
---

# IMFMediaEngine::GetDefaultPlaybackRate


## -description

Gets the default playback rate.



## -returns

Returns the default playback rate, as a multiple of normal (1×) playback. A negative value indicates reverse playback.

## -remarks

This method corresponds to getting the <b>defaultPlaybackRate</b> attribute of the <b>HTMLMediaElement</b> interface in HTML5. 

The default playback rate is used for the next call to the <a href="/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengine-play">IMFMediaEngine::Play</a> method. To change the current playback rate, call <a href="/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengine-setplaybackrate">IMFMediaEngine::SetPlaybackRate</a>.

## -see-also

<a href="/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediaengine">IMFMediaEngine</a>
