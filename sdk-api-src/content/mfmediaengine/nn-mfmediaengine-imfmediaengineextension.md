---
UID: NN:mfmediaengine.IMFMediaEngineExtension
title: IMFMediaEngineExtension (mfmediaengine.h)
description: Enables an application to load media resources in the Media Engine.
helpviewer_keywords: ["IMFMediaEngineExtension","IMFMediaEngineExtension interface [Media Foundation]","IMFMediaEngineExtension interface [Media Foundation]","described","mf.imfmediaengineextension","mfmediaengine/IMFMediaEngineExtension"]
old-location: mf\imfmediaengineextension.htm
tech.root: mf
ms.assetid: A032E0D0-2201-4B81-9FE0-8E9CE2707FDB
ms.date: 12/05/2018
ms.keywords: IMFMediaEngineExtension, IMFMediaEngineExtension interface [Media Foundation], IMFMediaEngineExtension interface [Media Foundation],described, mf.imfmediaengineextension, mfmediaengine/IMFMediaEngineExtension
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
 - IMFMediaEngineExtension
 - mfmediaengine/IMFMediaEngineExtension
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
 - IMFMediaEngineExtension
---

# IMFMediaEngineExtension interface


## -description

Enables an application to load media resources in the Media Engine.

## -inheritance

The <b>IMFMediaEngineExtension</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IMFMediaEngineExtension</b> also has these types of members:

## -remarks

To use this interface, set the <a href="/windows/desktop/medfound/mf-media-engine-extension">MF_MEDIA_ENGINE_EXTENSION</a> attribute when you call the <a href="/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengineclassfactory-createinstance">IMFMediaEngineClassFactory::CreateInstance</a> method.

## -see-also

<a href="/windows/desktop/medfound/media-foundation-interfaces">Media Foundation Interfaces</a>
