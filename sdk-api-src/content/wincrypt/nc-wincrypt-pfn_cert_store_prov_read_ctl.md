---
UID: NC:wincrypt.PFN_CERT_STORE_PROV_READ_CTL
title: PFN_CERT_STORE_PROV_READ_CTL (wincrypt.h)
description: The CertStoreProvReadCTL callback function is called to read the provider's copy of the CTL context and, if it exists, to create a new CTL context.
helpviewer_keywords: ["CertStoreProvReadCTL","PFN_CERT_STORE_PROV_READ_CTL","PFN_CERT_STORE_PROV_READ_CTL callback","PFN_CERT_STORE_PROV_READ_CTL callback function [Security]","_crypto2_certstoreprovreadctl","security.certstoreprovreadctl","wincrypt/PFN_CERT_STORE_PROV_READ_CTL"]
old-location: security\certstoreprovreadctl.htm
tech.root: security
ms.assetid: 09fbf42d-ed7a-4b1d-bad6-3bf8f216603c
ms.date: 12/05/2018
ms.keywords: CertStoreProvReadCTL, PFN_CERT_STORE_PROV_READ_CTL, PFN_CERT_STORE_PROV_READ_CTL callback, PFN_CERT_STORE_PROV_READ_CTL callback function [Security], _crypto2_certstoreprovreadctl, security.certstoreprovreadctl, wincrypt/PFN_CERT_STORE_PROV_READ_CTL
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
 - PFN_CERT_STORE_PROV_READ_CTL
 - wincrypt/PFN_CERT_STORE_PROV_READ_CTL
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
 - PFN_CERT_STORE_PROV_READ_CTL
---

# PFN_CERT_STORE_PROV_READ_CTL callback function


## -description

The <b>CertStoreProvReadCTL</b> callback function is called to read the provider's copy of the <a href="/windows/desktop/SecGloss/c-gly">CTL</a> context and, if it exists, to create a new CTL context. Currently, this callback function is not called directly by the store APIs but it can be exported to support other providers based on it.

## -parameters

### -param hStoreProv [in]

<b>HCERTSTOREPROV</b> handle to a <a href="/windows/desktop/SecGloss/c-gly">certificate store</a>.

### -param pStoreCtlContext [in]

A pointer to a 
<a href="/windows/desktop/api/wincrypt/ns-wincrypt-ctl_context">CTL_CONTEXT</a> structure.

### -param dwFlags [in]

Any needed flag values.

### -param ppProvCtlContext [out]

A pointer to a pointer to a <a href="/windows/desktop/api/wincrypt/ns-wincrypt-ctl_context">CTL_CONTEXT</a> structure to be returned by the function. The context will be freed by calling <a href="/windows/desktop/api/wincrypt/nf-wincrypt-certfreectlcontext">CertFreeCTLContext</a>.

## -returns

Returns <b>TRUE</b> if the function succeeds or <b>FALSE</b> if it fails.

## -see-also

<a href="/windows/desktop/api/wincrypt/ns-wincrypt-ctl_context">CTL_CONTEXT</a>
