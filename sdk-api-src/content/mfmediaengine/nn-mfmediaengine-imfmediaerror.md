---
UID: NN:mfmediaengine.IMFMediaError
title: IMFMediaError (mfmediaengine.h)
description: Provides the current error status for the Media Engine.
helpviewer_keywords: ["IMFMediaError","IMFMediaError interface [Media Foundation]","IMFMediaError interface [Media Foundation]","described","mf.imfmediaerror","mfmediaengine/IMFMediaError"]
old-location: mf\imfmediaerror.htm
tech.root: mf
ms.assetid: 08F161FE-C0E5-44EE-923E-646ADA534C42
ms.date: 12/05/2018
ms.keywords: IMFMediaError, IMFMediaError interface [Media Foundation], IMFMediaError interface [Media Foundation],described, mf.imfmediaerror, mfmediaengine/IMFMediaError
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
 - IMFMediaError
 - mfmediaengine/IMFMediaError
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
 - IMFMediaError
---

# IMFMediaError interface


## -description

Provides the current error status for the Media Engine.

## -inheritance

The <b>IMFMediaError</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IMFMediaError</b> also has these types of members:

## -remarks

The <b>IMFMediaError</b> interface corresponds to the <b>MediaError</b> object in HTML5.

To get a pointer to this interface, call <a href="/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengine-geterror">IMFMediaEngine::GetError</a>.

## -see-also

<a href="/windows/desktop/medfound/media-foundation-interfaces">Media Foundation Interfaces</a>
