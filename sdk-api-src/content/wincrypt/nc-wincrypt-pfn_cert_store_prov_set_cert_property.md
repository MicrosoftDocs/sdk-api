---
UID: NC:wincrypt.PFN_CERT_STORE_PROV_SET_CERT_PROPERTY
title: PFN_CERT_STORE_PROV_SET_CERT_PROPERTY (wincrypt.h)
description: An application-defined callback function that is called by CertSetCertificateContextProperty before setting the certificate's property.
helpviewer_keywords: ["CertStoreProvSetCertPropertyCallback","PFN_CERT_STORE_PROV_SET_CERT_PROPERTY","PFN_CERT_STORE_PROV_SET_CERT_PROPERTY callback","PFN_CERT_STORE_PROV_SET_CERT_PROPERTY callback function [Security]","_crypto2_certstoreprovsetcertpropertycallback","security.certstoreprovsetcertpropertycallback","wincrypt/PFN_CERT_STORE_PROV_SET_CERT_PROPERTY"]
old-location: security\certstoreprovsetcertpropertycallback.htm
tech.root: security
ms.assetid: 03d7e1f6-030f-4eae-b76d-5465748d9583
ms.date: 12/05/2018
ms.keywords: CertStoreProvSetCertPropertyCallback, PFN_CERT_STORE_PROV_SET_CERT_PROPERTY, PFN_CERT_STORE_PROV_SET_CERT_PROPERTY callback, PFN_CERT_STORE_PROV_SET_CERT_PROPERTY callback function [Security], _crypto2_certstoreprovsetcertpropertycallback, security.certstoreprovsetcertpropertycallback, wincrypt/PFN_CERT_STORE_PROV_SET_CERT_PROPERTY
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
 - PFN_CERT_STORE_PROV_SET_CERT_PROPERTY
 - wincrypt/PFN_CERT_STORE_PROV_SET_CERT_PROPERTY
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
 - PFN_CERT_STORE_PROV_SET_CERT_PROPERTY
---

# PFN_CERT_STORE_PROV_SET_CERT_PROPERTY callback function


## -description

An application-defined callback function that is called by 
<a href="/windows/desktop/api/wincrypt/nf-wincrypt-certsetcertificatecontextproperty">CertSetCertificateContextProperty</a> before setting the certificate's property. It is also called by 
<a href="/windows/desktop/api/wincrypt/nf-wincrypt-certgetcertificatecontextproperty">CertGetCertificateContextProperty</a> when getting a <a href="/windows/desktop/SecGloss/h-gly">hash</a> property that needs to be created and then persisted through the set.

Upon input, the property has not been set for the <i>pCertContext</i> parameter.

## -parameters

### -param hStoreProv [in]

Provider-specific value returned in 
<a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_store_prov_info">CERT_STORE_PROV_INFO</a> by 
<a href="/windows/desktop/api/wincrypt/nc-wincrypt-pfn_cert_dll_open_store_prov_func">CertDllOpenStoreProv</a>.

### -param pCertContext [in]

See 
<a href="/windows/desktop/api/wincrypt/nf-wincrypt-certsetcertificatecontextproperty">CertSetCertificateContextProperty</a>.

### -param dwPropId [in]

See <a href="/windows/desktop/api/wincrypt/nf-wincrypt-certsetcertificatecontextproperty">CertSetCertificateContextProperty</a>.

### -param dwFlags [in]

Copy of the <i>dwFlags</i> passed as a parameter to <a href="/windows/desktop/api/wincrypt/nf-wincrypt-certsetcertificatecontextproperty">CertSetCertificateContextProperty</a>.

### -param pvData [in]

See <a href="/windows/desktop/api/wincrypt/nf-wincrypt-certsetcertificatecontextproperty">CertSetCertificateContextProperty</a>.

## -returns

Returns <b>TRUE</b> if it is okay to set the property.

## -see-also

<a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_store_prov_info">CERT_STORE_PROV_INFO</a>



<a href="/windows/desktop/SecCrypto/cryptography-functions">Callback Functions</a>



<a href="/windows/desktop/api/wincrypt/nc-wincrypt-pfn_cert_dll_open_store_prov_func">CertDllOpenStoreProv</a>



<a href="/windows/desktop/api/wincrypt/nf-wincrypt-certgetcertificatecontextproperty">CertGetCertificateContextProperty</a>



<a href="/windows/desktop/api/wincrypt/nf-wincrypt-certsetcertificatecontextproperty">CertSetCertificateContextProperty</a>
