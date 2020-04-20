---
UID: NF:wincrypt.CertFreeCertificateContext
title: CertFreeCertificateContext function (wincrypt.h)
description: Frees a certificate context by decrementing its reference count. When the reference count goes to zero, CertFreeCertificateContext frees the memory used by a certificate context.helpviewer_keywords: ["CertFreeCertificateContext","CertFreeCertificateContext function [Security]","_crypto2_certfreecertificatecontext","security.certfreecertificatecontext","wincrypt/CertFreeCertificateContext"]
old-location: security\certfreecertificatecontext.htm
tech.root: SecCrypto
ms.assetid: 7d2f3237-3f8b-4234-b6db-3057384cd89b
ms.date: 12/05/2018
ms.keywords: CertFreeCertificateContext, CertFreeCertificateContext function [Security], _crypto2_certfreecertificatecontext, security.certfreecertificatecontext, wincrypt/CertFreeCertificateContext
f1_keywords:
- wincrypt/CertFreeCertificateContext
dev_langs:
- c++
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
- CertFreeCertificateContext
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# CertFreeCertificateContext function


## -description


The <b>CertFreeCertificateContext</b> function frees a <a href="https://docs.microsoft.com/windows/desktop/SecGloss/c-gly">certificate context</a> by decrementing its <a href="https://docs.microsoft.com/windows/desktop/SecGloss/r-gly">reference count</a>. When the reference count goes to zero, <b>CertFreeCertificateContext</b> frees the memory used by a certificate context.

To free a context obtained by a get, duplicate, or create function, call the appropriate free function.  To free a context obtained by a find or enumerate function, either pass it in   as the previous context parameter to a subsequent invocation of the function, or call the appropriate free function.  For more information, see the  reference topic for the function that obtains the context.


## -parameters




### -param pCertContext [in]

A pointer to the 
<a href="https://docs.microsoft.com/windows/desktop/api/wincrypt/ns-wincrypt-cert_context">CERT_CONTEXT</a> to be freed.


## -returns



The function always returns nonzero.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/wincrypt/nf-wincrypt-certfreecrlcontext">CertFreeCRLContext</a>



<a href="https://docs.microsoft.com/windows/desktop/SecCrypto/cryptography-functions">Certificate Functions</a>
 

 

