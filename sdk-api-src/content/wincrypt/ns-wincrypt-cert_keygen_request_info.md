---
UID: NS:wincrypt._CERT_KEYGEN_REQUEST_INFO
title: CERT_KEYGEN_REQUEST_INFO (wincrypt.h)
description: Contains information stored in the Netscape key generation request. The subject and subject public key BLOBs are encoded.
helpviewer_keywords: ["*PCERT_KEYGEN_REQUEST_INFO","CERT_KEYGEN_REQUEST_INFO","CERT_KEYGEN_REQUEST_INFO structure [Security]","PCERT_KEYGEN_REQUEST_INFO","PCERT_KEYGEN_REQUEST_INFO structure pointer [Security]","_crypto2_cert_keygen_request_info","security.cert_keygen_request_info","wincrypt/CERT_KEYGEN_REQUEST_INFO","wincrypt/PCERT_KEYGEN_REQUEST_INFO"]
old-location: security\cert_keygen_request_info.htm
tech.root: security
ms.assetid: 44cbe4de-a9cc-48b2-ad04-9acd42fac07c
ms.date: 12/05/2018
ms.keywords: '*PCERT_KEYGEN_REQUEST_INFO, CERT_KEYGEN_REQUEST_INFO, CERT_KEYGEN_REQUEST_INFO structure [Security], PCERT_KEYGEN_REQUEST_INFO, PCERT_KEYGEN_REQUEST_INFO structure pointer [Security], _crypto2_cert_keygen_request_info, security.cert_keygen_request_info, wincrypt/CERT_KEYGEN_REQUEST_INFO, wincrypt/PCERT_KEYGEN_REQUEST_INFO'
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
req.typenames: CERT_KEYGEN_REQUEST_INFO, *PCERT_KEYGEN_REQUEST_INFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _CERT_KEYGEN_REQUEST_INFO
 - wincrypt/_CERT_KEYGEN_REQUEST_INFO
 - PCERT_KEYGEN_REQUEST_INFO
 - wincrypt/PCERT_KEYGEN_REQUEST_INFO
 - CERT_KEYGEN_REQUEST_INFO
 - wincrypt/CERT_KEYGEN_REQUEST_INFO
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
 - CERT_KEYGEN_REQUEST_INFO
---

# CERT_KEYGEN_REQUEST_INFO structure


## -description

The <b>CERT_KEYGEN_REQUEST_INFO</b> structure contains information stored in the Netscape key generation request. The subject and subject <a href="/windows/desktop/SecGloss/p-gly">public key BLOBs</a> are encoded.

## -struct-fields

### -field dwVersion

The version number of the certificate. <b>CERT_KEYGEN_REQUEST_V1</b> (0) is the only defined version number.

### -field SubjectPublicKeyInfo

A <a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_public_key_info">CERT_PUBLIC_KEY_INFO</a> structure that contains the encoded <a href="/windows/desktop/SecGloss/p-gly">public key</a> and <a href="/windows/desktop/SecGloss/p-gly">public key algorithm</a>.

### -field pwszChallengeString

A random printable string. This string is used by the server to ensure that the key that it is certifying matches the client on the page.

## -see-also

<a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_request_info">CERT_REQUEST_INFO</a>