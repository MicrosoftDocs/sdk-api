---
UID: NF:wincrypt.CertFreeCertificateChain
title: CertFreeCertificateChain function (wincrypt.h)
description: The CertFreeCertificateChain function frees a certificate chain by reducing its reference count. If the reference count becomes zero, memory allocated for the chain is released.
helpviewer_keywords: ["CertFreeCertificateChain","CertFreeCertificateChain function [Security]","_crypto2_certfreecertificatechain","security.certfreecertificatechain","wincrypt/CertFreeCertificateChain"]
old-location: security\certfreecertificatechain.htm
tech.root: security
ms.assetid: 5ba181c2-6936-4848-a571-2bb58f46f081
ms.date: 12/05/2018
ms.keywords: CertFreeCertificateChain, CertFreeCertificateChain function [Security], _crypto2_certfreecertificatechain, security.certfreecertificatechain, wincrypt/CertFreeCertificateChain
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CertFreeCertificateChain
 - wincrypt/CertFreeCertificateChain
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Crypt32.dll
api_name:
 - CertFreeCertificateChain
---

# CertFreeCertificateChain function


## -description

The <b>CertFreeCertificateChain</b> function frees a certificate chain by reducing its <a href="/windows/desktop/SecGloss/r-gly">reference count</a>. If the reference count becomes zero, memory allocated for the chain is released.

To free a context obtained by a get, duplicate, or create function, call the appropriate free function.  To free a context obtained by a find or enumerate function, either pass it in   as the previous context parameter to a subsequent invocation of the function, or call the appropriate free function.  For more information, see the  reference topic for the function that obtains the context.

## -parameters

### -param pChainContext [in]

A pointer to a 
<a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_chain_context">CERT_CHAIN_CONTEXT</a> certificate chain context to be freed. If the <a href="/windows/desktop/SecGloss/r-gly">reference count</a> on the context reaches zero, the storage allocated for the context is freed.

## -see-also

<a href="/windows/desktop/api/wincrypt/nf-wincrypt-certgetcertificatechain">CertGetCertificateChain</a>



<a href="/windows/desktop/SecCrypto/cryptography-functions">Certificate Chain Verification Functions</a>