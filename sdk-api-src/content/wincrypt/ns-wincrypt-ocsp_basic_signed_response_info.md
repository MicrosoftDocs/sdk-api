---
UID: NS:wincrypt._OCSP_BASIC_SIGNED_RESPONSE_INFO
title: OCSP_BASIC_SIGNED_RESPONSE_INFO (wincrypt.h)
description: Contains a basic online certificate status protocol (OCSP) response with a signature.
helpviewer_keywords: ["*POCSP_BASIC_SIGNED_RESPONSE_INFO","OCSP_BASIC_SIGNED_RESPONSE_INFO","OCSP_BASIC_SIGNED_RESPONSE_INFO structure [Security]","POCSP_BASIC_SIGNED_RESPONSE_INFO","POCSP_BASIC_SIGNED_RESPONSE_INFO structure pointer [Security]","security.ocsp_basic_signed_response_info","wincrypt/OCSP_BASIC_SIGNED_RESPONSE_INFO","wincrypt/POCSP_BASIC_SIGNED_RESPONSE_INFO"]
old-location: security\ocsp_basic_signed_response_info.htm
tech.root: security
ms.assetid: 4b88a946-030f-490a-b46a-c42507e1268d
ms.date: 12/05/2018
ms.keywords: '*POCSP_BASIC_SIGNED_RESPONSE_INFO, OCSP_BASIC_SIGNED_RESPONSE_INFO, OCSP_BASIC_SIGNED_RESPONSE_INFO structure [Security], POCSP_BASIC_SIGNED_RESPONSE_INFO, POCSP_BASIC_SIGNED_RESPONSE_INFO structure pointer [Security], security.ocsp_basic_signed_response_info, wincrypt/OCSP_BASIC_SIGNED_RESPONSE_INFO, wincrypt/POCSP_BASIC_SIGNED_RESPONSE_INFO'
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
req.typenames: OCSP_BASIC_SIGNED_RESPONSE_INFO, *POCSP_BASIC_SIGNED_RESPONSE_INFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _OCSP_BASIC_SIGNED_RESPONSE_INFO
 - wincrypt/_OCSP_BASIC_SIGNED_RESPONSE_INFO
 - POCSP_BASIC_SIGNED_RESPONSE_INFO
 - wincrypt/POCSP_BASIC_SIGNED_RESPONSE_INFO
 - OCSP_BASIC_SIGNED_RESPONSE_INFO
 - wincrypt/OCSP_BASIC_SIGNED_RESPONSE_INFO
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
 - OCSP_BASIC_SIGNED_RESPONSE_INFO
---

# OCSP_BASIC_SIGNED_RESPONSE_INFO structure


## -description

 The <b>OCSP_BASIC_SIGNED_RESPONSE_INFO</b> structure contains a basic <a href="/windows/desktop/SecGloss/o-gly">online certificate status protocol</a> (OCSP) response with a signature.

## -struct-fields

### -field ToBeSigned

A <a href="/windows/desktop/SecGloss/b-gly">BLOB</a> that has been encoded by using <a href="/windows/desktop/SecGloss/d-gly">Distinguished Encoding Rules</a> (DER) and that contains an encoded <a href="/windows/desktop/api/wincrypt/ns-wincrypt-ocsp_basic_response_info">OCSP_BASIC_RESPONSE_INFO</a> structure.

### -field SignatureInfo

A pointer to signature information for the <b>ToBeSigned</b> data.

## -remarks

In an OCSP responder service, this structure receives an encoded <a href="/windows/desktop/api/wincrypt/ns-wincrypt-ocsp_basic_response_info">OCSP_BASIC_RESPONSE_INFO</a> structure as its <b>ToBeSigned</b> member. The signature  of the <b>ToBeSigned</b>  member is stored in the <b>SignatureInfo</b> member. The encoded <b>OCSP_BASIC_SIGNED_RESPONSE_INFO</b> structure is stored in an <a href="/windows/desktop/api/wincrypt/ns-wincrypt-ocsp_response_info">OCSP_RESPONSE_INFO</a> structure.

On the receiving end, an OCSP client application must decode the <a href="/windows/desktop/api/wincrypt/ns-wincrypt-ocsp_response_info">OCSP_RESPONSE_INFO</a> <b>Value</b> member to obtain this structure and subsequently decode the <b>OCSP_BASIC_SIGNED_RESPONSE_INFO</b> <b>ToBeSigned</b> member to obtain an <a href="/windows/desktop/api/wincrypt/ns-wincrypt-ocsp_basic_response_info">OCSP_BASIC_RESPONSE_INFO</a> structure.

OCSP applications can encode or decode this structure by using <b>X509_ASN_ENCODING</b> or <b>PKCS_7_ASN_ENCODING</b>.

## -see-also

<a href="/previous-versions/windows/desktop/legacy/aa381414(v=vs.85)">CRYPT_DER_BLOB</a>



<a href="/windows/desktop/api/wincrypt/ns-wincrypt-ocsp_signature_info">OCSP_SIGNATURE_INFO</a>