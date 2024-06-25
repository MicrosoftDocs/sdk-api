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

The <b>CertGetCertificateContextProperty</b> function retrieves the information contained in an extended property of a <a href="/windows/desktop/SecGloss/c-gly">certificate context</a>.

## -parameters

### -param pCertContext [in]

A pointer to the 
<a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_context">CERT_CONTEXT</a> structure of the <a href="/windows/desktop/SecGloss/c-gly">certificate</a> that contains the property to be retrieved.

### -param dwPropId [in]

The property to be retrieved. 
			 Currently defined identifiers and the data type to be 
			 returned in <i>pvData</i> are listed in the 
			 following table.



#### CERT_ACCESS_STATE_PROP_ID

Data type of <i>pvData</i>: A pointer to a <b>DWORD</b> value.

Returns a <b>DWORD</b> value that indicates whether 
			    write operations to the certificate are persisted. 
				 The <b>DWORD</b> value is not set if the certificate 
				 is in a memory store or in a registry-based store 
				 that is opened as read-only.



#### CERT_AIA_URL_RETRIEVED_PROP_ID

This identifier is reserved.

#### CERT_ARCHIVED_KEY_HASH_PROP_ID

Data type of <i>pvData</i>: A pointer to an array of <b>BYTE</b> values. The size of this array is specified in the <i>pcbData</i> parameter.

Returns a previously saved encrypted key <a href="/windows/desktop/SecGloss/h-gly">hash</a> for the certificate context.

#### CERT_ARCHIVED_PROP_ID

Data type of <i>pvData</i>: <b>NULL</b>. If the <b>CertGetCertificateContextProperty</b> function returns true, then the specified property ID exists for the <a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_context">CERT_CONTEXT</a>.

Indicates the certificate is skipped during  enumerations. A certificate with this property set is found with explicit search operations, such as those used to find a certificate with a specific hash or a serial number. No data in <i>pvData</i> is associated with this property.



#### CERT_AUTHORITY_INFO_ACCESS_PROP_ID

This identifier is reserved.



#### CERT_AUTO_ENROLL_PROP_ID

Data type of <i>pvData</i>: A pointer to an array of <b>BYTE</b> values. The size of this array is specified in the <i>pcbData</i> parameter.

Returns a null-terminated Unicode string that names the certificate type for which the certificate has been auto enrolled.



#### CERT_AUTO_ENROLL_RETRY_PROP_ID

This identifier is reserved.



#### CERT_BACKED_UP_PROP_ID

This identifier is reserved.



#### CERT_CA_DISABLE_CRL_PROP_ID

Data type of <i>pvData</i>: A pointer to an array of <b>BYTE</b> values. The size of this array is specified in the <i>pcbData</i> parameter. 

Disables <a href="/windows/desktop/SecGloss/c-gly">certificate revocation list</a> (CRL) retrieval for certificates used by the <a href="/windows/desktop/SecGloss/c-gly">certification authority</a> (CA). If the CA certificate contains this property, it must also include the <b>CERT_CA_OCSP_AUTHORITY_INFO_ACCESS_PROP_ID</b> property.



#### CERT_CA_OCSP_AUTHORITY_INFO_ACCESS_PROP_ID

Data type of <i>pvData</i>: A pointer to an array of <b>BYTE</b> values. The size of this array is specified in the <i>pcbData</i> parameter. 

Contains the list of <a href="/windows/desktop/SecGloss/o-gly">online certificate status protocol</a> (OCSP) URLs to use for certificates issued by the CA certificate. The array contents are the <a href="/windows/desktop/SecGloss/a-gly">Abstract Syntax Notation One</a> (ASN.1)-encoded bytes of an <b>X509_AUTHORITY_INFO_ACCESS</b> structure where <b>pszAccessMethod</b> is set to <b>szOID_PKIX_OCSP</b>.



#### CERT_CROSS_CERT_DIST_POINTS_PROP_ID

Data type of <i>pvData</i>: A pointer to an array of <b>BYTE</b> values. The size of this array is specified in the <i>pcbData</i> parameter.

Location of the cross certificates. Currently, this identifier is only applicable to certificates and not to CRLs or <a href="/windows/desktop/SecGloss/c-gly">certificate trust lists</a> (CTLs).

The <b>BYTE</b> array contains an ASN.1-encoded <a href="/windows/desktop/api/wincrypt/ns-wincrypt-cross_cert_dist_points_info">CROSS_CERT_DIST_POINTS_INFO</a> structure decoded by using the <a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptdecodeobject">CryptDecodeObject</a> function with a X509_CROSS_CERT_DIST_POINTS value for the <i>lpszStuctType</i> parameter.



#### CERT_CTL_USAGE_PROP_ID

Data type of <i>pvData</i>: A pointer to an array of <b>BYTE</b> values. The size of this array is specified in the <i>pcbData</i> parameter.

Returns an array of bytes that contain an ASN.1-encoded <a href="/windows/desktop/api/wincrypt/ns-wincrypt-ctl_usage">CTL_USAGE</a> structure.



#### CERT_DATE_STAMP_PROP_ID

Data type of <i>pvData</i>: A pointer to a <b>FILETIME</b> structure.

Time when the certificate was added to the store.



#### CERT_DESCRIPTION_PROP_ID

Data type of <i>pvData</i>: A pointer to an array of <b>BYTE</b> values. The size of this array is specified in the <i>pcbData</i> parameter.

Returns the property displayed by the certificate UI. This property allows the user to describe the certificate's use.



#### CERT_EFS_PROP_ID

This identifier is reserved.



#### CERT_ENHKEY_USAGE_PROP_ID

Data type of <i>pvData</i>: A pointer to an array of <b>BYTE</b> values. The size of this array is specified in the <i>pcbData</i> parameter.

Returns an array of bytes that contain an ASN.1-encoded <a href="/windows/desktop/api/wincrypt/ns-wincrypt-ctl_usage">CERT_ENHKEY_USAGE</a> structure. 
			 This structure contains an array of 
			 Enhanced Key Usage <a href="/windows/desktop/SecGloss/o-gly">object identifiers</a> (OIDs),
			 each of which specifies a valid use of the certificate.



#### CERT_ENROLLMENT_PROP_ID

Data type of <i>pvData</i>: A pointer to an array of <b>BYTE</b> values. The size of this array is specified in the <i>pcbData</i> parameter.

Enrollment information of the pending request that contains 
			RequestID, CADNSName, CAName, and DisplayName. The data format 
			is defined as follows.<table>
<tr>
<th>Bytes</th>
<th>Contents</th>
</tr>
<tr>
<td>
First 4 bytes

</td>
<td>
Pending request ID

</td>
</tr>
<tr>
<td>
Next 4 bytes

</td>
<td>
CADNSName size, in characters, including the terminating null character, followed 
			by CADNSName string with terminating null character

</td>
</tr>
<tr>
<td>
Next 4 bytes

</td>
<td>
CAName 
			size, in characters, including the terminating null character, followed by CAName 
			string with terminating null character

</td>
</tr>
<tr>
<td>
Next 4 bytes

</td>
<td>
DisplayName size, in 
			characters, including the terminating null character, followed by DisplayName 
			string with terminating null character

</td>
</tr>
</table>
 





#### CERT_EXTENDED_ERROR_INFO_PROP_ID

Data type of <i>pvData</i>: A pointer to an array of <b>BYTE</b> values. The size of this array is specified in the <i>pcbData</i> parameter.

Returns a null-terminated Unicode character 
			 string that contains extended error information for the certificate context.



#### CERT_FORTEZZA_DATA_PROP_ID

This identifier is reserved.



#### CERT_FRIENDLY_NAME_PROP_ID

Data type of <i>pvData</i>: A pointer to an array of <b>BYTE</b> values. The size of this array is specified in the <i>pcbData</i> parameter.

Returns a null-terminated Unicode character 
			 string that contains the display name for the 
			 certificate.



#### CERT_HASH_PROP_ID

Data type of <i>pvData</i>: A pointer to an array of <b>BYTE</b> values. The size of this array is specified in the <i>pcbData</i> parameter.

Returns the SHA1 hash. If the hash does not exist, 
			 it is computed by using the <a href="/windows/desktop/api/wincrypt/nf-wincrypt-crypthashcertificate">CryptHashCertificate</a> function.



#### CERT_HCRYPTPROV_OR_NCRYPT_KEY_HANDLE_PROP_ID

Data type of <i>pvData</i>: A pointer to an <a href="/windows/desktop/SecCrypto/hcryptprov-or-ncrypt-key-handle">HCRYPTPROV_OR_NCRYPT_KEY_HANDLE</a> data type.

Returns either the <b>HCRYPTPROV</b> or <b>NCRYPT_KEY_HANDLE</b> choice.



#### CERT_HCRYPTPROV_TRANSFER_PROP_ID

Returns the Cryptography API (CAPI)  key handle associated with the certificate. The caller is responsible for freeing the handle. It will not be freed when the context is freed. The property value is removed after it is returned. If you call this property on a context that has a CNG key, <b>CRYPT_E_NOT_FOUND</b> is returned.



#### CERT_IE30_RESERVED_PROP_ID

This identifier is reserved.



#### CERT_ISSUER_PUBLIC_KEY_MD5_HASH_PROP_ID

Data type of <i>pvData</i>: A pointer to an array of <b>BYTE</b> values. The size of this array is specified in the <i>pcbData</i> parameter.

MD5 hash of the <a href="/windows/desktop/SecGloss/p-gly">public key</a> associated with the <a href="/windows/desktop/SecGloss/p-gly">private key</a> 
			used to sign this certificate.



#### CERT_ISSUER_SERIAL_NUMBER_MD5_HASH_PROP_ID

Data type of <i>pvData</i>: A pointer to an array of <b>BYTE</b> values. The size of this array is specified in the <i>pcbData</i> parameter.

MD5 hash of the issuer name and serial number from this certificate.



#### CERT_KEY_CONTEXT_PROP_ID

Data type of <i>pvData</i>: A pointer to a <a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_key_context">CERT_KEY_CONTEXT</a> structure.

Returns a <a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_key_context">CERT_KEY_CONTEXT</a> structure.



#### CERT_KEY_IDENTIFIER_PROP_ID

Data type of <i>pvData</i>: A pointer to an array of <b>BYTE</b> values. The size of this array is specified in the <i>pcbData</i> parameter.

If nonexistent, searches for the 
			 szOID_SUBJECT_KEY_IDENTIFIER extension. 
			 If that fails, a SHA1 hash is done on the certificate's 
			 <b>SubjectPublicKeyInfo</b> member to produce the 
			 identifier values.



#### CERT_KEY_PROV_HANDLE_PROP_ID

Data type of <i>pvData</i>: A pointer to an <a href="/windows/desktop/SecCrypto/hcryptprov">HCRYPTPROV</a> value.

Returns the provider handle obtained from 
			CERT_KEY_CONTEXT_PROP_ID.



#### CERT_KEY_PROV_INFO_PROP_ID

Data type of <i>pvData</i>: A pointer to a <a href="/windows/desktop/api/wincrypt/ns-wincrypt-crypt_key_prov_info">CRYPT_KEY_PROV_INFO</a> structure.

Returns a pointer to a <a href="/windows/desktop/api/wincrypt/ns-wincrypt-crypt_key_prov_info">CRYPT_KEY_PROV_INFO</a> structure.



#### CERT_KEY_SPEC_PROP_ID

Data type of <i>pvData</i>: A pointer to a <b>DWORD</b> value.

Returns a <b>DWORD</b> value that specifies the private 
			key obtained from CERT_KEY_CONTEXT_PROP_ID if it exists. 
			Otherwise, if CERT_KEY_PROV_INFO_PROP_ID exists, 
			it is the source of the <i>dwKeySpec</i>.



#### CERT_MD5_HASH_PROP_ID

Data type of <i>pvData</i>: A pointer to an array of <b>BYTE</b> values. The size of this array is specified in the <i>pcbData</i> parameter.

Returns the MD5 hash. If the hash does not exist, 
			it is computed by using the <a href="/windows/desktop/api/wincrypt/nf-wincrypt-crypthashcertificate">CryptHashCertificate</a> function.



#### CERT_NCRYPT_KEY_HANDLE_PROP_ID

Data type of <i>pvData</i>: A pointer to an <b>NCRYPT_KEY_HANDLE</b> data type.

Returns a <b>CERT_NCRYPT_KEY_SPEC</b> choice where applicable.



#### CERT_NCRYPT_KEY_HANDLE_TRANSFER_PROP_ID

Returns the CNG key handle associated with the certificate. The caller is responsible for freeing the handle. It will not be freed when the context is freed. The property value is removed after it is returned. If you call this property on a context that has a legacy (CAPI) key, <b>CRYPT_E_NOT_FOUND</b> is returned.



#### CERT_NEW_KEY_PROP_ID

This identifier is reserved.



#### CERT_NEXT_UPDATE_LOCATION_PROP_ID

Data type of <i>pvData</i>: A pointer to an array of <b>BYTE</b> values. The size of this array is specified in the <i>pcbData</i> parameter.

Returns the ASN.1-encoded <a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_alt_name_info">CERT_ALT_NAME_INFO</a> structure.

CERT_NEXT_UPDATE_LOCATION_PROP_ID is currently used only 
			with CTLs.



#### CERT_NO_AUTO_EXPIRE_CHECK_PROP_ID

This identifier is reserved.



#### CERT_OCSP_CACHE_PREFIX_PROP_ID

This identifier is reserved.



#### CERT_OCSP_RESPONSE_PROP_ID

Data type of <i>pvData</i>: A pointer to an array of <b>BYTE</b> values. The size of this array is specified in the <i>pcbData</i> parameter.

Returns an encoded OCSP response for this certificate.



#### CERT_PUB_KEY_CNG_ALG_BIT_LENGTH_PROP_ID

Data type of <i>pvData</i>: Pointer to a null-terminated Unicode string.

Returns an L”<i>&lt;PUBKEY&gt;</i>/<i>&lt;BITLENGTH&gt;</i>” string representing the certificate’s public key algorithm and bit length. The following <i>&lt;PUBKEY&gt;</i> algorithms are supported:

<ul>
<li>L"RSA" (BCRYPT_RSA_ALGORITHM)</li>
<li>L"DSA" (BCRYPT_DSA_ALGORITHM)</li>
<li>L"ECDSA" (SSL_ECDSA_ALGORITHM)</li>
</ul>
<b>Windows 8 and Windows Server 2012:  </b>Support for this property begins.



#### CERT_PUBKEY_ALG_PARA_PROP_ID

Data type of <i>pvData</i>: A pointer to an array of <b>BYTE</b> values. The size of this array is specified in the <i>pcbData</i> parameter.

For public keys that support algorithm parameter inheritance, returns the ASN.1-encoded PublicKey Algorithm parameters. For <a href="/windows/desktop/SecGloss/d-gly">Digital Signature Standard</a> (DSS), returns the parameters encoded by using 
the <a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptencodeobject">CryptEncodeObject</a> function. This property is used only if CMS_PKCS7 is defined.



#### CERT_PUBKEY_HASH_RESERVED_PROP_ID

This identifier is reserved.



#### CERT_PVK_FILE_PROP_ID

Data type of <i>pvData</i>: A pointer to an array of <b>BYTE</b> values. The size of this array is specified in the <i>pcbData</i> parameter.

Returns a null-terminated Unicode wide character 
			string that contains the file name that contains the private key 
			associated with the certificate's public key.



#### CERT_RENEWAL_PROP_ID

Data type of <i>pvData</i>: A pointer to an array of <b>BYTE</b> values. The size of this array is specified in the <i>pcbData</i> parameter.

Returns the hash of the renewed certificate.



#### CERT_REQUEST_ORIGINATOR_PROP_ID

Data type of <i>pvData</i>: A pointer to an array of <b>BYTE</b> values. The size of this array is specified in the <i>pcbData</i> parameter.

Returns a null-terminated Unicode string that contains the DNS computer name for the origination of the certificate context request.



#### CERT_ROOT_PROGRAM_CERT_POLICIES_PROP_ID

Data type of <i>pvData</i>: A pointer to an array of <b>BYTE</b> values. The size of this array is specified in the <i>pcbData</i> parameter.

Returns a pointer to an encoded <a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_policies_info">CERT_POLICIES_INFO</a> structure that contains the application policies of the root certificate for the context. This property can be decoded by using the <a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptdecodeobject">CryptDecodeObject</a> function with the <i>lpszStructType</i> parameter set to <b>X509_CERT_POLICIES</b> and the <i>dwCertEncodingType</i> parameter set to a combination of <b>X509_ASN_ENCODING</b> bitwise <b>OR</b> <b>PKCS_7_ASN_ENCODING</b>.



#### CERT_ROOT_PROGRAM_NAME_CONSTRAINTS_PROP_ID

This identifier is reserved.



#### CERT_SHA1_HASH_PROP_ID

Data type of <i>pvData</i>: A pointer to an array of <b>BYTE</b> values. The size of this array is specified in the <i>pcbData</i> parameter.

Returns the SHA1 hash. If the hash does not exist, it is 
			computed by using the <a href="/windows/desktop/api/wincrypt/nf-wincrypt-crypthashcertificate">CryptHashCertificate</a> function.



#### CERT_SHA1_SHA256_HASH_PROP_ID

Data type of <i>pvData</i>: A pointer to an array of <b>BYTE</b> values. The size of this array is 52 bytes, 20 bytes for the SHA1 hash and 32 bytes for the SHA256 hash.

Returns a combination of the SHA1 hash and the SHA256 hash. If the hash does not exist, it is 
			computed by using the <a href="/windows/desktop/api/wincrypt/nf-wincrypt-crypthashcertificate">CryptHashCertificate</a> function.



#### CERT_SHA256_HASH_PROP_ID

Data type of <i>pvData</i>: A pointer to an array of <b>BYTE</b> values. The size of this array is specified in the <i>pcbData</i> parameter.

Returns the SHA256 hash. If the hash does not exist, it is 
			computed by using the <a href="/windows/desktop/api/wincrypt/nf-wincrypt-crypthashcertificate">CryptHashCertificate</a> function.



#### CERT_SIGN_HASH_CNG_ALG_PROP_ID

Data type of <i>pvData</i>: Pointer to a null-terminated Unicode string.

Returns the L”<i>&lt;SIGNATURE&gt;</i>/<i>&lt;HASH&gt;</i>” string representing the certificate signature. The <i>&lt;SIGNATURE&gt;</i> value identifies the CNG public key algorithm. The following algorithms are supported:

<ul>
<li>L"RSA" (BCRYPT_RSA_ALGORITHM)</li>
<li>L"DSA" (BCRYPT_DSA_ALGORITHM)</li>
<li>L"ECDSA" (SSL_ECDSA_ALGORITHM)</li>
</ul>
The <i>&lt;HASH&gt;</i> value identifies the CNG hash algorithm. The following algorithms are supported:

<ul>
<li>L"MD5" (BCRYPT_MD5_ALGORITHM)</li>
<li>L"SHA1" (BCRYPT_SHA1_ALGORITHM)</li>
<li>L"SHA256" (BCRYPT_SHA256_ALGORITHM)</li>
<li>L"SHA384" (BCRYPT_SHA384_ALGORITHM)</li>
<li>L"SHA512" (BCRYPT_SHA512_ALGORITHM)</li>
</ul>
The following are common examples:

<ul>
<li>L"RSA/SHA1"</li>
<li>L"RSA/SHA256"</li>
<li>L"ECDSA/SHA256" </li>
</ul>
<b>Windows 7 and Windows Server 2008 R2:  </b>Support for this property begins.



#### CERT_SIGNATURE_HASH_PROP_ID

Data type of <i>pvData</i>: A pointer to an array of <b>BYTE</b> values. The size of this array is specified in the <i>pcbData</i> parameter.

Returns the signature hash. If the hash does not exist, 
			it is computed by using the <a href="/windows/desktop/api/wincrypt/nf-wincrypt-crypthashtobesigned">CryptHashToBeSigned</a> function. 
			The length of the hash is 20 bytes for SHA and 16 for MD5.



#### CERT_SMART_CARD_DATA_PROP_ID

Data type of <i>pvData</i>: A pointer to an array of <b>BYTE</b> values. The size of this array is specified in the <i>pcbData</i> parameter.

Returns a pointer to encoded smart card data. Prior to calling <b>CertGetCertificateContextProperty</b>, you can use this constant to retrieve a smart card certificate by using the <a href="/windows/desktop/api/wincrypt/nf-wincrypt-certfindcertificateinstore">CertFindCertificateInStore</a> function with the <i>pvFindPara</i> parameter set to <b>CERT_SMART_CARD_DATA_PROP_ID</b> and the <i>dwFindType</i> parameter set to <b>CERT_FIND_PROPERTY</b>.



#### CERT_SMART_CARD_ROOT_INFO_PROP_ID

Data type of <i>pvData</i>: A pointer to an array of <b>BYTE</b> values. The size of this array is specified in the <i>pcbData</i> parameter.

Returns a pointer to an encoded <a href="/windows/desktop/api/wincrypt/ns-wincrypt-crypt_smart_card_root_info">CRYPT_SMART_CARD_ROOT_INFO</a> structure.



#### CERT_SOURCE_LOCATION_PROP_ID

This identifier is reserved.



#### CERT_SOURCE_URL_PROP_ID

This identifier is reserved.



#### CERT_SUBJECT_DISABLE_CRL_PROP_ID

This identifier is reserved.



#### CERT_SUBJECT_INFO_ACCESS_PROP_ID

Data type of <i>pvData</i>: A pointer to an array of <b>BYTE</b> values. The size of this array is specified in the <i>pcbData</i> parameter.

Returns the subject information access extension of the certificate context as an encoded <a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_authority_info_access">CERT_SUBJECT_INFO_ACCESS</a> structure.



#### CERT_SUBJECT_NAME_MD5_HASH_PROP_ID

Data type of <i>pvData</i>: A pointer to an array of <b>BYTE</b> values. The size of this array is specified in the <i>pcbData</i> parameter.

Returns an MD5 hash of the encoded subject name of the certificate context. 



#### CERT_SUBJECT_OCSP_AUTHORITY_INFO_ACCESS_PROP_ID

This identifier is reserved.



#### CERT_SUBJECT_PUB_KEY_BIT_LENGTH_PROP_ID

Data type of <i>pvData</i>: Pointer to a <b>DWORD</b> value.

Returns the length, in bits, of the public key in the certificate.

<b>Windows 8 and Windows Server 2012:  </b>Support for this property begins.



#### CERT_SUBJECT_PUBLIC_KEY_MD5_HASH_PROP_ID

Data type of <i>pvData</i>: A pointer to an array of <b>BYTE</b> values. The size of this array is specified in the <i>pcbData</i> parameter.

Returns the MD5 hash of this certificate's public key.

For all user-defined property identifiers, <i>pvData</i> points to an array of <b>BYTE</b> values.

For more information about each property identifier, see the documentation on the <i>dwPropId</i> parameter in 
<a href="/windows/desktop/api/wincrypt/nf-wincrypt-certsetcertificatecontextproperty">CertSetCertificateContextProperty</a>.

### -param pvData [out]

A pointer to a buffer to receive the data as determined by <i>dwPropId</i>. Structures pointed to by members of a structure returned are also returned following the base structure. Therefore, the size contained in <i>pcbData</i> often exceeds the size of the base structure.

This parameter can be <b>NULL</b> to set the size of the information for memory allocation purposes. For more information, see 
<a href="/windows/desktop/SecCrypto/retrieving-data-of-unknown-length">Retrieving Data of Unknown Length</a>.

### -param pcbData [in, out]

A pointer to a <b>DWORD</b> value that specifies the size, in bytes, of the buffer pointed to by the <i>pvData</i> parameter. When the function returns, the <b>DWORD</b> value contains the number of bytes to be stored in the buffer.

To obtain the required size of a buffer at run time, pass <b>NULL</b> for the <i>pvData</i> parameter, and set the value pointed to by this parameter to zero. If the <i>pvData</i> parameter is not <b>NULL</b> and the size specified in <i>pcbData</i>   is less than the number of bytes required to  contain the data, the function fails, <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> returns <b>ERROR_MORE_DATA</b>, and the required size is placed in the variable pointed to by the <i>pcbData</i> parameter.

<div class="alert"><b>Note</b>  When processing the data returned in the buffer, applications must use the actual size of the data returned. The actual size can be slightly smaller than the size of the buffer specified on input. (On input, buffer sizes are usually specified large enough to ensure that the largest possible output data fits in the buffer.) On output, the variable pointed to by this parameter is updated to reflect the actual size of the data copied to the buffer.</div>
<div> </div>

## -returns

If the function succeeds, the function returns <b>TRUE</b>.

If the function fails, it returns <b>FALSE</b>. For extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

 Some possible error codes follow.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>CRYPT_E_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
The certificate does not have the specified property.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_MORE_DATA</b></dt>
</dl>
</td>
<td width="60%">
If the buffer specified by the <i>pvData</i> parameter is not large enough to hold the returned data, the function sets the <b>ERROR_MORE_DATA</b> code and stores the required buffer size, in bytes, in the variable pointed to by <i>pcbData</i>.
							

</td>
</tr>
</table>
 

Errors from the called function 
<a href="/windows/desktop/api/wincrypt/nf-wincrypt-crypthashcertificate">CryptHashCertificate</a> can be propagated to this function.

## -remarks

Properties are not stored inside a certificate. Typically, they are associated with a certificate after the certificate response is received and then saved with the certificate in the store. For security reasons, we recommend that you validate property values before saving  them and that you save only informational properties such as the <b>CERT_FRIENDLY_NAME_PROP_ID</b> value in user stores. All other property types should be saved in local computer stores.

Your code can use a macro to evaluate the class of hash for a certificate context. For more information, see <a href="/windows/desktop/api/wincrypt/nf-wincrypt-certsetcertificatecontextproperty">CertSetCertificateContextProperty</a>.


#### Examples

For examples that use this function, see 
<a href="/windows/desktop/SecCrypto/example-c-program-getting-and-setting-certificate-properties">Example C Program: Getting and Setting Certificate Properties</a> and 
<a href="/windows/desktop/SecCrypto/example-c-program-listing-the-certificates-in-a-store">Example C Program: Listing the Certificates in a Store</a>.

<div class="code"></div>

## -see-also

<a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_key_context">CERT_KEY_CONTEXT</a>



<a href="/windows/desktop/api/wincrypt/nf-wincrypt-certcreatecertificatecontext">CertCreateCertificateContext</a>



<a href="/windows/desktop/api/wincrypt/nf-wincrypt-certsetcertificatecontextproperty">CertSetCertificateContextProperty</a>



<a href="/windows/desktop/api/wincrypt/nf-wincrypt-crypthashcertificate">CryptHashCertificate</a>



<a href="/windows/desktop/api/wincrypt/nf-wincrypt-crypthashtobesigned">CryptHashToBeSigned</a>



<a href="/windows/desktop/SecCrypto/cryptography-functions">Extended Property Functions</a>