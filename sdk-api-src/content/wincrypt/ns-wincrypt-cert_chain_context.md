---
UID: NS:wincrypt._CERT_CHAIN_CONTEXT
title: CERT_CHAIN_CONTEXT (wincrypt.h)
description: Contains an array of simple certificate chains and a trust status structure that indicates summary validity data on all of the connected simple chains.
helpviewer_keywords: ["*PCERT_CHAIN_CONTEXT","CERT_CHAIN_CONTEXT","CERT_CHAIN_CONTEXT structure [Security]","PCERT_CHAIN_CONTEXT","PCERT_CHAIN_CONTEXT structure pointer [Security]","_crypto2_cert_chain_context","security.cert_chain_context","wincrypt/CERT_CHAIN_CONTEXT","wincrypt/PCERT_CHAIN_CONTEXT"]
old-location: security\cert_chain_context.htm
tech.root: security
ms.assetid: 609311f4-9cd6-4945-9f93-7266b3fc4a74
ms.date: 12/05/2018
ms.keywords: '*PCERT_CHAIN_CONTEXT, CERT_CHAIN_CONTEXT, CERT_CHAIN_CONTEXT structure [Security], PCERT_CHAIN_CONTEXT, PCERT_CHAIN_CONTEXT structure pointer [Security], _crypto2_cert_chain_context, security.cert_chain_context, wincrypt/CERT_CHAIN_CONTEXT, wincrypt/PCERT_CHAIN_CONTEXT'
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
req.typenames: CERT_CHAIN_CONTEXT, *PCERT_CHAIN_CONTEXT
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _CERT_CHAIN_CONTEXT
 - wincrypt/_CERT_CHAIN_CONTEXT
 - PCERT_CHAIN_CONTEXT
 - wincrypt/PCERT_CHAIN_CONTEXT
 - CERT_CHAIN_CONTEXT
 - wincrypt/CERT_CHAIN_CONTEXT
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
 - CERT_CHAIN_CONTEXT
---

# CERT_CHAIN_CONTEXT structure


## -description

The <b>CERT_CHAIN_CONTEXT</b> structure contains an array of simple certificate chains and a trust status structure that indicates summary validity data on all of the connected simple chains.

## -struct-fields

### -field cbSize

The size, in bytes, of this structure.

### -field TrustStatus

A structure that indicates the combined trust status of the simple chains array. The structure includes an error status code and an information status code. For information about status code values, see 
<a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_trust_status">CERT_TRUST_STATUS</a>.

### -field cChain

The number of simple chains in the array.

### -field rgpChain

An array of pointers to simple chain structures. <b>rgpChain</b>[0] is the end certificate simple chain, and <b>rgpChain</b>[<b>cChain</b>–1] is the final chain. If the end certificate is to be considered valid, the final chain must begin with a certificate contained in the root store or an otherwise trusted, self-signed certificate. If the original chain begins with a trusted certificate, there will be only a single simple chain in the array.

### -field cLowerQualityChainContext

The number of chains in the  <b>rgpLowerQualityChainContext</b> array.

### -field rgpLowerQualityChainContext

An array of pointers to CERT_CHAIN_CONTEXT structures. Returned when CERT_CHAIN_RETURN_LOWER_QUALITY_CONTEXTS is set in dwFlags.

### -field fHasRevocationFreshnessTime

A Boolean value set to <b>TRUE</b> if <b>dwRevocationFreshnessTime</b> is available.

### -field dwRevocationFreshnessTime

The largest CurrentTime, in seconds, minus the <a href="/windows/desktop/SecGloss/c-gly">certificate revocation list's</a> (CRL's) ThisUpdate of all elements checked.

### -field dwCreateFlags

### -field ChainId

## -remarks

When a <b>CERT_CHAIN_CONTEXT</b> is built, the first simple chain begins with an end certificate and ends with a self-signed certificate. If that self-signed certificate is not a <a href="/windows/desktop/SecGloss/r-gly">root</a> or otherwise trusted certificate, an attempt is made to build a new chain. <a href="/windows/desktop/SecGloss/c-gly">CTLs</a> are used to create the new chain beginning with the self-signed certificate from the original chain as the end certificate of the new chain. This process continues building additional simple chains until the first self-signed certificate is a trusted certificate or until an additional simple chain cannot be built.

## -see-also

<a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_simple_chain">CERT_SIMPLE_CHAIN</a>



<a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_trust_status">CERT_TRUST_STATUS</a>



<a href="/windows/desktop/api/wincrypt/nf-wincrypt-certgetcertificatechain">CertGetCertificateChain</a>