---
UID: NS:wincrypt._OCSP_BASIC_RESPONSE_INFO
title: OCSP_BASIC_RESPONSE_INFO (wincrypt.h)
description: Contains a basic online certificate status protocol (OCSP) response as specified by RFC 2560.
helpviewer_keywords: ["*POCSP_BASIC_RESPONSE_INFO","OCSP_BASIC_BY_KEY_RESPONDER_ID","OCSP_BASIC_BY_NAME_RESPONDER_ID","OCSP_BASIC_RESPONSE_INFO","OCSP_BASIC_RESPONSE_INFO structure [Security]","OCSP_BASIC_RESPONSE_V1","POCSP_BASIC_RESPONSE_INFO","POCSP_BASIC_RESPONSE_INFO structure pointer [Security]","security.ocsp_basic_response_info","wincrypt/OCSP_BASIC_RESPONSE_INFO","wincrypt/POCSP_BASIC_RESPONSE_INFO"]
old-location: security\ocsp_basic_response_info.htm
tech.root: security
ms.assetid: f067bfa0-114b-4295-bbee-a963d8b64332
ms.date: 12/05/2018
ms.keywords: '*POCSP_BASIC_RESPONSE_INFO, OCSP_BASIC_BY_KEY_RESPONDER_ID, OCSP_BASIC_BY_NAME_RESPONDER_ID, OCSP_BASIC_RESPONSE_INFO, OCSP_BASIC_RESPONSE_INFO structure [Security], OCSP_BASIC_RESPONSE_V1, POCSP_BASIC_RESPONSE_INFO, POCSP_BASIC_RESPONSE_INFO structure pointer [Security], security.ocsp_basic_response_info, wincrypt/OCSP_BASIC_RESPONSE_INFO, wincrypt/POCSP_BASIC_RESPONSE_INFO'
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
req.typenames: OCSP_BASIC_RESPONSE_INFO, *POCSP_BASIC_RESPONSE_INFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _OCSP_BASIC_RESPONSE_INFO
 - wincrypt/_OCSP_BASIC_RESPONSE_INFO
 - POCSP_BASIC_RESPONSE_INFO
 - wincrypt/POCSP_BASIC_RESPONSE_INFO
 - OCSP_BASIC_RESPONSE_INFO
 - wincrypt/OCSP_BASIC_RESPONSE_INFO
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
 - OCSP_BASIC_RESPONSE_INFO
---

# OCSP_BASIC_RESPONSE_INFO structure


## -description

 The <b>OCSP_BASIC_RESPONSE_INFO</b> structure contains a basic <a href="/windows/desktop/SecGloss/o-gly">online certificate status protocol</a> (OCSP) response as specified by <a href="https://www.ietf.org/rfc/rfc2560.txt">RFC 2560</a>. The RFC specifies that a single response can contain a sequence of certificates for which statuses are provided. The  <b>rgResponseEntry</b> member of this structure contains an <a href="/windows/desktop/api/wincrypt/ns-wincrypt-ocsp_basic_response_entry">OCSP_BASIC_RESPONSE_ENTRY</a> structure for each certificate in a sequence.

## -struct-fields

### -field dwVersion

A value that indicates the protocol version of the response.



#### OCSP_BASIC_RESPONSE_V1 (0)

### -field dwResponderIdChoice

A value that indicates the type of ID the responder used in this response.



#### OCSP_BASIC_BY_NAME_RESPONDER_ID (1)



#### OCSP_BASIC_BY_KEY_RESPONDER_ID (2)

### -field DUMMYUNIONNAME

### -field DUMMYUNIONNAME.ByNameResponderId

A <a href="/previous-versions/windows/desktop/legacy/aa381414(v=vs.85)">CERT_NAME_BLOB</a> structure that contains the subject name of the responder signing <a href="/windows/desktop/SecGloss/c-gly">certificate</a>.

### -field DUMMYUNIONNAME.ByKeyResponderId

A <a href="/previous-versions/windows/desktop/legacy/aa381414(v=vs.85)">CRYPT_HASH_BLOB</a> that contains a hash of the responder signing certificate <a href="/windows/desktop/SecGloss/p-gly">public key</a>.

### -field ProducedAt

The date and time at which the response was signed.

### -field cResponseEntry

The number of elements in the <i>rgResponseEntry</i> array.

### -field rgResponseEntry

An array of pointers to <a href="/windows/desktop/api/wincrypt/ns-wincrypt-ocsp_basic_response_entry">OCSP_BASIC_RESPONSE_ENTRY</a> structures, each of which contains a certificate status.

### -field cExtension

The number of elements in the <b>rgExtension</b> array.

### -field rgExtension

An array of pointers to <a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_extension">CERT_EXTENSION</a> structures, each of which contains additional information about the response.

## -remarks

OCSP responder applications encode this structure and store it in an <a href="/windows/desktop/api/wincrypt/ns-wincrypt-ocsp_basic_signed_response_info">OCSP_BASIC_SIGNED_RESPONSE_INFO</a> <b>ToBeSigned</b> member. Conversely, OCSP client applications decode the <b>OCSP_BASIC_SIGNED_RESPONSE_INFO</b> structure to obtain this structure.

OCSP applications can encode or decode this structure by using <b>X509_ASN_ENCODING</b> or <b>PKCS_7_ASN_ENCODING</b>.

## -see-also

<a href="https://www.ietf.org/rfc/rfc2560.txt">RFC 2560 Online Certificate Status Protocol</a>