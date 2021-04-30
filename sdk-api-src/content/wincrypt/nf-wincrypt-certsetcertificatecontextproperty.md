---
UID: NF:wincrypt.CertSetCertificateContextProperty
title: CertSetCertificateContextProperty function (wincrypt.h)
description: Sets an extended property for a specified certificate context.
helpviewer_keywords: ["CERT_ACCESS_STATE_PROP_ID","CERT_AIA_URL_RETRIEVED_PROP_ID","CERT_ARCHIVED_KEY_HASH_PROP_ID","CERT_ARCHIVED_PROP_ID","CERT_AUTHORITY_INFO_ACCESS_PROP_ID","CERT_AUTO_ENROLL_PROP_ID","CERT_AUTO_ENROLL_RETRY_PROP_ID","CERT_BACKED_UP_PROP_ID","CERT_CA_DISABLE_CRL_PROP_ID","CERT_CA_OCSP_AUTHORITY_INFO_ACCESS_PROP_ID","CERT_CROSS_CERT_DIST_POINTS_PROP_ID","CERT_CTL_USAGE_PROP_ID","CERT_DATE_STAMP_PROP_ID","CERT_DESCRIPTION_PROP_ID","CERT_EFS_PROP_ID","CERT_ENHKEY_USAGE_PROP_ID","CERT_ENROLLMENT_PROP_ID","CERT_EXTENDED_ERROR_INFO_PROP_ID","CERT_FORTEZZA_DATA_PROP_ID","CERT_FRIENDLY_NAME_PROP_ID","CERT_HASH_PROP_ID","CERT_HCRYPTPROV_OR_NCRYPT_KEY_HANDLE_PROP_ID","CERT_HCRYPTPROV_TRANSFER_PROP_ID","CERT_IE30_RESERVED_PROP_ID","CERT_ISSUER_PUBLIC_KEY_MD5_HASH_PROP_ID","CERT_ISSUER_SERIAL_NUMBER_MD5_HASH_PROP_ID","CERT_KEY_CONTEXT_PROP_ID","CERT_KEY_IDENTIFIER_PROP_ID","CERT_KEY_PROV_HANDLE_PROP_ID","CERT_KEY_PROV_INFO_PROP_ID","CERT_KEY_SPEC_PROP_ID","CERT_MD5_HASH_PROP_ID","CERT_NCRYPT_KEY_HANDLE_PROP_ID","CERT_NCRYPT_KEY_HANDLE_TRANSFER_PROP_ID","CERT_NEW_KEY_PROP_ID","CERT_NEXT_UPDATE_LOCATION_PROP_ID","CERT_NO_AUTO_EXPIRE_CHECK_PROP_ID","CERT_OCSP_CACHE_PREFIX_PROP_ID","CERT_OCSP_RESPONSE_PROP_ID","CERT_PUBKEY_ALG_PARA_PROP_ID","CERT_PUBKEY_HASH_RESERVED_PROP_ID","CERT_PUB_KEY_CNG_ALG_BIT_LENGTH_PROP_ID","CERT_PVK_FILE_PROP_ID","CERT_RENEWAL_PROP_ID","CERT_REQUEST_ORIGINATOR_PROP_ID","CERT_ROOT_PROGRAM_CERT_POLICIES_PROP_ID","CERT_ROOT_PROGRAM_NAME_CONSTRAINTS_PROP_ID","CERT_SHA1_HASH_PROP_ID","CERT_SIGNATURE_HASH_PROP_ID","CERT_SIGN_HASH_CNG_ALG_PROP_ID","CERT_SMART_CARD_DATA_PROP_ID","CERT_SMART_CARD_ROOT_INFO_PROP_ID","CERT_SOURCE_LOCATION_PROP_ID","CERT_SOURCE_URL_PROP_ID","CERT_SUBJECT_DISABLE_CRL_PROP_ID","CERT_SUBJECT_INFO_ACCESS_PROP_ID","CERT_SUBJECT_NAME_MD5_HASH_PROP_ID","CERT_SUBJECT_OCSP_AUTHORITY_INFO_ACCESS_PROP_ID","CERT_SUBJECT_PUBLIC_KEY_MD5_HASH_PROP_ID","CERT_SUBJECT_PUB_KEY_BIT_LENGTH_PROP_ID","CertSetCertificateContextProperty","CertSetCertificateContextProperty function [Security]","_crypto2_certsetcertificatecontextproperty","security.certsetcertificatecontextproperty","wincrypt/CertSetCertificateContextProperty"]
old-location: security\certsetcertificatecontextproperty.htm
tech.root: security
ms.assetid: b4a0c66d-997f-49cb-935a-9187320037f1
ms.date: 12/05/2018
ms.keywords: CERT_ACCESS_STATE_PROP_ID, CERT_AIA_URL_RETRIEVED_PROP_ID, CERT_ARCHIVED_KEY_HASH_PROP_ID, CERT_ARCHIVED_PROP_ID, CERT_AUTHORITY_INFO_ACCESS_PROP_ID, CERT_AUTO_ENROLL_PROP_ID, CERT_AUTO_ENROLL_RETRY_PROP_ID, CERT_BACKED_UP_PROP_ID, CERT_CA_DISABLE_CRL_PROP_ID, CERT_CA_OCSP_AUTHORITY_INFO_ACCESS_PROP_ID, CERT_CROSS_CERT_DIST_POINTS_PROP_ID, CERT_CTL_USAGE_PROP_ID, CERT_DATE_STAMP_PROP_ID, CERT_DESCRIPTION_PROP_ID, CERT_EFS_PROP_ID, CERT_ENHKEY_USAGE_PROP_ID, CERT_ENROLLMENT_PROP_ID, CERT_EXTENDED_ERROR_INFO_PROP_ID, CERT_FORTEZZA_DATA_PROP_ID, CERT_FRIENDLY_NAME_PROP_ID, CERT_HASH_PROP_ID, CERT_HCRYPTPROV_OR_NCRYPT_KEY_HANDLE_PROP_ID, CERT_HCRYPTPROV_TRANSFER_PROP_ID, CERT_IE30_RESERVED_PROP_ID, CERT_ISSUER_PUBLIC_KEY_MD5_HASH_PROP_ID, CERT_ISSUER_SERIAL_NUMBER_MD5_HASH_PROP_ID, CERT_KEY_CONTEXT_PROP_ID, CERT_KEY_IDENTIFIER_PROP_ID, CERT_KEY_PROV_HANDLE_PROP_ID, CERT_KEY_PROV_INFO_PROP_ID, CERT_KEY_SPEC_PROP_ID, CERT_MD5_HASH_PROP_ID, CERT_NCRYPT_KEY_HANDLE_PROP_ID, CERT_NCRYPT_KEY_HANDLE_TRANSFER_PROP_ID, CERT_NEW_KEY_PROP_ID, CERT_NEXT_UPDATE_LOCATION_PROP_ID, CERT_NO_AUTO_EXPIRE_CHECK_PROP_ID, CERT_OCSP_CACHE_PREFIX_PROP_ID, CERT_OCSP_RESPONSE_PROP_ID, CERT_PUBKEY_ALG_PARA_PROP_ID, CERT_PUBKEY_HASH_RESERVED_PROP_ID, CERT_PUB_KEY_CNG_ALG_BIT_LENGTH_PROP_ID, CERT_PVK_FILE_PROP_ID, CERT_RENEWAL_PROP_ID, CERT_REQUEST_ORIGINATOR_PROP_ID, CERT_ROOT_PROGRAM_CERT_POLICIES_PROP_ID, CERT_ROOT_PROGRAM_NAME_CONSTRAINTS_PROP_ID, CERT_SHA1_HASH_PROP_ID, CERT_SIGNATURE_HASH_PROP_ID, CERT_SIGN_HASH_CNG_ALG_PROP_ID, CERT_SMART_CARD_DATA_PROP_ID, CERT_SMART_CARD_ROOT_INFO_PROP_ID, CERT_SOURCE_LOCATION_PROP_ID, CERT_SOURCE_URL_PROP_ID, CERT_SUBJECT_DISABLE_CRL_PROP_ID, CERT_SUBJECT_INFO_ACCESS_PROP_ID, CERT_SUBJECT_NAME_MD5_HASH_PROP_ID, CERT_SUBJECT_OCSP_AUTHORITY_INFO_ACCESS_PROP_ID, CERT_SUBJECT_PUBLIC_KEY_MD5_HASH_PROP_ID, CERT_SUBJECT_PUB_KEY_BIT_LENGTH_PROP_ID, CertSetCertificateContextProperty, CertSetCertificateContextProperty function [Security], _crypto2_certsetcertificatecontextproperty, security.certsetcertificatecontextproperty, wincrypt/CertSetCertificateContextProperty
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
 - CertSetCertificateContextProperty
 - wincrypt/CertSetCertificateContextProperty
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
 - CertSetCertificateContextProperty
---

# CertSetCertificateContextProperty function


## -description

The <b>CertSetCertificateContextProperty</b> function sets an extended property for a specified <a href="/windows/desktop/SecGloss/c-gly">certificate context</a>.

## -parameters

### -param pCertContext [in]

A pointer to a 
<a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_context">CERT_CONTEXT</a> structure.

### -param dwPropId [in]

The property to be set. The value of <i>dwPropId</i> determines the type and content of the <i>pvData</i> parameter. Currently defined identifiers and their related <i>pvData</i> types are as follows.

<div class="alert"><b>Note</b>  <a href="/previous-versions/windows/desktop/legacy/aa381414(v=vs.85)">CRYPT_HASH_BLOB</a> and <a href="/previous-versions/windows/desktop/legacy/aa381414(v=vs.85)">CRYPT_DATA_BLOB</a> are described in the <a href="/previous-versions/windows/desktop/legacy/aa381414(v=vs.85)">CRYPT_INTEGER_BLOB</a> topic.</div>
<div> </div>


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

Data type of <i>pvData</i>: 
  A pointer to a <a href="/previous-versions/windows/desktop/legacy/aa381414(v=vs.85)">CRYPT_HASH_BLOB</a> structure.

This property saves an encrypted key <a href="/windows/desktop/SecGloss/h-gly">hash</a> for the certificate context.



#### CERT_ARCHIVED_PROP_ID

Data type of <i>pvData</i>: A pointer to a <a href="/previous-versions/windows/desktop/legacy/aa381414(v=vs.85)">CRYPT_DATA_BLOB</a> structure.

Indicates that the <a href="/windows/desktop/SecGloss/c-gly">certificate</a> is skipped during enumerations. A certificate with this property set is still found with explicit search operations, such as finding a certificate with a specific <a href="/windows/desktop/SecGloss/h-gly">hash</a> or a specific serial number. This property can be set to the empty <a href="/windows/desktop/SecGloss/b-gly">BLOB</a>, <code>{0,NULL}</code>.



#### CERT_AUTHORITY_INFO_ACCESS_PROP_ID

This identifier is reserved.



#### CERT_AUTO_ENROLL_PROP_ID

Data type of <i>pvData</i>: A pointer to a <a href="/previous-versions/windows/desktop/legacy/aa381414(v=vs.85)">CRYPT_DATA_BLOB</a> structure.

A property that is set after a certificate has been enrolled by using Auto Enroll. The <a href="/previous-versions/windows/desktop/legacy/aa381414(v=vs.85)">CRYPT_DATA_BLOB</a> structure pointed to by <i>pvData</i> includes a null-terminated Unicode name of the certificate type for which the certificate has been auto enrolled. Any subsequent calls to Auto Enroll for the certificate checks for this property to determine whether the certificate has been enrolled.



#### CERT_AUTO_ENROLL_RETRY_PROP_ID

This identifier is reserved.



#### CERT_BACKED_UP_PROP_ID

This identifier is reserved.



#### CERT_CA_DISABLE_CRL_PROP_ID

Data type of <i>pvData</i>: A pointer to a <a href="/previous-versions/windows/desktop/legacy/aa381414(v=vs.85)">CRYPT_DATA_BLOB</a> structure.

Disables <a href="/windows/desktop/SecGloss/c-gly">certificate revocation list</a> (CRL) retrieval for certificates used by the <a href="/windows/desktop/SecGloss/c-gly">certification authority</a> (CA). If the CA certificate contains this property, it must also include the <b>CERT_CA_OCSP_AUTHORITY_INFO_ACCESS_PROP_ID</b> property.



#### CERT_CA_OCSP_AUTHORITY_INFO_ACCESS_PROP_ID

Data type of <i>pvData</i>: A pointer to a <a href="/previous-versions/windows/desktop/legacy/aa381414(v=vs.85)">CRYPT_DATA_BLOB</a> structure.

Contains the list of <a href="/windows/desktop/SecGloss/o-gly">online certificate status protocol</a> (OCSP) URLs to use for certificates issued by the CA certificate. The array contents are the <a href="/windows/desktop/SecGloss/a-gly">Abstract Syntax Notation One</a> (ASN.1)-encoded bytes of an <b>X509_AUTHORITY_INFO_ACCESS</b> structure where <b>pszAccessMethod</b> is set to <b>szOID_PKIX_OCSP</b>.



#### CERT_CROSS_CERT_DIST_POINTS_PROP_ID

Data type of <i>pvData</i>: A pointer to a <a href="/previous-versions/windows/desktop/legacy/aa381414(v=vs.85)">CRYPT_DATA_BLOB</a> structure.

Sets the location of the cross certificates. This value is only applicable to certificates and not to <a href="/windows/desktop/SecGloss/c-gly">certificate revocation lists</a> (CRLs) or <a href="/windows/desktop/SecGloss/c-gly">certificate trust lists</a> (CTLs). The <a href="/previous-versions/windows/desktop/legacy/aa381414(v=vs.85)">CRYPT_DATA_BLOB</a> structure contains an <a href="/windows/desktop/SecGloss/a-gly">Abstract Syntax Notation One</a> (ASN.1)-encoded 
<a href="/windows/desktop/api/wincrypt/ns-wincrypt-cross_cert_dist_points_info">CROSS_CERT_DIST_POINTS_INFO</a> structure that is encoded by using 
the <a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptencodeobject">CryptEncodeObject</a> function with a X509_CROSS_CERT_DIST_POINTS value for the <i>lpszStuctType</i> parameter.



#### CERT_CTL_USAGE_PROP_ID

Data type of <i>pvData</i>: A pointer to a <a href="/previous-versions/windows/desktop/legacy/aa381414(v=vs.85)">CRYPT_DATA_BLOB</a> structure.

The <a href="/previous-versions/windows/desktop/legacy/aa381414(v=vs.85)">CRYPT_DATA_BLOB</a> structure contains an ASN.1-encoded 
<a href="/windows/desktop/api/wincrypt/ns-wincrypt-ctl_usage">CTL_USAGE</a> structure. This structure is encoded by using the <a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptencodeobject">CryptEncodeObject</a> function with the X509_ENHANCED_KEY_USAGE value set.



#### CERT_DATE_STAMP_PROP_ID

Data type of <i>pvData</i>: A pointer to a <b>FILETIME</b> structure.

This property sets the time that the certificate was added to the store.



#### CERT_DESCRIPTION_PROP_ID

Data type of <i>pvData</i>: A pointer to a <a href="/previous-versions/windows/desktop/legacy/aa381414(v=vs.85)">CRYPT_DATA_BLOB</a> structure.

A property that is set and displayed by the certificate UI. This property allows the user to describe the certificate's use.



#### CERT_EFS_PROP_ID

This identifier is reserved.



#### CERT_ENHKEY_USAGE_PROP_ID

Data type of <i>pvData</i>: A pointer to a <a href="/previous-versions/windows/desktop/legacy/aa381414(v=vs.85)">CRYPT_DATA_BLOB</a> structure.

A property that indicates that the <i>pvData</i> parameter points to a <a href="/previous-versions/windows/desktop/legacy/aa381414(v=vs.85)">CRYPT_DATA_BLOB</a> structure that contains an ASN.1-encoded <a href="/windows/desktop/api/wincrypt/ns-wincrypt-ctl_usage">CERT_ENHKEY_USAGE</a> structure. This structure is encoded by using the <a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptencodeobject">CryptEncodeObject</a> function with the X509_ENHANCED_KEY_USAGE value set.



#### CERT_ENROLLMENT_PROP_ID

Data type of <i>pvData</i>: A pointer to a <a href="/previous-versions/windows/desktop/legacy/aa381414(v=vs.85)">CRYPT_DATA_BLOB</a> structure.

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

Data type of <i>pvData</i>: A pointer to a <a href="/previous-versions/windows/desktop/legacy/aa381414(v=vs.85)">CRYPT_DATA_BLOB</a> structure.

This property sets a string that contains extended error information for the certificate context.



#### CERT_FORTEZZA_DATA_PROP_ID

This identifier is reserved.



#### CERT_FRIENDLY_NAME_PROP_ID

Data type of <i>pvData</i>: A pointer to a <a href="/previous-versions/windows/desktop/legacy/aa381414(v=vs.85)">CRYPT_DATA_BLOB</a> structure.

The <a href="/previous-versions/windows/desktop/legacy/aa381414(v=vs.85)">CRYPT_DATA_BLOB</a> structure contains the display name of the certificate.



#### CERT_HASH_PROP_ID

Data type of <i>pvData</i>: A pointer to a <a href="/previous-versions/windows/desktop/legacy/aa381414(v=vs.85)">CRYPT_DATA_BLOB</a> structure.

This property is implicitly set by a call to 
the <a href="/windows/desktop/api/wincrypt/nf-wincrypt-certgetcertificatecontextproperty">CertGetCertificateContextProperty</a> function.



#### CERT_HCRYPTPROV_OR_NCRYPT_KEY_HANDLE_PROP_ID

Data type of <i>pvData</i>: A pointer to an <a href="/windows/desktop/SecCrypto/hcryptprov-or-ncrypt-key-handle">HCRYPTPROV_OR_NCRYPT_KEY_HANDLE</a> data type.

This property calls <a href="/windows/desktop/api/ncrypt/nf-ncrypt-ncryptiskeyhandle">NCryptIsKeyHandle</a> to determine whether this is an <b>NCRYPT_KEY_HANDLE</b>. For an <b>NCRYPT_KEY_HANDLE</b>,  sets <b>CERT_NCRYPT_KEY_HANDLE_PROP_ID</b>; otherwise, it sets <b>CERT_KEY_PROV_HANDLE_PROP_ID</b>.



#### CERT_HCRYPTPROV_TRANSFER_PROP_ID

Sets the handle of the CAPI key associated with the certificate.



#### CERT_IE30_RESERVED_PROP_ID

This identifier is reserved.



#### CERT_ISSUER_PUBLIC_KEY_MD5_HASH_PROP_ID

Data type of <i>pvData</i>: A pointer to a <a href="/previous-versions/windows/desktop/legacy/aa381414(v=vs.85)">CRYPT_DATA_BLOB</a> structure.

This property sets the <a href="/windows/desktop/SecGloss/m-gly">MD5</a> <a href="/windows/desktop/SecGloss/h-gly">hash</a> of the <a href="/windows/desktop/SecGloss/p-gly">public key</a> associated with the <a href="/windows/desktop/SecGloss/p-gly">private key</a> used to sign this certificate.



#### CERT_ISSUER_SERIAL_NUMBER_MD5_HASH_PROP_ID

Data type of <i>pvData</i>: A pointer to a <a href="/previous-versions/windows/desktop/legacy/aa381414(v=vs.85)">CRYPT_DATA_BLOB</a> structure.

The <a href="/previous-versions/windows/desktop/legacy/aa381414(v=vs.85)">CRYPT_DATA_BLOB</a> structure contains the MD5 hash of the issuer name and serial number from this certificate.



#### CERT_KEY_CONTEXT_PROP_ID

Data type of <i>pvData</i>: A pointer to a <a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_key_context">CERT_KEY_CONTEXT</a> structure.

The structure specifies the certificate's private key. It contains both the <a href="/windows/desktop/SecCrypto/hcryptprov">HCRYPTPROV</a> and key specification for the private key. For more information about the <b>hCryptProv</b> member and <i>dwFlags</i> settings, see CERT_KEY_PROV_HANDLE_PROP_ID, later in this topic.

<div class="alert"><b>Note</b>  More <a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_key_context">CERT_KEY_CONTEXT</a> structure members can be added for this property. If so, the <b>cbSize</b> member value will be adjusted accordingly. The <b>cbSize</b> member must be set to the size of the <b>CERT_KEY_CONTEXT</b> structure.</div>
<div> </div>


#### CERT_KEY_IDENTIFIER_PROP_ID

Data type of <i>pvData</i>: A pointer to a <a href="/previous-versions/windows/desktop/legacy/aa381414(v=vs.85)">CRYPT_DATA_BLOB</a> structure.

This property is typically implicitly set by a call to 
the <a href="/windows/desktop/api/wincrypt/nf-wincrypt-certgetcertificatecontextproperty">CertGetCertificateContextProperty</a> function.



#### CERT_KEY_PROV_HANDLE_PROP_ID

Data type of <i>pvData</i>:  A  <a href="/windows/desktop/SecCrypto/hcryptprov">HCRYPTPROV</a> value.

The <a href="/windows/desktop/SecCrypto/hcryptprov">HCRYPTPROV</a> handle for the certificate's private key is set. The <b>hCryptProv</b> member of the <a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_key_context">CERT_KEY_CONTEXT</a> structure is updated if it exists. If it does not exist, it is created with <b>dwKeySpec</b> and initialized by CERT_KEY_PROV_INFO_PROP_ID. If CERT_STORE_NO_CRYPT_RELEASE_FLAG is not set, the <b>hCryptProv</b> value is implicitly released either when the property is set to <b>NULL</b> or on the final freeing of the 
<a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_context">CERT_CONTEXT</a> structure.



#### CERT_KEY_PROV_INFO_PROP_ID

Data type of <i>pvData</i>: A pointer to a <a href="/windows/desktop/api/wincrypt/ns-wincrypt-crypt_key_prov_info">CRYPT_KEY_PROV_INFO</a> structure.

The structure specifies the certificate's private key.



#### CERT_KEY_SPEC_PROP_ID

Data type of <i>pvData</i>: A pointer to a <b>DWORD</b> value.

The <b>DWORD</b> value that specifies the private key. The <b>dwKeySpec</b> member of the <a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_key_context">CERT_KEY_CONTEXT</a> structure is updated if it exists. If it does not, it is created with <b>hCryptProv</b> set to zero.



#### CERT_MD5_HASH_PROP_ID

Data type of <i>pvData</i>: A pointer to a <a href="/previous-versions/windows/desktop/legacy/aa381414(v=vs.85)">CRYPT_HASH_BLOB</a> structure.

This property is implicitly set by a call to 
the <a href="/windows/desktop/api/wincrypt/nf-wincrypt-certgetcertificatecontextproperty">CertGetCertificateContextProperty</a> function.



#### CERT_NCRYPT_KEY_HANDLE_PROP_ID

Data type of <i>pvData</i>: A pointer to an <b>NCRYPT_KEY_HANDLE</b> data type.

This property sets the <b>NCRYPT_KEY_HANDLE</b> for the certificate private key and sets the <i>dwKeySpec</i>  to <b>CERT_NCRYPT_KEY_SPEC</b>.



#### CERT_NCRYPT_KEY_HANDLE_TRANSFER_PROP_ID

Sets the handle of the CNG key associated with the certificate.



#### CERT_NEW_KEY_PROP_ID

This identifier is reserved.



#### CERT_NEXT_UPDATE_LOCATION_PROP_ID

Data type of <i>pvData</i>: A pointer to a <a href="/previous-versions/windows/desktop/legacy/aa381414(v=vs.85)">CRYPT_DATA_BLOB</a> structure.

The <a href="/previous-versions/windows/desktop/legacy/aa381414(v=vs.85)">CRYPT_DATA_BLOB</a> structure contains an ASN.1-encoded 
<a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_alt_name_info">CERT_ALT_NAME_INFO</a> structure that is encoded by using the <a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptencodeobject">CryptEncodeObject</a> function with the X509_ALTERNATE_NAME value set.

CERT_NEXT_UPDATE_LOCATION_PROP_ID is currently used only with CTLs.



#### CERT_NO_AUTO_EXPIRE_CHECK_PROP_ID

This identifier is reserved.



#### CERT_OCSP_CACHE_PREFIX_PROP_ID

This identifier is reserved.



#### CERT_OCSP_RESPONSE_PROP_ID

Data type of <i>pvData</i>: A pointer to a <a href="/previous-versions/windows/desktop/legacy/aa381414(v=vs.85)">CRYPT_DATA_BLOB</a> structure.

This property sets the encoded <a href="/windows/win32/api/wincrypt/ns-wincrypt-cert_server_ocsp_response_context">online certificate status protocol</a> (OCSP) response from a <a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_server_ocsp_response_context">CERT_SERVER_OCSP_RESPONSE_CONTEXT</a> for this certificate.



#### CERT_PUB_KEY_CNG_ALG_BIT_LENGTH_PROP_ID

Data type of <i>pvData</i>: Pointer to a  <a href="/previous-versions/windows/desktop/legacy/aa381414(v=vs.85)">CRYPT_DATA_BLOB</a> structure.

This property is implicitly set by calling the <a href="/windows/desktop/api/wincrypt/nf-wincrypt-certgetcertificatecontextproperty">CertGetCertificateContextProperty</a> function.

<b>Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP:  </b>This identifier is not supported.



#### CERT_PUBKEY_ALG_PARA_PROP_ID

Data type of <i>pvData</i>: A pointer to a <a href="/previous-versions/windows/desktop/legacy/aa381414(v=vs.85)">CRYPT_DATA_BLOB</a> structure.

This property is used with public keys that support algorithm parameter inheritance. The data BLOB contains the ASN.1-encoded PublicKey Algorithm parameters. For DSS, these are parameters encoded by using 
the <a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptencodeobject">CryptEncodeObject</a> function. This is used only if CMS_PKCS7 is defined.



#### CERT_PUBKEY_HASH_RESERVED_PROP_ID

This identifier is reserved.



#### CERT_PVK_FILE_PROP_ID

Data type of <i>pvData</i>: A pointer to a <a href="/previous-versions/windows/desktop/legacy/aa381414(v=vs.85)">CRYPT_DATA_BLOB</a> structure.

The <a href="/previous-versions/windows/desktop/legacy/aa381414(v=vs.85)">CRYPT_DATA_BLOB</a> structure specifies the name of a file that contains the private key associated with the certificate's public key. Inside the <b>CRYPT_DATA_BLOB</b> structure, the <b>pbData</b> member is a pointer to a null-terminated Unicode wide-character string, and the <b>cbData</b> member indicates the length of the string.



#### CERT_RENEWAL_PROP_ID

Data type of <i>pvData</i>: A pointer to a <a href="/previous-versions/windows/desktop/legacy/aa381414(v=vs.85)">CRYPT_DATA_BLOB</a> structure.

This property specifies the hash of the renewed certificate.



#### CERT_REQUEST_ORIGINATOR_PROP_ID

Data type of <i>pvData</i>: A pointer to a <a href="/previous-versions/windows/desktop/legacy/aa381414(v=vs.85)">CRYPT_DATA_BLOB</a> structure.

The <a href="/previous-versions/windows/desktop/legacy/aa381414(v=vs.85)">CRYPT_DATA_BLOB</a> structure contains a null-terminated Unicode string that contains the DNS computer name for the origination of the certificate context request.



#### CERT_ROOT_PROGRAM_CERT_POLICIES_PROP_ID

Data type of <i>pvData</i>: A pointer to a <a href="/previous-versions/windows/desktop/legacy/aa381414(v=vs.85)">CRYPT_DATA_BLOB</a> structure.

Returns a pointer to an encoded <a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_policies_info">CERT_POLICIES_INFO</a> structure that contains the application policies of the root certificate for the context. This property can be decoded by using the <a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptdecodeobject">CryptDecodeObject</a> function with the <i>lpszStructType</i> parameter set to <b>X509_CERT_POLICIES</b> and the <i>dwCertEncodingType</i> parameter set to a combination of <b>X509_ASN_ENCODING</b> bitwise <b>OR</b> <b>PKCS_7_ASN_ENCODING</b>.



#### CERT_ROOT_PROGRAM_NAME_CONSTRAINTS_PROP_ID

This identifier is reserved.



#### CERT_SIGN_HASH_CNG_ALG_PROP_ID

Data type of <i>pvData</i>: Pointer to a <a href="/previous-versions/windows/desktop/legacy/aa381414(v=vs.85)">CRYPT_DATA_BLOB</a> structure.

This property is implicitly set by calling the <a href="/windows/desktop/api/wincrypt/nf-wincrypt-certgetcertificatecontextproperty">CertGetCertificateContextProperty</a> function.

<b>Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP:  </b>This identifier is not supported.



#### CERT_SHA1_HASH_PROP_ID

Data type of <i>pvData</i>: A pointer to a <a href="/previous-versions/windows/desktop/legacy/aa381414(v=vs.85)">CRYPT_HASH_BLOB</a> structure.

This property is implicitly set by a call to 
the <a href="/windows/desktop/api/wincrypt/nf-wincrypt-certgetcertificatecontextproperty">CertGetCertificateContextProperty</a> function.



#### CERT_SIGNATURE_HASH_PROP_ID

Data type of <i>pvData</i>: A pointer to a <a href="/previous-versions/windows/desktop/legacy/aa381414(v=vs.85)">CRYPT_HASH_BLOB</a> structure.

If a signature hash does not exist, it is computed by using the <a href="/windows/desktop/api/wincrypt/nf-wincrypt-crypthashtobesigned">CryptHashToBeSigned</a> function. <i>pvData</i> points to an existing or computed hash. Usually, the length of the hash is 20 bytes for SHA and 16 for MD5.



#### CERT_SMART_CARD_DATA_PROP_ID

Data type of <i>pvData</i>: A pointer to a <a href="/previous-versions/windows/desktop/legacy/aa381414(v=vs.85)">CRYPT_DATA_BLOB</a> structure.

This property sets the smart card data property of a smart card certificate context.



#### CERT_SMART_CARD_ROOT_INFO_PROP_ID

Data type of <i>pvData</i>: A pointer to a <a href="/previous-versions/windows/desktop/legacy/aa381414(v=vs.85)">CRYPT_DATA_BLOB</a> structure.

This property sets the information property  of a smart card root certificate context.



#### CERT_SOURCE_LOCATION_PROP_ID

This identifier is reserved.



#### CERT_SOURCE_URL_PROP_ID

This identifier is reserved.



#### CERT_SUBJECT_DISABLE_CRL_PROP_ID

This identifier is reserved.



#### CERT_SUBJECT_INFO_ACCESS_PROP_ID

Data type of <i>pvData</i>: A pointer to a <a href="/previous-versions/windows/desktop/legacy/aa381414(v=vs.85)">CRYPT_DATA_BLOB</a> structure.

This property sets the subject information access extension of the certificate context as an encoded <a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_authority_info_access">CERT_SUBJECT_INFO_ACCESS</a> structure.



#### CERT_SUBJECT_NAME_MD5_HASH_PROP_ID

Data type of <i>pvData</i>: A pointer to a <a href="/previous-versions/windows/desktop/legacy/aa381414(v=vs.85)">CRYPT_DATA_BLOB</a> structure.

Returns an MD5 hash of the encoded subject name of the certificate context. 



#### CERT_SUBJECT_OCSP_AUTHORITY_INFO_ACCESS_PROP_ID

This identifier is reserved.



#### CERT_SUBJECT_PUB_KEY_BIT_LENGTH_PROP_ID

Data type of <i>pvData</i>: Pointer to a <a href="/previous-versions/windows/desktop/legacy/aa381414(v=vs.85)">CRYPT_DATA_BLOB</a> structure.

This property is implicitly set by calling the <a href="/windows/desktop/api/wincrypt/nf-wincrypt-certgetcertificatecontextproperty">CertGetCertificateContextProperty</a> function.

<b>Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP:  </b>This identifier is not supported.



#### CERT_SUBJECT_PUBLIC_KEY_MD5_HASH_PROP_ID

Data type of <i>pvData</i>: A pointer to a <a href="/previous-versions/windows/desktop/legacy/aa381414(v=vs.85)">CRYPT_DATA_BLOB</a> structure.

This property sets the MD5 hash of this certificate's public key.

<i>pvData</i> is a pointer to a <a href="/previous-versions/windows/desktop/legacy/aa381414(v=vs.85)">CRYPT_DATA_BLOB</a> structure.

The user can define additional <i>dwPropId</i> types by using <b>DWORD</b> values from <b>CERT_FIRST_USER_PROP_ID</b> to <b>CERT_LAST_USER_PROP_ID</b>. For all user-defined <i>dwPropId</i> types, <i>pvData</i> points to an encoded <a href="/previous-versions/windows/desktop/legacy/aa381414(v=vs.85)">CRYPT_DATA_BLOB</a> structure.

### -param dwFlags [in]

CERT_STORE_NO_CRYPT_RELEASE_FLAG can be set for the CERT_KEY_PROV_HANDLE_PROP_ID or CERT_KEY_CONTEXT_PROP_ID <i>dwPropId</i> properties.

If the CERT_SET_PROPERTY_IGNORE_PERSIST_ERROR_FLAG value is set, any provider-write errors are ignored and the cached context's properties are always set.

If CERT_SET_PROPERTY_INHIBIT_PERSIST_FLAG is set, any context property set is not persisted.

### -param pvData [in]

A pointer to a data type determined by the value of <i>dwPropId</i>.

<div class="alert"><b>Note</b>  For any <i>dwPropId</i>, setting <i>pvData</i> to <b>NULL</b> deletes the property.</div>
<div> </div>

## -returns

If the function succeeds, the function returns <b>TRUE</b>.

If the function fails, the function returns <b>FALSE</b>. For extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>. One possible error code is the following.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The property is not valid. The identifier specified was greater than 0x0000FFFF, or, for the CERT_KEY_CONTEXT_PROP_ID property, a <b>cbSize</b> member that is not valid was specified in the <a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_key_context">CERT_KEY_CONTEXT</a> structure.

</td>
</tr>
</table>

## -remarks

If a property already exists, its old value is replaced.

<h3><a id="dwpropid_macro"></a><a id="DWPROPID_MACRO"></a></h3>
Your code can use a macro to evaluate the class of hash for a certificate context. The Wincrypt.h header  defines the following macros for this purpose. These macros are used internally by the <b>CertSetCertificateContextProperty</b> function.

<b>IS_CERT_HASH_PROP_ID(X)</b>
<b>IS_PUBKEY_HASH_PROP_ID(X)</b>
<b>IS_CHAIN_HASH_PROP_ID(X)</b>
Each macro takes the <i>dwPropId</i> (X) value as input and evaluates to a Boolean value. The following table  shows the <i>dwPropId</i> values that evaluate to <b>TRUE</b> for each macro.

<table>
<tr>
<th>Macro</th>
<th>Evaluates to <b>TRUE</b> if <i>dwPropId</i> is</th>
</tr>
<tr>
<td>
<b>IS_CERT_HASH_PROP_ID</b>(<i>dwPropId</i>)

</td>
<td>

<dl>
<dd><b>CERT_SHA1_HASH_PROP_ID</b>,</dd>
<dd><b>CERT_MD5_HASH_PROP_ID</b>, or</dd>
<dd><b>CERT_SIGNATURE_HASH_PROP_ID</b></dd>
</dl>


</td>
</tr>
<tr>
<td>
<b>IS_PUBKEY_HASH_PROP_ID</b>(<i>dwPropId</i>)

</td>
<td>

<dl>
<dd><b>CERT_ISSUER_PUBLIC_KEY_MD5_HASH_PROP_ID</b> or</dd>
<dd><b>CERT_SUBJECT_PUBLIC_KEY_MD5_HASH_PROP_ID</b></dd>
</dl>


</td>
</tr>
<tr>
<td>
<b>IS_CHAIN_HASH_PROP_ID</b>(<i>dwPropId</i>)

</td>
<td>

<dl>
<dd><b>CERT_ISSUER_PUBLIC_KEY_MD5_HASH_PROP_ID</b>,</dd>
<dd><b>CERT_SUBJECT_PUBLIC_KEY_MD5_HASH_PROP_ID</b>,</dd>
<dd><b>CERT_ISSUER_SERIAL_NUMBER_MD5_HASH_PROP_ID</b>, or</dd>
<dd><b>CERT_SUBJECT_NAME_MD5_HASH_PROP_ID</b></dd>
</dl>


</td>
</tr>
</table>
 

The <b>IS_STRONG_SIGN_PROP_ID(x)</b> macro evaluates to <b>TRUE</b> if the <b>CERT_SIGN_HASH_CNG_ALG_PROP_ID</b>,
<b>CERT_SUBJECT_PUB_KEY_BIT_LENGTH_PROP_ID</b>, or <b>CERT_PUB_KEY_CNG_ALG_BIT_LENGTH_PROP_ID</b> properties are set
in the <i>dwPropId</i> parameter.


#### Examples

For an example that uses this function, see 
<a href="/windows/desktop/SecCrypto/example-c-program-getting-and-setting-certificate-properties">Example C Program: Getting and Setting Certificate Properties</a>.

<div class="code"></div>

## -see-also

<a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_alt_name_info">CERT_ALT_NAME_INFO</a>



<a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_context">CERT_CONTEXT</a>



<a href="/windows/desktop/api/wincrypt/ns-wincrypt-ctl_usage">CERT_ENHKEY_USAGE</a>



<a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_key_context">CERT_KEY_CONTEXT</a>



<a href="/windows/desktop/api/wincrypt/ns-wincrypt-cross_cert_dist_points_info">CROSS_CERT_DIST_POINTS_INFO</a>



<a href="/previous-versions/windows/desktop/legacy/aa381414(v=vs.85)">CRYPT_DATA_BLOB</a>



<a href="/previous-versions/windows/desktop/legacy/aa381414(v=vs.85)">CRYPT_HASH_BLOB</a>



<a href="/windows/desktop/api/wincrypt/ns-wincrypt-crypt_key_prov_info">CRYPT_KEY_PROV_INFO</a>



<a href="/windows/desktop/api/wincrypt/ns-wincrypt-ctl_usage">CTL_USAGE</a>



<a href="/windows/desktop/api/wincrypt/nf-wincrypt-certgetcertificatecontextproperty">CertGetCertificateContextProperty</a>



<a href="/windows/desktop/api/wincrypt/nf-wincrypt-certsetcrlcontextproperty">CertSetCRLContextProperty</a>



<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptencodeobject">CryptEncodeObject</a>



<a href="/windows/desktop/api/wincrypt/nf-wincrypt-crypthashtobesigned">CryptHashToBeSigned</a>



<a href="/windows/desktop/SecCrypto/cryptography-functions">Extended Property Functions</a>