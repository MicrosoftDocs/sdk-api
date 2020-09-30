---
UID: NS:wincrypt._CERT_AUTHORITY_KEY_ID_INFO
title: CERT_AUTHORITY_KEY_ID_INFO (wincrypt.h)
description: Identifies the key used to sign a certificate or certificate revocation list (CRL).
helpviewer_keywords: ["*PCERT_AUTHORITY_KEY_ID_INFO","CERT_AUTHORITY_KEY_ID_INFO","CERT_AUTHORITY_KEY_ID_INFO structure [Security]","PCERT_AUTHORITY_KEY_ID_INFO","PCERT_AUTHORITY_KEY_ID_INFO structure pointer [Security]","_crypto2_cert_authority_key_id_info","security.cert_authority_key_id_info","wincrypt/CERT_AUTHORITY_KEY_ID_INFO","wincrypt/PCERT_AUTHORITY_KEY_ID_INFO"]
old-location: security\cert_authority_key_id_info.htm
tech.root: security
ms.assetid: 2f966d39-8d7c-41e7-bf6a-5a30170b100d
ms.date: 12/05/2018
ms.keywords: '*PCERT_AUTHORITY_KEY_ID_INFO, CERT_AUTHORITY_KEY_ID_INFO, CERT_AUTHORITY_KEY_ID_INFO structure [Security], PCERT_AUTHORITY_KEY_ID_INFO, PCERT_AUTHORITY_KEY_ID_INFO structure pointer [Security], _crypto2_cert_authority_key_id_info, security.cert_authority_key_id_info, wincrypt/CERT_AUTHORITY_KEY_ID_INFO, wincrypt/PCERT_AUTHORITY_KEY_ID_INFO'
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
req.typenames: CERT_AUTHORITY_KEY_ID_INFO, *PCERT_AUTHORITY_KEY_ID_INFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _CERT_AUTHORITY_KEY_ID_INFO
 - wincrypt/_CERT_AUTHORITY_KEY_ID_INFO
 - PCERT_AUTHORITY_KEY_ID_INFO
 - wincrypt/PCERT_AUTHORITY_KEY_ID_INFO
 - CERT_AUTHORITY_KEY_ID_INFO
 - wincrypt/CERT_AUTHORITY_KEY_ID_INFO
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
 - CERT_AUTHORITY_KEY_ID_INFO
---

# CERT_AUTHORITY_KEY_ID_INFO structure


## -description

The <b>CERT_AUTHORITY_KEY_ID_INFO</b> structure identifies the key used to sign a <a href="/windows/desktop/SecGloss/c-gly">certificate</a> or <a href="/windows/desktop/SecGloss/c-gly">certificate revocation list</a> (CRL). This structure differentiates among distinct keys used by the same <a href="/windows/desktop/SecGloss/c-gly">certification authority</a> as, for example, keys changed when an update occurs.

The key can be identified by an explicit key identifier, by giving a certificate's issuer and serial number, or by both. If both are used, the certificate issuer must ensure that the explicit key identifier, the certificate issuer and the serial number are consistent.


<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptdecodeobject">CryptDecodeObject</a> creates an instance of this structure when performed on a 
<a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_extension">CERT_EXTENSION</a> structure's <b>Value</b> member with its structure's <b>pszObjId</b> member set to szOID_AUTHORITY_KEY_IDENTIFIER.

An instance of this structure can be used as input to <a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptencodeobject">CryptEncodeObject</a> to create an appropriate <a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_extension">CERT_EXTENSION</a>.

## -struct-fields

### -field KeyId

A <a href="/previous-versions/windows/desktop/legacy/aa381414(v=vs.85)">CRYPT_DATA_BLOB</a> structure that contains a unique identifier of a public key.

### -field CertIssuer

A <a href="/previous-versions/windows/desktop/legacy/aa381414(v=vs.85)">CERT_NAME_BLOB</a> structure that contains the encoded distinguished name of the certification authority that issued the certificate.

### -field CertSerialNumber

A <a href="/previous-versions/windows/desktop/legacy/aa381414(v=vs.85)">CRYPT_INTEGER_BLOB</a> structure that contains the serial number of the certificate associated with the <a href="/windows/desktop/SecGloss/p-gly">private key</a> used to sign this certificate. For more information, see 
<a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_info">CERT_INFO</a>.

## -see-also

<a href="/previous-versions/windows/desktop/legacy/aa381414(v=vs.85)">CRYPT_INTEGER_BLOB</a>