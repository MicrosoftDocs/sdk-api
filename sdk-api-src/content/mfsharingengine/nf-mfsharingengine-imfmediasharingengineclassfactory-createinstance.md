---
UID: NF:mfsharingengine.IMFMediaSharingEngineClassFactory.CreateInstance
title: IMFMediaSharingEngineClassFactory::CreateInstance
author: windows-sdk-content
description: Creates an instance of the IMFMediaSharingEngine.
old-location: mf\imfmediasharingengineclassfactory_createinstance.htm
tech.root: MedFound
ms.assetid: D0FD55A1-0387-4450-8F05-3AC7E943F437
ms.author: windowssdkdev
ms.date: 09/27/2018
ms.keywords: CreateInstance, CreateInstance method [Media Foundation], CreateInstance method [Media Foundation],IMFMediaSharingEngineClassFactory interface, IMFMediaSharingEngineClassFactory interface [Media Foundation],CreateInstance method, IMFMediaSharingEngineClassFactory.CreateInstance, IMFMediaSharingEngineClassFactory::CreateInstance, mf.imfmediasharingengineclassfactory_createinstance, mfsharingengine/IMFMediaSharingEngineClassFactory::CreateInstance
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfsharingengine.h
api_name:
 - IMFMediaSharingEngineClassFactory.CreateInstance
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IMFMediaSharingEngineClassFactory::CreateInstance


## -description


Creates an instance of the <a href="https://msdn.microsoft.com/D56612FC-840A-41EE-B162-7AF16ED3D975">IMFMediaSharingEngine</a>.


## -parameters




### -param dwFlags [in]

A bitwise <b>OR</b> of zero or more flags from the <a href="https://msdn.microsoft.com/1709B08C-D4DC-4A33-9B92-1C4961208684">MF_MEDIA_ENGINE_CREATEFLAGS</a> enumeration.


### -param pAttr [in]

A pointer to the <a href="https://msdn.microsoft.com/e12259f4-b631-4d4a-a296-c1cc6334b962">IMFAttributes</a> interface of an attribute store. 


### -param ppEngine [out]

Receives a pointer to the <a href="https://msdn.microsoft.com/D56612FC-840A-41EE-B162-7AF16ED3D975">IMFMediaSharingEngine</a> interface. The caller must release the interface.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/C8732101-2512-4252-A8D0-677B394BDEB1">IMFMediaSharingEngineClassFactory</a>
 

 

