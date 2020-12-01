---
UID: NF:wincrypt.CertFreeCRLContext
title: CertFreeCRLContext function (wincrypt.h)
description: Frees a certificate revocation list (CRL) context by decrementing its reference count.
helpviewer_keywords: ["CertFreeCRLContext","CertFreeCRLContext function [Security]","_crypto2_certfreecrlcontext","security.certfreecrlcontext","wincrypt/CertFreeCRLContext"]
old-location: security\certfreecrlcontext.htm
tech.root: security
ms.assetid: 19a590a5-bd39-4bbe-ad86-4e648baa1ba8
ms.date: 12/05/2018
ms.keywords: CertFreeCRLContext, CertFreeCRLContext function [Security], _crypto2_certfreecrlcontext, security.certfreecrlcontext, wincrypt/CertFreeCRLContext
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
 - CertFreeCRLContext
 - wincrypt/CertFreeCRLContext
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
 - CertFreeCRLContext
---

# CertFreeCRLContext function


## -description

The <b>CertFreeCRLContext</b> function frees a <a href="/windows/desktop/SecGloss/c-gly">certificate revocation list</a> (CRL) context by decrementing its <a href="/windows/desktop/SecGloss/r-gly">reference count</a>. When the reference count goes to zero, <b>CertFreeCRLContext</b> frees the memory used by a CRL <a href="/windows/desktop/SecGloss/c-gly">context</a>.

To free a context obtained by a get, duplicate, or create function, call the appropriate free function.  To free a context obtained by a find or enumerate function, either pass it in   as the previous context parameter to a subsequent invocation of the function, or call the appropriate free function.  For more information, see the  reference topic for the function that obtains the context.

## -parameters

### -param pCrlContext [in]

A pointer to the 
<a href="/windows/desktop/api/wincrypt/ns-wincrypt-crl_context">CRL_CONTEXT</a> to be freed.

## -returns

The function always returns <b>TRUE</b>.

## -see-also

<a href="/windows/desktop/api/wincrypt/ns-wincrypt-crl_context">CRL_CONTEXT</a>



<a href="/windows/desktop/api/wincrypt/nf-wincrypt-certfreecertificatecontext">CertFreeCertificateContext</a>



<a href="/windows/desktop/SecCrypto/cryptography-functions">Certificate Revocation List Functions</a>