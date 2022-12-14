---
UID: NF:mfmediaengine.IMFMediaEngine.IsSeeking
title: IMFMediaEngine::IsSeeking (mfmediaengine.h)
description: Queries whether the Media Engine is currently seeking to a new playback position.
helpviewer_keywords: ["IMFMediaEngine interface [Media Foundation]","IsSeeking method","IMFMediaEngine.IsSeeking","IMFMediaEngine::IsSeeking","IsSeeking","IsSeeking method [Media Foundation]","IsSeeking method [Media Foundation]","IMFMediaEngine interface","mf.imfmediaengine_isseeking","mfmediaengine/IMFMediaEngine::IsSeeking"]
old-location: mf\imfmediaengine_isseeking.htm
tech.root: mf
ms.assetid: B314D5E7-EBD4-42CF-9E86-206ABC3027A0
ms.date: 12/05/2018
ms.keywords: IMFMediaEngine interface [Media Foundation],IsSeeking method, IMFMediaEngine.IsSeeking, IMFMediaEngine::IsSeeking, IsSeeking, IsSeeking method [Media Foundation], IsSeeking method [Media Foundation],IMFMediaEngine interface, mf.imfmediaengine_isseeking, mfmediaengine/IMFMediaEngine::IsSeeking
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
 - IMFMediaEngine::IsSeeking
 - mfmediaengine/IMFMediaEngine::IsSeeking
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
 - IMFMediaEngine.IsSeeking
---

# IMFMediaEngine::IsSeeking


## -description

Queries whether the Media Engine is currently seeking to a new playback position.



## -returns

Returns <b>TRUE</b> if the Media Engine is seeking, or <b>FALSE</b> otherwise.

## -remarks

This method corresponds to the <b>seeking</b> attribute of the <b>HTMLMediaElement</b> interface in HTML5.

## -see-also

<a href="/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediaengine">IMFMediaEngine</a>
