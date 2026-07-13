---
UID: NF:wincrypt.CryptRetrieveObjectByUrlA
title: CryptRetrieveObjectByUrlA function (wincrypt.h)
description: Retrieves the public key infrastructure (PKI) object from a location specified by a URL. (ANSI)
helpviewer_keywords: ["CONTEXT_OID_CAPI2_ANY", "CONTEXT_OID_CERTIFICATE", "CONTEXT_OID_CRL", "CONTEXT_OID_CTL", "CONTEXT_OID_OCSP_RESP", "CONTEXT_OID_PKCS7", "CRYPT_AIA_RETRIEVAL", "CRYPT_ASYNC_RETRIEVAL", "CRYPT_CACHE_ONLY_RETRIEVAL", "CRYPT_DONT_CACHE_RESULT", "CRYPT_HTTP_POST_RETRIEVAL", "CRYPT_LDAP_AREC_EXCLUSIVE_RETRIEVAL", "CRYPT_LDAP_INSERT_ENTRY_ATTRIBUTE", "CRYPT_LDAP_SCOPE_BASE_ONLY_RETRIEVAL", "CRYPT_LDAP_SIGN_RETRIEVAL", "CRYPT_NOT_MODIFIED_RETRIEVAL", "CRYPT_NO_AUTH_RETRIEVAL", "CRYPT_OFFLINE_CHECK_RETRIEVAL", "CRYPT_PROXY_CACHE_RETRIEVAL", "CRYPT_RETRIEVE_MULTIPLE_OBJECTS", "CRYPT_STICKY_CACHE_RETRIEVAL", "CRYPT_VERIFY_CONTEXT_SIGNATURE", "CRYPT_VERIFY_DATA_HASH", "CRYPT_WIRE_ONLY_RETRIEVAL", "CryptRetrieveObjectByUrlA", "NULL", "wincrypt/CryptRetrieveObjectByUrlA"]
old-location: security\cryptretrieveobjectbyurl.htm
tech.root: security
ms.assetid: 2e205f97-be9b-4358-ba22-d475b6a250b7
ms.date: 12/05/2018
ms.keywords: CONTEXT_OID_CAPI2_ANY, CONTEXT_OID_CERTIFICATE, CONTEXT_OID_CRL, CONTEXT_OID_CTL, CONTEXT_OID_OCSP_RESP, CONTEXT_OID_PKCS7, CRYPT_AIA_RETRIEVAL, CRYPT_ASYNC_RETRIEVAL, CRYPT_CACHE_ONLY_RETRIEVAL, CRYPT_DONT_CACHE_RESULT, CRYPT_HTTP_POST_RETRIEVAL, CRYPT_LDAP_AREC_EXCLUSIVE_RETRIEVAL, CRYPT_LDAP_INSERT_ENTRY_ATTRIBUTE, CRYPT_LDAP_SCOPE_BASE_ONLY_RETRIEVAL, CRYPT_LDAP_SIGN_RETRIEVAL, CRYPT_NOT_MODIFIED_RETRIEVAL, CRYPT_NO_AUTH_RETRIEVAL, CRYPT_OFFLINE_CHECK_RETRIEVAL, CRYPT_PROXY_CACHE_RETRIEVAL, CRYPT_RETRIEVE_MULTIPLE_OBJECTS, CRYPT_STICKY_CACHE_RETRIEVAL, CRYPT_VERIFY_CONTEXT_SIGNATURE, CRYPT_VERIFY_DATA_HASH, CRYPT_WIRE_ONLY_RETRIEVAL, CryptRetrieveObjectByUrl, CryptRetrieveObjectByUrl function [Security], CryptRetrieveObjectByUrlA, CryptRetrieveObjectByUrlW, NULL, _crypto2_cryptretrieveobjectbyurl, security.cryptretrieveobjectbyurl, wincrypt/CryptRetrieveObjectByUrl, wincrypt/CryptRetrieveObjectByUrlA, wincrypt/CryptRetrieveObjectByUrlW
req.header: wincrypt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: CryptRetrieveObjectByUrlW (Unicode) and CryptRetrieveObjectByUrlA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Cryptnet.lib
req.dll: Cryptnet.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CryptRetrieveObjectByUrlA
 - wincrypt/CryptRetrieveObjectByUrlA
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Cryptnet.dll
api_name:
 - CryptRetrieveObjectByUrl
 - CryptRetrieveObjectByUrlA
 - CryptRetrieveObjectByUrlW
---

# CryptRetrieveObjectByUrlA function


## -description

The <b>CryptRetrieveObjectByUrl</b> function retrieves the public key infrastructure (PKI) object from a location specified by a URL.

These remote objects are in encoded format and are retrieved in a "context" form.

## -parameters

### -param pszUrl [in]

The address of a PKI object to be retrieved. The following schemes are supported:

<ul>
<li>ldap (<a href="/windows/desktop/SecGloss/l-gly">Lightweight Directory Access Protocol</a>)</li>
<li>http</li>
<li>https (<a href="/windows/desktop/SecGloss/c-gly">certificate revocation list</a> (CRL) or <a href="/windows/desktop/SecGloss/o-gly">online certificate status protocol</a> (OCSP) retrievals only)</li>
<li>file</li>
</ul>

### -param pszObjectOid [in]

The address of a null-terminated ANSI string that identifies the type of object to retrieve. This can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="NULL"></a><a id="null"></a><dl>
<dt><b>NULL</b></dt>
<dt>BLOB</dt>
</dl>
</td>
<td width="60%">
Retrieve one or more data <a href="/windows/desktop/SecGloss/b-gly">BLOBs</a>. The encoded bits are returned in an array of BLOBs. <i>ppvObject</i> is the address of a <a href="/windows/desktop/api/wincrypt/ns-wincrypt-crypt_blob_array">CRYPT_BLOB_ARRAY</a> structure pointer that receives the BLOB array. When this structure is no longer needed, you must free it by passing the address of this structure to the <a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptmemfree">CryptMemFree</a> function.

</td>
</tr>
<tr>
<td width="40%"><a id="CONTEXT_OID_CERTIFICATE"></a><a id="context_oid_certificate"></a><dl>
<dt><b>CONTEXT_OID_CERTIFICATE</b></dt>
<dt>certificate</dt>
</dl>
</td>
<td width="60%">
Retrieve one or more certificates.

If a single object is being retrieved, <i>ppvObject</i> is the address of a <a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_context">CERT_CONTEXT</a> structure pointer that receives the context. When this context is no longer needed, you must free it by passing the <b>CERT_CONTEXT</b> structure pointer to the <a href="/windows/desktop/api/wincrypt/nf-wincrypt-certfreecertificatecontext">CertFreeCertificateContext</a> function.

If multiple objects are being retrieved, <i>ppvObject</i> is the address of an <b>HCERTSTORE</b> variable that receives the handle of a store that contains the certificates. When this store is no longer needed, you must close it by passing this handle to the <a href="/windows/desktop/api/wincrypt/nf-wincrypt-certclosestore">CertCloseStore</a> function.

</td>
</tr>
<tr>
<td width="40%"><a id="CONTEXT_OID_CRL"></a><a id="context_oid_crl"></a><dl>
<dt><b>CONTEXT_OID_CRL</b></dt>
<dt>CRL</dt>
</dl>
</td>
<td width="60%">
Retrieve one or more <a href="/windows/desktop/SecGloss/c-gly">certificate revocation lists</a> (CRLs). 

If a single object is being retrieved, <i>ppvObject</i> is the address of a <a href="/windows/desktop/api/wincrypt/ns-wincrypt-crl_context">CRL_CONTEXT</a> structure pointer that receives the context. When this context is no longer needed, you must free it by passing the <b>CRL_CONTEXT</b> structure pointer to the <a href="/windows/desktop/api/wincrypt/nf-wincrypt-certfreecrlcontext">CertFreeCRLContext</a> function.

If multiple objects are being retrieved, <i>ppvObject</i> is the address of an <b>HCERTSTORE</b> variable that receives the handle of a store that contains the CRLs. When this store is no longer needed, you must close it by passing this handle to the <a href="/windows/desktop/api/wincrypt/nf-wincrypt-certclosestore">CertCloseStore</a> function.

</td>
</tr>
<tr>
<td width="40%"><a id="CONTEXT_OID_CTL"></a><a id="context_oid_ctl"></a><dl>
<dt><b>CONTEXT_OID_CTL</b></dt>
<dt>CTL</dt>
</dl>
</td>
<td width="60%">
Retrieve one or more <a href="/windows/desktop/SecGloss/c-gly">certificate trust lists</a> (CTLs). 

If a single object is being retrieved, <i>ppvObject</i> is the address of a <a href="/windows/desktop/api/wincrypt/ns-wincrypt-ctl_context">CTL_CONTEXT</a> structure pointer that receives the context. When this context is no longer needed, you must free it by passing the <b>CTL_CONTEXT</b> structure pointer to the <a href="/windows/desktop/api/wincrypt/nf-wincrypt-certfreectlcontext">CertFreeCTLContext</a> function.

If multiple objects are being retrieved, <i>ppvObject</i> is the address of an <b>HCERTSTORE</b> variable that receives the handle of a store that contains the CTLs. When this store is no longer needed, you must close it by passing this handle to the <a href="/windows/desktop/api/wincrypt/nf-wincrypt-certclosestore">CertCloseStore</a> function.

</td>
</tr>
<tr>
<td width="40%"><a id="CONTEXT_OID_PKCS7"></a><a id="context_oid_pkcs7"></a><dl>
<dt><b>CONTEXT_OID_PKCS7</b></dt>
<dt>PKCS7</dt>
</dl>
</td>
<td width="60%">
<i>ppvObject</i> is the address of an <b>HCERTSTORE</b> variable that receives the handle of a store that contains the objects from the message. When this store is no longer needed, you must close it by passing this handle to the <a href="/windows/desktop/api/wincrypt/nf-wincrypt-certclosestore">CertCloseStore</a> function.

</td>
</tr>
<tr>
<td width="40%"><a id="CONTEXT_OID_CAPI2_ANY"></a><a id="context_oid_capi2_any"></a><dl>
<dt><b>CONTEXT_OID_CAPI2_ANY</b></dt>
<dt>Function will determine appropriate item</dt>
</dl>
</td>
<td width="60%">
<i>ppvObject</i> is the address of an <b>HCERTSTORE</b> variable that receives the handle of a store that contains the objects. When this store is no longer needed, you must close it by passing this handle to the <a href="/windows/desktop/api/wincrypt/nf-wincrypt-certclosestore">CertCloseStore</a> function.

</td>
</tr>
<tr>
<td width="40%"><a id="CONTEXT_OID_OCSP_RESP"></a><a id="context_oid_ocsp_resp"></a><dl>
<dt><b>CONTEXT_OID_OCSP_RESP</b></dt>
<dt>OCSP Response</dt>
</dl>
</td>
<td width="60%">
<i>ppvObject</i> is the address of a pointer to a <a href="/windows/desktop/api/wincrypt/ns-wincrypt-crypt_blob_array">CRYPT_BLOB_ARRAY</a> structure.

</td>
</tr>
</table>

### -param dwRetrievalFlags [in]

Determines whether to use the cached URL or a URL retrieved from the wire URL. The form in which objects are returned is determined by the value of <i>pszObjectOid</i>.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="CRYPT_AIA_RETRIEVAL"></a><a id="crypt_aia_retrieval"></a><dl>
<dt><b>CRYPT_AIA_RETRIEVAL</b></dt>
</dl>
</td>
<td width="60%">
Validates the content retrieved by a wire URL before writing the URL  to the cache.

The default provider does not support the HTTPS protocol for AIA retrievals.

</td>
</tr>
<tr>
<td width="40%"><a id="CRYPT_ASYNC_RETRIEVAL"></a><a id="crypt_async_retrieval"></a><dl>
<dt><b>CRYPT_ASYNC_RETRIEVAL</b></dt>
</dl>
</td>
<td width="60%">
This value is not supported.

</td>
</tr>
<tr>
<td width="40%"><a id="CRYPT_CACHE_ONLY_RETRIEVAL"></a><a id="crypt_cache_only_retrieval"></a><dl>
<dt><b>CRYPT_CACHE_ONLY_RETRIEVAL</b></dt>
</dl>
</td>
<td width="60%">
Retrieves the encoded bits from the URL cache only. Do not use the wire to retrieve the URL.

</td>
</tr>
<tr>
<td width="40%"><a id="CRYPT_DONT_CACHE_RESULT"></a><a id="crypt_dont_cache_result"></a><dl>
<dt><b>CRYPT_DONT_CACHE_RESULT</b></dt>
</dl>
</td>
<td width="60%">
Does not store the retrieved encoded bits to the URL cache. If this flag is not set, the retrieved URL is cached.

</td>
</tr>
<tr>
<td width="40%"><a id="CRYPT_HTTP_POST_RETRIEVAL"></a><a id="crypt_http_post_retrieval"></a><dl>
<dt><b>CRYPT_HTTP_POST_RETRIEVAL</b></dt>
</dl>
</td>
<td width="60%">
Uses the POST method instead of the default GET method for HTTP retrievals.

In a POST URL, additional binary data and header strings are appended to the base URL in the following format:

<i>BaseURL</i><b>/</b><i>OptionalURLEscaped&amp;Base64EncodedAdditionalData</i><b>?</b><i>OptionalAdditionalHTTPHeaders</i>

The following example shows the additional binary data delimited by the last slash mark (/) and  a Content-Type header delimited by a question mark (?) appended to a base URL.

<code>http://ocsp.openvalidation.org/MEIwQDA%2BMDwwOjAJBgUrDgMCGgUABBQdKNEwjytjKBQADcgM61jfflNpyQQUv1NDgnjQnsOA5RtnygUA37lIg6UCAQI%3D?Content-Type: application/ocsp-request</code>

When this flag is set, the <b>CryptRetrieveObjectByUrl</b> function parses the URL by using the last slash mark (/) and question mark (?) delimiters. The string, which is delimited by a slash mark (/), contains an unescaped URL (that is, a plain text URL without escape characters or escape sequences) and Base64 data decoded into binary form before being passed to the <a href="/windows/desktop/api/winhttp/nf-winhttp-winhttpsendrequest">WinHttpSendRequest</a> function as the <i>lpOptional</i> parameter. The string delimited by a question mark (?) is passed to the <b>WinHttpSendRequest</b> function as the <i>pwszHeaders</i> parameter.

</td>
</tr>
<tr>
<td width="40%"><a id="CRYPT_LDAP_AREC_EXCLUSIVE_RETRIEVAL"></a><a id="crypt_ldap_arec_exclusive_retrieval"></a><dl>
<dt><b>CRYPT_LDAP_AREC_EXCLUSIVE_RETRIEVAL</b></dt>
</dl>
</td>
<td width="60%">
Performs A-Record-only DNS lookup on the supplied host string, preventing the generation of false DNS queries when resolving host names. This flag should be used when passing a host name as opposed to a domain name.

</td>
</tr>
<tr>
<td width="40%"><a id="CRYPT_LDAP_INSERT_ENTRY_ATTRIBUTE"></a><a id="crypt_ldap_insert_entry_attribute"></a><dl>
<dt><b>CRYPT_LDAP_INSERT_ENTRY_ATTRIBUTE</b></dt>
</dl>
</td>
<td width="60%">
Retrieves the entry index and attribute name for each LDAP object. The beginning of each returned BLOB contains the following ANSI string:

"<i>entry index in decimal</i>\0<i>attribute name</i>\0"

When this flag is set, <i>pszObjectOid</i> must be <b>NULL</b> so that a BLOB is returned. This flag only applies to the ldap scheme.

</td>
</tr>
<tr>
<td width="40%"><a id="CRYPT_LDAP_SCOPE_BASE_ONLY_RETRIEVAL"></a><a id="crypt_ldap_scope_base_only_retrieval"></a><dl>
<dt><b>CRYPT_LDAP_SCOPE_BASE_ONLY_RETRIEVAL</b></dt>
</dl>
</td>
<td width="60%">
Fails if the LDAP search scope is not set to base in the URL. Use with LDAP only.

</td>
</tr>
<tr>
<td width="40%"><a id="CRYPT_LDAP_SIGN_RETRIEVAL"></a><a id="crypt_ldap_sign_retrieval"></a><dl>
<dt><b>CRYPT_LDAP_SIGN_RETRIEVAL</b></dt>
</dl>
</td>
<td width="60%">
Digitally signs all of the LDAP traffic to and from a server by using the Kerberos authentication protocol. This feature provides integrity required by some applications.

</td>
</tr>
<tr>
<td width="40%"><a id="CRYPT_NO_AUTH_RETRIEVAL"></a><a id="crypt_no_auth_retrieval"></a><dl>
<dt><b>CRYPT_NO_AUTH_RETRIEVAL</b></dt>
</dl>
</td>
<td width="60%">
Inhibits automatic authentication handling.

</td>
</tr>
<tr>
<td width="40%"><a id="CRYPT_NOT_MODIFIED_RETRIEVAL"></a><a id="crypt_not_modified_retrieval"></a><dl>
<dt><b>CRYPT_NOT_MODIFIED_RETRIEVAL</b></dt>
</dl>
</td>
<td width="60%">
Enables a conditional HTTP URL retrieval. When this flag is set, for a conditional retrieval that returns <b>HTTP_STATUS_NOT_MODIFIED</b>, <b>CryptRetrieveObjectByUrl</b> returns <b>TRUE</b> and <i>ppvObject</i> is set to <b>NULL</b>. If <i>pAuxInfo</i> is not <b>NULL</b>, <b>dwHttpStatusCode</b> is set to <b>HTTP_STATUS_NOT_MODIFIED</b>. Otherwise, <i>ppvObject</i> is updated for a successful retrieval.

</td>
</tr>
<tr>
<td width="40%"><a id="CRYPT_OFFLINE_CHECK_RETRIEVAL"></a><a id="crypt_offline_check_retrieval"></a><dl>
<dt><b>CRYPT_OFFLINE_CHECK_RETRIEVAL</b></dt>
</dl>
</td>
<td width="60%">
Keeps track of offline failures and delays before hitting the wire on subsequent retrievals. This value is for wire retrieval only.

</td>
</tr>
<tr>
<td width="40%"><a id="CRYPT_PROXY_CACHE_RETRIEVAL"></a><a id="crypt_proxy_cache_retrieval"></a><dl>
<dt><b>CRYPT_PROXY_CACHE_RETRIEVAL</b></dt>
</dl>
</td>
<td width="60%">
Enables proxy cache retrieval of an object. If a proxy cache was not explicitly bypassed, <b>fProxyCacheRetrieval</b> is set to <b>TRUE</b> in <i>pAuxInfo</i>. This value only applies to HTTP URL retrievals.

</td>
</tr>
<tr>
<td width="40%"><a id="CRYPT_RETRIEVE_MULTIPLE_OBJECTS"></a><a id="crypt_retrieve_multiple_objects"></a><dl>
<dt><b>CRYPT_RETRIEVE_MULTIPLE_OBJECTS</b></dt>
</dl>
</td>
<td width="60%">
Retrieves multiple objects if available. All objects must be of a homogeneous object type as determined by the value of <i>pszObjectOid</i>, unless the <a href="/windows/desktop/SecGloss/o-gly">object identifier</a> (OID) value is CONTEXT_OID_CAPI2_ANY.

</td>
</tr>
<tr>
<td width="40%"><a id="CRYPT_STICKY_CACHE_RETRIEVAL"></a><a id="crypt_sticky_cache_retrieval"></a><dl>
<dt><b>CRYPT_STICKY_CACHE_RETRIEVAL</b></dt>
</dl>
</td>
<td width="60%">
Tags the URL as exempt from being flushed from the cache. For more information, see STICKY_CACHE_ENTRY in INTERNET_CACHE_ENTRY_INFO.

</td>
</tr>
<tr>
<td width="40%"><a id="CRYPT_VERIFY_CONTEXT_SIGNATURE"></a><a id="crypt_verify_context_signature"></a><dl>
<dt><b>CRYPT_VERIFY_CONTEXT_SIGNATURE</b></dt>
</dl>
</td>
<td width="60%">
Acquires signature verification on the context created. In this case <i>pszObjectOid</i> must be non-<b>NULL</b> and <i>pvVerify</i> points to the signer certificate context.

</td>
</tr>
<tr>
<td width="40%"><a id="CRYPT_VERIFY_DATA_HASH"></a><a id="crypt_verify_data_hash"></a><dl>
<dt><b>CRYPT_VERIFY_DATA_HASH</b></dt>
</dl>
</td>
<td width="60%">
This flag is not implemented. Do not use it.

</td>
</tr>
<tr>
<td width="40%"><a id="CRYPT_WIRE_ONLY_RETRIEVAL"></a><a id="crypt_wire_only_retrieval"></a><dl>
<dt><b>CRYPT_WIRE_ONLY_RETRIEVAL</b></dt>
</dl>
</td>
<td width="60%">
Retrieves the encoded bits from the wire only. Does not use the URL cache.

</td>
</tr>
</table>

### -param dwTimeout [in]

Specifies the maximum number of milliseconds to wait for retrieval. If a value of zero is specified, this function does not time out. This parameter is not used if the URL scheme is file:///.

### -param ppvObject [out]

The address of a pointer to the returned object. The return type can be one of the supported types shown in <i>pszObjectOid</i>.

### -param hAsyncRetrieve [in]

This parameter is reserved and must be set to <b>NULL</b>.

### -param pCredentials [in, optional]

This parameter is not used.

### -param pvVerify [in, optional]

A pointer to a verification object. This object is a function of the <i>dwRetrievalFlags</i> parameter. It can be <b>NULL</b> to indicate that the caller is not interested in getting the certificate context or index of the signer if <i>dwRetrievalFlags</i> is CRYPT_VERIFY_CONTEXT_SIGNATURE.

### -param pAuxInfo [in]

An optional pointer to a 
<a href="/windows/desktop/api/wincrypt/ns-wincrypt-crypt_retrieve_aux_info">CRYPT_RETRIEVE_AUX_INFO</a> structure. If not <b>NULL</b> and if the <b>cbSize</b> member of the structure is set, this parameter returns the time of the last successful wire retrieval.

## -returns

If the function succeeds, the return value is nonzero (<b>TRUE</b>).

If the function fails, the return value is zero (<b>FALSE</b>).

## -remarks

The remote object retrieval manager exposes two provider models. One is the Scheme Provider model that allows for installable protocol providers as defined by the URL scheme, that is, ldap, http, ftp, or file. The scheme provider entry point is the same as the <b>CryptRetrieveObjectByUrl</b> function; however, the *<i>ppvObject</i> returned is always a counted array of encoded bits (one per object retrieved).

The second provider model is the Context Provider model that allows for installable creators of the context handles (objects) based on the retrieved encoded bits. These are dispatched based on the <a href="/windows/desktop/SecGloss/o-gly">object identifier</a> (OID) specified in the call to <b>CryptRetrieveObjectByUrl</b>.

Individual PKI objects such as certificates, trusts lists, revocation lists, PKCS #7 messages, and multiple homogeneous objects can be retrieved. Starting with Windows Vista with Service Pack 1 (SP1) and Windows Server 2008, security of "http:" and "ldap:" retrievals have been hardened.
This function supports "http:" and "ldap:" URL schemes as well as newly defined schemes.

<b>Windows XP:  </b>"ftp:" is not supported for network retrieval.

<div class="alert"><b>Note</b>  By default, "file:" is not supported for network retrieval.</div>
<div> </div>




> [!NOTE]
> The wincrypt.h header defines CryptRetrieveObjectByUrl as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptgetobjecturl">CryptGetObjectUrl</a>
