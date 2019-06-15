---
UID: NF:wincrypt.CertDuplicateCertificateChain
title: CertDuplicateCertificateChain function (wincrypt.h)
author: windows-sdk-content
description: The CertDuplicateCertificateChain function duplicates a pointer to a certificate chain by incrementing the chain's reference count.
old-location: security\certduplicatecertificatechain.htm
tech.root: SecCrypto
ms.assetid: fea72a3e-5a22-47c7-8f6e-0d76fc3339f8
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: CertDuplicateCertificateChain, CertDuplicateCertificateChain function [Security], _crypto2_certduplicatecertificatechain, security.certduplicatecertificatechain, wincrypt/CertDuplicateCertificateChain
ms.topic: function
f1_keywords: ["wincrypt/CertDuplicateCertificateChain"]
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
 - CertDuplicateCertificateChain
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# CertDuplicateCertificateChain function


## -description


The <b>CertDuplicateCertificateChain</b> function duplicates a pointer to a certificate chain by incrementing the chain's <a href="https://docs.microsoft.com/windows/desktop/SecGloss/r-gly">reference count</a>.


## -parameters




### -param pChainContext [in]

A pointer to a 
<a href="https://docs.microsoft.com/windows/desktop/api/wincrypt/ns-wincrypt-_cert_chain_context">CERT_CHAIN_CONTEXT</a> chain context to be duplicated.


## -returns



If the function succeeds, a pointer is returned to the chain context. This pointer has the same value as the <i>pChainContext</i> passed into the function. When you have finished using the chain context, release the chain context by calling the <a href="https://docs.microsoft.com/windows/desktop/api/wincrypt/nf-wincrypt-certfreecertificatechain">CertFreeCertificateChain</a> function.

If the function fails, <b>NULL</b> is returned.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/wincrypt/nf-wincrypt-certgetcertificatechain">CertGetCertificateChain</a>



<a href="https://docs.microsoft.com/windows/desktop/SecCrypto/cryptography-functions">Certificate Chain Verification Functions</a>
 

 

