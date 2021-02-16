---
UID: NS:wincrypt._CERT_AUTHORITY_KEY_ID2_INFO
title: CERT_AUTHORITY_KEY_ID2_INFO (wincrypt.h)
description: The CERT_AUTHORITY_KEY_ID2_INFO structure identifies the key used to sign a certificate or CRL.
helpviewer_keywords: ["*PCERT_AUTHORITY_KEY_ID2_INFO","CERT_AUTHORITY_KEY_ID2_INFO","CERT_AUTHORITY_KEY_ID2_INFO structure [Security]","PCERT_AUTHORITY_KEY_ID2_INFO","PCERT_AUTHORITY_KEY_ID2_INFO structure pointer [Security]","_crypto2_cert_authority_key_id2_info","security.cert_authority_key_id2_info","wincrypt/CERT_AUTHORITY_KEY_ID2_INFO","wincrypt/PCERT_AUTHORITY_KEY_ID2_INFO"]
old-location: security\cert_authority_key_id2_info.htm
tech.root: security
ms.assetid: 0a5005a5-71be-4f4d-8de8-c7452402b646
ms.date: 12/05/2018
ms.keywords: '*PCERT_AUTHORITY_KEY_ID2_INFO, CERT_AUTHORITY_KEY_ID2_INFO, CERT_AUTHORITY_KEY_ID2_INFO structure [Security], PCERT_AUTHORITY_KEY_ID2_INFO, PCERT_AUTHORITY_KEY_ID2_INFO structure pointer [Security], _crypto2_cert_authority_key_id2_info, security.cert_authority_key_id2_info, wincrypt/CERT_AUTHORITY_KEY_ID2_INFO, wincrypt/PCERT_AUTHORITY_KEY_ID2_INFO'
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
req.typenames: CERT_AUTHORITY_KEY_ID2_INFO, *PCERT_AUTHORITY_KEY_ID2_INFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _CERT_AUTHORITY_KEY_ID2_INFO
 - wincrypt/_CERT_AUTHORITY_KEY_ID2_INFO
 - PCERT_AUTHORITY_KEY_ID2_INFO
 - wincrypt/PCERT_AUTHORITY_KEY_ID2_INFO
 - CERT_AUTHORITY_KEY_ID2_INFO
 - wincrypt/CERT_AUTHORITY_KEY_ID2_INFO
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
 - CERT_AUTHORITY_KEY_ID2_INFO
---

# CERT_AUTHORITY_KEY_ID2_INFO structure


## -description

The <b>CERT_AUTHORITY_KEY_ID2_INFO</b> structure identifies the key used to sign a <a href="/windows/desktop/SecGloss/c-gly">certificate</a> or <a href="/windows/desktop/SecGloss/c-gly">CRL</a>. It differs from the 
<a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_authority_key_id_info">CERT_AUTHORITY_KEY_ID_INFO</a> structure in that the certificate issuer is a 
<a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_alt_name_info">CERT_ALT_NAME_INFO</a> instead of a <a href="/previous-versions/windows/desktop/legacy/aa381414(v=vs.85)">CERT_NAME_BLOB</a>. Otherwise, the structures are used in the same way.

The key can be identified by an explicit key identifier, by giving a certificate's issuer and serial number, or by both. If both are used, the certificate issuer must ensure that the explicit key identifier, the certificate issuer and the serial number are consistent.


<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptdecodeobject">CryptDecodeObject</a> creates an instance of this structure when performed on a 
<a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_extension">CERT_EXTENSION</a> structure's <b>Value</b> member with its the structure's <b>pszObjId</b> member set to szOID_AUTHORITY_KEY_IDENTIFIER2.

An instance of this structure can be used as input to <a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptencodeobject">CryptEncodeObject</a> to create an appropriate <a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_extension">CERT_EXTENSION</a>.

## -struct-fields

### -field KeyId

A <a href="/previous-versions/windows/desktop/legacy/aa381414(v=vs.85)">CRYPT_DATA_BLOB</a> structure that contains a unique identifier of a public key.

### -field AuthorityCertIssuer

<a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_alt_name_info">CERT_ALT_NAME_INFO</a> that includes the encoded name of the CA that issued the certificate. The <b>cAltEntry</b> member of the structure may be set to zero if the name is not to be used to identify the CA.

### -field AuthorityCertSerialNumber

A <a href="/previous-versions/windows/desktop/legacy/aa381414(v=vs.85)">CRYPT_INTEGER_BLOB</a> structure that includes the serial number of the certificate associated with the private key used to sign this certificate. For more information, see 
<a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_info">CERT_INFO</a>.

## -see-also

<a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_alt_name_info">CERT_ALT_NAME_INFO</a>



<a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_authority_key_id_info">CERT_AUTHORITY_KEY_ID_INFO</a>