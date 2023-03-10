---
UID: NF:mfmediaengine.IMFMediaEngine.SetLoop
title: IMFMediaEngine::SetLoop (mfmediaengine.h)
description: Specifies whether the Media Engine loops playback.
helpviewer_keywords: ["IMFMediaEngine interface [Media Foundation]","SetLoop method","IMFMediaEngine.SetLoop","IMFMediaEngine::SetLoop","SetLoop","SetLoop method [Media Foundation]","SetLoop method [Media Foundation]","IMFMediaEngine interface","mf.imfmediaengine_setloop","mfmediaengine/IMFMediaEngine::SetLoop"]
old-location: mf\imfmediaengine_setloop.htm
tech.root: mf
ms.assetid: 0B8890EA-9207-428B-8EC2-18B51E1D8365
ms.date: 12/05/2018
ms.keywords: IMFMediaEngine interface [Media Foundation],SetLoop method, IMFMediaEngine.SetLoop, IMFMediaEngine::SetLoop, SetLoop, SetLoop method [Media Foundation], SetLoop method [Media Foundation],IMFMediaEngine interface, mf.imfmediaengine_setloop, mfmediaengine/IMFMediaEngine::SetLoop
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
 - IMFMediaEngine::SetLoop
 - mfmediaengine/IMFMediaEngine::SetLoop
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
 - IMFMediaEngine.SetLoop
---

# IMFMediaEngine::SetLoop


## -description

Specifies whether the Media Engine loops playback.

## -parameters

### -param Loop [in]

Specify <b>TRUE</b> to enable looping, or <b>FALSE</b> to disable looping.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

If <i>Loop</i> is <b>TRUE</b>, playback loops back to the beginning when it reaches the end of the source.

This method corresponds to setting the <b>loop</b> attribute of the <b>HTMLMediaElement</b> interface in HTML5.

## -see-also

<a href="/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediaengine">IMFMediaEngine</a>