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

# PFN_CERT_STORE_PROV_DELETE_CERT callback function


## -description



			An application-defined callback function that is called by 
<a href="https://msdn.microsoft.com/4390c8da-9c4d-47a4-9af4-d179829f77f3">CertDeleteCertificateFromStore</a> before deleting a certificate from the store.


## -parameters




### -param hStoreProv [in]

Provider-specific value returned in 
<a href="https://msdn.microsoft.com/dc6789a7-09a5-467a-b2e4-16acfa25b5f6">CERT_STORE_PROV_INFO</a> by 
<a href="https://msdn.microsoft.com/2fe291dd-23e2-49df-b9e4-a4ed29667123">CertDllOpenStoreProv</a>.


### -param pCertContext [in]

A pointer to the certificate context to be deleted.


### -param dwFlags [in]

Reserved for future use and is set to zero.


## -returns




						Returns <b>TRUE</b> if it is okay to delete the certificate from the store. Otherwise, returns <b>FALSE</b>.




## -see-also




<a href="cryptography_functions.htm">Callback Functions</a>
 

 

