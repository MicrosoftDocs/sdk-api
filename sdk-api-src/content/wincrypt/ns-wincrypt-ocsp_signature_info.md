---
UID: NS:wincrypt._OCSP_SIGNATURE_INFO
title: OCSP_SIGNATURE_INFO (wincrypt.h)
description: Contains a signature for an online certificate status protocol (OCSP) request or response.
helpviewer_keywords: ["*POCSP_SIGNATURE_INFO","OCSP_SIGNATURE_INFO","OCSP_SIGNATURE_INFO structure [Security]","POCSP_SIGNATURE_INFO","POCSP_SIGNATURE_INFO structure pointer [Security]","security.ocsp_signature_info","wincrypt/OCSP_SIGNATURE_INFO","wincrypt/POCSP_SIGNATURE_INFO"]
old-location: security\ocsp_signature_info.htm
tech.root: security
ms.assetid: 1489e2a4-36f3-4e8c-9b99-7c2e396b3814
ms.date: 12/05/2018
ms.keywords: '*POCSP_SIGNATURE_INFO, OCSP_SIGNATURE_INFO, OCSP_SIGNATURE_INFO structure [Security], POCSP_SIGNATURE_INFO, POCSP_SIGNATURE_INFO structure pointer [Security], security.ocsp_signature_info, wincrypt/OCSP_SIGNATURE_INFO, wincrypt/POCSP_SIGNATURE_INFO'
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
req.typenames: OCSP_SIGNATURE_INFO, *POCSP_SIGNATURE_INFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _OCSP_SIGNATURE_INFO
 - wincrypt/_OCSP_SIGNATURE_INFO
 - POCSP_SIGNATURE_INFO
 - wincrypt/POCSP_SIGNATURE_INFO
 - OCSP_SIGNATURE_INFO
 - wincrypt/OCSP_SIGNATURE_INFO
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
 - OCSP_SIGNATURE_INFO
---

# OCSP_SIGNATURE_INFO structure


## -description

The <b>OCSP_SIGNATURE_INFO</b> structure contains a signature for an <a href="/windows/desktop/SecGloss/o-gly">online certificate status protocol</a> (OCSP) request or response. The <a href="/windows/desktop/api/wincrypt/ns-wincrypt-ocsp_signed_request_info">OCSP_SIGNED_REQUEST_INFO</a> and <a href="/windows/desktop/api/wincrypt/ns-wincrypt-ocsp_basic_signed_response_info">OCSP_BASIC_SIGNED_RESPONSE_INFO</a> structures use this structure.

## -struct-fields

### -field SignatureAlgorithm

A <a href="/windows/desktop/api/wincrypt/ns-wincrypt-crypt_algorithm_identifier">CRYPT_ALGORITHM_IDENTIFIER</a> structure that specifies the algorithm used to create the <b>Signature</b>.

### -field Signature

A <a href="/windows/desktop/SecGloss/b-gly">BLOB</a> that contains a signed hash of an <a href="/windows/desktop/api/wincrypt/ns-wincrypt-ocsp_request_info">OCSP_REQUEST_INFO</a> or <a href="/windows/desktop/api/wincrypt/ns-wincrypt-ocsp_basic_response_info">OCSP_BASIC_RESPONSE_INFO</a> structure.

### -field cCertEncoded

The number of elements in the <b>rgCertEncoded</b> array.

### -field rgCertEncoded

An array of pointers to <a href="/previous-versions/windows/desktop/legacy/aa381414(v=vs.85)">CERT_BLOB</a> structures, each of which contains an encoded signature certificate.

## -see-also

<a href="/previous-versions/windows/desktop/legacy/aa381414(v=vs.85)">CERT_BLOB</a>



<a href="/windows/desktop/api/wincrypt/ns-wincrypt-crypt_algorithm_identifier">CRYPT_ALGORITHM_IDENTIFIER</a>



<a href="/windows/desktop/api/wincrypt/ns-wincrypt-crypt_bit_blob">CRYPT_BIT_BLOB</a>



<a href="/windows/desktop/api/wincrypt/ns-wincrypt-ocsp_basic_signed_response_info">OCSP_BASIC_SIGNED_RESPONSE_INFO</a>



<a href="/windows/desktop/api/wincrypt/ns-wincrypt-ocsp_signed_request_info">OCSP_SIGNED_REQUEST_INFO</a>



<a href="https://www.ietf.org/rfc/rfc2560.txt">RFC 2560  Online Certificate Status Protocol</a>