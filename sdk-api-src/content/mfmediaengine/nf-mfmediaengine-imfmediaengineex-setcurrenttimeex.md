---
UID: NF:mfmediaengine.IMFMediaEngineEx.SetCurrentTimeEx
title: IMFMediaEngineEx::SetCurrentTimeEx (mfmediaengine.h)
description: Seeks to a new playback position using the specified MF_MEDIA_ENGINE_SEEK_MODE.
helpviewer_keywords: ["IMFMediaEngineEx interface [Media Foundation]","SetCurrentTimeEx method","IMFMediaEngineEx.SetCurrentTimeEx","IMFMediaEngineEx::SetCurrentTimeEx","SetCurrentTimeEx","SetCurrentTimeEx method [Media Foundation]","SetCurrentTimeEx method [Media Foundation]","IMFMediaEngineEx interface","mf.imfmediaengineex_setcurrenttimeex","mfmediaengine/IMFMediaEngineEx::SetCurrentTimeEx"]
old-location: mf\imfmediaengineex_setcurrenttimeex.htm
tech.root: mf
ms.assetid: ee594f0c-af49-44c2-8c68-16120f76c5e1
ms.date: 12/05/2018
ms.keywords: IMFMediaEngineEx interface [Media Foundation],SetCurrentTimeEx method, IMFMediaEngineEx.SetCurrentTimeEx, IMFMediaEngineEx::SetCurrentTimeEx, SetCurrentTimeEx, SetCurrentTimeEx method [Media Foundation], SetCurrentTimeEx method [Media Foundation],IMFMediaEngineEx interface, mf.imfmediaengineex_setcurrenttimeex, mfmediaengine/IMFMediaEngineEx::SetCurrentTimeEx
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
 - IMFMediaEngineEx::SetCurrentTimeEx
 - mfmediaengine/IMFMediaEngineEx::SetCurrentTimeEx
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
 - IMFMediaEngineEx.SetCurrentTimeEx
---

# IMFMediaEngineEx::SetCurrentTimeEx


## -description

Seeks to a new playback position using the  specified <a href="/windows/desktop/api/mfmediaengine/ne-mfmediaengine-mf_media_engine_seek_mode">MF_MEDIA_ENGINE_SEEK_MODE</a>.

## -parameters

### -param seekTime [in]

The new playback position, in seconds.

### -param seekMode [in]

Specifies if the seek is a normal seek or an approximate seek.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediaengineex">IMFMediaEngineEx</a>