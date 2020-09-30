---
UID: NF:wincrypt.CertDuplicateCRLContext
title: CertDuplicateCRLContext function (wincrypt.h)
description: The CertDuplicateCRLContext function duplicates a certificate revocation list (CRL) context by incrementing its reference count.
helpviewer_keywords: ["CertDuplicateCRLContext","CertDuplicateCRLContext function [Security]","_crypto2_certduplicatecrlcontext","security.certduplicatecrlcontext","wincrypt/CertDuplicateCRLContext"]
old-location: security\certduplicatecrlcontext.htm
tech.root: security
ms.assetid: ea14c494-d1c7-46d0-9d56-fc89a4b4afa9
ms.date: 12/05/2018
ms.keywords: CertDuplicateCRLContext, CertDuplicateCRLContext function [Security], _crypto2_certduplicatecrlcontext, security.certduplicatecrlcontext, wincrypt/CertDuplicateCRLContext
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
 - CertDuplicateCRLContext
 - wincrypt/CertDuplicateCRLContext
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
 - CertDuplicateCRLContext
---

# CertDuplicateCRLContext function


## -description

The <b>CertDuplicateCRLContext</b> function duplicates a <a href="/windows/desktop/SecGloss/c-gly">certificate revocation list</a> (CRL) context by incrementing its <a href="/windows/desktop/SecGloss/r-gly">reference count</a>.

## -parameters

### -param pCrlContext [in]

A pointer to the 
<a href="/windows/desktop/api/wincrypt/ns-wincrypt-crl_context">CRL_CONTEXT</a> structure for which the <a href="/windows/desktop/SecGloss/r-gly">reference count</a> is being incremented.

## -returns

Currently, a copy is not made of the context, and the returned context is the same as the context that was input. If the pointer passed into this function is <b>NULL</b>, <b>NULL</b> is returned.

## -see-also

<a href="/windows/desktop/api/wincrypt/ns-wincrypt-crl_context">CRL_CONTEXT</a>



<a href="/windows/desktop/SecCrypto/cryptography-functions">Certificate Revocation List Functions</a>