---
UID: NC:wincrypt.PFN_CERT_STORE_PROV_SET_CTL_PROPERTY
title: PFN_CERT_STORE_PROV_SET_CTL_PROPERTY (wincrypt.h)
description: The CertStoreProvSetCTLProperty callback function determines whether a property can be set on a CTL.
helpviewer_keywords: ["CertStoreProvSetCTLProperty","PFN_CERT_STORE_PROV_SET_CTL_PROPERTY","PFN_CERT_STORE_PROV_SET_CTL_PROPERTY callback","PFN_CERT_STORE_PROV_SET_CTL_PROPERTY callback function [Security]","_crypto2_certstoreprovsetctlproperty","security.certstoreprovsetctlproperty","wincrypt/PFN_CERT_STORE_PROV_SET_CTL_PROPERTY"]
old-location: security\certstoreprovsetctlproperty.htm
tech.root: security
ms.assetid: d062c875-b8c1-454f-8a0d-2ada74e5028d
ms.date: 12/05/2018
ms.keywords: CertStoreProvSetCTLProperty, PFN_CERT_STORE_PROV_SET_CTL_PROPERTY, PFN_CERT_STORE_PROV_SET_CTL_PROPERTY callback, PFN_CERT_STORE_PROV_SET_CTL_PROPERTY callback function [Security], _crypto2_certstoreprovsetctlproperty, security.certstoreprovsetctlproperty, wincrypt/PFN_CERT_STORE_PROV_SET_CTL_PROPERTY
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
 - PFN_CERT_STORE_PROV_SET_CTL_PROPERTY
 - wincrypt/PFN_CERT_STORE_PROV_SET_CTL_PROPERTY
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
 - PFN_CERT_STORE_PROV_SET_CTL_PROPERTY
---

# PFN_CERT_STORE_PROV_SET_CTL_PROPERTY callback function


## -description

The <b>CertStoreProvSetCTLProperty</b> callback function determines whether a property can be set on a CTL. It is called by 
<a href="/windows/desktop/api/wincrypt/nf-wincrypt-certsetctlcontextproperty">CertSetCTLContextProperty</a> before setting a CTL's property. It can also be called by 
<a href="/windows/desktop/api/wincrypt/nf-wincrypt-certgetctlcontextproperty">CertGetCTLContextProperty</a>, when getting a hash property that needs to be created and then persisted. This callback function does not set the 
<a href="/windows/desktop/api/wincrypt/ns-wincrypt-ctl_context">CTL_CONTEXT</a>'s property.

## -parameters

### -param hStoreProv [in]

A handle to a <a href="/windows/desktop/SecGloss/c-gly">certificate store</a>.

### -param pCtlContext [in]

A pointer to a 
<a href="/windows/desktop/api/wincrypt/ns-wincrypt-ctl_context">CTL_CONTEXT</a> structure.

### -param dwPropId [in]

Identifier of the property to be set.

### -param dwFlags [in]

Any needed flag values.

### -param pvData [in]

A pointer to a buffer containing the property value to be set.

## -returns

Returns <b>TRUE</b> if the property can be set. Returns <b>FALSE</b> if the property cannot be set.

## -see-also

<a href="/windows/desktop/api/wincrypt/ns-wincrypt-ctl_context">CTL_CONTEXT</a>



<a href="/windows/desktop/api/wincrypt/nf-wincrypt-certgetctlcontextproperty">CertGetCTLContextProperty</a>



<a href="/windows/desktop/api/wincrypt/nf-wincrypt-certsetctlcontextproperty">CertSetCTLContextProperty</a>
