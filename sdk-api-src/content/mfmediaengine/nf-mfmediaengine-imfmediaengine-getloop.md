---
UID: NF:mfmediaengine.IMFMediaEngine.GetLoop
title: IMFMediaEngine::GetLoop (mfmediaengine.h)
description: Queries whether the Media Engine will loop playback.
helpviewer_keywords: ["GetLoop","GetLoop method [Media Foundation]","GetLoop method [Media Foundation]","IMFMediaEngine interface","IMFMediaEngine interface [Media Foundation]","GetLoop method","IMFMediaEngine.GetLoop","IMFMediaEngine::GetLoop","mf.imfmediaengine_getloop","mfmediaengine/IMFMediaEngine::GetLoop"]
old-location: mf\imfmediaengine_getloop.htm
tech.root: mf
ms.assetid: EBAB4E73-164D-4AE5-87A4-0D37C10071E9
ms.date: 12/05/2018
ms.keywords: GetLoop, GetLoop method [Media Foundation], GetLoop method [Media Foundation],IMFMediaEngine interface, IMFMediaEngine interface [Media Foundation],GetLoop method, IMFMediaEngine.GetLoop, IMFMediaEngine::GetLoop, mf.imfmediaengine_getloop, mfmediaengine/IMFMediaEngine::GetLoop
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
 - IMFMediaEngine::GetLoop
 - mfmediaengine/IMFMediaEngine::GetLoop
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
 - IMFMediaEngine.GetLoop
---

# IMFMediaEngine::GetLoop


## -description

Queries whether the Media Engine will loop playback.



## -returns

Returns <b>TRUE</b> if looping is enabled, or <b>FALSE</b> otherwise.

## -remarks

This method corresponds to getting the <b>loop</b> attribute of the <b>HTMLMediaElement</b> interface in HTML5.

If looping is enabled, the Media Engine seeks to the start of the content when playback reaches the end.

## -see-also

<a href="/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediaengine">IMFMediaEngine</a>
