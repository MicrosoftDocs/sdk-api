---
UID: NS:wincrypt._CERT_SIGNED_CONTENT_INFO
title: CERT_SIGNED_CONTENT_INFO (wincrypt.h)
description: The CERT_SIGNED_CONTENT_INFO structure contains encoded content to be signed and a BLOB to hold the signature. The ToBeSigned member is an encoded CERT_INFO, CRL_INFO, CTL_INFO or CERT_REQUEST_INFO.
helpviewer_keywords: ["*PCERT_SIGNED_CONTENT_INFO","CERT_SIGNED_CONTENT_INFO","CERT_SIGNED_CONTENT_INFO structure [Security]","PCERT_SIGNED_CONTENT_INFO","PCERT_SIGNED_CONTENT_INFO structure pointer [Security]","_crypto2_cert_signed_content_info","security.cert_signed_content_info","wincrypt/CERT_SIGNED_CONTENT_INFO","wincrypt/PCERT_SIGNED_CONTENT_INFO"]
old-location: security\cert_signed_content_info.htm
tech.root: security
ms.assetid: f650765e-7a72-42a3-baf7-29779fd04adc
ms.date: 12/05/2018
ms.keywords: '*PCERT_SIGNED_CONTENT_INFO, CERT_SIGNED_CONTENT_INFO, CERT_SIGNED_CONTENT_INFO structure [Security], PCERT_SIGNED_CONTENT_INFO, PCERT_SIGNED_CONTENT_INFO structure pointer [Security], _crypto2_cert_signed_content_info, security.cert_signed_content_info, wincrypt/CERT_SIGNED_CONTENT_INFO, wincrypt/PCERT_SIGNED_CONTENT_INFO'
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
req.typenames: CERT_SIGNED_CONTENT_INFO, *PCERT_SIGNED_CONTENT_INFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _CERT_SIGNED_CONTENT_INFO
 - wincrypt/_CERT_SIGNED_CONTENT_INFO
 - PCERT_SIGNED_CONTENT_INFO
 - wincrypt/PCERT_SIGNED_CONTENT_INFO
 - CERT_SIGNED_CONTENT_INFO
 - wincrypt/CERT_SIGNED_CONTENT_INFO
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
 - CERT_SIGNED_CONTENT_INFO
---

# CERT_SIGNED_CONTENT_INFO structure


## -description

The <b>CERT_SIGNED_CONTENT_INFO</b> structure contains encoded content to be signed and a <a href="/windows/desktop/SecGloss/b-gly">BLOB</a> to hold the signature. The <b>ToBeSigned</b> member is an encoded 
<a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_info">CERT_INFO</a>, 
<a href="/windows/desktop/api/wincrypt/ns-wincrypt-crl_info">CRL_INFO</a>, 
<a href="/windows/desktop/api/wincrypt/ns-wincrypt-ctl_info">CTL_INFO</a> or 
<a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_request_info">CERT_REQUEST_INFO</a>.

## -struct-fields

### -field ToBeSigned

A BLOB that has been encoded by using <a href="/windows/desktop/SecGloss/d-gly">Distinguished Encoding Rules</a> (DER) and that is to be signed.

### -field SignatureAlgorithm

A 
<a href="/windows/desktop/api/wincrypt/ns-wincrypt-crypt_algorithm_identifier">CRYPT_ALGORITHM_IDENTIFIER</a> structure that contains the signature algorithm type and any associated additional parameters.

### -field Signature

BLOB containing a signed <a href="/windows/desktop/SecGloss/h-gly">hash</a> of the encoded data.

## -see-also

<a href="/windows/desktop/api/wincrypt/ns-wincrypt-crypt_algorithm_identifier">CRYPT_ALGORITHM_IDENTIFIER</a>



<a href="/windows/desktop/api/wincrypt/ns-wincrypt-crypt_bit_blob">CRYPT_BIT_BLOB</a>



<a href="/previous-versions/windows/desktop/legacy/aa381414(v=vs.85)">CRYPT_INTEGER_BLOB</a>