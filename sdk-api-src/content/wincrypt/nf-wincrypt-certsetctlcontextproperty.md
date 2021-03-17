---
UID: NF:wincrypt.CertSetCTLContextProperty
title: CertSetCTLContextProperty function (wincrypt.h)
description: Sets an extended property for the specified certificate trust list (CTL) context.
helpviewer_keywords: ["CERT_ARCHIVED_PROP_ID","CERT_AUTO_ENROLL_PROP_ID","CERT_CTL_USAGE_PROP_ID","CERT_DESCRIPTION_PROP_ID","CERT_ENHKEY_USAGE_PROP_ID","CERT_FRIENDLY_NAME_PROP_ID","CERT_HASH_PROP_ID","CERT_KEY_CONTEXT_PROP_ID","CERT_KEY_IDENTIFIER_PROP_ID","CERT_KEY_PROV_HANDLE_PROP_ID","CERT_KEY_PROV_INFO_PROP_ID","CERT_KEY_SPEC_PROP_ID","CERT_MD5_HASH_PROP_ID","CERT_NEXT_UPDATE_LOCATION_PROP_ID","CERT_PVK_FILE_PROP_ID","CERT_SHA1_HASH_PROP_ID","CERT_SIGNATURE_HASH_PROP_ID","CertSetCTLContextProperty","CertSetCTLContextProperty function [Security]","_crypto2_certsetctlcontextproperty","security.certsetctlcontextproperty","wincrypt/CertSetCTLContextProperty"]
old-location: security\certsetctlcontextproperty.htm
tech.root: security
ms.assetid: 3af01ca6-6fa1-4510-872a-b5e13e07f49f
ms.date: 12/05/2018
ms.keywords: CERT_ARCHIVED_PROP_ID, CERT_AUTO_ENROLL_PROP_ID, CERT_CTL_USAGE_PROP_ID, CERT_DESCRIPTION_PROP_ID, CERT_ENHKEY_USAGE_PROP_ID, CERT_FRIENDLY_NAME_PROP_ID, CERT_HASH_PROP_ID, CERT_KEY_CONTEXT_PROP_ID, CERT_KEY_IDENTIFIER_PROP_ID, CERT_KEY_PROV_HANDLE_PROP_ID, CERT_KEY_PROV_INFO_PROP_ID, CERT_KEY_SPEC_PROP_ID, CERT_MD5_HASH_PROP_ID, CERT_NEXT_UPDATE_LOCATION_PROP_ID, CERT_PVK_FILE_PROP_ID, CERT_SHA1_HASH_PROP_ID, CERT_SIGNATURE_HASH_PROP_ID, CertSetCTLContextProperty, CertSetCTLContextProperty function [Security], _crypto2_certsetctlcontextproperty, security.certsetctlcontextproperty, wincrypt/CertSetCTLContextProperty
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
 - CertSetCTLContextProperty
 - wincrypt/CertSetCTLContextProperty
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
 - CertSetCTLContextProperty
---

# CertSetCTLContextProperty function


## -description

The <b>CertSetCTLContextProperty</b> function sets an extended property for the specified <a href="/windows/desktop/SecGloss/c-gly">certificate trust list</a> (CTL) context.

## -parameters

### -param pCtlContext [in]

A pointer to the 
<a href="/windows/desktop/api/wincrypt/ns-wincrypt-ctl_context">CTL_CONTEXT</a> structure.

### -param dwPropId [in]

Identifies the property to be set. The value of <i>dwPropId</i> determines the type and content of the <i>pvData</i> parameter. Currently defined identifiers and their related <i>pvData</i> types are as follows. 




					

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="CERT_ARCHIVED_PROP_ID"></a><a id="cert_archived_prop_id"></a><dl>
<dt><b>CERT_ARCHIVED_PROP_ID</b></dt>
</dl>
</td>
<td width="60%">
Data type of <i>pvData</i>: <b>NULL</b>

Indicates the certificate is skipped during enumerations. A certificate with this property set is still found with explicit search operations—such as finding a certificate with a specific <a href="/windows/desktop/SecGloss/h-gly">hash</a> or a specific serial number.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_AUTO_ENROLL_PROP_ID"></a><a id="cert_auto_enroll_prop_id"></a><dl>
<dt><b>CERT_AUTO_ENROLL_PROP_ID</b></dt>
</dl>
</td>
<td width="60%">
Data type of <i>pvData</i>: pointer to a <a href="/previous-versions/windows/desktop/legacy/aa381414(v=vs.85)">CRYPT_DATA_BLOB</a>


Property set after a certificate has been enrolled using Auto Enroll. The <a href="/previous-versions/windows/desktop/legacy/aa381414(v=vs.85)">CRYPT_DATA_BLOB</a> structure pointed to by <i>pvData</i> includes a <b>null</b>-terminated, Unicode name of the certificate type for which the certificates has been auto enrolled. Any subsequent calls to Auto Enroll for the certificate checks for this property to determine whether the certificate has been enrolled.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_CTL_USAGE_PROP_ID"></a><a id="cert_ctl_usage_prop_id"></a><dl>
<dt><b>CERT_CTL_USAGE_PROP_ID</b></dt>
</dl>
</td>
<td width="60%">
Data type of <i>pvData</i>: pointer to a <a href="/previous-versions/windows/desktop/legacy/aa381414(v=vs.85)">CRYPT_DATA_BLOB</a>


<i>pvData</i> points to a <a href="/previous-versions/windows/desktop/legacy/aa381414(v=vs.85)">CRYPT_DATA_BLOB</a> structure containing an <a href="/windows/desktop/SecGloss/a-gly">Abstract Syntax Notation One</a> (ASN.1) encoded 
<a href="/windows/desktop/api/wincrypt/ns-wincrypt-ctl_usage">CTL_USAGE</a> structure. This structure was encoded using <a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptencodeobject">CryptEncodeObject</a> with X509_ENHANCED_KEY_USAGE value set.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_DESCRIPTION_PROP_ID"></a><a id="cert_description_prop_id"></a><dl>
<dt><b>CERT_DESCRIPTION_PROP_ID</b></dt>
</dl>
</td>
<td width="60%">
Data type of <i>pvData</i>: pointer to a <a href="/previous-versions/windows/desktop/legacy/aa381414(v=vs.85)">CRYPT_DATA_BLOB</a>


Property set and displayed by the certificate UI. This property allows the user to describe the certificate's use.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_ENHKEY_USAGE_PROP_ID"></a><a id="cert_enhkey_usage_prop_id"></a><dl>
<dt><b>CERT_ENHKEY_USAGE_PROP_ID</b></dt>
</dl>
</td>
<td width="60%">
Data type of <i>pvData</i>: pointer to a <a href="/previous-versions/windows/desktop/legacy/aa381414(v=vs.85)">CRYPT_DATA_BLOB</a>


The <a href="/previous-versions/windows/desktop/legacy/aa381414(v=vs.85)">CRYPT_DATA_BLOB</a> structure containing an ASN.1 encoded <a href="/windows/desktop/api/wincrypt/ns-wincrypt-ctl_usage">CERT_ENHKEY_USAGE</a> structure. This structure was encoded using <a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptencodeobject">CryptEncodeObject</a> with X509_ENHANCED_KEY_USAGE value set.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_FRIENDLY_NAME_PROP_ID"></a><a id="cert_friendly_name_prop_id"></a><dl>
<dt><b>CERT_FRIENDLY_NAME_PROP_ID</b></dt>
</dl>
</td>
<td width="60%">
Data type of <i>pvData</i>: pointer to a <a href="/previous-versions/windows/desktop/legacy/aa381414(v=vs.85)">CRYPT_DATA_BLOB</a>


The  <a href="/previous-versions/windows/desktop/legacy/aa381414(v=vs.85)">CRYPT_DATA_BLOB</a> structure specifies the display name of the certificate.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_HASH_PROP_ID"></a><a id="cert_hash_prop_id"></a><dl>
<dt><b>CERT_HASH_PROP_ID</b></dt>
</dl>
</td>
<td width="60%">
Data type of <i>pvData</i>: pointer to a <a href="/previous-versions/windows/desktop/legacy/aa381414(v=vs.85)">CRYPT_HASH_BLOB</a>


This property is implicitly set by a call to 
<a href="/windows/desktop/api/wincrypt/nf-wincrypt-certgetcertificatecontextproperty">CertGetCertificateContextProperty</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_KEY_CONTEXT_PROP_ID"></a><a id="cert_key_context_prop_id"></a><dl>
<dt><b>CERT_KEY_CONTEXT_PROP_ID</b></dt>
</dl>
</td>
<td width="60%">
Data type of <i>pvData</i>: pointer to a <a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_key_context">CERT_KEY_CONTEXT</a>


The <a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_key_context">CERT_KEY_CONTEXT</a> structure  contains both the <a href="/windows/desktop/SecCrypto/hcryptprov">HCRYPTPROV</a> value and the key specification for the private key. For more information about the <b>hCryptProv</b> member and <i>dwFlags</i> settings, see CERT_KEY_PROV_HANDLE_PROP_ID, following. Note that more <b>CERT_KEY_CONTEXT</b> structure members can be added for this property. If so, the <b>cbSize</b> member value will be adjusted accordingly. The <b>cbSize</b> member must be set to the size of the <b>CERT_KEY_CONTEXT</b> structure

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_KEY_IDENTIFIER_PROP_ID"></a><a id="cert_key_identifier_prop_id"></a><dl>
<dt><b>CERT_KEY_IDENTIFIER_PROP_ID</b></dt>
</dl>
</td>
<td width="60%">
Data type of <i>pvData</i>: pointer to a <a href="/previous-versions/windows/desktop/legacy/aa381414(v=vs.85)">CRYPT_DATA_BLOB</a>


This property is typically implicitly set by a call to 
<a href="/windows/desktop/api/wincrypt/nf-wincrypt-certgetcertificatecontextproperty">CertGetCertificateContextProperty</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_KEY_PROV_HANDLE_PROP_ID"></a><a id="cert_key_prov_handle_prop_id"></a><dl>
<dt><b>CERT_KEY_PROV_HANDLE_PROP_ID</b></dt>
</dl>
</td>
<td width="60%">
Data type of <i>pvData</i>: pointer to a <a href="/windows/desktop/SecCrypto/hcryptprov">HCRYPTPROV</a>


An <a href="/windows/desktop/SecCrypto/hcryptprov">HCRYPTPROV</a> handle for the certificate's private key is passed. The <b>hCryptProv</b> member of the <a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_key_context">CERT_KEY_CONTEXT</a> structure is updated if it exists. If it does not exist, it is created with <b>dwKeySpec</b> initialized by CERT_KEY_PROV_INFO_PROP_ID. If CERT_STORE_NO_CRYPT_RELEASE_FLAG is not set, the <b>hCryptProv</b> value is implicitly released either when the property is set to <b>NULL</b> or on the final freeing of the 
<a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_context">CERT_CONTEXT</a> structure.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_KEY_PROV_INFO_PROP_ID"></a><a id="cert_key_prov_info_prop_id"></a><dl>
<dt><b>CERT_KEY_PROV_INFO_PROP_ID</b></dt>
</dl>
</td>
<td width="60%">
Data type of <i>pvData</i>: pointer to a <a href="/windows/desktop/api/wincrypt/ns-wincrypt-crypt_key_prov_info">CRYPT_KEY_PROV_INFO</a>


The <a href="/windows/desktop/api/wincrypt/ns-wincrypt-crypt_key_prov_info">CRYPT_KEY_PROV_INFO</a> structure specifies the certificate's private key.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_KEY_SPEC_PROP_ID"></a><a id="cert_key_spec_prop_id"></a><dl>
<dt><b>CERT_KEY_SPEC_PROP_ID</b></dt>
</dl>
</td>
<td width="60%">
Data type of <i>pvData</i>: pointer to a <b>DWORD</b>

The <b>DWORD</b> value specifies the private key. The <b>dwKeySpec</b> member of the <a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_key_context">CERT_KEY_CONTEXT</a> structure is updated if it exists. If it does not, it is created with <b>hCryptProv</b> set to zero.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_MD5_HASH_PROP_ID"></a><a id="cert_md5_hash_prop_id"></a><dl>
<dt><b>CERT_MD5_HASH_PROP_ID</b></dt>
</dl>
</td>
<td width="60%">
Data type of <i>pvData</i>: pointer to a <a href="/previous-versions/windows/desktop/legacy/aa381414(v=vs.85)">CRYPT_HASH_BLOB</a>


This property is implicitly set by a call to 
<a href="/windows/desktop/api/wincrypt/nf-wincrypt-certgetcertificatecontextproperty">CertGetCertificateContextProperty</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_NEXT_UPDATE_LOCATION_PROP_ID"></a><a id="cert_next_update_location_prop_id"></a><dl>
<dt><b>CERT_NEXT_UPDATE_LOCATION_PROP_ID</b></dt>
</dl>
</td>
<td width="60%">
Data type of <i>pvData</i>: pointer to a <a href="/previous-versions/windows/desktop/legacy/aa381414(v=vs.85)">CRYPT_DATA_BLOB</a>


The <a href="/previous-versions/windows/desktop/legacy/aa381414(v=vs.85)">CRYPT_DATA_BLOB</a> structure contains an ASN.1 encoded 
<a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_alt_name_info">CERT_ALT_NAME_INFO</a> structure encoded using <a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptencodeobject">CryptEncodeObject</a> with the X509_ALTERNATE_NAME value set. CERT_NEXT_UPDATE_LOCATION_PROP_ID is currently used only with CTLs.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_PVK_FILE_PROP_ID"></a><a id="cert_pvk_file_prop_id"></a><dl>
<dt><b>CERT_PVK_FILE_PROP_ID</b></dt>
</dl>
</td>
<td width="60%">
Data type of <i>pvData</i>: pointer to a <a href="/previous-versions/windows/desktop/legacy/aa381414(v=vs.85)">CRYPT_DATA_BLOB</a>


The <a href="/previous-versions/windows/desktop/legacy/aa381414(v=vs.85)">CRYPT_DATA_BLOB</a> structure specifies the name of a file containing the private key associated with the certificate's public key. Inside the <b>CRYPT_DATA_BLOB</b> structure, the <b>pbData</b> member is a pointer to a <b>null</b>-terminated Unicode, wide-character string, and the <b>cbData</b> member indicates the length of the string.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_SHA1_HASH_PROP_ID"></a><a id="cert_sha1_hash_prop_id"></a><dl>
<dt><b>CERT_SHA1_HASH_PROP_ID</b></dt>
</dl>
</td>
<td width="60%">
Data type of <i>pvData</i>: pointer to a <a href="/previous-versions/windows/desktop/legacy/aa381414(v=vs.85)">CRYPT_HASH_BLOB</a>


This property is implicitly set by a call to 
<a href="/windows/desktop/api/wincrypt/nf-wincrypt-certgetcertificatecontextproperty">CertGetCertificateContextProperty</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_SIGNATURE_HASH_PROP_ID"></a><a id="cert_signature_hash_prop_id"></a><dl>
<dt><b>CERT_SIGNATURE_HASH_PROP_ID</b></dt>
<dt>
<a href="/previous-versions/windows/desktop/legacy/aa381414(v=vs.85)">CRYPT_HASH_BLOB</a>
</dt>
</dl>
</td>
<td width="60%">
Data type of <i>pvData</i>: pointer to a <a href="/previous-versions/windows/desktop/legacy/aa381414(v=vs.85)">CRYPT_HASH_BLOB</a>


If a signature hash does not exist, it is computed with 
<a href="/windows/desktop/api/wincrypt/nf-wincrypt-crypthashtobesigned">CryptHashToBeSigned</a>. <i>pvData</i> points to an existing or computed hash. Usually, the length of the hash is 20 bytes for SHA and 16 for MD5.

</td>
</tr>
</table>
 

Typically, only the CERT_NEXT_UPDATE_LOCATION_PROP_ID property is set.

Additional <i>dwPropId</i> types can be defined by the user using <b>DWORD</b> values from CERT_FIRST_USER_PROP_ID to CERT_LAST_USER_PROP_ID. For all user-defined <i>dwPropId</i> types, <i>pvData</i> points to an encoded <a href="/previous-versions/windows/desktop/legacy/aa381414(v=vs.85)">CRYPT_DATA_BLOB</a> structure.

### -param dwFlags [in]

CERT_STORE_NO_CRYPT_RELEASE_FLAG can be set for the CERT_KEY_PROV_HANDLE_PROP_ID or CERT_KEY_CONTEXT_PROP_ID <i>dwPropId</i> properties. 




If the CERT_SET_PROPERTY_IGNORE_PERSIST_ERROR_FLAG value is set, any provider-write errors are ignored and the cached context's properties are always set.

If CERT_SET_PROPERTY_INHIBIT_PERSIST_FLAG is set, any property set is not persisted.

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
Invalid property identifier. For details, see 
<a href="/windows/desktop/api/wincrypt/nf-wincrypt-certsetcertificatecontextproperty">CertSetCertificateContextProperty</a>.

</td>
</tr>
</table>

## -remarks

If a property already exists, its old value is replaced.


#### Examples

See 
<a href="/windows/desktop/SecCrypto/example-c-program-getting-and-setting-certificate-properties">Example C Program: Getting and Setting Certificate Properties</a>.

<div class="code"></div>

## -see-also

<a href="/windows/desktop/api/wincrypt/nf-wincrypt-certgetctlcontextproperty">CertGetCTLContextProperty</a>



<a href="/windows/desktop/api/wincrypt/nf-wincrypt-certsetcertificatecontextproperty">CertSetCertificateContextProperty</a>



<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptencodeobject">CryptEncodeObject</a>



<a href="/windows/desktop/SecCrypto/cryptography-functions">Extended Property Functions</a>