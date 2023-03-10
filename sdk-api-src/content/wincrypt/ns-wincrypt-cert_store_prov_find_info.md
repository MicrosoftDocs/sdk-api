---
UID: NS:wincrypt._CERT_STORE_PROV_FIND_INFO
title: CERT_STORE_PROV_FIND_INFO (wincrypt.h)
description: Used by many of the store provider callback functions.
helpviewer_keywords: ["*PCERT_STORE_PROV_FIND_INFO","CCERT_STORE_PROV_FIND_INFO","CCERT_STORE_PROV_FIND_INFO structure [Security]","CERT_FIND_ANY","CERT_FIND_CERT_ID","CERT_FIND_CTL_USAGE","CERT_FIND_ENHKEY_USAGE","CERT_FIND_EXISTING","CERT_FIND_HASH","CERT_FIND_ISSUER_ATTR","CERT_FIND_ISSUER_NAME","CERT_FIND_ISSUER_OF","CERT_FIND_ISSUER_STR","CERT_FIND_KEY_IDENTIFIER","CERT_FIND_KEY_SPEC","CERT_FIND_MD5_HASH","CERT_FIND_PROPERTY","CERT_FIND_PUBLIC_KEY","CERT_FIND_SHA1_HASH","CERT_FIND_SIGNATURE_HASH","CERT_FIND_SUBJECT_ATTR","CERT_FIND_SUBJECT_CERT","CERT_FIND_SUBJECT_NAME","CERT_FIND_SUBJECT_STR","CERT_STORE_PROV_FIND_INFO","CERT_STORE_PROV_FIND_INFO structure [Security]","PCCERT_STORE_PROV_FIND_INFO","PCCERT_STORE_PROV_FIND_INFO structure pointer [Security]","PCERT_STORE_PROV_FIND_INFO","PCERT_STORE_PROV_FIND_INFO structure pointer [Security]","_crypto2_cert_store_prov_find_info","security.cert_store_prov_find_info","wincrypt/CCERT_STORE_PROV_FIND_INFO","wincrypt/CERT_STORE_PROV_FIND_INFO","wincrypt/PCCERT_STORE_PROV_FIND_INFO","wincrypt/PCERT_STORE_PROV_FIND_INFO"]
old-location: security\cert_store_prov_find_info.htm
tech.root: security
ms.assetid: b3c5960c-7800-485c-b030-199fee027154
ms.date: 12/05/2018
ms.keywords: '*PCERT_STORE_PROV_FIND_INFO, CCERT_STORE_PROV_FIND_INFO, CCERT_STORE_PROV_FIND_INFO structure [Security], CERT_FIND_ANY, CERT_FIND_CERT_ID, CERT_FIND_CTL_USAGE, CERT_FIND_ENHKEY_USAGE, CERT_FIND_EXISTING, CERT_FIND_HASH, CERT_FIND_ISSUER_ATTR, CERT_FIND_ISSUER_NAME, CERT_FIND_ISSUER_OF, CERT_FIND_ISSUER_STR, CERT_FIND_KEY_IDENTIFIER, CERT_FIND_KEY_SPEC, CERT_FIND_MD5_HASH, CERT_FIND_PROPERTY, CERT_FIND_PUBLIC_KEY, CERT_FIND_SHA1_HASH, CERT_FIND_SIGNATURE_HASH, CERT_FIND_SUBJECT_ATTR, CERT_FIND_SUBJECT_CERT, CERT_FIND_SUBJECT_NAME, CERT_FIND_SUBJECT_STR, CERT_STORE_PROV_FIND_INFO, CERT_STORE_PROV_FIND_INFO structure [Security], PCCERT_STORE_PROV_FIND_INFO, PCCERT_STORE_PROV_FIND_INFO structure pointer [Security], PCERT_STORE_PROV_FIND_INFO, PCERT_STORE_PROV_FIND_INFO structure pointer [Security], _crypto2_cert_store_prov_find_info, security.cert_store_prov_find_info, wincrypt/CCERT_STORE_PROV_FIND_INFO, wincrypt/CERT_STORE_PROV_FIND_INFO, wincrypt/PCCERT_STORE_PROV_FIND_INFO, wincrypt/PCERT_STORE_PROV_FIND_INFO'
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
req.typenames: CERT_STORE_PROV_FIND_INFO, *PCERT_STORE_PROV_FIND_INFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _CERT_STORE_PROV_FIND_INFO
 - wincrypt/_CERT_STORE_PROV_FIND_INFO
 - PCERT_STORE_PROV_FIND_INFO
 - wincrypt/PCERT_STORE_PROV_FIND_INFO
 - CERT_STORE_PROV_FIND_INFO
 - wincrypt/CERT_STORE_PROV_FIND_INFO
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
 - CERT_STORE_PROV_FIND_INFO
---

# CERT_STORE_PROV_FIND_INFO structure


## -description

The <b>CERT_STORE_PROV_FIND_INFO</b> structure is used by many of the store provider callback functions. It contains find criteria for finding a <a href="/windows/desktop/SecGloss/c-gly">certificate</a>, <a href="/windows/desktop/SecGloss/c-gly">certificate revocation list</a> (CRL), or <a href="/windows/desktop/SecGloss/c-gly">certificate trust list</a> (CTL) in a <a href="/windows/desktop/SecGloss/c-gly">certificate store</a>.

## -struct-fields

### -field cbSize

Size of the structure.

### -field dwMsgAndCertEncodingType

Specifies the encoding type used for messages and certificates. The certificate and <a href="/windows/desktop/SecGloss/m-gly">message encoding types</a> can be combined with a bitwise-<b>OR</b> operation. Here are the defined encoding types:

<ul>
<li>X509_ASN_ENCODING</li>
<li>PKCS_7_ASN_ENCODING</li>
</ul>

### -field dwFindFlags

Used with some <b>dwFindType</b> values to modify the search criteria. For most <b>dwFindType</b> values, <b>dwFindFlags</b> is not used and should be set to zero.

### -field dwFindType

Specifies the type of search being made. The search type determines the data type, contents, and the use of <b>pvFindPara</b>. Currently defined <b>dwFindType</b> values and the data type each requires for <b>pvFindPara</b> are as follows.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="CERT_FIND_ANY"></a><a id="cert_find_any"></a><dl>
<dt><b>CERT_FIND_ANY</b></dt>
<dt><b>NULL</b>; <b>pvFindPara</b> not used</dt>
</dl>
</td>
<td width="60%">
No search criteria used. Returns the next certificate in the store.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_FIND_CERT_ID"></a><a id="cert_find_cert_id"></a><dl>
<dt><b>CERT_FIND_CERT_ID</b></dt>
<dt>CERT_ID structure</dt>
</dl>
</td>
<td width="60%">
Finds the certificate identified by the specified <b>CERT_ID</b>.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_FIND_CTL_USAGE"></a><a id="cert_find_ctl_usage"></a><dl>
<dt><b>CERT_FIND_CTL_USAGE</b></dt>
<dt>CTL_USAGE structure</dt>
</dl>
</td>
<td width="60%">
Searches for a certificate having a szOID_ENHANCED_KEY_USAGE extension or a CERT_CTL_PROP_ID that matches the <b>pszUsageIdentifier</b> member of the <a href="/windows/desktop/api/wincrypt/ns-wincrypt-ctl_usage">CTL_USAGE</a> structure.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_FIND_ENHKEY_USAGE"></a><a id="cert_find_enhkey_usage"></a><dl>
<dt><b>CERT_FIND_ENHKEY_USAGE</b></dt>
<dt>CERT_ENHKEY_USAGE structure</dt>
</dl>
</td>
<td width="60%">
Searches for a certificate in the store having either an <a href="/windows/desktop/SecGloss/e-gly">enhanced key usage</a> extension or an enhanced key usage property and a usage identifier that matches the <b>pszUsageIdentifier</b> member in the <a href="/windows/desktop/api/wincrypt/ns-wincrypt-ctl_usage">CERT_ENHKEY_USAGE</a> structure. 




A certificate has an enhanced key usage extension if it has a <a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_extension">CERT_EXTENSION</a> structure with the <b>pszObjId</b> member set to szOID_ENHANCED_KEY_USAGE. A certificate has an enhanced key usage property if its CERT_ENHKEY_USAGE_PROP_ID identifier is set.

If <b>pvFindPara</b> is <b>NULL</b> or the <b>cUsageIdentifier</b> member of <a href="/windows/desktop/api/wincrypt/ns-wincrypt-ctl_usage">CERT_ENHKEY_USAGE</a> is zero, any certificate that has either the enhanced key usage extension or the enhanced key usage property meets the selection criteria.

If <b>pvFindPara</b> is <b>NULL</b> or the <b>cUsageIdentifier</b> member of the <a href="/windows/desktop/api/wincrypt/ns-wincrypt-ctl_usage">CERT_ENHKEY_USAGE</a> structure is zero, any certificate having enhanced key usage is a match.

If CERT_FIND_OPTIONAL_ENHKEY_USAGE_FLAG is set in <b>dwFindFlags</b>, certificates without the key usage extension or property are also matches. Setting this flag takes precedence over passing <b>NULL</b> in <b>pvFindPara</b>.

If CERT_FIND_EXT_ONLY_ENHKEY_USAGE_FLAG is set, a match is done only on the key usage extension.

For information about flag modifications to search criteria, see  Remarks.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_FIND_EXISTING"></a><a id="cert_find_existing"></a><dl>
<dt><b>CERT_FIND_EXISTING</b></dt>
<dt>CERT_CONTEXT structure</dt>
</dl>
</td>
<td width="60%">
Searches for a certificate that is an exact match of the specified certificate context.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_FIND_HASH"></a><a id="cert_find_hash"></a><dl>
<dt><b>CERT_FIND_HASH</b></dt>
<dt>
<a href="/previous-versions/windows/desktop/legacy/aa381414(v=vs.85)">CRYPT_HASH_BLOB</a> structure</dt>
</dl>
</td>
<td width="60%">
Searches for a certificate with a SHA1 hash that matches the hash in the <a href="/previous-versions/windows/desktop/legacy/aa381414(v=vs.85)">CRYPT_HASH_BLOB</a> structure.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_FIND_ISSUER_ATTR"></a><a id="cert_find_issuer_attr"></a><dl>
<dt><b>CERT_FIND_ISSUER_ATTR</b></dt>
<dt>CERT_RDN structure</dt>
</dl>
</td>
<td width="60%">
Search for a certificate with specified issuer attributes that match attributes in the <a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_rdn">CERT_RDN</a> structure. If these values are set, the function compares attributes of the issuer in a certificate with elements of the <a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_rdn_attr">CERT_RDN_ATTR</a> array in this <b>CERT_RDN</b> structure. Comparisons iterate through the <b>CERT_RDN_ATTR</b> attributes looking for a match with the certificate's issuer attributes. 




If the <b>pszObjId</b> member of <a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_rdn_attr">CERT_RDN_ATTR</a> is <b>NULL</b>, the attribute object identifier is ignored.

If the <b>dwValueType</b> member of <a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_rdn_attr">CERT_RDN_ATTR</a> is CERT_RDN_ANY_TYPE, the value type is ignored.

If the <b>pbData</b> member of <a href="/previous-versions/windows/desktop/legacy/aa381414(v=vs.85)">CERT_RDN_VALUE_BLOB</a> is <b>NULL</b>, any value is a match.

Currently, only an exact, case-sensitive match is supported. For information about Unicode options, see  Remarks. When these values are set, the search is restricted to certificates whose encoding type matches <b>dwMsgAndCertEncodingType</b>.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_FIND_ISSUER_NAME"></a><a id="cert_find_issuer_name"></a><dl>
<dt><b>CERT_FIND_ISSUER_NAME</b></dt>
<dt>
<a href="/previous-versions/windows/desktop/legacy/aa381414(v=vs.85)">CERT_NAME_BLOB</a> structure</dt>
</dl>
</td>
<td width="60%">
Search for a certificate with an exact match of the entire issuer name with the name in <a href="/previous-versions/windows/desktop/legacy/aa381414(v=vs.85)">CERT_NAME_BLOB</a>. The search is restricted to certificates that match the <b>dwMsgAndCertEncodingType</b>.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_FIND_ISSUER_OF"></a><a id="cert_find_issuer_of"></a><dl>
<dt><b>CERT_FIND_ISSUER_OF</b></dt>
<dt>CERT_CONTEXT structure</dt>
</dl>
</td>
<td width="60%">
Searches for a certificate with an issuer that matches the issuer in <a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_context">CERT_CONTEXT</a>. 




Instead of using the <a href="/windows/desktop/api/wincrypt/nf-wincrypt-certfindcertificateinstore">CertFindCertificateInStore</a> function with this value, use the 
<a href="/windows/desktop/api/wincrypt/nf-wincrypt-certgetcertificatechain">CertGetCertificateChain</a> function.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_FIND_ISSUER_STR"></a><a id="cert_find_issuer_str"></a><dl>
<dt><b>CERT_FIND_ISSUER_STR</b></dt>
<dt><b>Null</b>-terminated wide (Unicode) string</dt>
</dl>
</td>
<td width="60%">
Search for a certificate that contains the specified issuer name string. The certificate's issuer member is converted to a name string of the appropriate type using the appropriate form of 
<a href="/windows/desktop/api/wincrypt/nf-wincrypt-certnametostra">CertNameToStr</a> formatted as CERT_SIMPLE_NAME_STR. Then a case-insensitive substring-within-a-string match is performed. When this value is set, the search is restricted to certificates whose encoding type matches <b>dwMsgAndCertEncodingType</b>.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_FIND_KEY_IDENTIFIER"></a><a id="cert_find_key_identifier"></a><dl>
<dt><b>CERT_FIND_KEY_IDENTIFIER</b></dt>
<dt>
<a href="/previous-versions/windows/desktop/legacy/aa381414(v=vs.85)">CRYPT_HASH_BLOB</a> structure</dt>
</dl>
</td>
<td width="60%">
Searches for a certificate with a CERT_KEY_IDENTIFIER_PROP_ID property matching the key identifier in <a href="/previous-versions/windows/desktop/legacy/aa381414(v=vs.85)">CRYPT_HASH_BLOB</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_FIND_KEY_SPEC"></a><a id="cert_find_key_spec"></a><dl>
<dt><b>CERT_FIND_KEY_SPEC</b></dt>
<dt>DWORD containing a key specification</dt>
</dl>
</td>
<td width="60%">
Searches for a certificate having a CERT_KEY_SPEC_PROP_ID property matching the key specification in <b>pvFindPara</b>.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_FIND_MD5_HASH"></a><a id="cert_find_md5_hash"></a><dl>
<dt><b>CERT_FIND_MD5_HASH</b></dt>
<dt>
<a href="/previous-versions/windows/desktop/legacy/aa381414(v=vs.85)">CRYPT_HASH_BLOB</a> structure</dt>
</dl>
</td>
<td width="60%">
Searches for a certificate with an MD5 hash that matches the hash in <a href="/previous-versions/windows/desktop/legacy/aa381414(v=vs.85)">CRYPT_HASH_BLOB</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_FIND_PROPERTY"></a><a id="cert_find_property"></a><dl>
<dt><b>CERT_FIND_PROPERTY</b></dt>
<dt>DWORD that contains a property identifier</dt>
</dl>
</td>
<td width="60%">
Searches for a certificate with a property that matches the property identifier specified by the <b>DWORD</b> in <b>pvFindPara</b>.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_FIND_PUBLIC_KEY"></a><a id="cert_find_public_key"></a><dl>
<dt><b>CERT_FIND_PUBLIC_KEY</b></dt>
<dt>CERT_PUBLIC_KEY_INFO structure</dt>
</dl>
</td>
<td width="60%">
Searches for a certificate with a public key that matches the public key in the <a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_public_key_info">CERT_PUBLIC_KEY_INFO</a> structure.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_FIND_SHA1_HASH"></a><a id="cert_find_sha1_hash"></a><dl>
<dt><b>CERT_FIND_SHA1_HASH</b></dt>
<dt>
<a href="/previous-versions/windows/desktop/legacy/aa381414(v=vs.85)">CRYPT_HASH_BLOB</a> structure</dt>
</dl>
</td>
<td width="60%">
Searches for a certificate with a SHA1 hash that matches the hash in the <a href="/previous-versions/windows/desktop/legacy/aa381414(v=vs.85)">CRYPT_HASH_BLOB</a> structure.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_FIND_SIGNATURE_HASH"></a><a id="cert_find_signature_hash"></a><dl>
<dt><b>CERT_FIND_SIGNATURE_HASH</b></dt>
<dt>
<a href="/previous-versions/windows/desktop/legacy/aa381414(v=vs.85)">CRYPT_HASH_BLOB</a> structure</dt>
</dl>
</td>
<td width="60%">
Searches for a certificate with a signature hash that matches the signature hash in the <a href="/previous-versions/windows/desktop/legacy/aa381414(v=vs.85)">CRYPT_HASH_BLOB</a> structure.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_FIND_SUBJECT_ATTR"></a><a id="cert_find_subject_attr"></a><dl>
<dt><b>CERT_FIND_SUBJECT_ATTR</b></dt>
<dt>CERT_RDN structure</dt>
</dl>
</td>
<td width="60%">
Searches for a certificate with specified subject attributes that match attributes in the <a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_rdn">CERT_RDN</a> structure. If RDN values are set, the function compares attributes of the subject in a certificate with elements of the <a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_rdn_attr">CERT_RDN_ATTR</a> array in this <b>CERT_RDN</b> structure. Comparisons iterate through the <b>CERT_RDN_ATTR</b> attributes looking for a match with the certificate's subject's attributes. 




If the <b>pszObjId</b> member of <a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_rdn_attr">CERT_RDN_ATTR</a> is <b>NULL</b>, the attribute object identifier is ignored.

If the <b>dwValueType</b> member of <a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_rdn_attr">CERT_RDN_ATTR</a> is CERT_RDN_ANY_TYPE, the value type is ignored.

If the <b>pbData</b> member of <a href="/previous-versions/windows/desktop/legacy/aa381414(v=vs.85)">CERT_RDN_VALUE_BLOB</a> is <b>NULL</b>, any value is a match.

Currently, only an exact, case-sensitive match is supported.

For information about Unicode options, see  Remarks. When these values are set, the search is restricted to certificates whose encoding type matches <b>dwMsgAndCertEncodingType</b>.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_FIND_SUBJECT_CERT"></a><a id="cert_find_subject_cert"></a><dl>
<dt><b>CERT_FIND_SUBJECT_CERT</b></dt>
<dt>CERT_INFO structure</dt>
</dl>
</td>
<td width="60%">
Searches for a certificate with both an issuer and a serial number that match the issuer and serial number in the <a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_info">CERT_INFO</a> structure.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_FIND_SUBJECT_NAME"></a><a id="cert_find_subject_name"></a><dl>
<dt><b>CERT_FIND_SUBJECT_NAME</b></dt>
<dt>
<a href="/previous-versions/windows/desktop/legacy/aa381414(v=vs.85)">CERT_NAME_BLOB</a> structure</dt>
</dl>
</td>
<td width="60%">
Searches for a certificate with an exact match of the entire subject name with the name in the <a href="/previous-versions/windows/desktop/legacy/aa381414(v=vs.85)">CERT_NAME_BLOB</a> structure. The search is restricted to certificates that match the value of <b>dwMsgAndCertEncodingType</b>.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_FIND_SUBJECT_STR"></a><a id="cert_find_subject_str"></a><dl>
<dt><b>CERT_FIND_SUBJECT_STR</b></dt>
<dt><b>Null</b>-terminated wide (Unicode) string</dt>
</dl>
</td>
<td width="60%">
Searches for a certificate that contains the specified subject name string. The certificate's subject member is converted to a name string of the appropriate type using the appropriate form of 
<a href="/windows/desktop/api/wincrypt/nf-wincrypt-certnametostra">CertNameToStr</a> formatted as CERT_SIMPLE_NAME_STR. Then a case-insensitive substring-within-a-string match is performed. When this value is set, the search is restricted to certificates whose encoding type matches <b>dwMsgAndCertEncodingType</b>.

</td>
</tr>
</table>
 

<div class="alert"><b>Note</b>  There are alternate forms of  the value of <b>dwFindType</b> that pass a string in <b>pvFindPara</b>. One form uses a Unicode string, and the other an <a href="/windows/desktop/SecGloss/a-gly">ASCII</a> string. Values that end in "_W" or without a suffix use Unicode. Values that end with "_A" use <i>ASCII</i> strings.</div>
<div> </div>

### -field pvFindPara

Points to a data item or structure to be used with the find type indicated by the value of <b>dwFindType</b>.

## -remarks

The <b>dwFindFlags</b> member is used to modify the criteria of some search types.

The <b>dwFindFlags</b> value of CERT_UNICODE_IS_RDN_ATTRS_FLAG is used only with the CERT_FIND_SUBJECT_ATTR and CERT_FIND_ISSUER_ATTR values for <b>dwFindType</b>. CERT_UNICODE_IS_RDN_ATTRS_FLAG must be set if the <a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_rdn_attr">CERT_RDN_ATTR</a> structure pointed to by <b>pvFindPara</b> was initialized with Unicode strings. Before any comparison is made, the string to be matched is converted by using X509_UNICODE_NAME to provide for Unicode comparisons.

The following <b>dwFindFlags</b> values are used only with the CERT_FIND_ENKEY_USAGE value for <b>dwFindType</b>.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td>CERT_FIND_OR_ENHKEY_USAGE_FLAG</td>
<td>The search criteria can be altered by setting one or more flags. By default, if the <b>pszUsageIdentifier</b> member of the <a href="/windows/desktop/api/wincrypt/ns-wincrypt-ctl_usage">CERT_ENHKEY_USAGE</a> structure pointed to by <b>pvFindPara</b> is to be matched, each identifier must be matched to satisfy the search criteria. However, if CERT_FIND_OR_ENHKEY_USAGE_FLAG is set, a match can be made to all identifiers combined by using a bitwise-<b>OR</b> operation; thus, matching any one of the identifiers is sufficient.</td>
</tr>
<tr>
<td>CERT_FIND_OPTIONAL_ENHKEY_USAGE_FLAG</td>
<td>When this flag is set, in addition to usual matches, any certificate that has neither the enhanced key usage extension nor the enhanced key usage property meets the search criteria.</td>
</tr>
<tr>
<td>CERT_FIND_NO_ENHKEY_USAGE_FLAG</td>
<td>When this flag is set, only those certificates that have neither an enhanced key usage nor the enhanced key usage property are matches. This flag setting takes precedence over <b>pvFindPara</b> being <b>NULL</b>.</td>
</tr>
<tr>
<td>CERT_FIND_VALID_ENHKEY_USAGE_FLAG</td>
<td>When this flag is set, the function only matches those certificates that are valid for the specified usage. By default, in order to match, a certificate must be valid for all usages. 


CERT_FIND_OR_ENHKEY_USAGE_FLAG can also be set if the certificate only needs to be valid for one of the specified usages. Note that <a href="/windows/desktop/api/wincrypt/nf-wincrypt-certgetvalidusages">CertGetValidUsages</a> is called to get the list of valid uses for the certificate. Only CERT_FIND_OR_ENHKEY_USAGE_FLAG can also apply when CERT_FIND_VALID_ENHKEY_USAGE_FLAG is set.

</td>
</tr>
<tr>
<td>CERT_FIND_EXT_ONLY_ENHKEY_USAGE_FLAG</td>
<td>When this flag is set, the matching process involves only the extension usage identifiers. If <b>pvFindPara</b> is <b>NULL</b> or the <b>cUsageIdentifier</b> member of the <a href="/windows/desktop/api/wincrypt/ns-wincrypt-ctl_usage">CERT_ENHKEY_USAGE</a> structure pointed to by <b>pvFindPara</b> is zero, any certificate having an enhanced key usage extension is a match. If CERT_FIND_OPTIONAL_ENHKEY_USAGE_FLAG is also set, any certificate without the enhanced key usage extension is also a match. If CERT_FIND_NO_ENHKEY_USAGE_FLAG is also set, only certificates without the enhanced key usage extension are matches.</td>
</tr>
<tr>
<td>CERT_FIND_EXT_PROP_ENHKEY_USAGE_FLAG</td>
<td>When this flag is set, the matching process involves only usage identifiers that are properties. If <b>pvFindPara</b> is <b>NULL</b> or <b>cUsageIdentifier</b> is set to zero, any certificate having an enhanced key usage property is a match. If CERT_FIND_OPTIONAL_ENHKEY_USAGE_FLAG is also set, any certificate without the enhanced key usage property is also a match. If CERT_FIND_NO_ENHKEY_USAGE_FLAG is set, only certificates without the enhanced key usage property are matches.</td>
</tr>
<tr>
<td>CERT_CASE_INSENSITIVE_IS_RDN_ATTRS_FLAG</td>
<td>Used only with CERT_FIND_SUBJECT_ATTR and CERT_FIND_ISSUER-ATTR values of <b>dwFindType</b>. By default, a case-sensitive, exact match is made. If this flag is set, the match is case-insensitive.</td>
</tr>
</table>