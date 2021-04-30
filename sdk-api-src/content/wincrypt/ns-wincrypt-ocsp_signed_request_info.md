---
UID: NS:wincrypt._OCSP_SIGNED_REQUEST_INFO
title: OCSP_SIGNED_REQUEST_INFO (wincrypt.h)
description: Contains information for an online certificate status protocol (OCSP) request with optional signature information.
helpviewer_keywords: ["*POCSP_SIGNED_REQUEST_INFO","OCSP_SIGNED_REQUEST_INFO","OCSP_SIGNED_REQUEST_INFO structure [Security]","POCSP_SIGNED_REQUEST_INFO","POCSP_SIGNED_REQUEST_INFO structure pointer [Security]","security.ocsp_signed_request_info","wincrypt/OCSP_SIGNED_REQUEST_INFO","wincrypt/POCSP_SIGNED_REQUEST_INFO"]
old-location: security\ocsp_signed_request_info.htm
tech.root: security
ms.assetid: b3ff0843-77d8-4a9e-a3ba-97e9c398919a
ms.date: 12/05/2018
ms.keywords: '*POCSP_SIGNED_REQUEST_INFO, OCSP_SIGNED_REQUEST_INFO, OCSP_SIGNED_REQUEST_INFO structure [Security], POCSP_SIGNED_REQUEST_INFO, POCSP_SIGNED_REQUEST_INFO structure pointer [Security], security.ocsp_signed_request_info, wincrypt/OCSP_SIGNED_REQUEST_INFO, wincrypt/POCSP_SIGNED_REQUEST_INFO'
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
req.typenames: OCSP_SIGNED_REQUEST_INFO, *POCSP_SIGNED_REQUEST_INFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _OCSP_SIGNED_REQUEST_INFO
 - wincrypt/_OCSP_SIGNED_REQUEST_INFO
 - POCSP_SIGNED_REQUEST_INFO
 - wincrypt/POCSP_SIGNED_REQUEST_INFO
 - OCSP_SIGNED_REQUEST_INFO
 - wincrypt/OCSP_SIGNED_REQUEST_INFO
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
 - OCSP_SIGNED_REQUEST_INFO
---

# OCSP_SIGNED_REQUEST_INFO structure


## -description

The <b>OCSP_SIGNED_REQUEST_INFO</b> structure contains information for an <a href="/windows/desktop/SecGloss/o-gly">online certificate status protocol</a> (OCSP) request with optional signature information.

## -struct-fields

### -field ToBeSigned

A BLOB that has been encoded by using <a href="/windows/desktop/SecGloss/d-gly">Distinguished Encoding Rules</a> (DER) and that contains the OCSP request information.

### -field pOptionalSignatureInfo

A pointer to an <a href="/windows/desktop/api/wincrypt/ns-wincrypt-ocsp_signature_info">OCSP_SIGNATURE_INFO</a> structure that contains optional signature information.

## -remarks

In an OCSP client application, this structure receives an encoded <a href="/windows/desktop/api/wincrypt/ns-wincrypt-ocsp_request_info">OCSP_REQUEST_INFO</a> structure as its <b>ToBeSigned</b> member. Optionally, a signature  of the <b>ToBeSigned</b>  member is stored in the <b>pOptionalSignatureInfo</b> member.

On the receiving end, an OCSP responder application decodes the incoming request to populate an <b>OCSP_SIGNED_REQUEST_INFO</b> structure and subsequently decodes the <b>ToBeSigned</b> member to obtain an <a href="/windows/desktop/api/wincrypt/ns-wincrypt-ocsp_request_info">OCSP_REQUEST_INFO</a> structure.

OCSP applications can encode or decode this structure by using <b>X509_ASN_ENCODING</b> or <b>PKCS_7_ASN_ENCODING</b>.

## -see-also

<a href="/windows/desktop/SecCrypto/constants-for-cryptencodeobject-and-cryptdecodeobject">Constants for CryptEncodeObject and CryptDecodeObject</a>



<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptdecodeobject">CryptDecodeObject</a>



<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptdecodeobjectex">CryptDecodeObjectEx</a>



<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptencodeobject">CryptEncodeObject</a>



<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptencodeobjectex">CryptEncodeObjectEx</a>



<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptsignandencodecertificate">CryptSignAndEncodeCertificate</a>



<a href="/windows/desktop/api/wincrypt/ns-wincrypt-ocsp_signature_info">OCSP_SIGNATURE_INFO</a>