---
UID: NF:mfmediaengine.IMFMediaEngine.GetAutoPlay
title: IMFMediaEngine::GetAutoPlay (mfmediaengine.h)
description: Queries whether the Media Engine automatically begins playback.
helpviewer_keywords: ["GetAutoPlay","GetAutoPlay method [Media Foundation]","GetAutoPlay method [Media Foundation]","IMFMediaEngine interface","IMFMediaEngine interface [Media Foundation]","GetAutoPlay method","IMFMediaEngine.GetAutoPlay","IMFMediaEngine::GetAutoPlay","mf.imfmediaengine_getautoplay","mfmediaengine/IMFMediaEngine::GetAutoPlay"]
old-location: mf\imfmediaengine_getautoplay.htm
tech.root: mf
ms.assetid: CEF50308-D4F9-435F-A81A-3746A27846F0
ms.date: 12/05/2018
ms.keywords: GetAutoPlay, GetAutoPlay method [Media Foundation], GetAutoPlay method [Media Foundation],IMFMediaEngine interface, IMFMediaEngine interface [Media Foundation],GetAutoPlay method, IMFMediaEngine.GetAutoPlay, IMFMediaEngine::GetAutoPlay, mf.imfmediaengine_getautoplay, mfmediaengine/IMFMediaEngine::GetAutoPlay
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
 - IMFMediaEngine::GetAutoPlay
 - mfmediaengine/IMFMediaEngine::GetAutoPlay
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
 - IMFMediaEngine.GetAutoPlay
---

# IMFMediaEngine::GetAutoPlay


## -description

Queries whether the Media Engine automatically begins playback.



## -returns

Returns <b>TRUE</b> if the Media Engine automatically begins playback, or <b>FALSE</b> otherwise.

## -remarks

This method corresponds to the <b>autoplay</b> attribute of the <b>HTMLMediaElement</b> interface in HTML5.

If this method returns <b>TRUE</b>, playback begins automatically after the <a href="/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengine-load">IMFMediaEngine::Load</a> method completes. Otherwise, playback begins when the application calls <a href="/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengine-play">IMFMediaEngine::Play</a>.

## -see-also

<a href="/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediaengine">IMFMediaEngine</a>



<a href="/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengine-setautoplay">IMFMediaEngine::SetAutoPlay</a>
