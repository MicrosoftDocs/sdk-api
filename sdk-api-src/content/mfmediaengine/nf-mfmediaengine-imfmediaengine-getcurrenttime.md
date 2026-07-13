---
UID: NF:mfmediaengine.IMFMediaEngine.GetCurrentTime
title: IMFMediaEngine::GetCurrentTime (mfmediaengine.h)
description: Gets the current playback position. (IMFMediaEngine.GetCurrentTime)
helpviewer_keywords: ["GetCurrentTime","GetCurrentTime method [Media Foundation]","GetCurrentTime method [Media Foundation]","IMFMediaEngine interface","IMFMediaEngine interface [Media Foundation]","GetCurrentTime method","IMFMediaEngine.GetCurrentTime","IMFMediaEngine::GetCurrentTime","mf.imfmediaengine_getcurrenttime","mfmediaengine/IMFMediaEngine::GetCurrentTime"]
old-location: mf\imfmediaengine_getcurrenttime.htm
tech.root: mf
ms.assetid: 49FA2383-8AEC-4DDF-8998-25987EEC8223
ms.date: 12/05/2018
ms.keywords: GetCurrentTime, GetCurrentTime method [Media Foundation], GetCurrentTime method [Media Foundation],IMFMediaEngine interface, IMFMediaEngine interface [Media Foundation],GetCurrentTime method, IMFMediaEngine.GetCurrentTime, IMFMediaEngine::GetCurrentTime, mf.imfmediaengine_getcurrenttime, mfmediaengine/IMFMediaEngine::GetCurrentTime
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
 - IMFMediaEngine::GetCurrentTime
 - mfmediaengine/IMFMediaEngine::GetCurrentTime
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
 - IMFMediaEngine.GetCurrentTime
---

# IMFMediaEngine::GetCurrentTime


## -description

Gets the current playback position.



## -returns

Returns the playback position, in seconds.

## -remarks

This method corresponds to the <b>currentTime</b> attribute of the <b>HTMLMediaElement</b> interface in HTML5. 

Note that after you call <a href="/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengine-pause">Pause</a>, the time returned by <b>GetCurrentTime</b> may not be precisely accurate. Apps that need a frame-accurate position value, such as media editors, should call <a href="/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengineex-framestep">FrameStep</a> immediately after calling **Pause** before calling <b>GetCurrentTime</b>.

## -see-also

<a href="/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediaengine">IMFMediaEngine</a>
