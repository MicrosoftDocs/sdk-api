---
UID: NF:wincrypt.CertDuplicateCertificateContext
title: CertDuplicateCertificateContext function (wincrypt.h)
description: Duplicates a certificate context by incrementing its reference count.
helpviewer_keywords: ["CertDuplicateCertificateContext","CertDuplicateCertificateContext function [Security]","_crypto2_certduplicatecertificatecontext","security.certduplicatecertificatecontext","wincrypt/CertDuplicateCertificateContext"]
old-location: security\certduplicatecertificatecontext.htm
tech.root: security
ms.assetid: 589edd25-c8d0-4f93-83b2-9df2ed2e2812
ms.date: 12/05/2018
ms.keywords: CertDuplicateCertificateContext, CertDuplicateCertificateContext function [Security], _crypto2_certduplicatecertificatecontext, security.certduplicatecertificatecontext, wincrypt/CertDuplicateCertificateContext
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
 - CertDuplicateCertificateContext
 - wincrypt/CertDuplicateCertificateContext
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
 - CertDuplicateCertificateContext
---

# CertDuplicateCertificateContext function


## -description

The <b>CertDuplicateCertificateContext</b> function duplicates a <a href="/windows/desktop/SecGloss/c-gly">certificate context</a> by incrementing its <a href="/windows/desktop/SecGloss/r-gly">reference count</a>.

## -parameters

### -param pCertContext [in]

A pointer to the 
<a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_context">CERT_CONTEXT</a> structure for which the <a href="/windows/desktop/SecGloss/r-gly">reference count</a> is incremented.

## -returns

Currently, a copy is not made of the <a href="/windows/desktop/SecGloss/c-gly">context</a>, and the returned pointer to a context has the same value as the pointer to a context that was input. If the pointer passed into this function is <b>NULL</b>, <b>NULL</b> is returned. When you have finished using the duplicate context, decrease its reference count by calling the <a href="/windows/desktop/api/wincrypt/nf-wincrypt-certfreecertificatecontext">CertFreeCertificateContext</a> function.

## -see-also

<a href="/windows/desktop/api/wincrypt/nf-wincrypt-certduplicatecrlcontext">CertDuplicateCRLContext</a>



<a href="/windows/desktop/api/wincrypt/nf-wincrypt-certfreecertificatecontext">CertFreeCertificateContext</a>



<a href="/windows/desktop/SecCrypto/cryptography-functions">Certificate Functions</a>