---
UID: NF:wincrypt.CertFindCertificateInStore
title: CertFindCertificateInStore function (wincrypt.h)
description: Finds the first or next certificate context in a certificate store that matches a search criteria established by the dwFindType and its associated pvFindPara.
helpviewer_keywords: ["CERT_FIND_ANY","CERT_FIND_CERT_ID","CERT_FIND_CROSS_CERT_DIST_POINTS","CERT_FIND_CTL_USAGE","CERT_FIND_ENHKEY_USAGE","CERT_FIND_EXISTING","CERT_FIND_HASH","CERT_FIND_HAS_PRIVATE_KEY","CERT_FIND_ISSUER_ATTR","CERT_FIND_ISSUER_NAME","CERT_FIND_ISSUER_OF","CERT_FIND_ISSUER_STR","CERT_FIND_KEY_IDENTIFIER","CERT_FIND_KEY_SPEC","CERT_FIND_MD5_HASH","CERT_FIND_PROPERTY","CERT_FIND_PUBKEY_MD5_HASH","CERT_FIND_PUBLIC_KEY","CERT_FIND_SHA1_HASH","CERT_FIND_SHA1_SHA256_HASH","CERT_FIND_SHA256_HASH","CERT_FIND_SIGNATURE_HASH","CERT_FIND_SUBJECT_ATTR","CERT_FIND_SUBJECT_CERT","CERT_FIND_SUBJECT_NAME","CERT_FIND_SUBJECT_STR","CertFindCertificateInStore","CertFindCertificateInStore function [Security]","_crypto2_certfindcertificateinstore","security.certfindcertificateinstore","wincrypt/CertFindCertificateInStore"]
old-location: security\certfindcertificateinstore.htm
tech.root: security
ms.assetid: 20b3fcfb-55df-46ff-80a5-70f31a3d03b2
ms.date: 07/11/2024
ms.keywords: CERT_FIND_ANY, CERT_FIND_CERT_ID, CERT_FIND_CROSS_CERT_DIST_POINTS, CERT_FIND_CTL_USAGE, CERT_FIND_ENHKEY_USAGE, CERT_FIND_EXISTING, CERT_FIND_HASH, CERT_FIND_HAS_PRIVATE_KEY, CERT_FIND_ISSUER_ATTR, CERT_FIND_ISSUER_NAME, CERT_FIND_ISSUER_OF, CERT_FIND_ISSUER_STR, CERT_FIND_KEY_IDENTIFIER, CERT_FIND_KEY_SPEC, CERT_FIND_MD5_HASH, CERT_FIND_PROPERTY, CERT_FIND_PUBKEY_MD5_HASH, CERT_FIND_PUBLIC_KEY, CERT_FIND_SHA1_HASH, CERT_FIND_SHA1_SHA256_HASH, CERT_FIND_SHA256_HASH, CERT_FIND_SIGNATURE_HASH, CERT_FIND_SUBJECT_ATTR, CERT_FIND_SUBJECT_CERT, CERT_FIND_SUBJECT_NAME, CERT_FIND_SUBJECT_STR, CertFindCertificateInStore, CertFindCertificateInStore function [Security], _crypto2_certfindcertificateinstore, security.certfindcertificateinstore, wincrypt/CertFindCertificateInStore
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
 - CertFindCertificateInStore
 - wincrypt/CertFindCertificateInStore
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
 - CertFindCertificateInStore
---

# CertFindCertificateInStore function


## -description

The <b>CertFindCertificateInStore</b> function finds the first or next certificate <a href="/windows/desktop/SecGloss/c-gly">context</a> in a <a href="/windows/desktop/SecGloss/c-gly">certificate store</a> that matches a search criteria established by the <i>dwFindType</i> and its associated <i>pvFindPara</i>. This function can be used in a loop to find all of the <a href="/windows/desktop/SecGloss/c-gly">certificates</a> in a <a href="/windows/desktop/SecGloss/c-gly">certificate store</a> that match the specified find criteria.

## -parameters

### -param hCertStore [in]

A handle of the <a href="/windows/desktop/SecGloss/c-gly">certificate store</a> to be searched.

### -param dwCertEncodingType [in]

Specifies the type of encoding used. Both the certificate and <a href="/windows/desktop/SecGloss/m-gly">message encoding types</a> must be specified by combining them with a bitwise-<b>OR</b> operation as shown in the following example:

X509_ASN_ENCODING | PKCS_7_ASN_ENCODING Currently defined encoding types are:

<ul>
<li>X509_ASN_ENCODING</li>
<li>PKCS_7_ASN_ENCODING</li>
</ul>

### -param dwFindFlags [in]

Used with some <i>dwFindType</i> values to modify the search criteria. For most <i>dwFindType</i> values, <i>dwFindFlags</i> is not used and should be set to zero. For detailed information, see  Remarks.

### -param dwFindType [in]

Specifies the type of search being made. The search type determines the data type, contents, and the use of <i>pvFindPara</i>. This parameter can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="CERT_FIND_ANY"></a><a id="cert_find_any"></a><dl>
<dt><b>CERT_FIND_ANY</b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
Data type of <i>pvFindPara</i>: <b>NULL</b>, not used.

No search criteria used. Returns the next certificate in the store.

<div class="alert"><b>Note</b>  The order of the certificate context may not be preserved within the store. 
To access a specific certificate you must iterate across the certificates in the store.</div>
<div> </div>
</td>
</tr>
<tr>
<td width="40%"><a id="CERT_FIND_CERT_ID"></a><a id="cert_find_cert_id"></a><dl>
<dt><b>CERT_FIND_CERT_ID</b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
Data type of <i>pvFindPara</i>: <a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_id">CERT_ID</a> structure.

Find the certificate identified by the specified <a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_id">CERT_ID</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_FIND_CTL_USAGE"></a><a id="cert_find_ctl_usage"></a><dl>
<dt><b>CERT_FIND_CTL_USAGE</b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
Data type of <i>pvFindPara</i>: <a href="/windows/desktop/api/wincrypt/ns-wincrypt-ctl_usage">CTL_USAGE</a> structure.

Searches for a certificate that has a szOID_ENHANCED_KEY_USAGE extension or a CERT_CTL_PROP_ID that matches the <b>pszUsageIdentifier</b> member of the <a href="/windows/desktop/api/wincrypt/ns-wincrypt-ctl_usage">CTL_USAGE</a> structure.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_FIND_ENHKEY_USAGE"></a><a id="cert_find_enhkey_usage"></a><dl>
<dt><b>CERT_FIND_ENHKEY_USAGE</b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
Data type of <i>pvFindPara</i>: <a href="/windows/desktop/api/wincrypt/ns-wincrypt-ctl_usage">CERT_ENHKEY_USAGE</a> structure.

Searches for a certificate in the store that has either an <a href="/windows/desktop/SecGloss/e-gly">enhanced key usage</a> extension or an enhanced key usage property and a usage identifier that matches the <b>cUsageIdentifier</b> member in the <a href="/windows/desktop/api/wincrypt/ns-wincrypt-ctl_usage"> CERT_ENHKEY_USAGE</a> structure.

A certificate has an enhanced key usage extension if it has a <a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_extension">CERT_EXTENSION</a> structure with the <b>pszObjId</b> member set to szOID_ENHANCED_KEY_USAGE.

A certificate has an enhanced key usage property if its CERT_ENHKEY_USAGE_PROP_ID identifier is set.

If CERT_FIND_OPTIONAL_ENHKEY_USAGE_FLAG is set in <i>dwFindFlags</i>, certificates without the key usage extension or property are also matches. Setting this flag takes precedence over passing <b>NULL</b> in <i>pvFindPara</i>.

If CERT_FIND_EXT_ONLY_ENHKEY_USAGE_FLAG is set, a match is done only on the key usage extension.

For information about flag modifications to search criteria, see  Remarks.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_FIND_EXISTING"></a><a id="cert_find_existing"></a><dl>
<dt><b>CERT_FIND_EXISTING</b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
Data type of <i>pvFindPara</i>: <a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_context">CERT_CONTEXT</a> structure.

Searches for a certificate that is an exact match of the specified certificate context.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_FIND_HASH"></a><a id="cert_find_hash"></a><dl>
<dt><b>CERT_FIND_HASH</b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
Data type of <i>pvFindPara</i>: <a href="/previous-versions/windows/desktop/legacy/aa381414(v=vs.85)">CRYPT_HASH_BLOB</a> structure.

Searches for a certificate with a SHA1 hash that matches the hash in the <a href="/previous-versions/windows/desktop/legacy/aa381414(v=vs.85)">CRYPT_HASH_BLOB</a> structure.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_FIND_HAS_PRIVATE_KEY"></a><a id="cert_find_has_private_key"></a><dl>
<dt><b>CERT_FIND_HAS_PRIVATE_KEY</b></dt>
</dl>
</td>
<td width="60%">
Data type of <i>pvFindPara</i>: <b>NULL</b>, not used.

Searches for a certificate that has a private key. The key can be ephemeral or saved on disk. The key can be a legacy Cryptography API (CAPI) key or a CNG key.

<div class="alert"><b>Note</b>  The order of the certificate context may not be preserved within the store. Therefore, to access a specific certificate, you must iterate across all certificates.</div>
<div> </div>
<b>Windows 8 and Windows Server 2012:  </b>Support for this flag begins.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_FIND_ISSUER_ATTR"></a><a id="cert_find_issuer_attr"></a><dl>
<dt><b>CERT_FIND_ISSUER_ATTR</b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
Data type of <i>pvFindPara</i>: <a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_rdn">CERT_RDN</a> structure.

Searches for a certificate with specified issuer attributes that match attributes in the <a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_rdn">CERT_RDN</a> structure. If these values are set, the function compares attributes of the issuer in a certificate with elements of the <a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_rdn_attr">CERT_RDN_ATTR</a> array in this <b>CERT_RDN</b> structure. Comparisons iterate through the <b>CERT_RDN_ATTR</b> attributes looking for a match with the certificate's issuer attributes.

If the <b>pszObjId</b> member of <a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_rdn_attr">CERT_RDN_ATTR</a> is <b>NULL</b>, the attribute object identifier is ignored.

If the <b>dwValueType</b> member of <a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_rdn_attr">CERT_RDN_ATTR</a> is CERT_RDN_ANY_TYPE, the value type is ignored.

If the <b>pbData</b> member of <a href="/previous-versions/windows/desktop/legacy/aa381414(v=vs.85)">CERT_RDN_VALUE_BLOB</a> is <b>NULL</b>, any value is a match.

Currently only an exact, case-sensitive match is supported. For information about Unicode options, see  Remarks. When these values are set, the search is restricted to certificates whose encoding type matches <i>dwCertEncodingType</i>.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_FIND_ISSUER_NAME"></a><a id="cert_find_issuer_name"></a><dl>
<dt><b>CERT_FIND_ISSUER_NAME</b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
Data type of <i>pvFindPara</i>: <a href="/previous-versions/windows/desktop/legacy/aa381414(v=vs.85)">CERT_NAME_BLOB</a> structure.

Search for a certificate with an exact match of the entire issuer name with the name in <a href="/previous-versions/windows/desktop/legacy/aa381414(v=vs.85)">CERT_NAME_BLOB</a> The search is restricted to certificates that match the <i>dwCertEncodingType</i>.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_FIND_ISSUER_OF"></a><a id="cert_find_issuer_of"></a><dl>
<dt><b>CERT_FIND_ISSUER_OF</b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
Data type of <i>pvFindPara</i>: <a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_context">CERT_CONTEXT</a> structure.

Searches for a certificate with a subject that matches the issuer in <a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_context">CERT_CONTEXT</a>.

Instead of using <b>CertFindCertificateInStore</b> with this value, use the <a href="/windows/desktop/api/wincrypt/nf-wincrypt-certgetcertificatechain">CertGetCertificateChain</a> function.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_FIND_ISSUER_STR"></a><a id="cert_find_issuer_str"></a><dl>
<dt><b>CERT_FIND_ISSUER_STR</b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
Data type of <i>pvFindPara</i>: Null-terminated Unicode string.

Searches for a certificate that contains the specified issuer name string. The certificate's issuer member is converted to a name string of the appropriate type using the appropriate form of <a href="/windows/desktop/api/wincrypt/nf-wincrypt-certnametostra">CertNameToStr</a> formatted as CERT_SIMPLE_NAME_STR. Then a case-insensitive substring-within-a-string match is performed. When this value is set, the search is restricted to certificates whose encoding type matches <i>dwCertEncodingType</i>.

If the substring match fails and the subject contains an email RDN with Punycode encoded string, <b>CERT_NAME_STR_ENABLE_PUNYCODE_FLAG</b> is used to convert the subject to a Unicode string and the substring match is performed again. 

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_FIND_KEY_IDENTIFIER"></a><a id="cert_find_key_identifier"></a><dl>
<dt><b>CERT_FIND_KEY_IDENTIFIER</b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
Data type of <i>pvFindPara</i>: <a href="/previous-versions/windows/desktop/legacy/aa381414(v=vs.85)">CRYPT_HASH_BLOB</a> structure.

Searches for a certificate with a CERT_KEY_IDENTIFIER_PROP_ID property that matches the key identifier in <a href="/previous-versions/windows/desktop/legacy/aa381414(v=vs.85)">CRYPT_HASH_BLOB</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_FIND_KEY_SPEC"></a><a id="cert_find_key_spec"></a><dl>
<dt><b>CERT_FIND_KEY_SPEC</b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
Data type of <i>pvFindPara</i>: <b>DWORD</b> variable that contains a key specification.

Searches for a certificate that has a CERT_KEY_SPEC_PROP_ID property that matches the key specification in <i>pvFindPara</i>.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_FIND_MD5_HASH"></a><a id="cert_find_md5_hash"></a><dl>
<dt><b>CERT_FIND_MD5_HASH</b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
Data type of <i>pvFindPara</i>: <a href="/previous-versions/windows/desktop/legacy/aa381414(v=vs.85)">CRYPT_HASH_BLOB</a> structure.

Searches for a certificate with an MD5 hash that matches the hash in <a href="/previous-versions/windows/desktop/legacy/aa381414(v=vs.85)">CRYPT_HASH_BLOB</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_FIND_PROPERTY"></a><a id="cert_find_property"></a><dl>
<dt><b>CERT_FIND_PROPERTY</b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
Data type of <i>pvFindPara</i>: <b>DWORD</b> variable that contains a property identifier.

Searches for a certificate with a property that matches the property identifier specified by the <b>DWORD</b> value in <i>pvFindPara</i>.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_FIND_PUBLIC_KEY"></a><a id="cert_find_public_key"></a><dl>
<dt><b>CERT_FIND_PUBLIC_KEY</b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
Data type of <i>pvFindPara</i>: <a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_public_key_info">CERT_PUBLIC_KEY_INFO</a> structure.

Searches for a certificate with a public key that matches the public key in the <a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_public_key_info">CERT_PUBLIC_KEY_INFO</a> structure.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_FIND_SHA1_HASH"></a><a id="cert_find_sha1_hash"></a><dl>
<dt><b>CERT_FIND_SHA1_HASH</b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
Data type of <i>pvFindPara</i>: <a href="/previous-versions/windows/desktop/legacy/aa381414(v=vs.85)">CRYPT_HASH_BLOB</a> structure.

Searches for a certificate with a SHA1 hash that matches the hash in the <a href="/previous-versions/windows/desktop/legacy/aa381414(v=vs.85)">CRYPT_HASH_BLOB</a> structure.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_FIND_SHA1_SHA256_HASH"></a><a id="cert_find_sha1_sha256_hash"></a><dl>
<dt><b>CERT_FIND_SHA1_SHA256_HASH</b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
Data type of <i>pvFindPara</i>: <a href="/previous-versions/windows/desktop/legacy/aa381414(v=vs.85)">CRYPT_HASH_BLOB</a> structure.

Searches for a certificate with a SHA1 + SHA256 hash that matches the hash in the <a href="/previous-versions/windows/desktop/legacy/aa381414(v=vs.85)">CRYPT_HASH_BLOB</a> structure.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_FIND_SHA256_HASH"></a><a id="cert_find_sha256_hash"></a><dl>
<dt><b>CERT_FIND_SHA256_HASH</b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
Data type of <i>pvFindPara</i>: <a href="/previous-versions/windows/desktop/legacy/aa381414(v=vs.85)">CRYPT_HASH_BLOB</a> structure.

Searches for a certificate with a SHA256 hash that matches the hash in the <a href="/previous-versions/windows/desktop/legacy/aa381414(v=vs.85)">CRYPT_HASH_BLOB</a> structure.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_FIND_SIGNATURE_HASH"></a><a id="cert_find_signature_hash"></a><dl>
<dt><b>CERT_FIND_SIGNATURE_HASH</b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
Data type of <i>pvFindPara</i>: <a href="/previous-versions/windows/desktop/legacy/aa381414(v=vs.85)">CRYPT_HASH_BLOB</a> structure.

Searches for a certificate with a signature hash that matches the signature hash in the <a href="/previous-versions/windows/desktop/legacy/aa381414(v=vs.85)">CRYPT_HASH_BLOB</a> structure.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_FIND_SUBJECT_ATTR"></a><a id="cert_find_subject_attr"></a><dl>
<dt><b>CERT_FIND_SUBJECT_ATTR</b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
Data type of <i>pvFindPara</i>: <a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_rdn">CERT_RDN</a> structure.

Searches for a certificate with specified subject attributes that match attributes in the <a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_rdn">CERT_RDN</a> structure. If RDN values are set, the function compares attributes of the subject in a certificate with elements of the <a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_rdn_attr">CERT_RDN_ATTR</a> array in this <b>CERT_RDN</b> structure. Comparisons iterate through the <b>CERT_RDN_ATTR</b> attributes looking for a match with the certificate's subject's attributes.

If the <b>pszObjId</b> member of <a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_rdn_attr">CERT_RDN_ATTR</a> is <b>NULL</b>, the attribute object identifier is ignored.

If the <b>dwValueType</b> member of <a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_rdn_attr">CERT_RDN_ATTR</a> is CERT_RDN_ANY_TYPE, the value type is ignored.

If the <b>pbData</b> member of <a href="/previous-versions/windows/desktop/legacy/aa381414(v=vs.85)">CERT_RDN_VALUE_BLOB</a> is <b>NULL</b>, any value is a match.

Currently only an exact, case-sensitive match is supported.

For information about Unicode options, see  Remarks. When these values are set, the search is restricted to certificates whose encoding type matches <i>dwCertEncodingType</i>.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_FIND_SUBJECT_CERT"></a><a id="cert_find_subject_cert"></a><dl>
<dt><b>CERT_FIND_SUBJECT_CERT</b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
Data type of <i>pvFindPara</i>: <a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_info">CERT_INFO</a> structure.

Searches for a certificate with both an issuer and a serial number that match the issuer and serial number in the <a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_info">CERT_INFO</a> structure.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_FIND_SUBJECT_NAME"></a><a id="cert_find_subject_name"></a><dl>
<dt><b>CERT_FIND_SUBJECT_NAME</b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
Data type of <i>pvFindPara</i>: <a href="/previous-versions/windows/desktop/legacy/aa381414(v=vs.85)">CERT_NAME_BLOB</a> structure.

Searches for a certificate with an exact match of the entire subject name with the name in the <a href="/previous-versions/windows/desktop/legacy/aa381414(v=vs.85)">CERT_NAME_BLOB</a> structure. The search is restricted to certificates that match the value of <i>dwCertEncodingType</i>.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_FIND_SUBJECT_STR"></a><a id="cert_find_subject_str"></a><dl>
<dt><b>CERT_FIND_SUBJECT_STR</b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
Data type of <i>pvFindPara</i>: Null-terminated Unicode string.

Searches for a certificate that contains the specified subject name string. The certificate's subject member is converted to a name string of the appropriate type using the appropriate form of <a href="/windows/desktop/api/wincrypt/nf-wincrypt-certnametostra">CertNameToStr</a> formatted as CERT_SIMPLE_NAME_STR. Then a case-insensitive substring-within-a-string match is performed. When this value is set, the search is restricted to certificates whose encoding type matches <i>dwCertEncodingType</i>.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_FIND_CROSS_CERT_DIST_POINTS"></a><a id="cert_find_cross_cert_dist_points"></a><dl>
<dt><b>CERT_FIND_CROSS_CERT_DIST_POINTS</b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
Data type of <i>pvFindPara</i>: Not used.

Find a certificate that has either a cross certificate distribution point extension or property.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_FIND_PUBKEY_MD5_HASH"></a><a id="cert_find_pubkey_md5_hash"></a><dl>
<dt><b>CERT_FIND_PUBKEY_MD5_HASH</b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
Data type of <i>pvFindPara</i>: <a href="/previous-versions/windows/desktop/legacy/aa381414(v=vs.85)">CRYPT_HASH_BLOB</a> structure.

Find a certificate whose MD5-hashed public key matches the specified hash.

</td>
</tr>
</table>
 

<div class="alert"><b>Note</b>  There are alternate forms of the value of <i>dwFindType</i> that pass a string in <i>pvFindPara</i>. One form uses a Unicode string, and the other an <a href="/windows/desktop/SecGloss/a-gly">ASCII</a> string. Values that end in "_W" or without a suffix use Unicode. Values that end with "_A" use ASCII strings.</div>
<div> </div>

### -param pvFindPara [in]

Points to a data item or structure used with <i>dwFindType</i>.

### -param pPrevCertContext [in]

A pointer to the last 
<a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_context">CERT_CONTEXT</a> structure returned by this function. This parameter must be <b>NULL</b> on the first call of the function. To find successive certificates meeting the search criteria,  set <i>pPrevCertContext</i> to the pointer returned by the previous call to the function. This function frees the <b>CERT_CONTEXT</b> referenced by non-<b>NULL</b> values of this parameter.

## -returns

If the function succeeds, the function returns a pointer to a read-only <a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_context">CERT_CONTEXT</a> structure.

If the function fails and a certificate that matches the search criteria is not found, the return value is <b>NULL</b>.

A non-<b>NULL</b> <a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_context">CERT_CONTEXT</a> that <b>CertFindCertificateInStore</b> returns must be freed by 
<a href="/windows/desktop/api/wincrypt/nf-wincrypt-certfreecertificatecontext">CertFreeCertificateContext</a> or by being passed as the <i>pPrevCertContext</i> parameter on a subsequent call to <b>CertFindCertificateInStore</b>.

For extended error information, call 
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
No certificate was found matching the search criteria. This can happen if the store is empty or the end of the store's list is reached.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The handle in the <i>hCertStore</i> parameter is not the same as that in the certificate <a href="/windows/desktop/SecGloss/c-gly">context</a> pointed to by the <i>pPrevCertContext</i> parameter, or a value that is not valid was specified in the <i>dwFindType</i> parameter.

</td>
</tr>
</table>

## -remarks

The <i>dwFindFlags</i> parameter is used to modify the criteria of some search types.

The CERT_UNICODE_IS_RDN_ATTRS_FLAG <i>dwFindFlags</i> value is used only with the CERT_FIND_SUBJECT_ATTR and CERT_FIND_ISSUER_ATTR values for <i>dwFindType</i>. CERT_UNICODE_IS_RDN_ATTRS_FLAG must be set if the <a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_rdn_attr">CERT_RDN_ATTR</a> structure pointed to by <i>pvFindPara</i> was initialized with Unicode strings. Before any comparison is made, the string to be matched is converted by using X509_UNICODE_NAME to provide for Unicode comparisons.

The following <i>dwFindFlags</i> values are used only with the CERT_FIND_ENKEY_USAGE value for <i>dwFindType</i>:




<a href="/windows/desktop/api/wincrypt/nf-wincrypt-certduplicatecertificatecontext">CertDuplicateCertificateContext</a> can be called to make a duplicate of the returned context. The returned context can be added to a different <a href="/windows/desktop/SecGloss/c-gly">certificate store</a> by using 
<a href="/windows/desktop/api/wincrypt/nf-wincrypt-certaddcertificatecontexttostore">CertAddCertificateContextToStore</a>, or a link to that certificate context can be added to a store that is not a collection store by using 
<a href="/windows/desktop/api/wincrypt/nf-wincrypt-certaddcertificatelinktostore">CertAddCertificateLinkToStore</a>.

The returned pointer is freed when passed as the <i>pPrevCertContext</i> parameter on a subsequent call to the function. Otherwise, the pointer must be explicitly freed by calling 
<a href="/windows/desktop/api/wincrypt/nf-wincrypt-certfreecertificatecontext">CertFreeCertificateContext</a>. A <i>pPrevCertContext</i> that is not <b>NULL</b> is always freed by <b>CertFindCertificateInStore</b> using a call to <b>CertFreeCertificateContext</b>, even if there is an error in the function.


#### Examples

The following example shows finding a certificate context in the certificate store meeting a search criterion. For a complete example that includes the  context for this example, see 
<a href="/windows/desktop/SecCrypto/example-c-program-certificate-store-operations">Example C Program: Certificate Store Operations</a>.

For another example that uses this function, see <a href="/windows/desktop/SecCrypto/example-c-program-collection-and-sibling-certificate-store-operations">Example C Program: Collection and Sibling Certificate Store Operations</a>.


```cpp
#include <windows.h>
#include <stdio.h>
#include <Wincrypt.h>
#pragma comment(lib, "crypt32.lib")

#define MY_ENCODING_TYPE  (PKCS_7_ASN_ENCODING | X509_ASN_ENCODING)

void main()
{
//-------------------------------------------------------------------
// Declare and initialize variables.
HCERTSTORE  hSystemStore;              // The system store handle.
PCCERT_CONTEXT  pDesiredCert = NULL;   // Set to NULL for the first 
                                       // call to
                                       // CertFindCertificateInStore.
LPCSTR lpszCertSubject = (LPCSTR) "Cert_subject_1";


//-------------------------------------------------------------------
// Open the certificate store to be searched.

if(hSystemStore = CertOpenStore(
     CERT_STORE_PROV_SYSTEM, 
     0,                      // Encoding type not needed 
                             // with this PROV.
     NULL,                   // Accept the default HCRYPTPROV. 
     CERT_SYSTEM_STORE_CURRENT_USER,
                             // Set the system store location in 
                             // the registry.
     L"MY"))                 // Could have used other predefined 
                             // system stores
                             // including Trust, CA, or Root.
{
   printf("Opened the MY system store. \n");
}
else
{
   printf( "Could not open the MY system store.\n");
   exit(1);
}
//-------------------------------------------------------------------
// Get a certificate that has lpszCertSubject as its 
// subject. 

if(pDesiredCert=CertFindCertificateInStore(
      hSystemStore,
      MY_ENCODING_TYPE,           // Use X509_ASN_ENCODING.
      0,                          // No dwFlags needed. 
      CERT_FIND_SUBJECT_STR,      // Find a certificate with a
                                  // subject that matches the string
                                  // in the next parameter.
      lpszCertSubject ,           // The Unicode string to be found
                                  // in a certificate's subject.
      NULL))                      // NULL for the first call to the
                                  // function. In all subsequent
                                  // calls, it is the last pointer
                                  // returned by the function.
{
  printf("The desired certificate was found. \n");
}
else
{
   printf("Could not find the desired certificate.\n");
}
//-------------------------------------------------------------------
// Clean up. 

if(pDesiredCert)
    CertFreeCertificateContext(pDesiredCert);
if(hSystemStore)
    CertCloseStore(
        hSystemStore, 
        CERT_CLOSE_STORE_CHECK_FLAG);

```

## -see-also

<a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_context">CERT_CONTEXT</a>



<a href="/windows/desktop/api/wincrypt/nf-wincrypt-certaddcertificatecontexttostore">CertAddCertificateContextToStore</a>



<a href="/windows/desktop/api/wincrypt/nf-wincrypt-certaddcertificatelinktostore">CertAddCertificateLinkToStore</a>



<a href="/windows/desktop/api/wincrypt/nf-wincrypt-certduplicatecertificatecontext">CertDuplicateCertificateContext</a>



<a href="/windows/desktop/api/wincrypt/nf-wincrypt-certenumcertificatesinstore">CertEnumCertificatesInStore</a>



<a href="/windows/desktop/api/wincrypt/nf-wincrypt-certfreecertificatecontext">CertFreeCertificateContext</a>



<a href="/windows/desktop/api/wincrypt/nf-wincrypt-certgetcertificatechain">CertGetCertificateChain</a>



<a href="/windows/desktop/api/wincrypt/nf-wincrypt-certnametostra">CertNameToStr</a>



<a href="/windows/desktop/SecCrypto/cryptography-functions">Certificate Functions</a>
