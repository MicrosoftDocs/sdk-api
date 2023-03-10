---
UID: NF:mfmediaengine.IMFMediaEngine.GetPreload
title: IMFMediaEngine::GetPreload (mfmediaengine.h)
description: Gets the preload flag.
helpviewer_keywords: ["GetPreload","GetPreload method [Media Foundation]","GetPreload method [Media Foundation]","IMFMediaEngine interface","IMFMediaEngine interface [Media Foundation]","GetPreload method","IMFMediaEngine.GetPreload","IMFMediaEngine::GetPreload","mf.imfmediaengine_getpreload","mfmediaengine/IMFMediaEngine::GetPreload"]
old-location: mf\imfmediaengine_getpreload.htm
tech.root: mf
ms.assetid: AA1942B2-C5BB-46F7-B163-1BCB3372D453
ms.date: 12/05/2018
ms.keywords: GetPreload, GetPreload method [Media Foundation], GetPreload method [Media Foundation],IMFMediaEngine interface, IMFMediaEngine interface [Media Foundation],GetPreload method, IMFMediaEngine.GetPreload, IMFMediaEngine::GetPreload, mf.imfmediaengine_getpreload, mfmediaengine/IMFMediaEngine::GetPreload
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
 - IMFMediaEngine::GetPreload
 - mfmediaengine/IMFMediaEngine::GetPreload
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
 - IMFMediaEngine.GetPreload
---

# IMFMediaEngine::GetPreload


## -description

Gets the preload flag.



## -returns

Returns an <a href="/windows/desktop/api/mfmediaengine/ne-mfmediaengine-mf_media_engine_preload">MF_MEDIA_ENGINE_PRELOAD</a> enumeration value.

## -remarks

This method corresponds to the <b>preload</b> attribute of the <b>HTMLMediaElement</b> interface in HTML5. The value is a hint to the user-agent whether to preload the media resource.

## -see-also

<a href="/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediaengine">IMFMediaEngine</a>
