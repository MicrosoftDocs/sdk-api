---
UID: NF:mfmediaengine.IMFMediaEngineClassFactory.CreateError
title: IMFMediaEngineClassFactory::CreateError (mfmediaengine.h)
author: windows-sdk-content
description: Creates a media error object.
old-location: mf\imfmediaengineclassfactory_createerror.htm
tech.root: medfound
ms.assetid: C089473D-CD35-4F5D-8C78-EDE0FA8C13EB
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: CreateError, CreateError method [Media Foundation], CreateError method [Media Foundation],IMFMediaEngineClassFactory interface, IMFMediaEngineClassFactory interface [Media Foundation],CreateError method, IMFMediaEngineClassFactory.CreateError, IMFMediaEngineClassFactory::CreateError, mf.imfmediaengineclassfactory_createerror, mfmediaengine/IMFMediaEngineClassFactory::CreateError
ms.topic: method
f1_keywords: 
 - "mfmediaengine/IMFMediaEngineClassFactory.CreateError"
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
 - IMFMediaEngineClassFactory.CreateError
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMFMediaEngineClassFactory::CreateError


## -description


Creates a media error object.


## -parameters




### -param ppError [out]

Receives a pointer to the <a href="https://docs.microsoft.com/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediaerror">IMFMediaError</a> interface. The caller must release the interface.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediaengineclassfactory">IMFMediaEngineClassFactory</a>
 

 

