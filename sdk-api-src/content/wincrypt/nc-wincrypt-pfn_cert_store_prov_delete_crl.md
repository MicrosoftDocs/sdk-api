---
UID: NC:wincrypt.PFN_CERT_STORE_PROV_DELETE_CRL
title: PFN_CERT_STORE_PROV_DELETE_CRL (wincrypt.h)
description: An application-defined callback function that is called by CertDeleteCRLFromStore before deleting the CRL from the store.
helpviewer_keywords: ["CertStoreProvDeleteCRLCallback","PFN_CERT_STORE_PROV_DELETE_CRL","PFN_CERT_STORE_PROV_DELETE_CRL callback","PFN_CERT_STORE_PROV_DELETE_CRL callback function [Security]","_crypto2_certstoreprovdeletecrlcallback","security.certstoreprovdeletecrlcallback","wincrypt/PFN_CERT_STORE_PROV_DELETE_CRL"]
old-location: security\certstoreprovdeletecrlcallback.htm
tech.root: security
ms.assetid: aa93cfaf-238f-4d77-a1cd-433a856ed133
ms.date: 12/05/2018
ms.keywords: CertStoreProvDeleteCRLCallback, PFN_CERT_STORE_PROV_DELETE_CRL, PFN_CERT_STORE_PROV_DELETE_CRL callback, PFN_CERT_STORE_PROV_DELETE_CRL callback function [Security], _crypto2_certstoreprovdeletecrlcallback, security.certstoreprovdeletecrlcallback, wincrypt/PFN_CERT_STORE_PROV_DELETE_CRL
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
 - PFN_CERT_STORE_PROV_DELETE_CRL
 - wincrypt/PFN_CERT_STORE_PROV_DELETE_CRL
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
 - PFN_CERT_STORE_PROV_DELETE_CRL
---

# PFN_CERT_STORE_PROV_DELETE_CRL callback function


## -description

An application-defined callback function that is called by 
<a href="/windows/desktop/api/wincrypt/nf-wincrypt-certdeletecrlfromstore">CertDeleteCRLFromStore</a> before deleting the CRL from the store.

## -parameters

### -param hStoreProv [in]

Provider-specific value returned in 
<a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_store_prov_info">CERT_STORE_PROV_INFO</a> by 
<a href="/windows/desktop/api/wincrypt/nc-wincrypt-pfn_cert_dll_open_store_prov_func">CertDllOpenStoreProv</a>.

### -param pCrlContext [in]

A pointer to the CRL context to be deleted.

### -param dwFlags [in]

Reserved for future use and is set to zero.

## -returns

Returns <b>TRUE</b> if it is okay to delete from the store. Otherwise, returns <b>FALSE</b>.

## -see-also

<a href="/windows/desktop/SecCrypto/cryptography-functions">Callback Functions</a>