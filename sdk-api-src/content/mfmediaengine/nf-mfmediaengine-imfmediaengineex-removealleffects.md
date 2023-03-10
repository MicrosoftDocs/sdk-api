---
UID: NF:mfmediaengine.IMFMediaEngineEx.RemoveAllEffects
title: IMFMediaEngineEx::RemoveAllEffects (mfmediaengine.h)
description: Removes all audio and video effects.
helpviewer_keywords: ["IMFMediaEngineEx interface [Media Foundation]","RemoveAllEffects method","IMFMediaEngineEx.RemoveAllEffects","IMFMediaEngineEx::RemoveAllEffects","RemoveAllEffects","RemoveAllEffects method [Media Foundation]","RemoveAllEffects method [Media Foundation]","IMFMediaEngineEx interface","mf.imfmediaengineex_removealleffects","mfmediaengine/IMFMediaEngineEx::RemoveAllEffects"]
old-location: mf\imfmediaengineex_removealleffects.htm
tech.root: mf
ms.assetid: B9EF1440-27DA-48C6-B840-FF61DBF19E63
ms.date: 12/05/2018
ms.keywords: IMFMediaEngineEx interface [Media Foundation],RemoveAllEffects method, IMFMediaEngineEx.RemoveAllEffects, IMFMediaEngineEx::RemoveAllEffects, RemoveAllEffects, RemoveAllEffects method [Media Foundation], RemoveAllEffects method [Media Foundation],IMFMediaEngineEx interface, mf.imfmediaengineex_removealleffects, mfmediaengine/IMFMediaEngineEx::RemoveAllEffects
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
 - IMFMediaEngineEx::RemoveAllEffects
 - mfmediaengine/IMFMediaEngineEx::RemoveAllEffects
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
 - IMFMediaEngineEx.RemoveAllEffects
---

# IMFMediaEngineEx::RemoveAllEffects


## -description

Removes all audio and video effects.



## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

 Call this method to remove all of the effects that were added with the <a href="/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengineex-insertaudioeffect">InsertAudioEffect</a> and <a href="/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengineex-insertvideoeffect">InsertVideoEffect</a> methods.

## -see-also

<a href="/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediaengineex">IMFMediaEngineEx</a>
