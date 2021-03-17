---
UID: NF:wincrypt.CertSetCRLContextProperty
title: CertSetCRLContextProperty function (wincrypt.h)
description: Sets an extended property for the specified certificate revocation list (CRL) context.
helpviewer_keywords: ["CERT_ACCESS_STATE_PROP_ID","CERT_ARCHIVED_PROP_ID","CERT_AUTO_ENROLL_PROP_ID","CERT_CTL_USAGE_PROP_ID","CERT_DESCRIPTION_PROP_ID","CERT_ENHKEY_USAGE_PROP_ID","CERT_FRIENDLY_NAME_PROP_ID","CERT_ISSUER_CHAIN_PUB_KEY_CNG_ALG_BIT_LENGTH_PROP_ID","CERT_ISSUER_CHAIN_SIGN_HASH_CNG_ALG_PROP_ID","CERT_ISSUER_PUB_KEY_BIT_LENGTH_PROP_ID","CERT_KEY_CONTEXT_PROP_ID","CERT_KEY_IDENTIFIER_PROP_ID","CERT_KEY_PROV_HANDLE_PROP_ID","CERT_KEY_PROV_INFO_PROP_ID","CERT_KEY_SPEC_PROP_ID","CERT_MD5_HASH_PROP_ID","CERT_NEXT_UPDATE_LOCATION_PROP_ID","CERT_PVK_FILE_PROP_ID","CERT_SHA1_HASH_PROP_ID","CERT_SIGNATURE_HASH_PROP_ID","CERT_SIGN_HASH_CNG_ALG_PROP_ID","CertSetCRLContextProperty","CertSetCRLContextProperty function [Security]","_crypto2_certsetcrlcontextproperty","security.certsetcrlcontextproperty","wincrypt/CertSetCRLContextProperty"]
old-location: security\certsetcrlcontextproperty.htm
tech.root: security
ms.assetid: 7e4a0a39-ce55-4171-9b66-31c1c28d895f
ms.date: 12/05/2018
ms.keywords: CERT_ACCESS_STATE_PROP_ID, CERT_ARCHIVED_PROP_ID, CERT_AUTO_ENROLL_PROP_ID, CERT_CTL_USAGE_PROP_ID, CERT_DESCRIPTION_PROP_ID, CERT_ENHKEY_USAGE_PROP_ID, CERT_FRIENDLY_NAME_PROP_ID, CERT_ISSUER_CHAIN_PUB_KEY_CNG_ALG_BIT_LENGTH_PROP_ID, CERT_ISSUER_CHAIN_SIGN_HASH_CNG_ALG_PROP_ID, CERT_ISSUER_PUB_KEY_BIT_LENGTH_PROP_ID, CERT_KEY_CONTEXT_PROP_ID, CERT_KEY_IDENTIFIER_PROP_ID, CERT_KEY_PROV_HANDLE_PROP_ID, CERT_KEY_PROV_INFO_PROP_ID, CERT_KEY_SPEC_PROP_ID, CERT_MD5_HASH_PROP_ID, CERT_NEXT_UPDATE_LOCATION_PROP_ID, CERT_PVK_FILE_PROP_ID, CERT_SHA1_HASH_PROP_ID, CERT_SIGNATURE_HASH_PROP_ID, CERT_SIGN_HASH_CNG_ALG_PROP_ID, CertSetCRLContextProperty, CertSetCRLContextProperty function [Security], _crypto2_certsetcrlcontextproperty, security.certsetcrlcontextproperty, wincrypt/CertSetCRLContextProperty
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
 - CertSetCRLContextProperty
 - wincrypt/CertSetCRLContextProperty
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
 - CertSetCRLContextProperty
---

# CertSetCRLContextProperty function


## -description

The <b>CertSetCRLContextProperty</b> function sets an extended property for the specified <a href="/windows/desktop/SecGloss/c-gly">certificate revocation list</a> (CRL) context.

## -parameters

### -param pCrlContext [in]

A pointer to the 
<a href="/windows/desktop/api/wincrypt/ns-wincrypt-crl_context">CRL_CONTEXT</a> structure.

### -param dwPropId [in]

Identifies the property to be set. The value of <i>dwPropId</i> determines the type and content of the <i>pvData</i> parameter. Currently defined identifiers and the data type to be returned in <i>pvData</i> are listed in the following table.

Usually, only the following properties are set:<ul>
<li>CERT_HASH_PROP_ID</li>
<li>CERT_SHA1_HASH_PROP_ID</li>
<li>CERT_MD5_HASH_PROP_ID</li>
<li>CERT_SIGNATURE_HASH_PROP_ID</li>
</ul>


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

Sets a <b>DWORD</b> value indicating whether write operations to the certificate are persisted. The <b>DWORD</b> value is not set if the certificate is in a memory store or in a registry-based store that is opened as read-only.

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

Sets a <b>null</b>-terminated Unicode string naming the certificate type for which the certificate has been auto enrolled.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_CTL_USAGE_PROP_ID"></a><a id="cert_ctl_usage_prop_id"></a><dl>
<dt><b>CERT_CTL_USAGE_PROP_ID</b></dt>
</dl>
</td>
<td width="60%">
Data type for <i>pvData</i>: pointer to a <b>BYTE</b> array

Sets an array of bytes containing an <a href="/windows/desktop/SecGloss/a-gly">Abstract Syntax Notation One</a> (ASN.1) encoded <a href="/windows/desktop/api/wincrypt/ns-wincrypt-ctl_usage">CTL_USAGE</a> structure.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_DESCRIPTION_PROP_ID"></a><a id="cert_description_prop_id"></a><dl>
<dt><b>CERT_DESCRIPTION_PROP_ID</b></dt>
</dl>
</td>
<td width="60%">
Data type for <i>pvData</i>: pointer to a <b>BYTE</b> array

Sets the property displayed by the certificate UI. This property allows the user to describe the certificate's use.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_ENHKEY_USAGE_PROP_ID"></a><a id="cert_enhkey_usage_prop_id"></a><dl>
<dt><b>CERT_ENHKEY_USAGE_PROP_ID</b></dt>
</dl>
</td>
<td width="60%">
Data type for <i>pvData</i>: 

Sets an array of bytes containing an ASN.1 encoded <a href="/windows/desktop/api/wincrypt/ns-wincrypt-ctl_usage">CERT_ENHKEY_USAGE</a> structure.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_FRIENDLY_NAME_PROP_ID"></a><a id="cert_friendly_name_prop_id"></a><dl>
<dt><b>CERT_FRIENDLY_NAME_PROP_ID</b></dt>
</dl>
</td>
<td width="60%">
Data type for <i>pvData</i>: pointer to a <b>BYTE</b> array

Sets a <b>null</b>-terminated Unicode character string that contains the display name for the CRL.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_ISSUER_CHAIN_PUB_KEY_CNG_ALG_BIT_LENGTH_PROP_ID"></a><a id="cert_issuer_chain_pub_key_cng_alg_bit_length_prop_id"></a><dl>
<dt><b>CERT_ISSUER_CHAIN_PUB_KEY_CNG_ALG_BIT_LENGTH_PROP_ID</b></dt>
</dl>
</td>
<td width="60%">
Data type for <i>pvData</i>: Pointer to a <a href="/windows/win32/api/dpapi/ns-dpapi-crypt_integer_blob">CRYPT_DATA_BLOB</a> structure.



Sets a string containing a set of L"<i>&lt;PUBKEY&gt;</i>/<i>&lt;BITLENGTH&gt;</i>" public key algorithm and bit length pairs. The semicolon, L";", is used as the delimiter.

The <i>&lt;PUBKEY&gt;</i> value identifies the CNG public key algorithm. The following algorithms are supported:

<ul>
<li>L"RSA" (BCRYPT_RSA_ALGORITHM)</li>
<li>L"DSA" (BCRYPT_DSA_ALGORITHM)</li>
<li>L"ECDSA" (SSL_ECDSA_ALGORITHM)</li>
</ul>
A <i>&lt;PUBKEY&gt;</i>/<i>&lt;BITLENGTH&gt;</i> pair is set for each certificate in the CRL issuer chain excluding the leaf. This property can be set when an OCSP response with an independent signer chain is converted to a CRL.

<div class="alert"><b>Note</b>  This property should not be set for a delegated OCSP signer certificate. A delegated signer certificate is signed with the same key used to sign the subject certificate and is checked there.</div>
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
Data type for <i>pvData</i>: Pointer to a <a href="/windows/win32/api/dpapi/ns-dpapi-crypt_integer_blob">CRYPT_DATA_BLOB</a> structure.



Sets a string that contains a set of L"<i>&lt;SIGNATURE&gt;</i>/<i>&lt;HASH&gt;</i>" algorithm pairs. The semicolon, L";", is used as the delimiter between pairs.

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
The following is an  example:

<ul>
<li>L"RSA/SHA256;RSA/SHA256"</li>
</ul>
This property is explicitly set by the verify revocation functions.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_ISSUER_PUB_KEY_BIT_LENGTH_PROP_ID"></a><a id="cert_issuer_pub_key_bit_length_prop_id"></a><dl>
<dt><b>CERT_ISSUER_PUB_KEY_BIT_LENGTH_PROP_ID</b></dt>
</dl>
</td>
<td width="60%">
Data type for <i>pvData</i>: Pointer to a <a href="/windows/win32/api/dpapi/ns-dpapi-crypt_integer_blob">CRYPT_DATA_BLOB</a> structure.



Sets the length, in bits, of the public key in the CRL issuer certificate. This property is also applicable to an OCSP that has been converted to a CRL.

This property is explicitly set by the verify revocation functions.

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


Sets a 
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

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_KEY_PROV_HANDLE_PROP_ID"></a><a id="cert_key_prov_handle_prop_id"></a><dl>
<dt><b>CERT_KEY_PROV_HANDLE_PROP_ID</b></dt>
</dl>
</td>
<td width="60%">
Data type for <i>pvData</i>:  pointer to an <a href="/windows/desktop/SecCrypto/hcryptprov">HCRYPTPROV</a>


Sets the provider handle obtained from the CERT_KEY_CONTEXT_PROP_ID.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_KEY_PROV_INFO_PROP_ID"></a><a id="cert_key_prov_info_prop_id"></a><dl>
<dt><b>CERT_KEY_PROV_INFO_PROP_ID</b></dt>
</dl>
</td>
<td width="60%">
Data type for <i>pvData</i>:  pointer to a <a href="/windows/desktop/api/wincrypt/ns-wincrypt-crypt_key_prov_info">CRYPT_KEY_PROV_INFO</a>


Sets a pointer to a <a href="/windows/desktop/api/wincrypt/ns-wincrypt-crypt_key_prov_info">CRYPT_KEY_PROV_INFO</a> structure.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_KEY_SPEC_PROP_ID"></a><a id="cert_key_spec_prop_id"></a><dl>
<dt><b>CERT_KEY_SPEC_PROP_ID</b></dt>
</dl>
</td>
<td width="60%">
Data type for <i>pvData</i>: pointer to a <b>DWORD</b>

Sets a <b>DWORD</b> value specifying the private key obtained from CERT_KEY_CONTEXT_PROP_ID property if it exists. Otherwise, if CERT_KEY_PROV_INFO_PROP_ID exists, it is the source of the <i>dwKeySpec</i>.
							

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_MD5_HASH_PROP_ID"></a><a id="cert_md5_hash_prop_id"></a><dl>
<dt><b>CERT_MD5_HASH_PROP_ID</b></dt>
</dl>
</td>
<td width="60%">
Data type for <i>pvData</i>: pointer to a <b>BYTE</b> array

Sets the MD5 hash. You can compute the hash by using the <a href="/windows/desktop/api/wincrypt/nf-wincrypt-crypthashcertificate">CryptHashCertificate</a> function.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_NEXT_UPDATE_LOCATION_PROP_ID"></a><a id="cert_next_update_location_prop_id"></a><dl>
<dt><b>CERT_NEXT_UPDATE_LOCATION_PROP_ID</b></dt>
</dl>
</td>
<td width="60%">
Data type for <i>pvData</i>: pointer to a <b>BYTE</b> array

Sets the ASN.1 encoded 
<a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_alt_name_info">CERT_ALT_NAME_INFO</a> structure on a CTL.
							

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_PVK_FILE_PROP_ID"></a><a id="cert_pvk_file_prop_id"></a><dl>
<dt><b>CERT_PVK_FILE_PROP_ID</b></dt>
</dl>
</td>
<td width="60%">
Data type for <i>pvData</i>: pointer to a <b>BYTE</b> array

Sets a <b>null</b>-terminated Unicode, wide character string specifying the name of the file that contains the private key associated with the certificate's public key.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_SHA1_HASH_PROP_ID"></a><a id="cert_sha1_hash_prop_id"></a><dl>
<dt><b>CERT_SHA1_HASH_PROP_ID</b></dt>
</dl>
</td>
<td width="60%">
Data type for <i>pvData</i>: pointer to a <b>BYTE</b> array

Sets the SHA1 hash. You can compute the hash by using 
<a href="/windows/desktop/api/wincrypt/nf-wincrypt-crypthashcertificate">CryptHashCertificate</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_SIGN_HASH_CNG_ALG_PROP_ID"></a><a id="cert_sign_hash_cng_alg_prop_id"></a><dl>
<dt><b>CERT_SIGN_HASH_CNG_ALG_PROP_ID</b></dt>
</dl>
</td>
<td width="60%">
Data type of <i>pvData</i>: Pointer to a <a href="/windows/win32/api/dpapi/ns-dpapi-crypt_integer_blob">CRYPT_DATA_BLOB</a> structure.

Sets the L”<i>&lt;SIGNATURE&gt;</i>/<i>&lt;HASH&gt;</i>” string representing the certificate signature. The <i>&lt;SIGNATURE&gt;</i> value identifies the CNG public key algorithm. The following algorithms are supported:

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
This property is also applicable to an OCSP response that has been converted to a  CRL.

This property is explicitly set by the verify revocation functions.

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

Sets the signature hash. If the hash does not exist, it is computed with 
<a href="/windows/desktop/api/wincrypt/nf-wincrypt-crypthashtobesigned">CryptHashToBeSigned</a>. The length of the hash is 20 bytes for SHA and 16 for MD5.

</td>
</tr>
</table>
 

The user can define additional <i>dwPropId</i> types by using <b>DWORD</b> values from CERT_FIRST_USER_PROP_ID to CERT_LAST_USER_PROP_ID. For all user-defined <i>dwPropId</i> types, <i>pvData</i> points to an encoded <a href="/previous-versions/windows/desktop/legacy/aa381414(v=vs.85)">CRYPT_DATA_BLOB</a>.

For all the other property identifiers, <i>pvData</i> points to an encoded <a href="/previous-versions/windows/desktop/legacy/aa381414(v=vs.85)">CRYPT_DATA_BLOB</a> structure.

### -param dwFlags [in]

CERT_STORE_NO_CRYPT_RELEASE_FLAG can be set for the CERT_KEY_PROV_HANDLE_PROP_ID or CERT_KEY_CONTEXT_PROP_ID <i>dwPropId</i> properties. 




If the CERT_SET_PROPERTY_IGNORE_PERSIST_ERROR_FLAG value is set, any provider-write errors are ignored and the cached context's properties are always set.

If the CERT_SET_PROPERTY_INHIBIT_PERSIST_FLAG is set, any property set is not persisted.

### -param pvData [in]

A pointer to a data type that is determined by the value passed in <i>dwPropId</i>. 




<div class="alert"><b>Note</b>  For any <i>dwPropId</i>, setting <i>pvData</i> to <b>NULL</b> deletes the property.</div>
<div> </div>

## -returns

If the function succeeds, the return value is <b>TRUE</b>.

If the function fails, the return value is <b>FALSE</b>. For extended error information, call 
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


#### Examples

For an example that uses this function, see 
<a href="/windows/desktop/SecCrypto/example-c-program-getting-and-setting-certificate-properties">Example C Program: Getting and Setting Certificate Properties</a>.

<div class="code"></div>

## -see-also

<a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_alt_name_info">CERT_ALT_NAME_INFO</a>



<a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_context">CERT_CONTEXT</a>



<a href="/windows/desktop/api/wincrypt/ns-wincrypt-ctl_usage">CERT_ENHKEY_USAGE</a>



<a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_key_context">CERT_KEY_CONTEXT</a>



<a href="/windows/desktop/api/wincrypt/ns-wincrypt-crl_context">CRL_CONTEXT</a>



<a href="/previous-versions/windows/desktop/legacy/aa381414(v=vs.85)">CRYPT_DATA_BLOB</a>



<a href="/previous-versions/windows/desktop/legacy/aa381414(v=vs.85)">CRYPT_HASH_BLOB</a>



<a href="/windows/desktop/api/wincrypt/ns-wincrypt-crypt_key_prov_info">CRYPT_KEY_PROV_INFO</a>



<a href="/windows/desktop/api/wincrypt/ns-wincrypt-ctl_usage">CTL_USAGE</a>



<a href="/windows/desktop/api/wincrypt/nf-wincrypt-certgetcrlcontextproperty">CertGetCRLContextProperty</a>



<a href="/windows/desktop/api/wincrypt/nf-wincrypt-certsetcertificatecontextproperty">CertSetCertificateContextProperty</a>



<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptencodeobject">CryptEncodeObject</a>



<a href="/windows/desktop/api/wincrypt/nf-wincrypt-crypthashtobesigned">CryptHashToBeSigned</a>



<a href="/windows/desktop/SecCrypto/cryptography-functions">Extended Property Functions</a>