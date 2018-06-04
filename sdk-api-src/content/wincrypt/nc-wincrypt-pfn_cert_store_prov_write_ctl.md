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

# PFN_CERT_STORE_PROV_WRITE_CTL callback function


## -description



			The <b>CertStoreProvWriteCTL</b> callback function can be called by 
<a href="https://msdn.microsoft.com/4239d43e-187d-4f40-99ae-6f914b7577ac">CertAddEncodedCTLToStore</a>, 
<a href="https://msdn.microsoft.com/e8858f75-77a1-4c5f-a3e3-a645c5e0f053">CertAddCTLContextToStore</a> or 
<a href="https://msdn.microsoft.com/2726cd34-51ba-4f68-9a3c-7cd505eb32a1">CertAddSerializedElementToStore</a> before a CTL is added to the store.


## -parameters




### -param hStoreProv [in]

<b>HCERTSTOREPROV</b> handle to a <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">certificate store</a>.


### -param pCtlContext [in]

A pointer to a 
<a href="https://msdn.microsoft.com/780edddf-1b44-4292-9156-4dfd5100adb8">CTL_CONTEXT</a> structure.


### -param dwFlags [in]

Any needed flag values.


## -returns




						Returns <b>TRUE</b> if elements can be added to the store.




## -see-also




<a href="https://msdn.microsoft.com/780edddf-1b44-4292-9156-4dfd5100adb8">CTL_CONTEXT</a>



<a href="https://msdn.microsoft.com/e8858f75-77a1-4c5f-a3e3-a645c5e0f053">CertAddCTLContextToStore</a>



<a href="https://msdn.microsoft.com/4239d43e-187d-4f40-99ae-6f914b7577ac">CertAddEncodedCTLToStore</a>



<a href="https://msdn.microsoft.com/2726cd34-51ba-4f68-9a3c-7cd505eb32a1">CertAddSerializedElementToStore</a>
 

 

