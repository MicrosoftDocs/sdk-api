---
UID: NC:wincrypt.PFN_CERT_STORE_PROV_READ_CERT
title: PFN_CERT_STORE_PROV_READ_CERT (wincrypt.h)
description: An application-defined callback function that reads the provider's copy of the certificate context.
helpviewer_keywords: ["CertStoreProvReadCertCallback","PFN_CERT_STORE_PROV_READ_CERT","PFN_CERT_STORE_PROV_READ_CERT callback","PFN_CERT_STORE_PROV_READ_CERT callback function [Security]","_crypto2_certstoreprovreadcertcallback","security.certstoreprovreadcertcallback","wincrypt/PFN_CERT_STORE_PROV_READ_CERT"]
old-location: security\certstoreprovreadcertcallback.htm
tech.root: security
ms.assetid: 9073f41e-19cd-46af-9e05-3f55607802c3
ms.date: 12/05/2018
ms.keywords: CertStoreProvReadCertCallback, PFN_CERT_STORE_PROV_READ_CERT, PFN_CERT_STORE_PROV_READ_CERT callback, PFN_CERT_STORE_PROV_READ_CERT callback function [Security], _crypto2_certstoreprovreadcertcallback, security.certstoreprovreadcertcallback, wincrypt/PFN_CERT_STORE_PROV_READ_CERT
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - PFN_CERT_STORE_PROV_READ_CERT
 - wincrypt/PFN_CERT_STORE_PROV_READ_CERT
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Wincrypt.h
api_name:
 - PFN_CERT_STORE_PROV_READ_CERT
---

# PFN_CERT_STORE_PROV_READ_CERT callback function


## -description

An application-defined callback function that reads the provider's copy of the <a href="/windows/desktop/SecGloss/c-gly">certificate context</a>. If one exists, a new certificate context is created. Currently not called directly by the <a href="/windows/desktop/SecGloss/c-gly">certificate store</a> functions. However, it might be exported to support other providers.

## -parameters

### -param hStoreProv [in]

Provider-specific value returned in 
<a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_store_prov_info">CERT_STORE_PROV_INFO</a> by 
<a href="/windows/desktop/api/wincrypt/nc-wincrypt-pfn_cert_dll_open_store_prov_func">CertDllOpenStoreProv</a>.

### -param pStoreCertContext [in]

A pointer to the 
<a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_context">CERT_CONTEXT</a> of the certificate to be read.

### -param dwFlags [in]

Reserved for future use and is set to zero.

### -param ppProvCertContext [out]

A pointer to a pointer to provider's copy of the <a href="/windows/desktop/SecGloss/c-gly">certificate context</a>. The context will be freed by calling 
<a href="/windows/desktop/api/wincrypt/nf-wincrypt-certfreecertificatecontext">CertFreeCertificateContext</a>.

## -returns

Returns <b>TRUE</b> if the certificate was successfully read.

## -see-also

<a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_context">CERT_CONTEXT</a>



<a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_store_prov_info">CERT_STORE_PROV_INFO</a>



<a href="/windows/desktop/SecCrypto/cryptography-functions">Callback Functions</a>



<a href="/windows/desktop/api/wincrypt/nc-wincrypt-pfn_cert_dll_open_store_prov_func">CertDllOpenStoreProv</a>



<a href="/windows/desktop/api/wincrypt/nf-wincrypt-certfreecertificatecontext">CertFreeCertificateContext</a>
