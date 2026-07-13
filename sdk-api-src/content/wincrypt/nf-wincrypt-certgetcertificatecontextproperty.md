---
UID: NF:wincrypt.CertGetCertificateContextProperty
title: CertGetCertificateContextProperty function (wincrypt.h)
description: Retrieves the information contained in an extended property of a certificate context.
helpviewer_keywords: ["CERT_ACCESS_STATE_PROP_ID","CERT_AIA_URL_RETRIEVED_PROP_ID","CERT_ARCHIVED_KEY_HASH_PROP_ID","CERT_ARCHIVED_PROP_ID","CERT_AUTHORITY_INFO_ACCESS_PROP_ID","CERT_AUTO_ENROLL_PROP_ID","CERT_AUTO_ENROLL_RETRY_PROP_ID","CERT_BACKED_UP_PROP_ID","CERT_CA_DISABLE_CRL_PROP_ID","CERT_CA_OCSP_AUTHORITY_INFO_ACCESS_PROP_ID","CERT_CROSS_CERT_DIST_POINTS_PROP_ID","CERT_CTL_USAGE_PROP_ID","CERT_DATE_STAMP_PROP_ID","CERT_DESCRIPTION_PROP_ID","CERT_EFS_PROP_ID","CERT_ENHKEY_USAGE_PROP_ID","CERT_ENROLLMENT_PROP_ID","CERT_EXTENDED_ERROR_INFO_PROP_ID","CERT_FORTEZZA_DATA_PROP_ID","CERT_FRIENDLY_NAME_PROP_ID","CERT_HASH_PROP_ID","CERT_HCRYPTPROV_OR_NCRYPT_KEY_HANDLE_PROP_ID","CERT_HCRYPTPROV_TRANSFER_PROP_ID","CERT_IE30_RESERVED_PROP_ID","CERT_ISSUER_PUBLIC_KEY_MD5_HASH_PROP_ID","CERT_ISSUER_SERIAL_NUMBER_MD5_HASH_PROP_ID","CERT_KEY_CONTEXT_PROP_ID","CERT_KEY_IDENTIFIER_PROP_ID","CERT_KEY_PROV_HANDLE_PROP_ID","CERT_KEY_PROV_INFO_PROP_ID","CERT_KEY_SPEC_PROP_ID","CERT_MD5_HASH_PROP_ID","CERT_NCRYPT_KEY_HANDLE_PROP_ID","CERT_NCRYPT_KEY_HANDLE_TRANSFER_PROP_ID","CERT_NEW_KEY_PROP_ID","CERT_NEXT_UPDATE_LOCATION_PROP_ID","CERT_NO_AUTO_EXPIRE_CHECK_PROP_ID","CERT_OCSP_CACHE_PREFIX_PROP_ID","CERT_OCSP_RESPONSE_PROP_ID","CERT_PUBKEY_ALG_PARA_PROP_ID","CERT_PUBKEY_HASH_RESERVED_PROP_ID","CERT_PUB_KEY_CNG_ALG_BIT_LENGTH_PROP_ID","CERT_PVK_FILE_PROP_ID","CERT_RENEWAL_PROP_ID","CERT_REQUEST_ORIGINATOR_PROP_ID","CERT_ROOT_PROGRAM_CERT_POLICIES_PROP_ID","CERT_ROOT_PROGRAM_NAME_CONSTRAINTS_PROP_ID","CERT_SHA1_HASH_PROP_ID","CERT_SHA1_SHA256_HASH_PROP_ID","CERT_SHA256_HASH_PROP_ID","CERT_SIGNATURE_HASH_PROP_ID","CERT_SIGN_HASH_CNG_ALG_PROP_ID","CERT_SMART_CARD_DATA_PROP_ID","CERT_SMART_CARD_ROOT_INFO_PROP_ID","CERT_SOURCE_LOCATION_PROP_ID","CERT_SOURCE_URL_PROP_ID","CERT_SUBJECT_DISABLE_CRL_PROP_ID","CERT_SUBJECT_INFO_ACCESS_PROP_ID","CERT_SUBJECT_NAME_MD5_HASH_PROP_ID","CERT_SUBJECT_OCSP_AUTHORITY_INFO_ACCESS_PROP_ID","CERT_SUBJECT_PUBLIC_KEY_MD5_HASH_PROP_ID","CERT_SUBJECT_PUB_KEY_BIT_LENGTH_PROP_ID","CertGetCertificateContextProperty","CertGetCertificateContextProperty function [Security]","_crypto2_certgetcertificatecontextproperty","security.certgetcertificatecontextproperty","wincrypt/CertGetCertificateContextProperty"]
old-location: security\certgetcertificatecontextproperty.htm
tech.root: security
ms.assetid: f766db64-3121-4f70-ac83-ce25ee634efa
ms.date: 06/24/2024
ms.keywords: CERT_ACCESS_STATE_PROP_ID, CERT_AIA_URL_RETRIEVED_PROP_ID, CERT_ARCHIVED_KEY_HASH_PROP_ID, CERT_ARCHIVED_PROP_ID, CERT_AUTHORITY_INFO_ACCESS_PROP_ID, CERT_AUTO_ENROLL_PROP_ID, CERT_AUTO_ENROLL_RETRY_PROP_ID, CERT_BACKED_UP_PROP_ID, CERT_CA_DISABLE_CRL_PROP_ID, CERT_CA_OCSP_AUTHORITY_INFO_ACCESS_PROP_ID, CERT_CROSS_CERT_DIST_POINTS_PROP_ID, CERT_CTL_USAGE_PROP_ID, CERT_DATE_STAMP_PROP_ID, CERT_DESCRIPTION_PROP_ID, CERT_EFS_PROP_ID, CERT_ENHKEY_USAGE_PROP_ID, CERT_ENROLLMENT_PROP_ID, CERT_EXTENDED_ERROR_INFO_PROP_ID, CERT_FORTEZZA_DATA_PROP_ID, CERT_FRIENDLY_NAME_PROP_ID, CERT_HASH_PROP_ID, CERT_HCRYPTPROV_OR_NCRYPT_KEY_HANDLE_PROP_ID, CERT_HCRYPTPROV_TRANSFER_PROP_ID, CERT_IE30_RESERVED_PROP_ID, CERT_ISSUER_PUBLIC_KEY_MD5_HASH_PROP_ID, CERT_ISSUER_SERIAL_NUMBER_MD5_HASH_PROP_ID, CERT_KEY_CONTEXT_PROP_ID, CERT_KEY_IDENTIFIER_PROP_ID, CERT_KEY_PROV_HANDLE_PROP_ID, CERT_KEY_PROV_INFO_PROP_ID, CERT_KEY_SPEC_PROP_ID, CERT_MD5_HASH_PROP_ID, CERT_NCRYPT_KEY_HANDLE_PROP_ID, CERT_NCRYPT_KEY_HANDLE_TRANSFER_PROP_ID, CERT_NEW_KEY_PROP_ID, CERT_NEXT_UPDATE_LOCATION_PROP_ID, CERT_NO_AUTO_EXPIRE_CHECK_PROP_ID, CERT_OCSP_CACHE_PREFIX_PROP_ID, CERT_OCSP_RESPONSE_PROP_ID, CERT_PUBKEY_ALG_PARA_PROP_ID, CERT_PUBKEY_HASH_RESERVED_PROP_ID, CERT_PUB_KEY_CNG_ALG_BIT_LENGTH_PROP_ID, CERT_PVK_FILE_PROP_ID, CERT_RENEWAL_PROP_ID, CERT_REQUEST_ORIGINATOR_PROP_ID, CERT_ROOT_PROGRAM_CERT_POLICIES_PROP_ID, CERT_ROOT_PROGRAM_NAME_CONSTRAINTS_PROP_ID, CERT_SHA1_HASH_PROP_ID, CERT_SHA1_SHA256_HASH_PROP_ID, CERT_SHA256_HASH_PROP_ID, CERT_SIGNATURE_HASH_PROP_ID, CERT_SIGN_HASH_CNG_ALG_PROP_ID, CERT_SMART_CARD_DATA_PROP_ID, CERT_SMART_CARD_ROOT_INFO_PROP_ID, CERT_SOURCE_LOCATION_PROP_ID, CERT_SOURCE_URL_PROP_ID, CERT_SUBJECT_DISABLE_CRL_PROP_ID, CERT_SUBJECT_INFO_ACCESS_PROP_ID, CERT_SUBJECT_NAME_MD5_HASH_PROP_ID, CERT_SUBJECT_OCSP_AUTHORITY_INFO_ACCESS_PROP_ID, CERT_SUBJECT_PUBLIC_KEY_MD5_HASH_PROP_ID, CERT_SUBJECT_PUB_KEY_BIT_LENGTH_PROP_ID, CertGetCertificateContextProperty, CertGetCertificateContextProperty function [Security], _crypto2_certgetcertificatecontextproperty, security.certgetcertificatecontextproperty, wincrypt/CertGetCertificateContextProperty
req.header: wincrypt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2003 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Crypt32.lib
req.dll: Crypt32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CertGetCertificateContextProperty
 - wincrypt/CertGetCertificateContextProperty
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Crypt32.dll
api_name:
 - CertGetCertificateContextProperty
---

# CertGetCertificateContextProperty function

## -description

The **CertGetCertificateContextProperty** function retrieves the information contained in an extended property of a [certificate context](/windows/win32/SecGloss/c-gly).

## -parameters

### -param pCertContext [in]

A pointer to the [CERT_CONTEXT](/windows/win32/api/wincrypt/ns-wincrypt-cert_context) structure of the [certificate](/windows/win32/SecGloss/c-gly) that contains the property to be retrieved.

### -param dwPropId [in]

The property to be retrieved. Currently defined identifiers and the data type to be returned in *pvData* are listed in the following table.

#### CERT_ACCESS_STATE_PROP_ID

Data type of *pvData*: A pointer to a **DWORD** value.

Returns a **DWORD** value that indicates whether write operations to the certificate are persisted. The **DWORD** value is not set if the certificate is in a memory store or in a registry-based store that is opened as read-only.

#### CERT_AIA_URL_RETRIEVED_PROP_ID

This identifier is reserved.

#### CERT_ARCHIVED_KEY_HASH_PROP_ID

Data type of *pvData*: A pointer to an array of **BYTE** values. The size of this array is specified in the *pcbData* parameter.

Returns a previously saved encrypted key [hash](/windows/win32/SecGloss/h-gly) for the certificate context.

#### CERT_ARCHIVED_PROP_ID

Data type of *pvData*: **NULL**. If the **CertGetCertificateContextProperty** function returns true, then the specified property ID exists for the [CERT_CONTEXT](/windows/win32/api/wincrypt/ns-wincrypt-cert_context).

Indicates the certificate is skipped during  enumerations. A certificate with this property set is found with explicit search operations, such as those used to find a certificate with a specific hash or a serial number. No data in *pvData* is associated with this property.

#### CERT_AUTHORITY_INFO_ACCESS_PROP_ID

This identifier is reserved.

#### CERT_AUTO_ENROLL_PROP_ID

Data type of *pvData*: A pointer to an array of **BYTE** values. The size of this array is specified in the *pcbData* parameter.

Returns a null-terminated Unicode string that names the certificate type for which the certificate has been auto enrolled.

#### CERT_AUTO_ENROLL_RETRY_PROP_ID

This identifier is reserved.

#### CERT_BACKED_UP_PROP_ID

This identifier is reserved.

#### CERT_CA_DISABLE_CRL_PROP_ID

Data type of *pvData*: A pointer to an array of **BYTE** values. The size of this array is specified in the *pcbData* parameter.

Disables [certificate revocation list](/windows/win32/SecGloss/c-gly) (CRL) retrieval for certificates used by the [certification authority](/windows/win32/SecGloss/c-gly) (CA). If the CA certificate contains this property, it must also include the **CERT_CA_OCSP_AUTHORITY_INFO_ACCESS_PROP_ID** property.

#### CERT_CA_OCSP_AUTHORITY_INFO_ACCESS_PROP_ID

Data type of *pvData*: A pointer to an array of **BYTE** values. The size of this array is specified in the *pcbData* parameter.

Contains the list of [online certificate status protocol](/windows/win32/SecGloss/o-gly) (OCSP) URLs to use for certificates issued by the CA certificate. The array contents are the [Abstract Syntax Notation One](/windows/win32/SecGloss/a-gly) (ASN.1)-encoded bytes of an **X509_AUTHORITY_INFO_ACCESS** structure where **pszAccessMethod** is set to **szOID_PKIX_OCSP**.

#### CERT_CROSS_CERT_DIST_POINTS_PROP_ID

Data type of *pvData*: A pointer to an array of **BYTE** values. The size of this array is specified in the *pcbData* parameter.

Location of the cross certificates. Currently, this identifier is only applicable to certificates and not to CRLs or [certificate trust lists](/windows/win32/SecGloss/c-gly) (CTLs).

The **BYTE** array contains an ASN.1-encoded [CROSS_CERT_DIST_POINTS_INFO](/windows/win32/api/wincrypt/ns-wincrypt-cross_cert_dist_points_info) structure decoded by using the [CryptDecodeObject](/windows/win32/api/wincrypt/nf-wincrypt-cryptdecodeobject) function with a **X509_CROSS_CERT_DIST_POINTS** value for the *lpszStuctType* parameter.

#### CERT_CTL_USAGE_PROP_ID

Data type of *pvData*: A pointer to an array of **BYTE** values. The size of this array is specified in the *pcbData* parameter.

Returns an array of bytes that contain an ASN.1-encoded [CTL_USAGE](/windows/win32/api/wincrypt/ns-wincrypt-ctl_usage) structure.

#### CERT_DATE_STAMP_PROP_ID

Data type of *pvData*: A pointer to a **FILETIME** structure.

Time when the certificate was added to the store.

#### CERT_DESCRIPTION_PROP_ID

Data type of *pvData*: A pointer to an array of **BYTE** values. The size of this array is specified in the *pcbData* parameter.

Returns the property displayed by the certificate UI. This property allows the user to describe the certificate's use.

#### CERT_EFS_PROP_ID

This identifier is reserved.

#### CERT_ENHKEY_USAGE_PROP_ID

Data type of *pvData*: A pointer to an array of **BYTE** values. The size of this array is specified in the *pcbData* parameter.

Returns an array of bytes that contain an ASN.1-encoded [CERT_ENHKEY_USAGE](/windows/win32/api/wincrypt/ns-wincrypt-ctl_usage) structure. This structure contains an array of Enhanced Key Usage [object identifiers](/windows/win32/SecGloss/o-gly) (OIDs),each of which specifies a valid use of the certificate.

#### CERT_ENROLLMENT_PROP_ID

Data type of *pvData*: A pointer to an array of **BYTE** values. The size of this array is specified in the *pcbData* parameter.

Enrollment information of the pending request that contains RequestID, CADNSName, CAName, and DisplayName. The data format is defined as follows:

| Bytes | Contents |
|-------|----------|
| First 4 bytes | Pending request ID |
| Next 4 bytes | CADNSName size, in characters, including the terminating null character, followed by CADNSName string with terminating null character |
| Next 4 bytes | CAName size, in characters, including the terminating null character, followed by CAName string with terminating null character |
| Next 4 bytes | DisplayName size, in characters, including the terminating null character, followed by DisplayName string with terminating null character |

#### CERT_EXTENDED_ERROR_INFO_PROP_ID

Data type of *pvData*: A pointer to an array of **BYTE** values. The size of this array is specified in the *pcbData* parameter.

Returns a null-terminated Unicode character string that contains extended error information for the certificate context.

#### CERT_FORTEZZA_DATA_PROP_ID

This identifier is reserved.

#### CERT_FRIENDLY_NAME_PROP_ID

Data type of *pvData*: A pointer to an array of **BYTE** values. The size of this array is specified in the *pcbData* parameter.

Returns a null-terminated Unicode character string that contains the display name for the certificate.

#### CERT_HASH_PROP_ID

Data type of *pvData*: A pointer to an array of **BYTE** values. The size of this array is specified in the *pcbData* parameter.

Returns the SHA1 hash. If the hash does not exist, it is computed by using the [CryptHashCertificate](/windows/win32/api/wincrypt/nf-wincrypt-crypthashcertificate) function.

#### CERT_HCRYPTPROV_OR_NCRYPT_KEY_HANDLE_PROP_ID

Data type of *pvData*: A pointer to an [HCRYPTPROV_OR_NCRYPT_KEY_HANDLE](/windows/win32/SecCrypto/hcryptprov-or-ncrypt-key-handle) data type.

Returns either the **HCRYPTPROV** or **NCRYPT_KEY_HANDLE** choice.

#### CERT_HCRYPTPROV_TRANSFER_PROP_ID

Returns the Cryptography API (CAPI) key handle associated with the certificate. The caller is responsible for freeing the handle. It will not be freed when the context is freed. The property value is removed after it is returned. If you call this property on a context that has a CNG key, **CRYPT_E_NOT_FOUND** is returned.

#### CERT_IE30_RESERVED_PROP_ID

This identifier is reserved.

#### CERT_ISSUER_PUBLIC_KEY_MD5_HASH_PROP_ID

Data type of *pvData*: A pointer to an array of **BYTE** values. The size of this array is specified in the *pcbData* parameter.

MD5 hash of the [public key](/windows/win32/SecGloss/p-gly) associated with the [private key](/windows/win32/SecGloss/p-gly) used to sign this certificate.

#### CERT_ISSUER_SERIAL_NUMBER_MD5_HASH_PROP_ID

Data type of *pvData*: A pointer to an array of **BYTE** values. The size of this array is specified in the *pcbData* parameter.

MD5 hash of the issuer name and serial number from this certificate.

#### CERT_KEY_CONTEXT_PROP_ID

Data type of *pvData*: A pointer to a [CERT_KEY_CONTEXT](/windows/win32/api/wincrypt/ns-wincrypt-cert_key_context) structure.

Returns a [CERT_KEY_CONTEXT](/windows/win32/api/wincrypt/ns-wincrypt-cert_key_context) structure.

#### CERT_KEY_IDENTIFIER_PROP_ID

Data type of *pvData*: A pointer to an array of **BYTE** values. The size of this array is specified in the *pcbData* parameter.

If nonexistent, searches for the **szOID_SUBJECT_KEY_IDENTIFIER** extension. If that fails, a SHA1 hash is done on the certificate's **SubjectPublicKeyInfo** member to produce the identifier values.

#### CERT_KEY_PROV_HANDLE_PROP_ID

Data type of *pvData*: A pointer to an [HCRYPTPROV](/windows/win32/SecCrypto/hcryptprov) value.

Returns the provider handle obtained from CERT_KEY_CONTEXT_PROP_ID.

#### CERT_KEY_PROV_INFO_PROP_ID

Data type of *pvData*: A pointer to a [CRYPT_KEY_PROV_INFO](/windows/win32/api/wincrypt/ns-wincrypt-crypt_key_prov_info) structure.

Returns a pointer to a [CRYPT_KEY_PROV_INFO](/windows/win32/api/wincrypt/ns-wincrypt-crypt_key_prov_info) structure.

#### CERT_KEY_SPEC_PROP_ID

Data type of *pvData*: A pointer to a **DWORD** value.

Returns a **DWORD** value that specifies the private key obtained from CERT_KEY_CONTEXT_PROP_ID if it exists. Otherwise, if CERT_KEY_PROV_INFO_PROP_ID exists, it is the source of the *dwKeySpec*.

#### CERT_MD5_HASH_PROP_ID

Data type of *pvData*: A pointer to an array of **BYTE** values. The size of this array is specified in the *pcbData* parameter.

Returns the MD5 hash. If the hash does not exist, it is computed by using the [CryptHashCertificate](/windows/win32/api/wincrypt/nf-wincrypt-crypthashcertificate) function.

#### CERT_NCRYPT_KEY_HANDLE_PROP_ID

Data type of *pvData*: A pointer to an **NCRYPT_KEY_HANDLE** data type.

Returns a **CERT_NCRYPT_KEY_SPEC** choice where applicable.

#### CERT_NCRYPT_KEY_HANDLE_TRANSFER_PROP_ID

Returns the CNG key handle associated with the certificate. The caller is responsible for freeing the handle. It will not be freed when the context is freed. The property value is removed after it is returned. If you call this property on a context that has a legacy (CAPI) key, **CRYPT_E_NOT_FOUND** is returned.

#### CERT_NEW_KEY_PROP_ID

This identifier is reserved.

#### CERT_NEXT_UPDATE_LOCATION_PROP_ID

Data type of *pvData*: A pointer to an array of **BYTE** values. The size of this array is specified in the *pcbData* parameter.

Returns the ASN.1-encoded [CERT_ALT_NAME_INFO](/windows/win32/api/wincrypt/ns-wincrypt-cert_alt_name_info) structure.

CERT_NEXT_UPDATE_LOCATION_PROP_ID is currently used only with CTLs.

#### CERT_NO_AUTO_EXPIRE_CHECK_PROP_ID

This identifier is reserved.

#### CERT_OCSP_CACHE_PREFIX_PROP_ID

This identifier is reserved.

#### CERT_OCSP_RESPONSE_PROP_ID

Data type of *pvData*: A pointer to an array of **BYTE** values. The size of this array is specified in the *pcbData* parameter.

Returns an encoded OCSP response for this certificate.

#### CERT_PUB_KEY_CNG_ALG_BIT_LENGTH_PROP_ID

Data type of *pvData*: Pointer to a null-terminated Unicode string.

Returns an `L"<PUBKEY><BITLENGTH>"` string representing the certificate’s public key algorithm and bit length. The following `<PUBKEY>` algorithms are supported:

- L"RSA" (BCRYPT_RSA_ALGORITHM)
- L"DSA" (BCRYPT_DSA_ALGORITHM)
- L"ECDSA" (SSL_ECDSA_ALGORITHM)

**Windows 8 and Windows Server 2012:** Support for this property begins.

#### CERT_PUBKEY_ALG_PARA_PROP_ID

Data type of *pvData*: A pointer to an array of **BYTE** values. The size of this array is specified in the *pcbData* parameter.

For public keys that support algorithm parameter inheritance, returns the ASN.1-encoded PublicKey Algorithm parameters. For [Digital Signature Standard](/windows/win32/SecGloss/d-gly) (DSS), returns the parameters encoded by using the [CryptEncodeObject](/windows/desktop/api/wincrypt/nf-wincrypt-cryptencodeobject) function. This property is used only if CMS_PKCS7 is defined.

#### CERT_PUBKEY_HASH_RESERVED_PROP_ID

This identifier is reserved.

#### CERT_PVK_FILE_PROP_ID

Data type of *pvData*: A pointer to an array of **BYTE** values. The size of this array is specified in the *pcbData* parameter.

Returns a null-terminated Unicode wide character string that contains the file name that contains the private key associated with the certificate's public key.

#### CERT_RENEWAL_PROP_ID

Data type of *pvData*: A pointer to an array of **BYTE** values. The size of this array is specified in the *pcbData* parameter.

Returns the hash of the renewed certificate.

#### CERT_REQUEST_ORIGINATOR_PROP_ID

Data type of *pvData*: A pointer to an array of **BYTE** values. The size of this array is specified in the *pcbData* parameter.

Returns a null-terminated Unicode string that contains the DNS computer name for the origination of the certificate context request.

#### CERT_ROOT_PROGRAM_CERT_POLICIES_PROP_ID

Data type of *pvData*: A pointer to an array of **BYTE** values. The size of this array is specified in the *pcbData* parameter.

Returns a pointer to an encoded [CERT_POLICIES_INFO](/windows/win32/api/wincrypt/ns-wincrypt-cert_policies_info) structure that contains the application policies of the root certificate for the context. This property can be decoded by using the [CryptDecodeObject](/windows/win32/api/wincrypt/nf-wincrypt-cryptdecodeobject) function with the *lpszStructType* parameter set to **X509_CERT_POLICIES** and the *dwCertEncodingType* parameter set to a combination of **X509_ASN_ENCODING** bitwise **OR** **PKCS_7_ASN_ENCODING**.

#### CERT_ROOT_PROGRAM_NAME_CONSTRAINTS_PROP_ID

This identifier is reserved.

#### CERT_SHA1_HASH_PROP_ID

Data type of *pvData*: A pointer to an array of **BYTE** values. The size of this array is specified in the *pcbData* parameter.

Returns the SHA1 hash. If the hash does not exist, it is computed by using the [CryptHashCertificate](/windows/win32/api/wincrypt/nf-wincrypt-crypthashcertificate) function.

#### CERT_SHA1_SHA256_HASH_PROP_ID

Data type of <i>pvData</i>: A pointer to an array of <b>BYTE</b> values. The size of this array is 52 bytes, 20 bytes for the SHA1 hash and 32 bytes for the SHA256 hash.

Returns a combination of the SHA1 hash and the SHA256 hash. If the hash does not exist, it is 
			computed by using the <a href="/windows/desktop/api/wincrypt/nf-wincrypt-crypthashcertificate">CryptHashCertificate</a> function.



#### CERT_SHA256_HASH_PROP_ID

Data type of <i>pvData</i>: A pointer to an array of <b>BYTE</b> values. The size of this array is specified in the <i>pcbData</i> parameter.

Returns the SHA256 hash. If the hash does not exist, it is 
			computed by using the <a href="/windows/desktop/api/wincrypt/nf-wincrypt-crypthashcertificate">CryptHashCertificate</a> function.



#### CERT_SIGN_HASH_CNG_ALG_PROP_ID

Data type of *pvData*: Pointer to a null-terminated Unicode string.

Returns the `L"<SIGNATURE>/<HASH>"` string representing the certificate signature. The `<SIGNATURE>` value identifies the CNG public key algorithm. The following algorithms are supported:

- L"RSA" (BCRYPT_RSA_ALGORITHM)
- L"DSA" (BCRYPT_DSA_ALGORITHM)
- L"ECDSA" (SSL_ECDSA_ALGORITHM)

The `<HASH>` value identifies the CNG hash algorithm. The following algorithms are supported:

- L"MD5" (BCRYPT_MD5_ALGORITHM)
- L"SHA1" (BCRYPT_SHA1_ALGORITHM)
- L"SHA256" (BCRYPT_SHA256_ALGORITHM)
- L"SHA384" (BCRYPT_SHA384_ALGORITHM)
- L"SHA512" (BCRYPT_SHA512_ALGORITHM)

The following are common examples:

- L"RSA/SHA1"
- L"RSA/SHA256"
- L"ECDSA/SHA256"

**Windows 7 and Windows Server 2008 R2:** Support for this property begins.

#### CERT_SIGNATURE_HASH_PROP_ID

Data type of *pvData*: A pointer to an array of **BYTE** values. The size of this array is specified in the *pcbData* parameter.

Returns the signature hash. If the hash does not exist, it is computed by using the [CryptHashToBeSigned](/windows/win32/api/wincrypt/nf-wincrypt-crypthashtobesigned) function. The length of the hash is 20 bytes for SHA and 16 for MD5.

#### CERT_SMART_CARD_DATA_PROP_ID

Data type of *pvData*: A pointer to an array of **BYTE** values. The size of this array is specified in the *pcbData* parameter.

Returns a pointer to encoded smart card data. Prior to calling **CertGetCertificateContextProperty**, you can use this constant to retrieve a smart card certificate by using the [CertFindCertificateInStore](/windows/win32/api/wincrypt/nf-wincrypt-certfindcertificateinstore) function with the *pvFindPara* parameter set to **CERT_SMART_CARD_DATA_PROP_ID** and the *dwFindType* parameter set to **CERT_FIND_PROPERTY**.

#### CERT_SMART_CARD_ROOT_INFO_PROP_ID

Data type of *pvData*: A pointer to an array of **BYTE** values. The size of this array is specified in the *pcbData* parameter.

Returns a pointer to an encoded [CRYPT_SMART_CARD_ROOT_INFO](/windows/win32/api/wincrypt/ns-wincrypt-crypt_smart_card_root_info) structure.

#### CERT_SOURCE_LOCATION_PROP_ID

This identifier is reserved.

#### CERT_SOURCE_URL_PROP_ID

This identifier is reserved.

#### CERT_SUBJECT_DISABLE_CRL_PROP_ID

This identifier is reserved.

#### CERT_SUBJECT_INFO_ACCESS_PROP_ID

Data type of *pvData*: A pointer to an array of **BYTE** values. The size of this array is specified in the *pcbData* parameter.

Returns the subject information access extension of the certificate context as an encoded [CERT_SUBJECT_INFO_ACCESS](/windows/win32/api/wincrypt/ns-wincrypt-cert_authority_info_access) structure.

#### CERT_SUBJECT_NAME_MD5_HASH_PROP_ID

Data type of *pvData*: A pointer to an array of **BYTE** values. The size of this array is specified in the *pcbData* parameter.

Returns an MD5 hash of the encoded subject name of the certificate context.

#### CERT_SUBJECT_OCSP_AUTHORITY_INFO_ACCESS_PROP_ID

This identifier is reserved.

#### CERT_SUBJECT_PUB_KEY_BIT_LENGTH_PROP_ID

Data type of *pvData*: Pointer to a **DWORD** value.

Returns the length, in bits, of the public key in the certificate.

**Windows 8 and Windows Server 2012:** Support for this property begins.

#### CERT_SUBJECT_PUBLIC_KEY_MD5_HASH_PROP_ID

Data type of *pvData*: A pointer to an array of **BYTE** values. The size of this array is specified in the *pcbData* parameter.

Returns the MD5 hash of this certificate's public key.

For all user-defined property identifiers, *pvData* points to an array of **BYTE** values.

For more information about each property identifier, see the documentation on the *dwPropId* parameter in [CertSetCertificateContextProperty](/windows/win32/api/wincrypt/nf-wincrypt-certsetcertificatecontextproperty).

### -param pvData [out]

A pointer to a buffer to receive the data as determined by *dwPropId*. Structures pointed to by members of a structure returned are also returned following the base structure. Therefore, the size contained in *pcbData* often exceeds the size of the base structure.

This parameter can be **NULL** to set the size of the information for memory allocation purposes. For more information, see [Retrieving Data of Unknown Length](/windows/win32/SecCrypto/retrieving-data-of-unknown-length).

### -param pcbData [in, out]

A pointer to a **DWORD** value that specifies the size, in bytes, of the buffer pointed to by the *pvData* parameter. When the function returns, the **DWORD** value contains the number of bytes to be stored in the buffer.

To obtain the required size of a buffer at run time, pass **NULL** for the *pvData* parameter, and set the value pointed to by this parameter to zero. If the *pvData* parameter is not **NULL** and the size specified in *pcbData* is less than the number of bytes required to contain the data, the function fails, [GetLastError](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) returns **ERROR_MORE_DATA**, and the required size is placed in the variable pointed to by the *pcbData* parameter.

> [!NOTE]
> When processing the data returned in the buffer, applications must use the actual size of the data returned. The actual size can be slightly smaller than the size of the buffer specified on input. (On input, buffer sizes are usually specified large enough to ensure that the largest possible output data fits in the buffer.) On output, the variable pointed to by this parameter is updated to reflect the actual size of the data copied to the buffer.

## -returns

If the function succeeds, the function returns **TRUE**.

If the function fails, it returns **FALSE**. For extended error information, call [GetLastError](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror).

Some possible error codes follow:

| Return code | Description |
|-------------|-------------|
| **CRYPT_E_NOT_FOUND** | The certificate does not have the specified property. |
| **ERROR_MORE_DATA** | If the buffer specified by the *pvData* parameter is not large enough to hold the returned data, the function sets the **ERROR_MORE_DATA** code and stores the required buffer size, in bytes, in the variable pointed to by *pcbData*. |

Errors from the called function [CryptHashCertificate](/windows/win32/api/wincrypt/nf-wincrypt-crypthashcertificate) can be propagated to this function.

## -remarks

Properties are not stored inside a certificate. Typically, they are associated with a certificate after the certificate response is received and then saved with the certificate in the store. For security reasons, we recommend that you validate property values before saving  them and that you save only informational properties such as the **CERT_FRIENDLY_NAME_PROP_ID** value in user stores. All other property types should be saved in local computer stores.

Your code can use a macro to evaluate the class of hash for a certificate context. For more information, see [CertSetCertificateContextProperty](/windows/win32/api/wincrypt/nf-wincrypt-certsetcertificatecontextproperty).

### Examples

For examples that use this function, see [Example C Program: Getting and Setting Certificate Properties](/windows/win32/SecCrypto/example-c-program-getting-and-setting-certificate-properties) and [Example C Program: Listing the Certificates in a Store](/windows/win32/SecCrypto/example-c-program-listing-the-certificates-in-a-store).

## -see-also

[CERT_KEY_CONTEXT](/windows/win32/api/wincrypt/ns-wincrypt-cert_key_context)

[CertCreateCertificateContext](/windows/win32/api/wincrypt/nf-wincrypt-certcreatecertificatecontext)

[CertSetCertificateContextProperty](/windows/win32/api/wincrypt/nf-wincrypt-certsetcertificatecontextproperty)

[CryptHashCertificate](/windows/win32/api/wincrypt/nf-wincrypt-crypthashcertificate)

[CryptHashToBeSigned](/windows/win32/api/wincrypt/nf-wincrypt-crypthashtobesigned)

[Extended Property Functions](/windows/win32/SecCrypto/cryptography-functions)
