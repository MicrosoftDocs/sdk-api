---
UID: NS:wincrypt._CERT_KEY_USAGE_RESTRICTION_INFO
title: CERT_KEY_USAGE_RESTRICTION_INFO (wincrypt.h)
description: The CERT_KEY_USAGE_RESTRICTION_INFO structure contains restrictions imposed on the usage of a certificate's public key. This includes purposes for use of the key and policies under which the key can be used.
helpviewer_keywords: ["*PCERT_KEY_USAGE_RESTRICTION_INFO","CERT_KEY_USAGE_RESTRICTION_INFO","CERT_KEY_USAGE_RESTRICTION_INFO structure [Security]","PCERT_KEY_USAGE_RESTRICTION_INFO","PCERT_KEY_USAGE_RESTRICTION_INFO structure pointer [Security]","_crypto2_cert_key_usage_restriction_info","security.cert_key_usage_restriction_info","wincrypt/CERT_KEY_USAGE_RESTRICTION_INFO","wincrypt/PCERT_KEY_USAGE_RESTRICTION_INFO"]
old-location: security\cert_key_usage_restriction_info.htm
tech.root: security
ms.assetid: f949c8e5-055d-4919-abcc-441880ccce56
ms.date: 12/05/2018
ms.keywords: '*PCERT_KEY_USAGE_RESTRICTION_INFO, CERT_KEY_USAGE_RESTRICTION_INFO, CERT_KEY_USAGE_RESTRICTION_INFO structure [Security], PCERT_KEY_USAGE_RESTRICTION_INFO, PCERT_KEY_USAGE_RESTRICTION_INFO structure pointer [Security], _crypto2_cert_key_usage_restriction_info, security.cert_key_usage_restriction_info, wincrypt/CERT_KEY_USAGE_RESTRICTION_INFO, wincrypt/PCERT_KEY_USAGE_RESTRICTION_INFO'
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
req.typenames: CERT_KEY_USAGE_RESTRICTION_INFO, *PCERT_KEY_USAGE_RESTRICTION_INFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _CERT_KEY_USAGE_RESTRICTION_INFO
 - wincrypt/_CERT_KEY_USAGE_RESTRICTION_INFO
 - PCERT_KEY_USAGE_RESTRICTION_INFO
 - wincrypt/PCERT_KEY_USAGE_RESTRICTION_INFO
 - CERT_KEY_USAGE_RESTRICTION_INFO
 - wincrypt/CERT_KEY_USAGE_RESTRICTION_INFO
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
 - CERT_KEY_USAGE_RESTRICTION_INFO
---

# CERT_KEY_USAGE_RESTRICTION_INFO structure


## -description

The <b>CERT_KEY_USAGE_RESTRICTION_INFO</b> structure contains restrictions imposed on the usage of a certificate's public key. This includes purposes for use of the key and policies under which the key can be used.


<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptdecodeobject">CryptDecodeObject</a> creates an instance of this structure when performed on a 
<a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_extension">CERT_EXTENSION</a> structure's <b>Value</b> member with its structure's <b>pszObjId</b> member set to szOID_KEY_USAGE_RESTRICTION.

An instance of this structure can be used as input to the <a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptencodeobject">CryptEncodeObject</a> function to create an appropriate <a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_extension">CERT_EXTENSION</a>.

## -struct-fields

### -field cCertPolicyId

The number of elements in the <b>rgCertPolicyId</b> array.

### -field rgCertPolicyId

An array of pointers to 
<a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_policy_id">CERT_POLICY_ID</a> structures.

### -field RestrictedKeyUsage

A 
						<a href="/windows/desktop/api/wincrypt/ns-wincrypt-crypt_bit_blob">CRYPT_BIT_BLOB</a> value that includes, as its <b>pbData</b>, a byte that indicates the purposes for which the key can be used. 




If the <b>cbData</b> member is zero, the key has no usage restrictions.

The following are currently defined values for the <b>pbData</b> member of <b>RestrictedKeyUsage</b>. These can be combined using a bitwise-<b>OR</b> operation.

<ul>
<li>CERT_DATA_ENCIPHERMENT_KEY_USAGE</li>
<li>CERT_DIGITAL_SIGNATURE_KEY_USAGE</li>
<li>CERT_KEY_AGREEMENT_KEY_USAGE</li>
<li>CERT_KEY_CERT_SIGN_KEY_USAGE</li>
<li>CERT_KEY_ENCIPHERMENT_KEY_USAGE</li>
<li>CERT_NON_REPUDIATION_KEY_USAGE</li>
<li>CERT_OFFLINE_CRL_SIGN_KEY_USAGE</li>
</ul>

## -see-also

<a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_extension">CERT_EXTENSION</a>



<a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_policy_id">CERT_POLICY_ID</a>



<a href="/windows/desktop/api/wincrypt/ns-wincrypt-crypt_bit_blob">CRYPT_BIT_BLOB</a>



<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptdecodeobject">CryptDecodeObject</a>



<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptencodeobject">CryptEncodeObject</a>