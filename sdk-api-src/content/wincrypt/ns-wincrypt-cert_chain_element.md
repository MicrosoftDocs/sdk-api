---
UID: NS:wincrypt._CERT_CHAIN_ELEMENT
title: CERT_CHAIN_ELEMENT (wincrypt.h)
description: The CERT_CHAIN_ELEMENT structure is a single element in a simple certificate chain.
helpviewer_keywords: ["*PCERT_CHAIN_ELEMENT","CERT_CHAIN_ELEMENT","CERT_CHAIN_ELEMENT structure [Security]","PCERT_CHAIN_ELEMENT","PCERT_CHAIN_ELEMENT structure pointer [Security]","_crypto2_cert_chain_element","security.cert_chain_element","wincrypt/CERT_CHAIN_ELEMENT","wincrypt/PCERT_CHAIN_ELEMENT"]
old-location: security\cert_chain_element.htm
tech.root: security
ms.assetid: a1f6ba18-63ef-43ac-a17f-900fa13398aa
ms.date: 12/05/2018
ms.keywords: '*PCERT_CHAIN_ELEMENT, CERT_CHAIN_ELEMENT, CERT_CHAIN_ELEMENT structure [Security], PCERT_CHAIN_ELEMENT, PCERT_CHAIN_ELEMENT structure pointer [Security], _crypto2_cert_chain_element, security.cert_chain_element, wincrypt/CERT_CHAIN_ELEMENT, wincrypt/PCERT_CHAIN_ELEMENT'
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
req.typenames: CERT_CHAIN_ELEMENT, *PCERT_CHAIN_ELEMENT
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _CERT_CHAIN_ELEMENT
 - wincrypt/_CERT_CHAIN_ELEMENT
 - PCERT_CHAIN_ELEMENT
 - wincrypt/PCERT_CHAIN_ELEMENT
 - CERT_CHAIN_ELEMENT
 - wincrypt/CERT_CHAIN_ELEMENT
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wincrypt.h
api_name:
 - CERT_CHAIN_ELEMENT
---

# CERT_CHAIN_ELEMENT structure


## -description

The <b>CERT_CHAIN_ELEMENT</b> structure is a single element in a simple certificate chain. Each element has a pointer to a <a href="/windows/desktop/SecGloss/c-gly">certificate context</a>, a pointer to a structure that indicates the error status and information status of the certificate, and a pointer to a structure that indicates the revocation status of the certificate.

## -struct-fields

### -field cbSize

Size of this structure in bytes.

### -field pCertContext

A pointer to a certificate <a href="/windows/desktop/SecGloss/c-gly">context</a>.

### -field TrustStatus

Structure indicating the status of the certificate. The structure includes an error status code and an information status code. For information about status code values, see CERT_TRUST_STATUS.

### -field pRevocationInfo

A pointer to a CERT_REVOCATION_INFO structure with information on the revocation status of the certificate. If revocation checking was not enabled, <b>pRevocationInfo</b> is <b>NULL</b>.

### -field pIssuanceUsage

A pointer to a CERT_ENHKEY_USAGE structure. If <b>NULL</b>, any issuance policy is acceptable.

### -field pApplicationUsage

A pointer to a CERT_ENHKEY_USAGE structure. If <b>NULL</b>, any enhanced key usage is acceptable.

### -field pwszExtendedErrorInfo

A pointer to a <b>null</b>-terminated wide character string that contains extended error information. If <b>NULL</b>, there is no extended error information.

## -see-also

<a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_revocation_info">CERT_REVOCATION_INFO</a>



<a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_simple_chain">CERT_SIMPLE_CHAIN</a>



<a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_trust_status">CERT_TRUST_STATUS</a>