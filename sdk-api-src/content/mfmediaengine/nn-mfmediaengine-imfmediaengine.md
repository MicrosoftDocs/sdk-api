---
UID: NN:mfmediaengine.IMFMediaEngine
title: IMFMediaEngine (mfmediaengine.h)
description: Enables an application to play audio or video files.
helpviewer_keywords: ["IMFMediaEngine","IMFMediaEngine interface [Media Foundation]","IMFMediaEngine interface [Media Foundation]","described","mf.imfmediaengine","mfmediaengine/IMFMediaEngine"]
old-location: mf\imfmediaengine.htm
tech.root: mf
ms.assetid: A0023F18-2D28-4F0D-9B00-B8FB11567034
ms.date: 12/05/2018
ms.keywords: IMFMediaEngine, IMFMediaEngine interface [Media Foundation], IMFMediaEngine interface [Media Foundation],described, mf.imfmediaengine, mfmediaengine/IMFMediaEngine
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
 - IMFMediaEngine
 - mfmediaengine/IMFMediaEngine
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
 - IMFMediaEngine
---

# IMFMediaEngine interface


## -description

Enables an application to play audio or video files.

## -inheritance

The <b>IMFMediaEngine</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IMFMediaEngine</b> also has these types of members:

## -remarks

The Media Engine implements this interface. To create an instance of the Media Engine, call <a href="/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengineclassfactory-createinstance">IMFMediaEngineClassFactory::CreateInstance</a>.

This interface is extended with <a href="/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediaengineex">IMFMediaEngineEx</a>.

## -see-also

<a href="https://github.com/microsoftarchive/msdn-code-gallery-microsoft/tree/411c271e537727d737a53fa2cbe99eaecac00cc0/Official%20Windows%20Platform%20Sample/Windows%208%20app%20samples/%5BC%2B%2B%5D-Windows%208%20app%20samples/C%2B%2B/Windows%208%20app%20samples/Media%20engine%20native%20C%2B%2B%20video%20playback%20sample%20(Windows%208)">Media Engine Sample</a>



<a href="/windows/desktop/medfound/media-foundation-interfaces">Media Foundation Interfaces</a>
