---
UID: NC:wincrypt.PFN_CERT_STORE_PROV_READ_CERT
title: PFN_CERT_STORE_PROV_READ_CERT
author: windows-sdk-content
description: An application-defined callback function that reads the provider's copy of the certificate context.
old-location: security\certstoreprovreadcertcallback.htm
tech.root: seccrypto
ms.assetid: 9073f41e-19cd-46af-9e05-3f55607802c3
ms.author: windowssdkdev
ms.date: 10/01/2018
ms.keywords: CertStoreProvReadCertCallback, PFN_CERT_STORE_PROV_READ_CERT, PFN_CERT_STORE_PROV_READ_CERT callback, PFN_CERT_STORE_PROV_READ_CERT callback function [Security], _crypto2_certstoreprovreadcertcallback, security.certstoreprovreadcertcallback, wincrypt/PFN_CERT_STORE_PROV_READ_CERT
ms.prod: windows
ms.technology: windows-sdk
ms.topic: callback
req.header: wincrypt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
 - UserDefined
api_location:
 - Wincrypt.h
api_name:
 - PFN_CERT_STORE_PROV_READ_CERT
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# PFN_CERT_STORE_PROV_READ_CERT callback function


## -description


An application-defined callback function that reads the provider's copy of the <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">certificate context</a>. If one exists, a new certificate context is created. Currently not called directly by the <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">certificate store</a> functions. However, it might be exported to support other providers.


## -parameters




### -param hStoreProv [in]

Provider-specific value returned in 
<a href="https://msdn.microsoft.com/dc6789a7-09a5-467a-b2e4-16acfa25b5f6">CERT_STORE_PROV_INFO</a> by 
<a href="https://msdn.microsoft.com/2fe291dd-23e2-49df-b9e4-a4ed29667123">CertDllOpenStoreProv</a>.


### -param pStoreCertContext [in]

A pointer to the 
<a href="https://msdn.microsoft.com/f0a3200e-6541-423d-a4a3-595a31026eea">CERT_CONTEXT</a> of the certificate to be read.


### -param dwFlags [in]

Reserved for future use and is set to zero.


### -param *ppProvCertContext [out]

A pointer to a pointer to provider's copy of the <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">certificate context</a>. The context will be freed by calling 
<a href="https://msdn.microsoft.com/7d2f3237-3f8b-4234-b6db-3057384cd89b">CertFreeCertificateContext</a>.


## -returns



Returns <b>TRUE</b> if the certificate was successfully read.




## -see-also




<a href="https://msdn.microsoft.com/f0a3200e-6541-423d-a4a3-595a31026eea">CERT_CONTEXT</a>



<a href="https://msdn.microsoft.com/dc6789a7-09a5-467a-b2e4-16acfa25b5f6">CERT_STORE_PROV_INFO</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa380252(v=VS.85).aspx">Callback Functions</a>



<a href="https://msdn.microsoft.com/2fe291dd-23e2-49df-b9e4-a4ed29667123">CertDllOpenStoreProv</a>



<a href="https://msdn.microsoft.com/7d2f3237-3f8b-4234-b6db-3057384cd89b">CertFreeCertificateContext</a>
 

 

