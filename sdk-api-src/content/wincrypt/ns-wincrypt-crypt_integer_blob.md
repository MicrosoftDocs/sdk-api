---
UID: NS:wincrypt._CRYPTOAPI_BLOB
title: CRYPT_INTEGER_BLOB (wincrypt.h)
description: The CryptoAPI CRYPT_INTEGER_BLOB structure (wincrypt.h) is used for an arbitrary array of bytes and gives flexibility to objects that can contain data types.
helpviewer_keywords: ["*PCERT_BLOB","*PCERT_NAME_BLOB","*PCERT_RDN_VALUE_BLOB","*PCRL_BLOB","*PCRYPT_ATTR_BLOB","*PCRYPT_DATA_BLOB","*PCRYPT_DER_BLOB","*PCRYPT_DIGEST_BLOB","*PCRYPT_HASH_BLOB","*PCRYPT_INTEGER_BLOB","*PCRYPT_OBJID_BLOB","*PCRYPT_UINT_BLOB","*PDATA_BLOB","CERT_BLOB","CERT_BLOB structure [Security]","CERT_NAME_BLOB","CERT_NAME_BLOB structure [Security]","CERT_RDN_VALUE_BLOB","CERT_RDN_VALUE_BLOB structure [Security]","CRL_BLOB","CRL_BLOB structure [Security]","CRYPTOAPI_BLOB","CRYPTOAPI_BLOB structure [Security]","CRYPT_ATTR_BLOB","CRYPT_ATTR_BLOB structure [Security]","CRYPT_DATA_BLOB","CRYPT_DATA_BLOB structure [Security]","CRYPT_DER_BLOB","CRYPT_DER_BLOB structure [Security]","CRYPT_DIGEST_BLOB","CRYPT_DIGEST_BLOB structure [Security]","CRYPT_HASH_BLOB","CRYPT_HASH_BLOB structure [Security]","CRYPT_INTEGER_BLOB","CRYPT_INTEGER_BLOB structure [Security]","CRYPT_OBJID_BLOB","CRYPT_OBJID_BLOB structure [Security]","CRYPT_UINT_BLOB","CRYPT_UINT_BLOB structure [Security]","DATA_BLOB","DATA_BLOB structure [Security]","PCERT_BLOB","PCERT_BLOB structure pointer [Security]","PCERT_NAME_BLOB","PCERT_NAME_BLOB structure pointer [Security]","PCERT_RDN_VALUE_BLOB","PCERT_RDN_VALUE_BLOB structure pointer [Security]","PCRL_BLOB","PCRL_BLOB structure pointer [Security]","PCRYPT_ATTR_BLOB","PCRYPT_ATTR_BLOB structure pointer [Security]","PCRYPT_DATA_BLOB","PCRYPT_DATA_BLOB structure pointer [Security]","PCRYPT_DER_BLOB","PCRYPT_DER_BLOB structure pointer [Security]","PCRYPT_DIGEST_BLOB","PCRYPT_DIGEST_BLOB structure pointer [Security]","PCRYPT_HASH_BLOB","PCRYPT_HASH_BLOB structure pointer [Security]","PCRYPT_INTEGER_BLOB","PCRYPT_INTEGER_BLOB structure pointer [Security]","PCRYPT_OBJID_BLOB","PCRYPT_OBJID_BLOB structure pointer [Security]","PCRYPT_UINT_BLOB","PCRYPT_UINT_BLOB structure pointer [Security]","PDATA_BLOB","PDATA_BLOB structure pointer [Security]","_CRYPTOAPI_BLOB","_crypto2_cryptoapi_blob","dpapi/CERT_BLOB","dpapi/CERT_NAME_BLOB","dpapi/CERT_RDN_VALUE_BLOB","dpapi/CRL_BLOB","dpapi/CRYPTOAPI_BLOB","dpapi/CRYPT_ATTR_BLOB","dpapi/CRYPT_DATA_BLOB","dpapi/CRYPT_DER_BLOB","dpapi/CRYPT_DIGEST_BLOB","dpapi/CRYPT_HASH_BLOB","dpapi/CRYPT_OBJID_BLOB","dpapi/CRYPT_UINT_BLOB","dpapi/DATA_BLOB","dpapi/PCERT_BLOB","dpapi/PCERT_NAME_BLOB","dpapi/PCERT_RDN_VALUE_BLOB","dpapi/PCRL_BLOB","dpapi/PCRYPT_ATTR_BLOB","dpapi/PCRYPT_DATA_BLOB","dpapi/PCRYPT_DER_BLOB","dpapi/PCRYPT_DIGEST_BLOB","dpapi/PCRYPT_HASH_BLOB","dpapi/PCRYPT_INTEGER_BLOB","dpapi/PCRYPT_OBJID_BLOB","dpapi/PCRYPT_UINT_BLOB","dpapi/PDATA_BLOB","security.cryptoapi_blob"]
old-location: security\cryptoapi_blob.htm
tech.root: security
ms.assetid: 1c2a07b8-f702-47f3-8d4c-6ac0cbc63f0f
ms.date: 08/03/2022
ms.keywords: '*PCERT_BLOB, *PCERT_NAME_BLOB, *PCERT_RDN_VALUE_BLOB, *PCRL_BLOB, *PCRYPT_ATTR_BLOB, *PCRYPT_DATA_BLOB, *PCRYPT_DER_BLOB, *PCRYPT_DIGEST_BLOB, *PCRYPT_HASH_BLOB, *PCRYPT_INTEGER_BLOB, *PCRYPT_OBJID_BLOB, *PCRYPT_UINT_BLOB, *PDATA_BLOB, CERT_BLOB, CERT_BLOB structure [Security], CERT_NAME_BLOB, CERT_NAME_BLOB structure [Security], CERT_RDN_VALUE_BLOB, CERT_RDN_VALUE_BLOB structure [Security], CRL_BLOB, CRL_BLOB structure [Security], CRYPTOAPI_BLOB, CRYPTOAPI_BLOB structure [Security], CRYPT_ATTR_BLOB, CRYPT_ATTR_BLOB structure [Security], CRYPT_DATA_BLOB, CRYPT_DATA_BLOB structure [Security], CRYPT_DER_BLOB, CRYPT_DER_BLOB structure [Security], CRYPT_DIGEST_BLOB, CRYPT_DIGEST_BLOB structure [Security], CRYPT_HASH_BLOB, CRYPT_HASH_BLOB structure [Security], CRYPT_INTEGER_BLOB, CRYPT_INTEGER_BLOB structure [Security], CRYPT_OBJID_BLOB, CRYPT_OBJID_BLOB structure [Security], CRYPT_UINT_BLOB, CRYPT_UINT_BLOB structure [Security], DATA_BLOB, DATA_BLOB structure [Security], PCERT_BLOB, PCERT_BLOB structure pointer [Security], PCERT_NAME_BLOB, PCERT_NAME_BLOB structure pointer [Security], PCERT_RDN_VALUE_BLOB, PCERT_RDN_VALUE_BLOB structure pointer [Security], PCRL_BLOB, PCRL_BLOB structure pointer [Security], PCRYPT_ATTR_BLOB, PCRYPT_ATTR_BLOB structure pointer [Security], PCRYPT_DATA_BLOB, PCRYPT_DATA_BLOB structure pointer [Security], PCRYPT_DER_BLOB, PCRYPT_DER_BLOB structure pointer [Security], PCRYPT_DIGEST_BLOB, PCRYPT_DIGEST_BLOB structure pointer [Security], PCRYPT_HASH_BLOB, PCRYPT_HASH_BLOB structure pointer [Security], PCRYPT_INTEGER_BLOB, PCRYPT_INTEGER_BLOB structure pointer [Security], PCRYPT_OBJID_BLOB, PCRYPT_OBJID_BLOB structure pointer [Security], PCRYPT_UINT_BLOB, PCRYPT_UINT_BLOB structure pointer [Security], PDATA_BLOB, PDATA_BLOB structure pointer [Security], _CRYPTOAPI_BLOB, _crypto2_cryptoapi_blob, dpapi/CERT_BLOB, dpapi/CERT_NAME_BLOB, dpapi/CERT_RDN_VALUE_BLOB, dpapi/CRL_BLOB, dpapi/CRYPTOAPI_BLOB, dpapi/CRYPT_ATTR_BLOB, dpapi/CRYPT_DATA_BLOB, dpapi/CRYPT_DER_BLOB, dpapi/CRYPT_DIGEST_BLOB, dpapi/CRYPT_HASH_BLOB, dpapi/CRYPT_OBJID_BLOB, dpapi/CRYPT_UINT_BLOB, dpapi/DATA_BLOB, dpapi/PCERT_BLOB, dpapi/PCERT_NAME_BLOB, dpapi/PCERT_RDN_VALUE_BLOB, dpapi/PCRL_BLOB, dpapi/PCRYPT_ATTR_BLOB, dpapi/PCRYPT_DATA_BLOB, dpapi/PCRYPT_DER_BLOB, dpapi/PCRYPT_DIGEST_BLOB, dpapi/PCRYPT_HASH_BLOB, dpapi/PCRYPT_INTEGER_BLOB, dpapi/PCRYPT_OBJID_BLOB, dpapi/PCRYPT_UINT_BLOB, dpapi/PDATA_BLOB, security.cryptoapi_blob'
req.header: wincrypt.h
req.include-header: Wincrypt.h
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
req.typenames: CRYPT_INTEGER_BLOB, *PCRYPT_INTEGER_BLOB, CRYPT_UINT_BLOB, *PCRYPT_UINT_BLOB, CRYPT_OBJID_BLOB, *PCRYPT_OBJID_BLOB, CERT_NAME_BLOB, *PCERT_NAME_BLOB, CERT_RDN_VALUE_BLOB, *PCERT_RDN_VALUE_BLOB, CERT_BLOB, *PCERT_BLOB, CRL_BLOB, *PCRL_BLOB, DATA_BLOB, *PDATA_BLOB, CRYPT_DATA_BLOB, *PCRYPT_DATA_BLOB, CRYPT_HASH_BLOB, *PCRYPT_HASH_BLOB, CRYPT_DIGEST_BLOB, *PCRYPT_DIGEST_BLOB, CRYPT_DER_BLOB, *PCRYPT_DER_BLOB, CRYPT_ATTR_BLOB, *PCRYPT_ATTR_BLOB
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _CRYPTOAPI_BLOB
 - wincrypt/_CRYPTOAPI_BLOB
 - PCRYPT_INTEGER_BLOB
 - wincrypt/PCRYPT_INTEGER_BLOB
 - CRYPT_INTEGER_BLOB
 - wincrypt/CRYPT_INTEGER_BLOB
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - dpapi.h
api_name:
 - CRYPT_INTEGER_BLOB
---

# CRYPT_INTEGER_BLOB structure


## -description

The CryptoAPI <a href="/previous-versions/windows/desktop/legacy/aa381414(v=vs.85)">CRYPT_INTEGER_BLOB</a> structure is used for an arbitrary array of bytes. It is declared in Wincrypt.h and provides flexibility for objects that can contain various data types.

## -struct-fields

### -field cbData

The count of bytes in the buffer pointed to by <i>pbData</i>.

### -field pbData

A pointer to a block of data bytes.

## -see-also

<a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_extension">CERT_EXTENSION</a>



<a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_policy_qualifier_info">CERT_POLICY_QUALIFIER_INFO</a>



<a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_request_info">CERT_REQUEST_INFO</a>



<a href="/windows/win32/api/wincrypt/ns-wincrypt-cmsg_ctrl_add_signer_unauth_attr_para">CMSG_CTRL_ADD_SIGNER_UNAUTH_ATTR_PARA</a>



<a href="/windows/desktop/api/wincrypt/ns-wincrypt-cmsg_signer_info">CMSG_SIGNER_INFO</a>



<a href="/windows/desktop/api/wincrypt/ns-wincrypt-crypt_attribute_type_value">CRYPT_ATTRIBUTE_TYPE_VALUE</a>



<a href="/windows/desktop/api/wincrypt/ns-wincrypt-crypt_time_stamp_request_info">CRYPT_TIME_STAMP_REQUEST_INFO</a>



<a href="/windows/desktop/api/wincrypt/nf-wincrypt-certcompareintegerblob">CertCompareIntegerBlob</a>



<a href="/windows/desktop/api/wincrypt/nf-wincrypt-certnametostra">CertNameToStr</a>
