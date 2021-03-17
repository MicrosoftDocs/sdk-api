---
UID: NS:wincrypt._OCSP_CERT_ID
title: OCSP_CERT_ID (wincrypt.h)
description: Contains information to identify a certificate in an online certificate status protocol (OCSP) request or response.
helpviewer_keywords: ["*POCSP_CERT_ID","OCSP_CERT_ID","OCSP_CERT_ID structure [Security]","POCSP_CERT_ID","POCSP_CERT_ID structure pointer [Security]","security.ocsp_cert_id","wincrypt/OCSP_CERT_ID","wincrypt/POCSP_CERT_ID"]
old-location: security\ocsp_cert_id.htm
tech.root: security
ms.assetid: 58717990-a7f7-4b41-aceb-cbce55411396
ms.date: 12/05/2018
ms.keywords: '*POCSP_CERT_ID, OCSP_CERT_ID, OCSP_CERT_ID structure [Security], POCSP_CERT_ID, POCSP_CERT_ID structure pointer [Security], security.ocsp_cert_id, wincrypt/OCSP_CERT_ID, wincrypt/POCSP_CERT_ID'
req.header: wincrypt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
req.typenames: OCSP_CERT_ID, *POCSP_CERT_ID
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _OCSP_CERT_ID
 - wincrypt/_OCSP_CERT_ID
 - POCSP_CERT_ID
 - wincrypt/POCSP_CERT_ID
 - OCSP_CERT_ID
 - wincrypt/OCSP_CERT_ID
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
 - OCSP_CERT_ID
---

# OCSP_CERT_ID structure


## -description

The <b>OCSP_CERT_ID</b> structure contains information to identify a certificate in an <a href="/windows/desktop/SecGloss/o-gly">online certificate status protocol</a> (OCSP) request or response. This structure is used in the <a href="/windows/desktop/api/wincrypt/ns-wincrypt-ocsp_request_entry">OCSP_REQUEST_ENTRY</a> and <a href="/windows/desktop/api/wincrypt/ns-wincrypt-ocsp_basic_response_entry">OCSP_BASIC_RESPONSE_ENTRY</a> structures.

## -struct-fields

### -field HashAlgorithm

A <a href="/windows/desktop/api/wincrypt/ns-wincrypt-crypt_algorithm_identifier">CRYPT_ALGORITHM_IDENTIFIER</a> structure that specifies the algorithm used to create <i>IssuerNameHash</i> and <i>IssuerKeyHash</i>.

### -field IssuerNameHash

A <a href="/previous-versions/windows/desktop/legacy/aa381414(v=vs.85)">CRYPT_HASH_BLOB</a> that contains a hash of the certificate issuer subject name.

### -field IssuerKeyHash

A <a href="/previous-versions/windows/desktop/legacy/aa381414(v=vs.85)">CRYPT_HASH_BLOB</a> that contains a hash of the certificate issuer public key.

### -field SerialNumber

A <a href="/windows/desktop/SecGloss/b-gly">BLOB</a> that contains the serial number of the certificate. For more information, see the <b>SerialNumber</b> member description for <a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_info">CERT_INFO</a>.

## -see-also

<a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_info">CERT_INFO</a>



<a href="/windows/desktop/api/wincrypt/ns-wincrypt-crypt_algorithm_identifier">CRYPT_ALGORITHM_IDENTIFIER</a>



<a href="/windows/desktop/api/wincrypt/ns-wincrypt-ocsp_basic_response_entry">OCSP_BASIC_RESPONSE_ENTRY</a>



<a href="/windows/desktop/api/wincrypt/ns-wincrypt-ocsp_request_entry">OCSP_REQUEST_ENTRY</a>