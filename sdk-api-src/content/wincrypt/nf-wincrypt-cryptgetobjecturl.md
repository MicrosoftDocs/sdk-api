---
UID: NF:wincrypt.CryptGetObjectUrl
title: CryptGetObjectUrl function (wincrypt.h)
description: Acquires the URL of the remote object from a certificate, certificate trust list (CTL), or certificate revocation list (CRL).
helpviewer_keywords: ["CRYPT_GET_URL_FROM_AUTH_ATTRIBUTE","CRYPT_GET_URL_FROM_EXTENSION","CRYPT_GET_URL_FROM_PROPERTY","CRYPT_GET_URL_FROM_UNAUTH_ATTRIBUTE","CryptGetObjectUrl","CryptGetObjectUrl function [Security]","URL_OID_CERTIFICATE_CRL_DIST_POINT","URL_OID_CERTIFICATE_CRL_DIST_POINT_AND_OCSP","URL_OID_CERTIFICATE_FRESHEST_CRL","URL_OID_CERTIFICATE_ISSUER","URL_OID_CERTIFICATE_OCSP","URL_OID_CERTIFICATE_OCSP_AND_CRL_DIST_POINT","URL_OID_CERTIFICATE_ONLY_OCSP","URL_OID_CRL_FRESHEST_CRL","URL_OID_CRL_ISSUER","URL_OID_CROSS_CERT_DIST_POINT","URL_OID_CROSS_CERT_SUBJECT_INFO_ACCESS","URL_OID_CTL_ISSUER","URL_OID_CTL_NEXT_UPDATE","_crypto2_cryptgetobjecturl","security.cryptgetobjecturl","wincrypt/CryptGetObjectUrl"]
old-location: security\cryptgetobjecturl.htm
tech.root: security
ms.assetid: a92117b8-9144-4480-b88a-b9ffe1026d63
ms.date: 12/05/2018
ms.keywords: CRYPT_GET_URL_FROM_AUTH_ATTRIBUTE, CRYPT_GET_URL_FROM_EXTENSION, CRYPT_GET_URL_FROM_PROPERTY, CRYPT_GET_URL_FROM_UNAUTH_ATTRIBUTE, CryptGetObjectUrl, CryptGetObjectUrl function [Security], URL_OID_CERTIFICATE_CRL_DIST_POINT, URL_OID_CERTIFICATE_CRL_DIST_POINT_AND_OCSP, URL_OID_CERTIFICATE_FRESHEST_CRL, URL_OID_CERTIFICATE_ISSUER, URL_OID_CERTIFICATE_OCSP, URL_OID_CERTIFICATE_OCSP_AND_CRL_DIST_POINT, URL_OID_CERTIFICATE_ONLY_OCSP, URL_OID_CRL_FRESHEST_CRL, URL_OID_CRL_ISSUER, URL_OID_CROSS_CERT_DIST_POINT, URL_OID_CROSS_CERT_SUBJECT_INFO_ACCESS, URL_OID_CTL_ISSUER, URL_OID_CTL_NEXT_UPDATE, _crypto2_cryptgetobjecturl, security.cryptgetobjecturl, wincrypt/CryptGetObjectUrl
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
req.lib: Cryptnet.lib
req.dll: Cryptnet.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CryptGetObjectUrl
 - wincrypt/CryptGetObjectUrl
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
 - CryptGetObjectUrl
---

# CryptGetObjectUrl function


## -description

The <b>CryptGetObjectUrl</b> function acquires the URL of the remote object from a <a href="/windows/desktop/SecGloss/c-gly">certificate</a>, <a href="/windows/desktop/SecGloss/c-gly">certificate trust list</a> (CTL), or <a href="/windows/desktop/SecGloss/c-gly">certificate revocation list</a> (CRL).

The function takes the object, decodes it, and provides a pointer to an array of URLs from the object. For example, from a certificate, a CRL distribution list of URLs would be in the array.

## -parameters

### -param pszUrlOid [in]

A pointer to an <a href="/windows/desktop/SecGloss/o-gly">object identifier</a> (OID) that identifies the URL being requested. If the <a href="/previous-versions/windows/desktop/legacy/ms632657(v=vs.85)">HIWORD</a> of the <i>pszUrlOid</i> parameter is zero, the <a href="/previous-versions/windows/desktop/legacy/ms632659(v=vs.85)">LOWORD</a> specifies the integer identifier for the type of the specified structure. 




This parameter can be one of the following values. For information about how these values affect the <i>pvPara</i> parameter, see the heading "For the <i>pvPara</i> parameter" in the <b>Meaning</b> column.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="URL_OID_CERTIFICATE_ISSUER"></a><a id="url_oid_certificate_issuer"></a><dl>
<dt><b>URL_OID_CERTIFICATE_ISSUER</b></dt>
</dl>
</td>
<td width="60%">
Provides the URL of the certificate issuer retrieved from the authority information access extension or property of a certificate.

For the <i>pvPara</i> parameter: A pointer to a 
<a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_context">CERT_CONTEXT</a> structure that was issued by the issuer whose URL is being requested.

</td>
</tr>
<tr>
<td width="40%"><a id="URL_OID_CERTIFICATE_CRL_DIST_POINT"></a><a id="url_oid_certificate_crl_dist_point"></a><dl>
<dt><b>URL_OID_CERTIFICATE_CRL_DIST_POINT</b></dt>
</dl>
</td>
<td width="60%">
Provides a list of URLs of the CRL distribution points retrieved from the CRL distribution point extension or property of a certificate.

For the <i>pvPara</i> parameter: A pointer to a 
<a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_context">CERT_CONTEXT</a> structure whose CRL distribution point is requested.

</td>
</tr>
<tr>
<td width="40%"><a id="URL_OID_CERTIFICATE_CRL_DIST_POINT_AND_OCSP"></a><a id="url_oid_certificate_crl_dist_point_and_ocsp"></a><dl>
<dt><b>URL_OID_CERTIFICATE_CRL_DIST_POINT_AND_OCSP</b></dt>
</dl>
</td>
<td width="60%">
Provides a list of OCSP and CRL distribution point URLs from the authority information access (AIA)   and CRL distribution point extensions or properties of a certificate. The function returns any CRL distribution point URLs first. Before using any OCSP URLs, you must remove the L"ocsp:" prefix.

For the <i>pvPara</i> parameter: A pointer to a 
<a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_context">CERT_CONTEXT</a> structure whose OCSP and CRL distribution point URLs are requested.

</td>
</tr>
<tr>
<td width="40%"><a id="URL_OID_CERTIFICATE_OCSP"></a><a id="url_oid_certificate_ocsp"></a><dl>
<dt><b>URL_OID_CERTIFICATE_OCSP</b></dt>
</dl>
</td>
<td width="60%">
Provides an OCSP URL from the authority information access (AIA)   extension or property of a certificate.

For the <i>pvPara</i> parameter: A pointer to a 
<a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_context">CERT_CONTEXT</a> structure whose OCSP URL is requested.

</td>
</tr>
<tr>
<td width="40%"><a id="URL_OID_CERTIFICATE_OCSP_AND_CRL_DIST_POINT"></a><a id="url_oid_certificate_ocsp_and_crl_dist_point"></a><dl>
<dt><b>URL_OID_CERTIFICATE_OCSP_AND_CRL_DIST_POINT</b></dt>
</dl>
</td>
<td width="60%">
Provides a list of OCSP and CRL distribution point URLs from the authority information access (AIA)   and CRL distribution point extensions or properties of a certificate. The function returns any OCSP URLs first. Before using any OCSP URLs, you must remove the L"ocsp:" prefix.

For the <i>pvPara</i> parameter: A pointer to a 
<a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_context">CERT_CONTEXT</a> structure whose OCSP and CRL distribution point URLs are requested.

</td>
</tr>
<tr>
<td width="40%"><a id="URL_OID_CERTIFICATE_ONLY_OCSP"></a><a id="url_oid_certificate_only_ocsp"></a><dl>
<dt><b>URL_OID_CERTIFICATE_ONLY_OCSP</b></dt>
</dl>
</td>
<td width="60%">
Provides a list of OCSP URLs from the authority information access (AIA)  extension or property of a certificate. Before using any OCSP URLs, you must remove the L"ocsp:" prefix.

For the <i>pvPara</i> parameter: A pointer to a 
<a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_context">CERT_CONTEXT</a> structure whose OCSP URLs are requested.

</td>
</tr>
<tr>
<td width="40%"><a id="URL_OID_CTL_ISSUER"></a><a id="url_oid_ctl_issuer"></a><dl>
<dt><b>URL_OID_CTL_ISSUER</b></dt>
</dl>
</td>
<td width="60%">
Provides the URL of the CTL issuer retrieved from an authority information access attribute method encoded in each signer information in the PKCS #7 CTL.

For the <i>pvPara</i> parameter: A pointer to a Signer Index 
<a href="/windows/desktop/api/wincrypt/ns-wincrypt-ctl_context">CTL_CONTEXT</a> structure that was issued by the issuer whose URL, identified by the signer index, is requested.

</td>
</tr>
<tr>
<td width="40%"><a id="URL_OID_CTL_NEXT_UPDATE"></a><a id="url_oid_ctl_next_update"></a><dl>
<dt><b>URL_OID_CTL_NEXT_UPDATE</b></dt>
</dl>
</td>
<td width="60%">
Provides the URL of the next update of that CTL retrieved from an authority information access CTL extension, property, or signer information attribute method.

For the <i>pvPara</i> parameter: A pointer to a Signer Index 
<a href="/windows/desktop/api/wincrypt/ns-wincrypt-ctl_context">CTL_CONTEXT</a> structure whose next update URL is requested, and an optional signer index, in case it is needed to check the signer information attributes.

</td>
</tr>
<tr>
<td width="40%"><a id="URL_OID_CRL_ISSUER"></a><a id="url_oid_crl_issuer"></a><dl>
<dt><b>URL_OID_CRL_ISSUER</b></dt>
</dl>
</td>
<td width="60%">
Provides the URL of the CRL issuer retrieved from a property on a CRL that was inherited from the subject certificate (either from the subject certificate issuer or the subject certificate distribution point extension). It is encoded as an authority information access extension method.

For the <i>pvPara</i> parameter: A pointer to a 
<a href="/windows/desktop/api/wincrypt/ns-wincrypt-crl_context">CRL_CONTEXT</a> structure that was issued by the issuer whose URL is requested.

</td>
</tr>
<tr>
<td width="40%"><a id="URL_OID_CERTIFICATE_FRESHEST_CRL"></a><a id="url_oid_certificate_freshest_crl"></a><dl>
<dt><b>URL_OID_CERTIFICATE_FRESHEST_CRL</b></dt>
</dl>
</td>
<td width="60%">
Retrieves the most recent CRL extension or property of the certificate.

For the <i>pvPara</i> parameter: The PCCERT_CONTEXT of a certificate whose most recent CRL distribution point is being requested.

</td>
</tr>
<tr>
<td width="40%"><a id="URL_OID_CRL_FRESHEST_CRL"></a><a id="url_oid_crl_freshest_crl"></a><dl>
<dt><b>URL_OID_CRL_FRESHEST_CRL</b></dt>
</dl>
</td>
<td width="60%">
Retrieves the most recent CRL extension or property of the CRL.

For the <i>pvPara</i> parameter: A pointer to a 
<a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_crl_context_pair">CERT_CRL_CONTEXT_PAIR</a> structure that contains the base CRL of a certificate whose most recent CRL distribution point is being requested.

</td>
</tr>
<tr>
<td width="40%"><a id="URL_OID_CROSS_CERT_DIST_POINT"></a><a id="url_oid_cross_cert_dist_point"></a><dl>
<dt><b>URL_OID_CROSS_CERT_DIST_POINT</b></dt>
</dl>
</td>
<td width="60%">
Retrieves the cross certificate distribution point extension or property of the certificate.

For the <i>pvPara</i> parameter: The PCCERT_CONTEXT of a certificate whose cross certificate distribution point is being requested.

</td>
</tr>
<tr>
<td width="40%"><a id="URL_OID_CROSS_CERT_SUBJECT_INFO_ACCESS"></a><a id="url_oid_cross_cert_subject_info_access"></a><dl>
<dt><b>URL_OID_CROSS_CERT_SUBJECT_INFO_ACCESS</b></dt>
</dl>
</td>
<td width="60%">
Retrieves the cross certificate Subject Information Access extension or property of the certificate.

For the <i>pvPara</i> parameter: The PCCERT_CONTEXT of a certificate whose cross certificate Subject Information Access is being requested.

</td>
</tr>
</table>

### -param pvPara [in]

A structure determined by the value of <i>pszUrlOid</i>. For details, see the description for the <i>pszUrlOid</i> parameter.

### -param dwFlags [in]

A set of flags used to get the URL locator for an object. This can be zero or a combination of one or more of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="CRYPT_GET_URL_FROM_PROPERTY"></a><a id="crypt_get_url_from_property"></a><dl>
<dt><b>CRYPT_GET_URL_FROM_PROPERTY</b></dt>
</dl>
</td>
<td width="60%">
Locates the URL from the property of the object (the location of the data).

</td>
</tr>
<tr>
<td width="40%"><a id="CRYPT_GET_URL_FROM_EXTENSION"></a><a id="crypt_get_url_from_extension"></a><dl>
<dt><b>CRYPT_GET_URL_FROM_EXTENSION</b></dt>
</dl>
</td>
<td width="60%">
Locates the URL from the extension of the object.

</td>
</tr>
<tr>
<td width="40%"><a id="CRYPT_GET_URL_FROM_UNAUTH_ATTRIBUTE"></a><a id="crypt_get_url_from_unauth_attribute"></a><dl>
<dt><b>CRYPT_GET_URL_FROM_UNAUTH_ATTRIBUTE</b></dt>
</dl>
</td>
<td width="60%">
Locates the URL from an unauthenticated attribute from the signer information data.

</td>
</tr>
<tr>
<td width="40%"><a id="CRYPT_GET_URL_FROM_AUTH_ATTRIBUTE"></a><a id="crypt_get_url_from_auth_attribute"></a><dl>
<dt><b>CRYPT_GET_URL_FROM_AUTH_ATTRIBUTE</b></dt>
</dl>
</td>
<td width="60%">
Locates the URL from an authenticated attribute from the signer information data.

</td>
</tr>
</table>

### -param pUrlArray [out]

A pointer to a buffer to receive the data for the value entry. This parameter can be <b>NULL</b> to find the length of the buffer required to hold the data. 


For more information, see 
<a href="/windows/desktop/SecCrypto/retrieving-data-of-unknown-length">Retrieving Data of Unknown Length</a>.

### -param pcbUrlArray [in, out]

A pointer to a <b>DWORD</b> that specifies the size, in bytes, of the buffer pointed to by the <i>pUrlArray</i> parameter. When the function returns, the <b>DWORD</b> contains the number of bytes stored in the buffer. This parameter can be <b>NULL</b> only if <i>pUrlArray</i> is <b>NULL</b>.

### -param pUrlInfo [out]

An optional pointer to a 
<a href="/windows/desktop/api/wincrypt/ns-wincrypt-crypt_url_info">CRYPT_URL_INFO</a> structure that receives the data for the value entry.

### -param pcbUrlInfo [in, out]

A pointer to a <b>DWORD</b> that specifies the size, in bytes, of the buffer pointed to by the <i>pUrlArray</i> parameter. When the function returns, the <b>DWORD</b> contains the number of bytes stored in the buffer. 




<div class="alert"><b>Note</b>  When processing the data returned in the buffer, applications must use the actual size of the data returned. The actual size can be slightly smaller than the size of the buffer specified on input. On input, buffer sizes are usually specified large enough to ensure that the largest possible output data will fit in the buffer. On output, the variable pointed to by this parameter is updated to reflect the actual size of the data copied to the buffer.</div>
<div> </div>

### -param pvReserved

Reserved for future use and must be <b>NULL</b>.

## -returns

If the function succeeds, the function returns nonzero (<b>TRUE</b>).

If the function fails, it returns zero (<b>FALSE</b>). For extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -see-also

<a href="/windows/desktop/SecCrypto/cryptography-functions">Remote Object Retrieval Functions</a>