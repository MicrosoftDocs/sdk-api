---
UID: NF:mfcaptureengine.IMFCaptureEngineClassFactory.CreateInstance
title: IMFCaptureEngineClassFactory::CreateInstance
author: windows-sdk-content
description: Creates an instance of the capture engine.
old-location: mf\imfcaptureengineclassfactory_createinstance.htm
tech.root: medfound
ms.assetid: D5E7D96B-9438-4332-AD05-249D2DA2481A
ms.author: windowssdkdev
ms.date: 10/10/2018
ms.keywords: CreateInstance, CreateInstance method [Media Foundation], CreateInstance method [Media Foundation],IMFCaptureEngineClassFactory interface, IMFCaptureEngineClassFactory interface [Media Foundation],CreateInstance method, IMFCaptureEngineClassFactory.CreateInstance, IMFCaptureEngineClassFactory::CreateInstance, mf.imfcaptureengineclassfactory_createinstance, mfcaptureengine/IMFCaptureEngineClassFactory::CreateInstance
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfcaptureengine.h
api_name:
 - IMFCaptureEngineClassFactory.CreateInstance
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMFCaptureEngineClassFactory::CreateInstance


## -description


Creates an instance of the capture engine.


## -parameters




### -param clsid [in]

The CLSID of the object to create.

Currently, this parameter must equal <b>CLSID_MFCaptureEngine</b>.


### -param riid [in]

The IID of the requested interface. The capture engine supports the <a href="https://msdn.microsoft.com/4A2A0536-4255-40AB-BCAB-228B09343583">IMFCaptureEngine</a> interface.


### -param ppvObject [out]

Receives a pointer to the requested interface. The caller must release the interface.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



Before calling this method, call the <a href="https://msdn.microsoft.com/b4472e40-3681-4b26-9385-4df7bf19c2d8">MFStartup</a> function.




## -see-also




<a href="https://msdn.microsoft.com/FAFA52AD-B96E-4ADC-BE79-3BE5F1ACC92A">IMFCaptureEngineClassFactory</a>
 

 

