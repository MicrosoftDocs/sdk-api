---
UID: NF:mfcaptureengine.IMFCaptureEngineClassFactory.CreateInstance
title: IMFCaptureEngineClassFactory::CreateInstance (mfcaptureengine.h)
description: Creates an instance of the capture engine. (IMFCaptureEngineClassFactory.CreateInstance)
helpviewer_keywords: ["CreateInstance","CreateInstance method [Media Foundation]","CreateInstance method [Media Foundation]","IMFCaptureEngineClassFactory interface","IMFCaptureEngineClassFactory interface [Media Foundation]","CreateInstance method","IMFCaptureEngineClassFactory.CreateInstance","IMFCaptureEngineClassFactory::CreateInstance","mf.imfcaptureengineclassfactory_createinstance","mfcaptureengine/IMFCaptureEngineClassFactory::CreateInstance"]
old-location: mf\imfcaptureengineclassfactory_createinstance.htm
tech.root: mf
ms.assetid: D5E7D96B-9438-4332-AD05-249D2DA2481A
ms.date: 12/05/2018
ms.keywords: CreateInstance, CreateInstance method [Media Foundation], CreateInstance method [Media Foundation],IMFCaptureEngineClassFactory interface, IMFCaptureEngineClassFactory interface [Media Foundation],CreateInstance method, IMFCaptureEngineClassFactory.CreateInstance, IMFCaptureEngineClassFactory::CreateInstance, mf.imfcaptureengineclassfactory_createinstance, mfcaptureengine/IMFCaptureEngineClassFactory::CreateInstance
req.header: mfcaptureengine.h
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
 - IMFCaptureEngineClassFactory::CreateInstance
 - mfcaptureengine/IMFCaptureEngineClassFactory::CreateInstance
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfcaptureengine.h
api_name:
 - IMFCaptureEngineClassFactory.CreateInstance
---

# IMFCaptureEngineClassFactory::CreateInstance


## -description

Creates an instance of the capture engine.

## -parameters

### -param clsid [in]

The CLSID of the object to create.

Currently, this parameter must equal <b>CLSID_MFCaptureEngine</b>.

### -param riid [in]

The IID of the requested interface. The capture engine supports the <a href="/windows/desktop/api/mfcaptureengine/nn-mfcaptureengine-imfcaptureengine">IMFCaptureEngine</a> interface.

### -param ppvObject [out]

Receives a pointer to the requested interface. The caller must release the interface.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

Before calling this method, call the <a href="/windows/desktop/api/mfapi/nf-mfapi-mfstartup">MFStartup</a> function.

## -see-also

<a href="/windows/desktop/api/mfcaptureengine/nn-mfcaptureengine-imfcaptureengineclassfactory">IMFCaptureEngineClassFactory</a>
