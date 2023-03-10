---
UID: NS:wincrypt._CERT_REVOCATION_INFO
title: CERT_REVOCATION_INFO (wincrypt.h)
description: Indicates the revocation status of a certificate in a CERT_CHAIN_ELEMENT.
helpviewer_keywords: ["*PCERT_REVOCATION_INFO","CERT_REVOCATION_INFO","CERT_REVOCATION_INFO structure [Security]","PCERT_REVOCATION_INFO","PCERT_REVOCATION_INFO structure pointer [Security]","_crypto2_cert_revocation_info","security.cert_revocation_info","wincrypt/CERT_REVOCATION_INFO","wincrypt/PCERT_REVOCATION_INFO"]
old-location: security\cert_revocation_info.htm
tech.root: security
ms.assetid: 798aa2d7-bf8a-425f-bc36-98a44ba3a9d6
ms.date: 12/05/2018
ms.keywords: '*PCERT_REVOCATION_INFO, CERT_REVOCATION_INFO, CERT_REVOCATION_INFO structure [Security], PCERT_REVOCATION_INFO, PCERT_REVOCATION_INFO structure pointer [Security], _crypto2_cert_revocation_info, security.cert_revocation_info, wincrypt/CERT_REVOCATION_INFO, wincrypt/PCERT_REVOCATION_INFO'
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
req.typenames: CERT_REVOCATION_INFO, *PCERT_REVOCATION_INFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _CERT_REVOCATION_INFO
 - wincrypt/_CERT_REVOCATION_INFO
 - PCERT_REVOCATION_INFO
 - wincrypt/PCERT_REVOCATION_INFO
 - CERT_REVOCATION_INFO
 - wincrypt/CERT_REVOCATION_INFO
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
 - CERT_REVOCATION_INFO
---

# CERT_REVOCATION_INFO structure


## -description

The <b>CERT_REVOCATION_INFO</b> structure indicates the revocation status of a certificate in a CERT_CHAIN_ELEMENT.

## -struct-fields

### -field cbSize

Size of this structure in bytes.

### -field dwRevocationResult

Currently defined values are:

<ul>
<li>CERT_TRUST_IS_REVOKED</li>
<li>CERT_TRUST_REVOCATION_STATUS_IS_UNKNOWN</li>
</ul>

### -field pszRevocationOid

Not currently used and is set to <b>NULL</b>.

### -field pvOidSpecificInfo

Not currently used and is set to <b>NULL</b>.

### -field fHasFreshnessTime

BOOL set to <b>TRUE</b> if dwFreshnessTime has been updated.

### -field dwFreshnessTime

If <b>fHasFreshnessTime</b> is <b>TRUE</b>, holds the CurrentTime minus the <a href="/windows/desktop/SecGloss/c-gly">certificate revocation list's</a> (CRL's). This time is in seconds.

### -field pCrlInfo

For CRL base revocation checking, a non-<b>NULL</b> pointer to a CERT_REVOCATION_CRL_INFO structure.

## -see-also

<a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_chain_element">CERT_CHAIN_ELEMENT</a>