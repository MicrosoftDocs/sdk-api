---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
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
 

 

