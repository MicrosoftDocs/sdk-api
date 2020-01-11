---
UID: NF:mfmediaengine.IMFMediaKeys.Shutdown
title: IMFMediaKeys::Shutdown (mfmediaengine.h)
description: 
old-location: mf\imfmediakeys_shutdown.htm
tech.root: medfound
ms.assetid: 464b598c-5fa7-40af-83ba-8619fbd84b04
ms.date: 12/05/2018
ms.keywords: IMFMediaKeys interface [Media Foundation],Shutdown method, IMFMediaKeys.Shutdown, IMFMediaKeys::Shutdown, Shutdown, Shutdown method [Media Foundation], Shutdown method [Media Foundation],IMFMediaKeys interface, mf.imfmediakeys_shutdown, mfmediaengine/IMFMediaKeys::Shutdown
f1_keywords:
- mfmediaengine/IMFMediaKeys.Shutdown
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- mfmediaengine.h
api_name:
- IMFMediaKeys.Shutdown
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMFMediaKeys::Shutdown


## -description





## -parameters






## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



<b>Shutdown</b> should be called by the application before final release.  The Content Decryption Module (CDM) reference and any other resources is released at this point.  However, related sessions are not freed or closed.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediakeys">IMFMediaKeys</a>
 

 

