---
UID: NF:mfmediaengine.IMFMediaEngine.GetReadyState
title: IMFMediaEngine::GetReadyState (mfmediaengine.h)
description: Gets the ready state, which indicates whether the current media resource can be rendered.
helpviewer_keywords: ["GetReadyState","GetReadyState method [Media Foundation]","GetReadyState method [Media Foundation]","IMFMediaEngine interface","IMFMediaEngine interface [Media Foundation]","GetReadyState method","IMFMediaEngine.GetReadyState","IMFMediaEngine::GetReadyState","mf.imfmediaengine_getreadystate","mfmediaengine/IMFMediaEngine::GetReadyState"]
old-location: mf\imfmediaengine_getreadystate.htm
tech.root: mf
ms.assetid: B8C9B600-87FD-4DE6-8794-5C1E41449554
ms.date: 12/05/2018
ms.keywords: GetReadyState, GetReadyState method [Media Foundation], GetReadyState method [Media Foundation],IMFMediaEngine interface, IMFMediaEngine interface [Media Foundation],GetReadyState method, IMFMediaEngine.GetReadyState, IMFMediaEngine::GetReadyState, mf.imfmediaengine_getreadystate, mfmediaengine/IMFMediaEngine::GetReadyState
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
 - IMFMediaEngine::GetReadyState
 - mfmediaengine/IMFMediaEngine::GetReadyState
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
 - IMFMediaEngine.GetReadyState
---

# IMFMediaEngine::GetReadyState


## -description

Gets the ready state, which indicates whether the current media resource can be rendered.



## -returns

Returns an <a href="/windows/desktop/api/mfmediaengine/ne-mfmediaengine-mf_media_engine_ready">MF_MEDIA_ENGINE_READY</a> enumeration value.

## -remarks

This method corresponds to the <b>readyState</b> attribute of the <b>HTMLMediaElement</b> interface in HTML5.

## -see-also

<a href="/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediaengine">IMFMediaEngine</a>
