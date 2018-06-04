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

# CertGetServerOcspResponseContext function


## -description


The <b>CertGetServerOcspResponseContext</b> function retrieves a non-blocking, time valid <a href="https://msdn.microsoft.com/e6be8932-015e-4058-b249-1671b3fea521">online certificate status protocol</a> (OCSP) response context for the specified handle.


## -parameters




### -param hServerOcspResponse [in]

The OCSP server response handle for which to retrieve a response context. This handle is returned by the <a href="https://msdn.microsoft.com/c29d1972-b329-4e32-aead-a038130fb85e">CertOpenServerOcspResponse</a> function.


### -param dwFlags [in]

This parameter is reserved for future use and must be zero.


### -param pvReserved

This parameter is reserved for future use and must be <b>NULL</b>.


## -returns



If the function succeeds, it returns a pointer to a <a href="https://msdn.microsoft.com/732e91a3-dcd2-491a-ba4f-e22b75b5a71e">CERT_SERVER_OCSP_RESPONSE_CONTEXT</a> structure.

For a response to be time valid, the current time on the system hosting this function call must be less than the next update time for the <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">certificate revocation list</a> (CRL) context. When a time valid OCSP response
is not available, this function returns <b>NULL</b> with the last error set to
CRYPT_E_REVOCATION_OFFLINE.




## -remarks



If you use the <b>CertGetServerOcspResponseContext</b> function to create multiple references to an OCSP response context, you must call <a href="https://msdn.microsoft.com/b7cdce9b-25fe-4fb9-b266-61989793699b">CertAddRefServerOcspResponseContext</a> to increment the reference count for the <a href="https://msdn.microsoft.com/732e91a3-dcd2-491a-ba4f-e22b75b5a71e">CERT_SERVER_OCSP_RESPONSE_CONTEXT</a> structure. When you have finished using the structure, you must free it by calling the <a href="https://msdn.microsoft.com/a07fc1e0-6f06-4336-b33c-d4d6a838b609">CertFreeServerOcspResponseContext</a> function.



