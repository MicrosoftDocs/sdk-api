---
UID: NC:wincrypt.PFN_CERT_STORE_PROV_WRITE_CTL
title: PFN_CERT_STORE_PROV_WRITE_CTL (wincrypt.h)
description: The CertStoreProvWriteCTL callback function can be called by CertAddEncodedCTLToStore, CertAddCTLContextToStore or CertAddSerializedElementToStore before a CTL is added to the store.
helpviewer_keywords: ["CertStoreProvWriteCTL","PFN_CERT_STORE_PROV_WRITE_CTL","PFN_CERT_STORE_PROV_WRITE_CTL callback","PFN_CERT_STORE_PROV_WRITE_CTL callback function [Security]","_crypto2_certstoreprovwritectl","security.certstoreprovwritectl","wincrypt/PFN_CERT_STORE_PROV_WRITE_CTL"]
old-location: security\certstoreprovwritectl.htm
tech.root: security
ms.assetid: 91344133-0785-4c4f-8df3-83301cf85e70
ms.date: 12/05/2018
ms.keywords: CertStoreProvWriteCTL, PFN_CERT_STORE_PROV_WRITE_CTL, PFN_CERT_STORE_PROV_WRITE_CTL callback, PFN_CERT_STORE_PROV_WRITE_CTL callback function [Security], _crypto2_certstoreprovwritectl, security.certstoreprovwritectl, wincrypt/PFN_CERT_STORE_PROV_WRITE_CTL
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
 - PFN_CERT_STORE_PROV_WRITE_CTL
 - wincrypt/PFN_CERT_STORE_PROV_WRITE_CTL
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
 - PFN_CERT_STORE_PROV_WRITE_CTL
---

# PFN_CERT_STORE_PROV_WRITE_CTL callback function


## -description

The <b>CertStoreProvWriteCTL</b> callback function can be called by 
<a href="/windows/desktop/api/wincrypt/nf-wincrypt-certaddencodedctltostore">CertAddEncodedCTLToStore</a>, 
<a href="/windows/desktop/api/wincrypt/nf-wincrypt-certaddctlcontexttostore">CertAddCTLContextToStore</a> or 
<a href="/windows/desktop/api/wincrypt/nf-wincrypt-certaddserializedelementtostore">CertAddSerializedElementToStore</a> before a CTL is added to the store.

## -parameters

### -param hStoreProv [in]

<b>HCERTSTOREPROV</b> handle to a <a href="/windows/desktop/SecGloss/c-gly">certificate store</a>.

### -param pCtlContext [in]

A pointer to a 
<a href="/windows/desktop/api/wincrypt/ns-wincrypt-ctl_context">CTL_CONTEXT</a> structure.

### -param dwFlags [in]

Any needed flag values.

## -returns

Returns <b>TRUE</b> if elements can be added to the store.

## -see-also

<a href="/windows/desktop/api/wincrypt/ns-wincrypt-ctl_context">CTL_CONTEXT</a>



<a href="/windows/desktop/api/wincrypt/nf-wincrypt-certaddctlcontexttostore">CertAddCTLContextToStore</a>



<a href="/windows/desktop/api/wincrypt/nf-wincrypt-certaddencodedctltostore">CertAddEncodedCTLToStore</a>



<a href="/windows/desktop/api/wincrypt/nf-wincrypt-certaddserializedelementtostore">CertAddSerializedElementToStore</a>