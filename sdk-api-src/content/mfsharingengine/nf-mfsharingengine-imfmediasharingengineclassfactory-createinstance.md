---
UID: NF:mfsharingengine.IMFMediaSharingEngineClassFactory.CreateInstance
title: IMFMediaSharingEngineClassFactory::CreateInstance (mfsharingengine.h)
description: Creates an instance of the IMFMediaSharingEngine. (IMFMediaSharingEngineClassFactory.CreateInstance)
helpviewer_keywords: ["CreateInstance","CreateInstance method [Media Foundation]","CreateInstance method [Media Foundation]","IMFMediaSharingEngineClassFactory interface","IMFMediaSharingEngineClassFactory interface [Media Foundation]","CreateInstance method","IMFMediaSharingEngineClassFactory.CreateInstance","IMFMediaSharingEngineClassFactory::CreateInstance","mf.imfmediasharingengineclassfactory_createinstance","mfsharingengine/IMFMediaSharingEngineClassFactory::CreateInstance"]
old-location: mf\imfmediasharingengineclassfactory_createinstance.htm
tech.root: mf
ms.assetid: D0FD55A1-0387-4450-8F05-3AC7E943F437
ms.date: 12/05/2018
ms.keywords: CreateInstance, CreateInstance method [Media Foundation], CreateInstance method [Media Foundation],IMFMediaSharingEngineClassFactory interface, IMFMediaSharingEngineClassFactory interface [Media Foundation],CreateInstance method, IMFMediaSharingEngineClassFactory.CreateInstance, IMFMediaSharingEngineClassFactory::CreateInstance, mf.imfmediasharingengineclassfactory_createinstance, mfsharingengine/IMFMediaSharingEngineClassFactory::CreateInstance
req.header: mfsharingengine.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
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
 - IMFMediaSharingEngineClassFactory::CreateInstance
 - mfsharingengine/IMFMediaSharingEngineClassFactory::CreateInstance
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfsharingengine.h
api_name:
 - IMFMediaSharingEngineClassFactory.CreateInstance
---

# IMFMediaSharingEngineClassFactory::CreateInstance


## -description

Creates an instance of the <a href="/windows/desktop/api/mfsharingengine/nn-mfsharingengine-imfmediasharingengine">IMFMediaSharingEngine</a>.

## -parameters

### -param dwFlags [in]

A bitwise <b>OR</b> of zero or more flags from the <a href="/windows/desktop/api/mfmediaengine/ne-mfmediaengine-mf_media_engine_createflags">MF_MEDIA_ENGINE_CREATEFLAGS</a> enumeration.

### -param pAttr [in]

A pointer to the <a href="/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes">IMFAttributes</a> interface of an attribute store.

### -param ppEngine [out]

Receives a pointer to the <a href="/windows/desktop/api/mfsharingengine/nn-mfsharingengine-imfmediasharingengine">IMFMediaSharingEngine</a> interface. The caller must release the interface.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/mfsharingengine/nn-mfsharingengine-imfmediasharingengineclassfactory">IMFMediaSharingEngineClassFactory</a>
