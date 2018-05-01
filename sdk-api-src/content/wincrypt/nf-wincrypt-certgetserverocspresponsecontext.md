---
UID: NF:wincrypt.CertGetServerOcspResponseContext
title: CertGetServerOcspResponseContext function
author: windows-driver-content
description: Retrieves a non-blocking, time valid online certificate status protocol (OCSP) response context for the specified handle.
old-location: security\certgetserverocspresponsecontext.htm
old-project: SecCrypto
ms.assetid: 07476e43-db6b-4119-8d6b-41143b98744e
ms.author: windowsdriverdev
ms.date: 4/18/2018
ms.keywords: CertGetServerOcspResponseContext, CertGetServerOcspResponseContext function [Security], security.certgetserverocspresponsecontext, wincrypt/CertGetServerOcspResponseContext
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: wincrypt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: USERNAME_TARGET_CREDENTIAL_INFO, *PUSERNAME_TARGET_CREDENTIAL_INFO
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Crypt32.dll
api_name:
-	CertGetServerOcspResponseContext
product: Windows
targetos: Windows
req.lib: Crypt32.lib
req.dll: Crypt32.dll
req.irql: 
req.product: Windows Address Book 5.0
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



