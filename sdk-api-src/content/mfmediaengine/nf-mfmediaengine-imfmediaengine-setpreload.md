---
UID: NF:mfmediaengine.IMFMediaEngine.SetPreload
title: IMFMediaEngine::SetPreload (mfmediaengine.h)
description: Sets the preload flag.
helpviewer_keywords: ["IMFMediaEngine interface [Media Foundation]","SetPreload method","IMFMediaEngine.SetPreload","IMFMediaEngine::SetPreload","SetPreload","SetPreload method [Media Foundation]","SetPreload method [Media Foundation]","IMFMediaEngine interface","mf.imfmediaengine_setpreload","mfmediaengine/IMFMediaEngine::SetPreload"]
old-location: mf\imfmediaengine_setpreload.htm
tech.root: mf
ms.assetid: 3480C16F-E4E4-469C-BE27-711044691A49
ms.date: 12/05/2018
ms.keywords: IMFMediaEngine interface [Media Foundation],SetPreload method, IMFMediaEngine.SetPreload, IMFMediaEngine::SetPreload, SetPreload, SetPreload method [Media Foundation], SetPreload method [Media Foundation],IMFMediaEngine interface, mf.imfmediaengine_setpreload, mfmediaengine/IMFMediaEngine::SetPreload
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
 - IMFMediaEngine::SetPreload
 - mfmediaengine/IMFMediaEngine::SetPreload
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
 - IMFMediaEngine.SetPreload
---

# IMFMediaEngine::SetPreload


## -description

Sets the preload flag.

## -parameters

### -param Preload [in]

An <a href="/windows/desktop/api/mfmediaengine/ne-mfmediaengine-mf_media_engine_preload">MF_MEDIA_ENGINE_PRELOAD</a> value equal to  the preload flag.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

This method corresponds to setting the <b>preload</b> attribute of the <b>HTMLMediaElement</b> interface in HTML5. The value is a hint to the user-agent whether to preload the media resource.

## -see-also

<a href="/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediaengine">IMFMediaEngine</a>