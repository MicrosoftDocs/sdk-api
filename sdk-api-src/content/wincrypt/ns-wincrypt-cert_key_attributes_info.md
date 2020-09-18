---
UID: NS:wincrypt._CERT_KEY_ATTRIBUTES_INFO
title: CERT_KEY_ATTRIBUTES_INFO (wincrypt.h)
description: The CERT_KEY_ATTRIBUTES_INFO structure contains optional additional information about the public key being certified.
helpviewer_keywords: ["*PCERT_KEY_ATTRIBUTES_INFO","CERT_KEY_ATTRIBUTES_INFO","CERT_KEY_ATTRIBUTES_INFO structure [Security]","PCERT_KEY_ATTRIBUTES_INFO","PCERT_KEY_ATTRIBUTES_INFO structure pointer [Security]","_crypto2_cert_key_attributes_info","security.cert_key_attributes_info","wincrypt/CERT_KEY_ATTRIBUTES_INFO","wincrypt/PCERT_KEY_ATTRIBUTES_INFO"]
old-location: security\cert_key_attributes_info.htm
tech.root: security
ms.assetid: cedf0321-4f5a-48a9-abfd-d8642bb89576
ms.date: 12/05/2018
ms.keywords: '*PCERT_KEY_ATTRIBUTES_INFO, CERT_KEY_ATTRIBUTES_INFO, CERT_KEY_ATTRIBUTES_INFO structure [Security], PCERT_KEY_ATTRIBUTES_INFO, PCERT_KEY_ATTRIBUTES_INFO structure pointer [Security], _crypto2_cert_key_attributes_info, security.cert_key_attributes_info, wincrypt/CERT_KEY_ATTRIBUTES_INFO, wincrypt/PCERT_KEY_ATTRIBUTES_INFO'
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
req.typenames: CERT_KEY_ATTRIBUTES_INFO, *PCERT_KEY_ATTRIBUTES_INFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _CERT_KEY_ATTRIBUTES_INFO
 - wincrypt/_CERT_KEY_ATTRIBUTES_INFO
 - PCERT_KEY_ATTRIBUTES_INFO
 - wincrypt/PCERT_KEY_ATTRIBUTES_INFO
 - CERT_KEY_ATTRIBUTES_INFO
 - wincrypt/CERT_KEY_ATTRIBUTES_INFO
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
 - CERT_KEY_ATTRIBUTES_INFO
---

# CERT_KEY_ATTRIBUTES_INFO structure


## -description

The <b>CERT_KEY_ATTRIBUTES_INFO</b> structure contains optional additional information about the public key being certified. It can include a key identifier, an indication of the intended use of that key, or an indication of the period of use of the corresponding private key.


<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptdecodeobject">CryptDecodeObject</a> creates an instance of this structure when performed on a 
<a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_extension">CERT_EXTENSION</a> structure's <b>Value</b> member with its the structure's <b>pszObjId</b> member set to szOID_KEY_ATTRIBUTES.

An instance of this structure can be used as input to <a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptencodeobject">CryptEncodeObject</a> to create an appropriate <a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_extension">CERT_EXTENSION</a>.

## -struct-fields

### -field KeyId

A <a href="/previous-versions/windows/desktop/legacy/aa381414(v=vs.85)">CRYPT_DATA_BLOB</a> structure with a unique identifier of a key.

### -field IntendedKeyUsage

<b>CRYPT_BIT_BLOB</b> with it <b>pbData</b> member indicating the intended purpose of the key. For a list of usage bit values, see the <b>RestrictedKeyUsage</b> member of 
the <a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_key_usage_restriction_info">CERT_KEY_USAGE_RESTRICTION_INFO</a> structure. 




This member can be used to find the correct key or certificate of a user who has multiple keys or certificates. Its indication of usage is advisory field, only, and does not imply that usage of the key is restricted to the purpose indicated. The list of intended uses is not necessarily all-inclusive, and the field can be omitted. If a key is to be restricted to a particular use a <a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_key_usage_restriction_info">CERT_KEY_USAGE_RESTRICTION_INFO</a> extension must be used.

### -field pPrivateKeyUsagePeriod

A pointer to a 
<a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_private_key_validity">CERT_PRIVATE_KEY_VALIDITY</a> structure that indicates the period of use of the private key corresponding to the certified public key. This member is optional and can be set to <b>NULL</b>.

## -see-also

<a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_extension">CERT_EXTENSION</a>



<a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_private_key_validity">CERT_PRIVATE_KEY_VALIDITY</a>



<a href="/windows/desktop/api/wincrypt/ns-wincrypt-crypt_bit_blob">CRYPT_BIT_BLOB</a>



<a href="/previous-versions/windows/desktop/legacy/aa381414(v=vs.85)">CRYPT_INTEGER_BLOB</a>



<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptdecodeobject">CryptDecodeObject</a>