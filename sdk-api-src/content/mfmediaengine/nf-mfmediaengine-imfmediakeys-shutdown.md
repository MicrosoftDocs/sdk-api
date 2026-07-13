---
UID: NF:mfmediaengine.IMFMediaKeys.Shutdown
title: IMFMediaKeys::Shutdown (mfmediaengine.h)
description: The IMFMediaKeys::Shutdown (mfmediaengine.h) method shuts down the associated Content Decryption Module (CDM). 
helpviewer_keywords: ["IMFMediaKeys interface [Media Foundation]","Shutdown method","IMFMediaKeys.Shutdown","IMFMediaKeys::Shutdown","Shutdown","Shutdown method [Media Foundation]","Shutdown method [Media Foundation]","IMFMediaKeys interface","mf.imfmediakeys_shutdown","mfmediaengine/IMFMediaKeys::Shutdown"]
old-location: mf\imfmediakeys_shutdown.htm
tech.root: mf
ms.assetid: 464b598c-5fa7-40af-83ba-8619fbd84b04
ms.date: 08/05/2022
ms.keywords: IMFMediaKeys interface [Media Foundation],Shutdown method, IMFMediaKeys.Shutdown, IMFMediaKeys::Shutdown, Shutdown, Shutdown method [Media Foundation], Shutdown method [Media Foundation],IMFMediaKeys interface, mf.imfmediakeys_shutdown, mfmediaengine/IMFMediaKeys::Shutdown
req.header: mfmediaengine.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Mfmediaengine.idl
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
 - IMFMediaKeys::Shutdown
 - mfmediaengine/IMFMediaKeys::Shutdown
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
 - IMFMediaKeys.Shutdown
---

# IMFMediaKeys::Shutdown


## -description

Shuts down the associated Content Decryption Module (CDM).



## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

<b>Shutdown</b> should be called by the application before final release.  The Content Decryption Module (CDM) reference and any other resources is released at this point.  However, related sessions are not freed or closed.

## -see-also

<a href="/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediakeys">IMFMediaKeys</a>
