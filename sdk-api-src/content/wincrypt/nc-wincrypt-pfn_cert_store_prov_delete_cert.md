---
UID: NC:wincrypt.PFN_CERT_STORE_PROV_DELETE_CERT
title: PFN_CERT_STORE_PROV_DELETE_CERT (wincrypt.h)
description: An application-defined callback function that is called by CertDeleteCertificateFromStore before deleting a certificate from the store.
helpviewer_keywords: ["CertStoreProvDeleteCertCallback","PFN_CERT_STORE_PROV_DELETE_CERT","PFN_CERT_STORE_PROV_DELETE_CERT callback","PFN_CERT_STORE_PROV_DELETE_CERT callback function [Security]","_crypto2_certstoreprovdeletecertcallback","security.certstoreprovdeletecertcallback","wincrypt/PFN_CERT_STORE_PROV_DELETE_CERT"]
old-location: security\certstoreprovdeletecertcallback.htm
tech.root: security
ms.assetid: 0ae64bbc-05f6-4fc2-a05d-895654b4b97d
ms.date: 12/05/2018
ms.keywords: CertStoreProvDeleteCertCallback, PFN_CERT_STORE_PROV_DELETE_CERT, PFN_CERT_STORE_PROV_DELETE_CERT callback, PFN_CERT_STORE_PROV_DELETE_CERT callback function [Security], _crypto2_certstoreprovdeletecertcallback, security.certstoreprovdeletecertcallback, wincrypt/PFN_CERT_STORE_PROV_DELETE_CERT
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
 - PFN_CERT_STORE_PROV_DELETE_CERT
 - wincrypt/PFN_CERT_STORE_PROV_DELETE_CERT
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
 - PFN_CERT_STORE_PROV_DELETE_CERT
---

# PFN_CERT_STORE_PROV_DELETE_CERT callback function


## -description

An application-defined callback function that is called by 
<a href="/windows/desktop/api/wincrypt/nf-wincrypt-certdeletecertificatefromstore">CertDeleteCertificateFromStore</a> before deleting a certificate from the store.

## -parameters

### -param hStoreProv [in]

Provider-specific value returned in 
<a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_store_prov_info">CERT_STORE_PROV_INFO</a> by 
<a href="/windows/desktop/api/wincrypt/nc-wincrypt-pfn_cert_dll_open_store_prov_func">CertDllOpenStoreProv</a>.

### -param pCertContext [in]

A pointer to the certificate context to be deleted.

### -param dwFlags [in]

Reserved for future use and is set to zero.

## -returns

Returns <b>TRUE</b> if it is okay to delete the certificate from the store. Otherwise, returns <b>FALSE</b>.

## -see-also

<a href="/windows/desktop/SecCrypto/cryptography-functions">Callback Functions</a>