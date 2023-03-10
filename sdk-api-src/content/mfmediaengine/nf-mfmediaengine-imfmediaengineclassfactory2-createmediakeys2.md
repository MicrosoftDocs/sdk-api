---
UID: NF:mfmediaengine.IMFMediaEngineClassFactory2.CreateMediaKeys2
title: IMFMediaEngineClassFactory2::CreateMediaKeys2 (mfmediaengine.h)
description: Creates a media keys object based on the specified key system. (IMFMediaEngineClassFactory2.CreateMediaKeys2)
helpviewer_keywords: ["CreateMediaKeys2","CreateMediaKeys2 method [Media Foundation]","CreateMediaKeys2 method [Media Foundation]","IMFMediaEngineClassFactory2 interface","IMFMediaEngineClassFactory2 interface [Media Foundation]","CreateMediaKeys2 method","IMFMediaEngineClassFactory2.CreateMediaKeys2","IMFMediaEngineClassFactory2::CreateMediaKeys2","mf.imfmediaengineclassfactory2_createmediakeys2","mfmediaengine/IMFMediaEngineClassFactory2::CreateMediaKeys2"]
old-location: mf\imfmediaengineclassfactory2_createmediakeys2.htm
tech.root: mf
ms.assetid: 857F4573-41B3-488C-88A9-4744EBE5D38B
ms.date: 12/05/2018
ms.keywords: CreateMediaKeys2, CreateMediaKeys2 method [Media Foundation], CreateMediaKeys2 method [Media Foundation],IMFMediaEngineClassFactory2 interface, IMFMediaEngineClassFactory2 interface [Media Foundation],CreateMediaKeys2 method, IMFMediaEngineClassFactory2.CreateMediaKeys2, IMFMediaEngineClassFactory2::CreateMediaKeys2, mf.imfmediaengineclassfactory2_createmediakeys2, mfmediaengine/IMFMediaEngineClassFactory2::CreateMediaKeys2
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
 - IMFMediaEngineClassFactory2::CreateMediaKeys2
 - mfmediaengine/IMFMediaEngineClassFactory2::CreateMediaKeys2
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
 - IMFMediaEngineClassFactory2.CreateMediaKeys2
---

# IMFMediaEngineClassFactory2::CreateMediaKeys2


## -description

Creates a media keys object based on the specified key system.

## -parameters

### -param keySystem [in]

The media key system.

### -param defaultCdmStorePath [in]

Points to the default file location for the  store Content Decryption Module (CDM) data.

### -param inprivateCdmStorePath [in, optional]

Points to a the inprivate location for the  store Content Decryption Module (CDM) data. Specifying this path allows the CDM to comply with the application’s privacy policy by putting personal information in the file location indicated by this path.

### -param ppKeys [out]

Receives the media keys.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediaengineclassfactory2">IMFMediaEngineClassFactory2</a>



<a href="/windows/desktop/api/mfmediaengine/nn-mfmediaengine-imfmediakeys">IMFMediaKeys</a>
