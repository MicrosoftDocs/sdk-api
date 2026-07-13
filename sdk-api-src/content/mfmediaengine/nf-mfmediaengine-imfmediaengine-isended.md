---
UID: NF:mfmediaengine.IMFMediaEngine.IsEnded
title: IMFMediaEngine::IsEnded (mfmediaengine.h)
description: Queries whether playback has ended.
helpviewer_keywords: ["IMFMediaEngine interface [Media Foundation]","IsEnded method","IMFMediaEngine.IsEnded","IMFMediaEngine::IsEnded","IsEnded","IsEnded method [Media Foundation]","IsEnded method [Media Foundation]","IMFMediaEngine interface","mf.imfmediaengine_isended","mfmediaengine/IMFMediaEngine::IsEnded"]
old-location: mf\imfmediaengine_isended.htm
tech.root: mf
ms.assetid: 0760707C-B25E-44FF-9263-6B59BF43A98E
ms.date: 12/05/2018
ms.keywords: IMFMediaEngine interface [Media Foundation],IsEnded method, IMFMediaEngine.IsEnded, IMFMediaEngine::IsEnded, IsEnded, IsEnded method [Media Foundation], IsEnded method [Media Foundation],IMFMediaEngine interface, mf.imfmediaengine_isended, mfmediaengine/IMFMediaEngine::IsEnded
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
 - IMFMediaEngine::IsEnded
 - mfmediaengine/IMFMediaEngine::IsEnded
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
 - IMFMediaEngine.IsEnded
---

# IMFMediaEngine::IsEnded


## -description

Queries whether playback has ended.



## -returns

Returns <b>TRUE</b> if the direction of playback is forward and playback has reached the end of the media resource. Returns <b>FALSE</b> otherwise.

## -remarks

This method corresponds to the <b>ended</b> attribute of the <b>HTMLMediaElement</b> interface in HTML5.

## -see-also

<a href="/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediaengine">IMFMediaEngine</a>
