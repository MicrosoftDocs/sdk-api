---
UID: NC:wincrypt.PFN_CERT_STORE_PROV_READ_CRL
title: PFN_CERT_STORE_PROV_READ_CRL
author: windows-sdk-content
description: An application-defined callback function that reads the provider's copy of the CRL context.
old-location: security\certstoreprovreadcrlcallback.htm
tech.root: seccrypto
ms.assetid: 9644c200-1b55-4287-8d98-27b5a8d38c90
ms.author: windowssdkdev
ms.date: 10/10/2018
ms.keywords: CertStoreProvReadCRLCallback, PFN_CERT_STORE_PROV_READ_CRL, PFN_CERT_STORE_PROV_READ_CRL callback, PFN_CERT_STORE_PROV_READ_CRL callback function [Security], _crypto2_certstoreprovreadcrlcallback, security.certstoreprovreadcrlcallback, wincrypt/PFN_CERT_STORE_PROV_READ_CRL
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
 - PFN_CERT_STORE_PROV_READ_CRL
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# PFN_CERT_STORE_PROV_READ_CRL callback function


## -description


An application-defined callback function that reads the provider's copy of the <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">CRL</a> context. If one exists, a new CRL context is created.

Currently not called directly by the <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">certificate store</a> functions. However, might be exported to support other providers.


## -parameters




### -param hStoreProv [in]

Provider-specific value returned in 
<a href="https://msdn.microsoft.com/dc6789a7-09a5-467a-b2e4-16acfa25b5f6">CERT_STORE_PROV_INFO</a> by 
<a href="https://msdn.microsoft.com/2fe291dd-23e2-49df-b9e4-a4ed29667123">CertDllOpenStoreProv</a>.


### -param pStoreCrlContext [in]

A pointer to the 
<a href="https://msdn.microsoft.com/cf7cabcd-b469-492a-b855-8870465ea1cc">CRL_CONTEXT</a> of the CRL to be read.


### -param dwFlags [in]

Reserved for future use and is set to zero.


### -param *ppProvCrlContext [out]

A pointer to a pointer to provider's copy of the CRL context. The context will be freed by calling 
<a href="https://msdn.microsoft.com/19a590a5-bd39-4bbe-ad86-4e648baa1ba8">CertFreeCRLContext</a>.


## -returns



Returns TRUE if the CRL was successfully read.




## -see-also




<a href="https://msdn.microsoft.com/dc6789a7-09a5-467a-b2e4-16acfa25b5f6">CERT_STORE_PROV_INFO</a>



<a href="https://msdn.microsoft.com/cf7cabcd-b469-492a-b855-8870465ea1cc">CRL_CONTEXT</a>



<a href="cryptography_functions.htm">Callback Functions</a>



<a href="https://msdn.microsoft.com/2fe291dd-23e2-49df-b9e4-a4ed29667123">CertDllOpenStoreProv</a>



<a href="https://msdn.microsoft.com/19a590a5-bd39-4bbe-ad86-4e648baa1ba8">CertFreeCRLContext</a>
 

 

