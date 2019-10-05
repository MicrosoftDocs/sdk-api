---
UID: NF:mfmediaengine.IMFMediaEngineExtension.CanPlayType
title: IMFMediaEngineExtension::CanPlayType (mfmediaengine.h)
author: windows-sdk-content
description: Queries whether the object can load a specified type of media resource.
old-location: mf\imfmediaengineextension_canplaytype.htm
tech.root: medfound
ms.assetid: F715B4CB-363E-4EF2-962C-C0AFB26B088E
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: CanPlayType, CanPlayType method [Media Foundation], CanPlayType method [Media Foundation],IMFMediaEngineExtension interface, IMFMediaEngineExtension interface [Media Foundation],CanPlayType method, IMFMediaEngineExtension.CanPlayType, IMFMediaEngineExtension::CanPlayType, mf.imfmediaengineextension_canplaytype, mfmediaengine/IMFMediaEngineExtension::CanPlayType
ms.topic: method
f1_keywords: 
 - "mfmediaengine/IMFMediaEngineExtension.CanPlayType"
dev_langs:
 - c++
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfmediaengine.h
api_name:
 - IMFMediaEngineExtension.CanPlayType
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
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

Receives a member of the <a href="https://docs.microsoft.com/windows/desktop/api/mfmediaengine/ne-mfmediaengine-mf_media_engine_canplay">MF_MEDIA_ENGINE_CANPLAY</a> enumeration.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



Implement this method if your Media Engine extension supports one or more MIME types.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediaengineextension">IMFMediaEngineExtension</a>
 

 

