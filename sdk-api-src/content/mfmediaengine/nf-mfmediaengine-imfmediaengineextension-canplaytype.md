---
UID: NF:mfmediaengine.IMFMediaEngineExtension.CanPlayType
title: IMFMediaEngineExtension::CanPlayType (mfmediaengine.h)
description: Queries whether the object can load a specified type of media resource.
helpviewer_keywords: ["CanPlayType","CanPlayType method [Media Foundation]","CanPlayType method [Media Foundation]","IMFMediaEngineExtension interface","IMFMediaEngineExtension interface [Media Foundation]","CanPlayType method","IMFMediaEngineExtension.CanPlayType","IMFMediaEngineExtension::CanPlayType","mf.imfmediaengineextension_canplaytype","mfmediaengine/IMFMediaEngineExtension::CanPlayType"]
old-location: mf\imfmediaengineextension_canplaytype.htm
tech.root: mf
ms.assetid: F715B4CB-363E-4EF2-962C-C0AFB26B088E
ms.date: 12/05/2018
ms.keywords: CanPlayType, CanPlayType method [Media Foundation], CanPlayType method [Media Foundation],IMFMediaEngineExtension interface, IMFMediaEngineExtension interface [Media Foundation],CanPlayType method, IMFMediaEngineExtension.CanPlayType, IMFMediaEngineExtension::CanPlayType, mf.imfmediaengineextension_canplaytype, mfmediaengine/IMFMediaEngineExtension::CanPlayType
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
 - IMFMediaEngineExtension::CanPlayType
 - mfmediaengine/IMFMediaEngineExtension::CanPlayType
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
 - IMFMediaEngineExtension.CanPlayType
---

# IMFMediaEngineExtension::CanPlayType


## -description

Queries whether the object can load a specified type of media resource.

## -parameters

### -param AudioOnly [in]

If <b>TRUE</b>, the Media Engine is set to audio-only mode. Otherwise, the Media Engine is set to audio-video mode.

### -param MimeType [in]

A string that contains a MIME type with an optional codecs parameter, as defined in RFC 4281.

### -param pAnswer [out]

Receives a member of the <a href="/windows/desktop/api/mfmediaengine/ne-mfmediaengine-mf_media_engine_canplay">MF_MEDIA_ENGINE_CANPLAY</a> enumeration.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

Implement this method if your Media Engine extension supports one or more MIME types.

## -see-also

<a href="/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediaengineextension">IMFMediaEngineExtension</a>