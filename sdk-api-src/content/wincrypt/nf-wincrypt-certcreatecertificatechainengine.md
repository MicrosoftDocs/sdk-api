---
UID: NF:wincrypt.CertCreateCertificateChainEngine
title: CertCreateCertificateChainEngine function (wincrypt.h)
author: windows-sdk-content
description: The CertCreateCertificateChainEngine function creates a new, nondefault chain engine for an application.
old-location: security\certcreatecertificatechainengine.htm
tech.root: SecCrypto
ms.assetid: e173016a-d3d7-42e0-aad8-e738abaf1df9
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: CertCreateCertificateChainEngine, CertCreateCertificateChainEngine function [Security], _crypto2_certcreatecertificatechainengine, security.certcreatecertificatechainengine, wincrypt/CertCreateCertificateChainEngine
ms.topic: function
f1_keywords:
- wincrypt/CertCreateCertificateChainEngine
req.header: wincrypt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2003 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Crypt32.lib
req.dll: Crypt32.dll
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- DllExport
api_location:
- Crypt32.dll
api_name:
- CertCreateCertificateChainEngine
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# CertCreateCertificateChainEngine function


## -description


The <b>CertCreateCertificateChainEngine</b> function creates a new, nondefault chain engine for an application. A chain engine restricts the certificates in the root store that can be used for verification, restricts the certificate stores to be searched for certificates and <a href="https://docs.microsoft.com/windows/desktop/SecGloss/c-gly">certificate trust lists</a> (CTLs), sets a time-out limit for searches that involve URLs, and limits the number of certificates checked between checking for a certificate cycle.


## -parameters




### -param pConfig [in]

A pointer to a 
<a href="https://docs.microsoft.com/windows/desktop/api/wincrypt/ns-wincrypt-cert_chain_engine_config">CERT_CHAIN_ENGINE_CONFIG</a> data structure that specifies the parameters for the chain engine.


### -param phChainEngine [out]

A pointer to the handle of the chain engine created. When you have finished using the chain engine, release the chain engine by calling the <a href="https://docs.microsoft.com/windows/desktop/api/wincrypt/nf-wincrypt-certfreecertificatechainengine">CertFreeCertificateChainEngine</a> function.


## -returns



If the function succeeds, the function returns nonzero (<b>TRUE</b>).

If the function fails, it returns zero (<b>FALSE</b>). For extended error information, call 
<a href="https://docs.microsoft.com/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

The <i>phChainEngine</i> parameter returns the chain engine handle.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/wincrypt/ns-wincrypt-cert_chain_engine_config">CERT_CHAIN_ENGINE_CONFIG</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wincrypt/nf-wincrypt-certfreecertificatechainengine">CertFreeCertificateChainEngine</a>



<a href="https://docs.microsoft.com/windows/desktop/SecCrypto/cryptography-functions">Certificate Chain Verification Functions</a>



<a href="https://docs.microsoft.com/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>
 

 

