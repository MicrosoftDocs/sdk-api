---
UID: NF:mfmediaengine.IMFMediaEngine.GetPlaybackRate
title: IMFMediaEngine::GetPlaybackRate (mfmediaengine.h)
description: Gets the current playback rate. (IMFMediaEngine.GetPlaybackRate)
helpviewer_keywords: ["GetPlaybackRate","GetPlaybackRate method [Media Foundation]","GetPlaybackRate method [Media Foundation]","IMFMediaEngine interface","IMFMediaEngine interface [Media Foundation]","GetPlaybackRate method","IMFMediaEngine.GetPlaybackRate","IMFMediaEngine::GetPlaybackRate","mf.imfmediaengine_getplaybackrate","mfmediaengine/IMFMediaEngine::GetPlaybackRate"]
old-location: mf\imfmediaengine_getplaybackrate.htm
tech.root: mf
ms.assetid: E270CB86-D90B-43FA-843B-F824970BD4F3
ms.date: 12/05/2018
ms.keywords: GetPlaybackRate, GetPlaybackRate method [Media Foundation], GetPlaybackRate method [Media Foundation],IMFMediaEngine interface, IMFMediaEngine interface [Media Foundation],GetPlaybackRate method, IMFMediaEngine.GetPlaybackRate, IMFMediaEngine::GetPlaybackRate, mf.imfmediaengine_getplaybackrate, mfmediaengine/IMFMediaEngine::GetPlaybackRate
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
 - IMFMediaEngine::GetPlaybackRate
 - mfmediaengine/IMFMediaEngine::GetPlaybackRate
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
 - IMFMediaEngine.GetPlaybackRate
---

# IMFMediaEngine::GetPlaybackRate


## -description

Gets the current playback rate.



## -returns

Returns the playback rate, as a multiple of normal (1×) playback. A negative value indicates reverse playback.

## -remarks

This method corresponds to getting the <b>playbackRate</b> attribute of the <b>HTMLMediaElement</b> interface in HTML5.

## -see-also

<a href="/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediaengine">IMFMediaEngine</a>
