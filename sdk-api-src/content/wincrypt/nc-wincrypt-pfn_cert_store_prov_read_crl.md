---
UID: NC:wincrypt.PFN_CERT_STORE_PROV_READ_CRL
title: PFN_CERT_STORE_PROV_READ_CRL (wincrypt.h)
description: An application-defined callback function that reads the provider's copy of the CRL context.
helpviewer_keywords: ["CertStoreProvReadCRLCallback","PFN_CERT_STORE_PROV_READ_CRL","PFN_CERT_STORE_PROV_READ_CRL callback","PFN_CERT_STORE_PROV_READ_CRL callback function [Security]","_crypto2_certstoreprovreadcrlcallback","security.certstoreprovreadcrlcallback","wincrypt/PFN_CERT_STORE_PROV_READ_CRL"]
old-location: security\certstoreprovreadcrlcallback.htm
tech.root: security
ms.assetid: 9644c200-1b55-4287-8d98-27b5a8d38c90
ms.date: 12/05/2018
ms.keywords: CertStoreProvReadCRLCallback, PFN_CERT_STORE_PROV_READ_CRL, PFN_CERT_STORE_PROV_READ_CRL callback, PFN_CERT_STORE_PROV_READ_CRL callback function [Security], _crypto2_certstoreprovreadcrlcallback, security.certstoreprovreadcrlcallback, wincrypt/PFN_CERT_STORE_PROV_READ_CRL
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
 - PFN_CERT_STORE_PROV_READ_CRL
 - wincrypt/PFN_CERT_STORE_PROV_READ_CRL
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
 - PFN_CERT_STORE_PROV_READ_CRL
---

# PFN_CERT_STORE_PROV_READ_CRL callback function


## -description

An application-defined callback function that reads the provider's copy of the <a href="/windows/desktop/SecGloss/c-gly">CRL</a> context. If one exists, a new CRL context is created.

Currently not called directly by the <a href="/windows/desktop/SecGloss/c-gly">certificate store</a> functions. However, might be exported to support other providers.

## -parameters

### -param hStoreProv [in]

Provider-specific value returned in 
<a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_store_prov_info">CERT_STORE_PROV_INFO</a> by 
<a href="/windows/desktop/api/wincrypt/nc-wincrypt-pfn_cert_dll_open_store_prov_func">CertDllOpenStoreProv</a>.

### -param pStoreCrlContext [in]

A pointer to the 
<a href="/windows/desktop/api/wincrypt/ns-wincrypt-crl_context">CRL_CONTEXT</a> of the CRL to be read.

### -param dwFlags [in]

Reserved for future use and is set to zero.

### -param ppProvCrlContext [out]

A pointer to a pointer to provider's copy of the CRL context. The context will be freed by calling 
<a href="/windows/desktop/api/wincrypt/nf-wincrypt-certfreecrlcontext">CertFreeCRLContext</a>.

## -returns

Returns TRUE if the CRL was successfully read.

## -see-also

<a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_store_prov_info">CERT_STORE_PROV_INFO</a>



<a href="/windows/desktop/api/wincrypt/ns-wincrypt-crl_context">CRL_CONTEXT</a>



<a href="/windows/desktop/SecCrypto/cryptography-functions">Callback Functions</a>



<a href="/windows/desktop/api/wincrypt/nc-wincrypt-pfn_cert_dll_open_store_prov_func">CertDllOpenStoreProv</a>



<a href="/windows/desktop/api/wincrypt/nf-wincrypt-certfreecrlcontext">CertFreeCRLContext</a>
