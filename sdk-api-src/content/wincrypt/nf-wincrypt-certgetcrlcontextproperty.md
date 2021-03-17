---
UID: NF:wincrypt.CertGetCRLContextProperty
title: CertGetCRLContextProperty function (wincrypt.h)
description: Gets an extended property for the specified certificate revocation list (CRL) context.
helpviewer_keywords: ["CERT_ACCESS_STATE_PROP_ID","CERT_ARCHIVED_PROP_ID","CERT_AUTO_ENROLL_PROP_ID","CERT_CTL_USAGE_PROP_ID","CERT_DESCRIPTION_PROP_ID","CERT_ENHKEY_USAGE_PROP_ID","CERT_FRIENDLY_NAME_PROP_ID","CERT_ISSUER_CHAIN_PUB_KEY_CNG_ALG_BIT_LENGTH_PROP_ID","CERT_ISSUER_CHAIN_SIGN_HASH_CNG_ALG_PROP_ID","CERT_ISSUER_PUB_KEY_BIT_LENGTH_PROP_ID","CERT_KEY_CONTEXT_PROP_ID","CERT_KEY_IDENTIFIER_PROP_ID","CERT_KEY_PROV_HANDLE_PROP_ID","CERT_KEY_PROV_INFO_PROP_ID","CERT_KEY_SPEC_PROP_ID","CERT_MD5_HASH_PROP_ID","CERT_NEXT_UPDATE_LOCATION_PROP_ID","CERT_PVK_FILE_PROP_ID","CERT_SHA1_HASH_PROP_ID","CERT_SIGNATURE_HASH_PROP_ID","CERT_SIGN_HASH_CNG_ALG_PROP_ID","CertGetCRLContextProperty","CertGetCRLContextProperty function [Security]","_crypto2_certgetcrlcontextproperty","security.certgetcrlcontextproperty","wincrypt/CertGetCRLContextProperty"]
old-location: security\certgetcrlcontextproperty.htm
tech.root: security
ms.assetid: 16c2cc06-28fd-42d9-a377-0df2eaeeae56
ms.date: 12/05/2018
ms.keywords: CERT_ACCESS_STATE_PROP_ID, CERT_ARCHIVED_PROP_ID, CERT_AUTO_ENROLL_PROP_ID, CERT_CTL_USAGE_PROP_ID, CERT_DESCRIPTION_PROP_ID, CERT_ENHKEY_USAGE_PROP_ID, CERT_FRIENDLY_NAME_PROP_ID, CERT_ISSUER_CHAIN_PUB_KEY_CNG_ALG_BIT_LENGTH_PROP_ID, CERT_ISSUER_CHAIN_SIGN_HASH_CNG_ALG_PROP_ID, CERT_ISSUER_PUB_KEY_BIT_LENGTH_PROP_ID, CERT_KEY_CONTEXT_PROP_ID, CERT_KEY_IDENTIFIER_PROP_ID, CERT_KEY_PROV_HANDLE_PROP_ID, CERT_KEY_PROV_INFO_PROP_ID, CERT_KEY_SPEC_PROP_ID, CERT_MD5_HASH_PROP_ID, CERT_NEXT_UPDATE_LOCATION_PROP_ID, CERT_PVK_FILE_PROP_ID, CERT_SHA1_HASH_PROP_ID, CERT_SIGNATURE_HASH_PROP_ID, CERT_SIGN_HASH_CNG_ALG_PROP_ID, CertGetCRLContextProperty, CertGetCRLContextProperty function [Security], _crypto2_certgetcrlcontextproperty, security.certgetcrlcontextproperty, wincrypt/CertGetCRLContextProperty
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
 - CertGetCRLContextProperty
 - wincrypt/CertGetCRLContextProperty
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
 - CertGetCRLContextProperty
---

# CertGetCRLContextProperty function


## -description

The <b>CertGetCRLContextProperty</b> function gets an extended property for the specified <a href="/windows/desktop/SecGloss/c-gly">certificate revocation list</a> (CRL) context.

## -parameters

### -param pCrlContext [in]

A pointer to the 
<a href="/windows/desktop/api/wincrypt/ns-wincrypt-crl_context">CRL_CONTEXT</a> structure.

### -param dwPropId [in]

Identifies the property to be retrieved. Currently defined identifiers and the data type to be returned in <i>pvData</i> are listed in the following table. 




						
					

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="CERT_ACCESS_STATE_PROP_ID"></a><a id="cert_access_state_prop_id"></a><dl>
<dt><b>CERT_ACCESS_STATE_PROP_ID</b></dt>
</dl>
</td>
<td width="60%">
Data type for <i>pvData</i>: pointer to a <b>DWORD</b>

Returns a <b>DWORD</b> value indicating whether write operations to the certificate are persisted. The <b>DWORD</b> value is not set if the certificate is in a memory store or in a registry-based store that is opened as read-only.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_ARCHIVED_PROP_ID"></a><a id="cert_archived_prop_id"></a><dl>
<dt><b>CERT_ARCHIVED_PROP_ID</b></dt>
</dl>
</td>
<td width="60%">
Data type for <i>pvData</i>: <b>NULL</b>

Indicates the certificate is skipped during enumerations. A certificate with this property set is found with explicit search operations, such as those used to find a certificate with a specific hash or a serial number. No data in <i>pvData</i> is associated with this property.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_AUTO_ENROLL_PROP_ID"></a><a id="cert_auto_enroll_prop_id"></a><dl>
<dt><b>CERT_AUTO_ENROLL_PROP_ID</b></dt>
</dl>
</td>
<td width="60%">
Data type for <i>pvData</i>: pointer to a <b>BYTE</b> array

Returns a <b>null</b>-terminated Unicode string naming the certificate type for which the certificate has been auto enrolled.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_CTL_USAGE_PROP_ID"></a><a id="cert_ctl_usage_prop_id"></a><dl>
<dt><b>CERT_CTL_USAGE_PROP_ID</b></dt>
</dl>
</td>
<td width="60%">
Data type for <i>pvData</i>: pointer to a <b>BYTE</b> array

Returns an array of bytes containing an <a href="/windows/desktop/SecGloss/a-gly">Abstract Syntax Notation One</a> (ASN.1) encoded <a href="/windows/desktop/api/wincrypt/ns-wincrypt-ctl_usage">CTL_USAGE</a> structure.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_DESCRIPTION_PROP_ID"></a><a id="cert_description_prop_id"></a><dl>
<dt><b>CERT_DESCRIPTION_PROP_ID</b></dt>
</dl>
</td>
<td width="60%">
Data type for <i>pvData</i>: pointer to a <b>BYTE</b> array

Returns the property displayed by the certificate UI. This property allows the user to describe the certificate's use.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_ENHKEY_USAGE_PROP_ID"></a><a id="cert_enhkey_usage_prop_id"></a><dl>
<dt><b>CERT_ENHKEY_USAGE_PROP_ID</b></dt>
</dl>
</td>
<td width="60%">
Data type for <i>pvData</i>: 

Returns an array of bytes containing an ASN.1 encoded <a href="/windows/desktop/api/wincrypt/ns-wincrypt-ctl_usage">CERT_ENHKEY_USAGE</a> structure.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_FRIENDLY_NAME_PROP_ID"></a><a id="cert_friendly_name_prop_id"></a><dl>
<dt><b>CERT_FRIENDLY_NAME_PROP_ID</b></dt>
</dl>
</td>
<td width="60%">
Data type for <i>pvData</i>: pointer to a <b>BYTE</b> array

Returns a <b>null</b>-terminated Unicode character string that contains the display name for the CRL.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_ISSUER_CHAIN_PUB_KEY_CNG_ALG_BIT_LENGTH_PROP_ID"></a><a id="cert_issuer_chain_pub_key_cng_alg_bit_length_prop_id"></a><dl>
<dt><b>CERT_ISSUER_CHAIN_PUB_KEY_CNG_ALG_BIT_LENGTH_PROP_ID</b></dt>
</dl>
</td>
<td width="60%">
Data type for <i>pvData</i>: Pointer to a null-terminated Unicode string.

Returns a string containing a set of L"<i>&lt;PUBKEY&gt;</i>/<i>&lt;BITLENGTH&gt;</i>" public key algorithm and bit length pairs. The semicolon, L";", is used as the delimiter.

The <i>&lt;PUBKEY&gt;</i> value identifies the CNG public key algorithm. The following algorithms are supported:

<ul>
<li>L"RSA" (BCRYPT_RSA_ALGORITHM)</li>
<li>L"DSA" (BCRYPT_DSA_ALGORITHM)</li>
<li>L"ECDSA" (SSL_ECDSA_ALGORITHM)</li>
</ul>
An <i>&lt;PUBKEY&gt;</i>/<i>&lt;BITLENGTH&gt;</i> pair is returned for each certificate in the CRL issuer chain excluding the leaf. This property is only set when an OCSP response with an independent signer chain is converted to a CRL.

<div class="alert"><b>Note</b>  This property cannot be retrieved for a delegated OCSP signer certificate. A delegated signer certificate is signed with the same key used to sign the subject certificate and is checked there.</div>
<div> </div>
The following is an example:

: L"RSA/2048;RSA/4096"

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_ISSUER_CHAIN_SIGN_HASH_CNG_ALG_PROP_ID"></a><a id="cert_issuer_chain_sign_hash_cng_alg_prop_id"></a><dl>
<dt><b>CERT_ISSUER_CHAIN_SIGN_HASH_CNG_ALG_PROP_ID</b></dt>
</dl>
</td>
<td width="60%">
Data type for <i>pvData</i>: Pointer to a null-terminated Unicode string.

Returns a string that contains a set of L"<i>&lt;SIGNATURE&gt;</i>/<i>&lt;HASH&gt;</i>" algorithm pairs. The semicolon, L";", is used as the delimiter between pairs.

This property is set only when an OCSP response is converted to a CRL. For a delegated OCSP signer certificate, only the algorithm pair for the signer certificate is returned. For an independent OCSP signer certificate chain, an algorithm pair is returned for each certificate in the chain excluding the root.

The <i>&lt;SIGNATURE&gt;</i> value identifies the CNG public key algorithm. The following algorithms are supported:

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
The following shows an  example:

<ul>
<li>L"RSA/SHA256;RSA/SHA256"</li>
</ul>
</td>
</tr>
<tr>
<td width="40%"><a id="CERT_ISSUER_PUB_KEY_BIT_LENGTH_PROP_ID"></a><a id="cert_issuer_pub_key_bit_length_prop_id"></a><dl>
<dt><b>CERT_ISSUER_PUB_KEY_BIT_LENGTH_PROP_ID</b></dt>
</dl>
</td>
<td width="60%">
Data type for <i>pvData</i>: Pointer to a <b>DWORD</b> value.

Returns the length, in bits, of the public key in the CRL issuer certificate. This property is also applicable to an OCSP response that has been converted to a CRL.

<b>Windows 8 and Windows Server 2012:  </b>Support for this property begins.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_KEY_CONTEXT_PROP_ID"></a><a id="cert_key_context_prop_id"></a><dl>
<dt><b>CERT_KEY_CONTEXT_PROP_ID</b></dt>
</dl>
</td>
<td width="60%">
Data type for <i>pvData</i>: pointer to a <a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_key_context">CERT_KEY_CONTEXT</a>


Returns a 
<a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_key_context">CERT_KEY_CONTEXT</a> structure.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_KEY_IDENTIFIER_PROP_ID"></a><a id="cert_key_identifier_prop_id"></a><dl>
<dt><b>CERT_KEY_IDENTIFIER_PROP_ID</b></dt>
</dl>
</td>
<td width="60%">
Data type for <i>pvData</i>: pointer to a <b>BYTE</b> array

If nonexistent, searches for the szOID_SUBJECT_KEY_IDENTIFIER extension. If that fails, a SHA1 hash is done on the certificate's <b>SubjectPublicKeyInfo</b> member to produce the identifier values.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_KEY_PROV_HANDLE_PROP_ID"></a><a id="cert_key_prov_handle_prop_id"></a><dl>
<dt><b>CERT_KEY_PROV_HANDLE_PROP_ID</b></dt>
</dl>
</td>
<td width="60%">
Data type for <i>pvData</i>:  pointer to an <a href="/windows/desktop/SecCrypto/hcryptprov">HCRYPTPROV</a>


Returns the provider handle obtained from the CERT_KEY_CONTEXT_PROP_ID.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_KEY_PROV_INFO_PROP_ID"></a><a id="cert_key_prov_info_prop_id"></a><dl>
<dt><b>CERT_KEY_PROV_INFO_PROP_ID</b></dt>
</dl>
</td>
<td width="60%">
Data type for <i>pvData</i>:  pointer to a <a href="/windows/desktop/api/wincrypt/ns-wincrypt-crypt_key_prov_info">CRYPT_KEY_PROV_INFO</a>


Returns a pointer to a <a href="/windows/desktop/api/wincrypt/ns-wincrypt-crypt_key_prov_info">CRYPT_KEY_PROV_INFO</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_KEY_SPEC_PROP_ID"></a><a id="cert_key_spec_prop_id"></a><dl>
<dt><b>CERT_KEY_SPEC_PROP_ID</b></dt>
</dl>
</td>
<td width="60%">
Data type for <i>pvData</i>: pointer to a <b>DWORD</b>

Returns a <b>DWORD</b> value specifying the private key obtained from CERT_KEY_CONTEXT_PROP_ID property if it exists. Otherwise, if CERT_KEY_PROV_INFO_PROP_ID exists, it is the source of the <i>dwKeySpec</i>.
							

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_MD5_HASH_PROP_ID"></a><a id="cert_md5_hash_prop_id"></a><dl>
<dt><b>CERT_MD5_HASH_PROP_ID</b></dt>
</dl>
</td>
<td width="60%">
Data type for <i>pvData</i>: pointer to a <b>BYTE</b> array

Returns the MD5 hash. If the hash does not exist, it is computed using 
<a href="/windows/desktop/api/wincrypt/nf-wincrypt-crypthashcertificate">CryptHashCertificate</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_NEXT_UPDATE_LOCATION_PROP_ID"></a><a id="cert_next_update_location_prop_id"></a><dl>
<dt><b>CERT_NEXT_UPDATE_LOCATION_PROP_ID</b></dt>
</dl>
</td>
<td width="60%">
Data type for <i>pvData</i>: pointer to a <b>BYTE</b> array

Returns the ASN.1 encoded 
<a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_alt_name_info">CERT_ALT_NAME_INFO</a> structure. 




CERT_NEXT_UPDATE_LOCATION_PROP_ID is currently used only with CTLs.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_PVK_FILE_PROP_ID"></a><a id="cert_pvk_file_prop_id"></a><dl>
<dt><b>CERT_PVK_FILE_PROP_ID</b></dt>
</dl>
</td>
<td width="60%">
Data type for <i>pvData</i>: pointer to a <b>BYTE</b> array

Returns a <b>null</b>-terminated Unicode, wide character string specifying the file name containing the private key associated with the certificate's public key.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_SHA1_HASH_PROP_ID"></a><a id="cert_sha1_hash_prop_id"></a><dl>
<dt><b>CERT_SHA1_HASH_PROP_ID</b></dt>
</dl>
</td>
<td width="60%">
Data type for <i>pvData</i>: pointer to a <b>BYTE</b> array

Returns the SHA1 hash. If the hash does not exist, it is computed using 
<a href="/windows/desktop/api/wincrypt/nf-wincrypt-crypthashcertificate">CryptHashCertificate</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_SIGN_HASH_CNG_ALG_PROP_ID"></a><a id="cert_sign_hash_cng_alg_prop_id"></a><dl>
<dt><b>CERT_SIGN_HASH_CNG_ALG_PROP_ID</b></dt>
</dl>
</td>
<td width="60%">
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
<li>L”RSA/SHA1”</li>
<li>L”RSA/SHA256”</li>
<li>L”ECDSA/SHA256” </li>
</ul>
This property is also applicable to an OCSP response that has been converted to a CRL.

<b>Windows 8 and Windows Server 2012:  </b>Support for this property begins.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_SIGNATURE_HASH_PROP_ID"></a><a id="cert_signature_hash_prop_id"></a><dl>
<dt><b>CERT_SIGNATURE_HASH_PROP_ID</b></dt>
</dl>
</td>
<td width="60%">
Data type for <i>pvData</i>: pointer to a <b>BYTE</b> array

Returns the signature hash. If the hash does not exist, it is computed with 
<a href="/windows/desktop/api/wincrypt/nf-wincrypt-crypthashtobesigned">CryptHashToBeSigned</a>. The length of the hash is 20 bytes for SHA and 16 for MD5.

</td>
</tr>
</table>
 

For many property identifiers, <i>pvData</i> points to an array of bytes and not a <a href="/previous-versions/windows/desktop/legacy/aa381414(v=vs.85)">CRYPT_DATA_BLOB</a> as pointed to by the <i>pvData</i> parameter in <a href="/windows/desktop/api/wincrypt/nf-wincrypt-certsetcrlcontextproperty">CertSetCRLContextProperty</a>.

For more information about each property identifier, see the documentation on the <i>dwPropId</i> parameter in 
<a href="/windows/desktop/api/wincrypt/nf-wincrypt-certsetcertificatecontextproperty">CertSetCertificateContextProperty</a>.

### -param pvData [out]

A pointer to a buffer to receive the data as determined by <i>dwPropId</i>. Structures pointed to by members of a structure returned are also returned following the base structure. Therefore, the size contained in <i>pcbData</i> often exceed the size of the base structure. 




This parameter can be <b>NULL</b> to set the size of the information for memory allocation purposes. For more information, see 
<a href="/windows/desktop/SecCrypto/retrieving-data-of-unknown-length">Retrieving Data of Unknown Length</a>.

### -param pcbData [in, out]

A pointer to a <b>DWORD</b> value specifying the size, in bytes, of the buffer pointed to by the <i>pvData</i> parameter. When the function returns, the <b>DWORD</b> value contains the number of bytes to be stored in the buffer. 




<div class="alert"><b>Note</b>  When processing the data returned in the buffer, applications must use the actual size of the data returned. The actual size can be slightly smaller than the size of the buffer specified on input. (On input, buffer sizes are usually specified large enough to ensure that the largest possible output data fits in the buffer.) On output, the variable pointed to by this parameter is updated to reflect the actual size of the data copied to the buffer.</div>
<div> </div>

## -returns

If the function succeeds, the return value is <b>TRUE</b>.

If the function fails, the return value is <b>FALSE</b>. 

Note that errors from the called function 
<a href="/windows/desktop/api/wincrypt/nf-wincrypt-crypthashcertificate">CryptHashCertificate</a> can be propagated to this function. For extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>. Some possible error codes follow.

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
The CRL does not have the specified property.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_MORE_DATA</b></dt>
</dl>
</td>
<td width="60%">
If the buffer specified by the <i>pvData</i> parameter is not large enough to hold the returned data, the function sets the ERROR_MORE_DATA code and stores the required buffer size, in bytes, in the variable pointed to by <i>pcbData</i>.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/wincrypt/nf-wincrypt-certenumcrlcontextproperties">CertEnumCRLContextProperties</a>



<a href="/windows/desktop/api/wincrypt/nf-wincrypt-certgetcertificatecontextproperty">CertGetCertificateContextProperty</a>



<a href="/windows/desktop/api/wincrypt/nf-wincrypt-crypthashcertificate">CryptHashCertificate</a>



<a href="/windows/desktop/SecCrypto/cryptography-functions">Extended Property Functions</a>