---
UID: NS:wincrypt._CRYPT_OID_INFO
title: CRYPT_OID_INFO (wincrypt.h)
description: Contains information about an object identifier (OID).
helpviewer_keywords: ["*PCRYPT_OID_INFO","CCRYPT_OID_INFO","CCRYPT_OID_INFO structure [Security]","CRYPT_ENCRYPT_ALG_OID_GROUP_ID","CRYPT_ENHKEY_USAGE_OID_GROUP_ID","CRYPT_EXT_OR_ATTR_OID_GROUP_ID","CRYPT_HASH_ALG_OID_GROUP_ID","CRYPT_OID_INFO","CRYPT_OID_INFO structure [Security]","CRYPT_OID_INFO_ECC_PARAMETERS_ALGORITHM","CRYPT_OID_INFO_ECC_WRAP_PARAMETERS_ALGORITHM","CRYPT_OID_INFO_HASH_PARAMETERS_ALGORITHM","CRYPT_OID_INFO_MGF1_PARAMETERS_ALGORITHM","CRYPT_OID_INFO_NO_SIGN_ALGORITHM","CRYPT_OID_INFO_OAEP_PARAMETERS_ALGORITHM","CRYPT_OID_INHIBIT_SIGNATURE_FORMAT_FLAG","CRYPT_OID_NO_NULL_ALGORITHM_PARA_FLAG","CRYPT_OID_PUBKEY_ENCRYPT_ONLY_FLAG","CRYPT_OID_PUBKEY_SIGN_ONLY_FLAG","CRYPT_OID_USE_PUBKEY_PARA_FOR_PKCS7_FLAG","CRYPT_POLICY_OID_GROUP_ID","CRYPT_PUBKEY_ALG_OID_GROUP_ID","CRYPT_RDN_ATTR_OID_GROUP_ID","CRYPT_SIGN_ALG_OID_GROUP_ID","PCCRYPT_OID_INFO","PCCRYPT_OID_INFO structure pointer [Security]","PCRYPT_OID_INFO","PCRYPT_OID_INFO structure pointer [Security]","_crypto2_crypt_oid_info","security.crypt_oid_info","wincrypt/CCRYPT_OID_INFO","wincrypt/CRYPT_OID_INFO","wincrypt/PCCRYPT_OID_INFO","wincrypt/PCRYPT_OID_INFO"]
old-location: security\crypt_oid_info.htm
tech.root: security
ms.assetid: 06ba0f60-778d-450b-8f71-23471b8c4e2c
ms.date: 12/05/2018
ms.keywords: '*PCRYPT_OID_INFO, CCRYPT_OID_INFO, CCRYPT_OID_INFO structure [Security], CRYPT_ENCRYPT_ALG_OID_GROUP_ID, CRYPT_ENHKEY_USAGE_OID_GROUP_ID, CRYPT_EXT_OR_ATTR_OID_GROUP_ID, CRYPT_HASH_ALG_OID_GROUP_ID, CRYPT_OID_INFO, CRYPT_OID_INFO structure [Security], CRYPT_OID_INFO_ECC_PARAMETERS_ALGORITHM, CRYPT_OID_INFO_ECC_WRAP_PARAMETERS_ALGORITHM, CRYPT_OID_INFO_HASH_PARAMETERS_ALGORITHM, CRYPT_OID_INFO_MGF1_PARAMETERS_ALGORITHM, CRYPT_OID_INFO_NO_SIGN_ALGORITHM, CRYPT_OID_INFO_OAEP_PARAMETERS_ALGORITHM, CRYPT_OID_INHIBIT_SIGNATURE_FORMAT_FLAG, CRYPT_OID_NO_NULL_ALGORITHM_PARA_FLAG, CRYPT_OID_PUBKEY_ENCRYPT_ONLY_FLAG, CRYPT_OID_PUBKEY_SIGN_ONLY_FLAG, CRYPT_OID_USE_PUBKEY_PARA_FOR_PKCS7_FLAG, CRYPT_POLICY_OID_GROUP_ID, CRYPT_PUBKEY_ALG_OID_GROUP_ID, CRYPT_RDN_ATTR_OID_GROUP_ID, CRYPT_SIGN_ALG_OID_GROUP_ID, PCCRYPT_OID_INFO, PCCRYPT_OID_INFO structure pointer [Security], PCRYPT_OID_INFO, PCRYPT_OID_INFO structure pointer [Security], _crypto2_crypt_oid_info, security.crypt_oid_info, wincrypt/CCRYPT_OID_INFO, wincrypt/CRYPT_OID_INFO, wincrypt/PCCRYPT_OID_INFO, wincrypt/PCRYPT_OID_INFO'
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
req.typenames: CRYPT_OID_INFO, *PCRYPT_OID_INFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _CRYPT_OID_INFO
 - wincrypt/_CRYPT_OID_INFO
 - PCRYPT_OID_INFO
 - wincrypt/PCRYPT_OID_INFO
 - CRYPT_OID_INFO
 - wincrypt/CRYPT_OID_INFO
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
 - CRYPT_OID_INFO
---

# CRYPT_OID_INFO structure


## -description

The <b>CRYPT_OID_INFO</b> structure contains information about an <a href="/windows/desktop/SecGloss/o-gly">object identifier</a> (OID). These structures give the relationship among an OID identifier, its name, its group, and other information about the OID. These structures can be listed by using 
the <a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptenumoidinfo">CryptEnumOIDInfo</a> function. New CRYPT_OID_STRUCTURES can be added by using 
the <a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptregisteroidinfo">CryptRegisterOIDInfo</a> function.

## -struct-fields

### -field cbSize

The size, in bytes, of this structure.

### -field pszOID

The OID associated with this OID information.

### -field pwszName

The display name associated with an OID.

### -field dwGroupId

The group identifier value associated with this OID information. 




This member can be one of the following <b>dwGroupId</b> group identifiers.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="CRYPT_ENCRYPT_ALG_OID_GROUP_ID"></a><a id="crypt_encrypt_alg_oid_group_id"></a><dl>
<dt><b>CRYPT_ENCRYPT_ALG_OID_GROUP_ID</b></dt>
</dl>
</td>
<td width="60%">
Encryption algorithms

</td>
</tr>
<tr>
<td width="40%"><a id="CRYPT_ENHKEY_USAGE_OID_GROUP_ID"></a><a id="crypt_enhkey_usage_oid_group_id"></a><dl>
<dt><b>CRYPT_ENHKEY_USAGE_OID_GROUP_ID</b></dt>
</dl>
</td>
<td width="60%">
Enhanced key usages

</td>
</tr>
<tr>
<td width="40%"><a id="CRYPT_EXT_OR_ATTR_OID_GROUP_ID"></a><a id="crypt_ext_or_attr_oid_group_id"></a><dl>
<dt><b>CRYPT_EXT_OR_ATTR_OID_GROUP_ID</b></dt>
</dl>
</td>
<td width="60%">
Extensions or attributes

</td>
</tr>
<tr>
<td width="40%"><a id="CRYPT_HASH_ALG_OID_GROUP_ID"></a><a id="crypt_hash_alg_oid_group_id"></a><dl>
<dt><b>CRYPT_HASH_ALG_OID_GROUP_ID</b></dt>
</dl>
</td>
<td width="60%">
Hash algorithms

</td>
</tr>
<tr>
<td width="40%"><a id="CRYPT_POLICY_OID_GROUP_ID"></a><a id="crypt_policy_oid_group_id"></a><dl>
<dt><b>CRYPT_POLICY_OID_GROUP_ID</b></dt>
</dl>
</td>
<td width="60%">
Policies

</td>
</tr>
<tr>
<td width="40%"><a id="CRYPT_PUBKEY_ALG_OID_GROUP_ID"></a><a id="crypt_pubkey_alg_oid_group_id"></a><dl>
<dt><b>CRYPT_PUBKEY_ALG_OID_GROUP_ID</b></dt>
</dl>
</td>
<td width="60%">
Public key algorithms

</td>
</tr>
<tr>
<td width="40%"><a id="CRYPT_RDN_ATTR_OID_GROUP_ID"></a><a id="crypt_rdn_attr_oid_group_id"></a><dl>
<dt><b>CRYPT_RDN_ATTR_OID_GROUP_ID</b></dt>
</dl>
</td>
<td width="60%">
RDN attributes

</td>
</tr>
<tr>
<td width="40%"><a id="CRYPT_SIGN_ALG_OID_GROUP_ID"></a><a id="crypt_sign_alg_oid_group_id"></a><dl>
<dt><b>CRYPT_SIGN_ALG_OID_GROUP_ID</b></dt>
</dl>
</td>
<td width="60%">
Signature algorithms

</td>
</tr>
</table>

### -field DUMMYUNIONNAME

### -field DUMMYUNIONNAME.dwValue

A numeric value associated with this OID information. This member is used with <b>dwGroupId</b> CRYPT_SIGN_ALG_OID_GROUP_ID.

### -field DUMMYUNIONNAME.Algid

The algorithm identifier associated with this OID information. 




This member applies for the following values of <b>dwGroupId</b>:

<ul>
<li>CRYPT_HASH_ALG_OID_GROUP_ID</li>
<li>CRYPT_ENCRYPT_ALG_OID_GROUP_ID</li>
<li>CRYPT_PUBKEY_ALG_OID_GROUP_ID</li>
<li>CRYPT_SIGN_ALG_OID_GROUP_ID</li>
</ul>

### -field DUMMYUNIONNAME.dwLength

This member is not implemented. It is always set to zero.

### -field ExtraInfo

Extra information used to find or register OID information. This member applies for the following values of <b>dwGroupId</b>: 




<ul>
<li>CRYPT_PUBKEY_ALG_OID_GROUP_ID</li>
<li>CRYPT_SIGN_ALG_OID_GROUP_ID</li>
<li>CRYPT_RDN_ATTR_OID_GROUP_ID</li>
</ul>
The OIDs in the CRYPT_ENCRYPT_ALG_OID_GROUP_ID OID group have a bit length set for the AES algorithms in the DWORD[0] member of the ExtraInfo member.

The OIDs in the CRYPT_PUBKEY_ALG_OID_GROUP_ID group have a flag set in the DWORD[0] member of the ExtraInfo member.

The OIDs in the ECC curve name public keys, for example, szOID_ECC_CURVE_P256 ("1.2.840.10045.3.1.7"), have a flag set in the DWORD[0] member, a BCRYPT_ECCKEY_BLOB dwMagic field value set in the DWORD[1] member, and a bit length where the BCRYPT_ECCKEY_BLOB cbKey value equals dwBitLength / 8 + ((dwBitLength % 8) ? 1 : 0) set in the DWORD[2] member of the ExtraInfo member.

The OIDs in the CRYPT_SIGN_ALG_OID_GROUP_ID group have a public key algorithm identifier set in the DWORD[0] member,  a flag set in the DWORD[1] member, and an optional provider type set in the DWORD[2] member of the ExtraInfo member.

The OIDs in the CRYPT_RDN_ATTR_OID_GROUP_ID group have a null-terminated list of acceptable RDN attribute value types set in an array of <b>DWORD</b> values in the ExtraInfo member. An omitted list implies an array of values where the first value in the array is  CERT_RDN_PRINTABLE_STRING, the second value in the array is CERT_RDN_UNICODE_STRING, and the third value in the array is zero.


The following values are used for the flags in the <b>ExtraInfo</b> member.



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="CRYPT_OID_INHIBIT_SIGNATURE_FORMAT_FLAG"></a><a id="crypt_oid_inhibit_signature_format_flag"></a><dl>
<dt><b>CRYPT_OID_INHIBIT_SIGNATURE_FORMAT_FLAG</b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
This flag is no longer used.

Stop the reformatting of the signature before the <a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptverifysignaturea">CryptVerifySignature</a> function is called or after the <a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptsignhasha">CryptSignHash</a> function is called.

</td>
</tr>
<tr>
<td width="40%"><a id="CRYPT_OID_NO_NULL_ALGORITHM_PARA_FLAG"></a><a id="crypt_oid_no_null_algorithm_para_flag"></a><dl>
<dt><b>CRYPT_OID_NO_NULL_ALGORITHM_PARA_FLAG</b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
Omit <b>NULL</b> parameters when encoding.

</td>
</tr>
<tr>
<td width="40%"><a id="CRYPT_OID_PUBKEY_ENCRYPT_ONLY_FLAG"></a><a id="crypt_oid_pubkey_encrypt_only_flag"></a><dl>
<dt><b>CRYPT_OID_PUBKEY_ENCRYPT_ONLY_FLAG</b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
The public key is only used for encryption.

</td>
</tr>
<tr>
<td width="40%"><a id="CRYPT_OID_PUBKEY_SIGN_ONLY_FLAG"></a><a id="crypt_oid_pubkey_sign_only_flag"></a><dl>
<dt><b>CRYPT_OID_PUBKEY_SIGN_ONLY_FLAG</b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
The public key is only used for signatures.

</td>
</tr>
<tr>
<td width="40%"><a id="CRYPT_OID_USE_PUBKEY_PARA_FOR_PKCS7_FLAG"></a><a id="crypt_oid_use_pubkey_para_for_pkcs7_flag"></a><dl>
<dt><b>CRYPT_OID_USE_PUBKEY_PARA_FOR_PKCS7_FLAG</b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
This flag is no longer used.

Include the parameters of the public key algorithm in the <i>digestEncryptionAlgorithm</i> parameters for the PKCS #7 message.

</td>
</tr>
</table>

### -field pwszCNGAlgid

The algorithm identifier string passed to the CNG functions (the BCrypt* and NCrypt* functions that are defined in Bcrypt.h and Ncrypt.h). CNG functions use algorithm identifier strings, such as L"SHA1", instead of the <a href="/windows/desktop/SecCrypto/alg-id">ALG_ID</a> data type constants, such as <b>CALG_SHA1</b>.<b>Windows Server 2003 and Windows XP:  </b>This member is not available.



<div class="alert"><b>Note</b>  The  <b>pwszCNGAlgid</b> member is only available if you include the following statement in your code.</div>
<div> </div>

```cpp
#define CRYPT_OID_INFO_HAS_EXTRA_FIELDS
```


This member applies for the following values of <b>dwGroupId</b>:

<ul>
<li>CRYPT_HASH_ALG_OID_GROUP_ID</li>
<li>CRYPT_ENCRYPT_ALG_OID_GROUP_ID</li>
<li>CRYPT_PUBKEY_ALG_OID_GROUP_ID</li>
<li>CRYPT_SIGN_ALG_OID_GROUP_ID</li>
</ul>
Set the <b>pwszCNGAlgid</b> member to the empty string, L"", for the other values of <b>dwGroupId</b>.


The <b>pwszCNGAlgid</b> member can also be set to a string value that is not passed directly to the CNG functions. The following table lists these values and their meanings.



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="CRYPT_OID_INFO_ECC_PARAMETERS_ALGORITHM"></a><a id="crypt_oid_info_ecc_parameters_algorithm"></a><dl>
<dt><b>CRYPT_OID_INFO_ECC_PARAMETERS_ALGORITHM</b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
The ECC curve algorithm is obtained from the encoded parameters of the OID algorithm.

</td>
</tr>
<tr>
<td width="40%"><a id="CRYPT_OID_INFO_ECC_WRAP_PARAMETERS_ALGORITHM"></a><a id="crypt_oid_info_ecc_wrap_parameters_algorithm"></a><dl>
<dt><b>CRYPT_OID_INFO_ECC_WRAP_PARAMETERS_ALGORITHM</b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
The key wrap algorithm is obtained from the encoded parameters of the OID algorithm.

</td>
</tr>
<tr>
<td width="40%"><a id="CRYPT_OID_INFO_HASH_PARAMETERS_ALGORITHM"></a><a id="crypt_oid_info_hash_parameters_algorithm"></a><dl>
<dt><b>CRYPT_OID_INFO_HASH_PARAMETERS_ALGORITHM</b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
The hash algorithm is obtained from the encoded parameters of the OID algorithm.

</td>
</tr>
<tr>
<td width="40%"><a id="CRYPT_OID_INFO_MGF1_PARAMETERS_ALGORITHM"></a><a id="crypt_oid_info_mgf1_parameters_algorithm"></a><dl>
<dt><b>CRYPT_OID_INFO_MGF1_PARAMETERS_ALGORITHM</b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
The PKCS #1 v2.1 mask generation hash algorithm is obtained from the encoded parameters of the OID algorithm.

</td>
</tr>
<tr>
<td width="40%"><a id="CRYPT_OID_INFO_NO_SIGN_ALGORITHM"></a><a id="crypt_oid_info_no_sign_algorithm"></a><dl>
<dt><b>CRYPT_OID_INFO_NO_SIGN_ALGORITHM</b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
A public key algorithm that indicates the signature value is an unsigned hash.

</td>
</tr>
<tr>
<td width="40%"><a id="CRYPT_OID_INFO_OAEP_PARAMETERS_ALGORITHM"></a><a id="crypt_oid_info_oaep_parameters_algorithm"></a><dl>
<dt><b>CRYPT_OID_INFO_OAEP_PARAMETERS_ALGORITHM</b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
The RSAES-OAEP padding hash algorithm is obtained from the encoded parameters of the OID algorithm.

</td>
</tr>
</table>

### -field pwszCNGExtraAlgid

An extra algorithm string, other than the string in the <b>pwszCNGAlgid</b> member,  that can be passed to the CNG functions (the BCrypt* and NCrypt* functions that are defined in Bcrypt.h and Ncrypt.h).


<b>Windows Server 2003 and Windows XP:  </b>This member is not available.

<div class="alert"><b>Note</b>  This member is only available if you include the following statement in your code.</div>
<div> </div>

```cpp
#define CRYPT_OID_INFO_HAS_EXTRA_FIELDS
```


For the signature algorithms (CRYPT_SIGN_ALG_OID_GROUP_ID), this member is the public key algorithm string to pass to the CNG functions.

For ECC signatures, this member is the special CRYPT_OID_INFO_ECC_PARAMETERS_ALGORITHM string value.

For unsigned signatures, this member is the special CRYPT_OID_INFO_NO_SIGN_ALGORITHM string value.

For ECC curve name public keys, for example, szOID_ECC_CURVE_P256 ("1.2.840.10045.3.1.7"), this is the special CRYPT_OID_INFO_ECC_PARAMETERS_ALGORITHM string value.

For the other values of <b>dwGroupId</b>, set the <b>pwszCNGExtraAlgid</b> member to the empty string, L"".

## -see-also

<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptfindoidinfo">CryptFindOIDInfo</a>



<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptregisteroidinfo">CryptRegisterOIDInfo</a>



<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptunregisteroidinfo">CryptUnregisterOIDInfo</a>