---
UID: NF:wincrypt.CertCreateSelfSignCertificate
title: CertCreateSelfSignCertificate function (wincrypt.h)
description: Builds a self-signed certificate and returns a pointer to a CERT_CONTEXT structure that represents the certificate.
helpviewer_keywords: ["CERT_CREATE_SELFSIGN_NO_KEY_INFO","CERT_CREATE_SELFSIGN_NO_SIGN","CertCreateSelfSignCertificate","CertCreateSelfSignCertificate function [Security]","_crypto2_certcreateselfsigncertificate","security.certcreateselfsigncertificate","wincrypt/CertCreateSelfSignCertificate"]
old-location: security\certcreateselfsigncertificate.htm
tech.root: security
ms.assetid: 89028c4e-f896-4c50-9fa2-bcb4e1784244
ms.date: 12/05/2018
ms.keywords: CERT_CREATE_SELFSIGN_NO_KEY_INFO, CERT_CREATE_SELFSIGN_NO_SIGN, CertCreateSelfSignCertificate, CertCreateSelfSignCertificate function [Security], _crypto2_certcreateselfsigncertificate, security.certcreateselfsigncertificate, wincrypt/CertCreateSelfSignCertificate
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
 - CertCreateSelfSignCertificate
 - wincrypt/CertCreateSelfSignCertificate
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
 - CertCreateSelfSignCertificate
---

# CertCreateSelfSignCertificate function


## -description

The <b>CertCreateSelfSignCertificate</b> function builds a self-signed certificate and returns a pointer to a 
<a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_context">CERT_CONTEXT</a> structure that represents the certificate.

## -parameters

### -param hCryptProvOrNCryptKey [in, optional]

A handle of a <a href="/windows/desktop/SecGloss/c-gly">cryptographic provider</a> used to sign the certificate created. If <b>NULL</b>, information from the <i>pKeyProvInfo</i> parameter is used to acquire the needed handle. If <i>pKeyProvInfo</i> is also <b>NULL</b>, the default provider type, PROV_RSA_FULL provider type, the default key specification, AT_SIGNATURE, and a newly created <a href="/windows/desktop/SecGloss/k-gly">key container</a> with a unique container name are used.

This handle must be an <a href="/windows/desktop/SecCrypto/hcryptprov">HCRYPTPROV</a> handle that has been created by using the 
<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptacquirecontexta">CryptAcquireContext</a> function or an <b>NCRYPT_KEY_HANDLE</b> handle that has been created by using the <a href="/windows/desktop/api/ncrypt/nf-ncrypt-ncryptopenkey">NCryptOpenKey</a> function. New applications should always pass in the <b>NCRYPT_KEY_HANDLE</b> handle of a CNG <a href="/windows/desktop/SecGloss/c-gly">cryptographic service provider</a> (CSP).

### -param pSubjectIssuerBlob [in]

A pointer to a <a href="/windows/desktop/SecGloss/b-gly">BLOB</a> that contains the distinguished name (DN) for the certificate subject. This parameter cannot be <b>NULL</b>. Minimally, a pointer to an empty DN must be provided. This BLOB is normally created by using the 
<a href="/windows/desktop/api/wincrypt/nf-wincrypt-certstrtonamea">CertStrToName</a> function. It can also be created by using the 
<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptencodeobject">CryptEncodeObject</a> function and specifying either the X509_NAME or X509_UNICODE_NAME <i>StructType</i>.

### -param dwFlags [in]

A set of flags that override the default behavior of this function. This can be zero or a combination of one or more of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="CERT_CREATE_SELFSIGN_NO_KEY_INFO"></a><a id="cert_create_selfsign_no_key_info"></a><dl>
<dt><b>CERT_CREATE_SELFSIGN_NO_KEY_INFO</b></dt>
<dt>2</dt>
</dl>
</td>
<td width="60%">
By default, the returned PCCERT_CONTEXT references the <a href="/windows/desktop/SecGloss/p-gly">private keys</a> by setting the CERT_KEY_PROV_INFO_PROP_ID. If you do not want the returned PCCERT_CONTEXT to reference private keys by setting the CERT_KEY_PROV_INFO_PROP_ID, specify CERT_CREATE_SELFSIGN_NO_KEY_INFO.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_CREATE_SELFSIGN_NO_SIGN"></a><a id="cert_create_selfsign_no_sign"></a><dl>
<dt><b>CERT_CREATE_SELFSIGN_NO_SIGN</b></dt>
<dt>1</dt>
</dl>
</td>
<td width="60%">
By default, the certificate being created is signed. If the certificate being created is only a dummy placeholder, the certificate might not need to be signed. Signing of the certificate is skipped if CERT_CREATE_SELFSIGN_NO_SIGN is specified.

</td>
</tr>
</table>

### -param pKeyProvInfo [in, optional]

A pointer to a <a href="/windows/desktop/api/wincrypt/ns-wincrypt-crypt_key_prov_info">CRYPT_KEY_PROV_INFO</a> structure. Before a certificate is created, the CSP is queried for the key provider, key provider type, and the <a href="/windows/desktop/SecGloss/k-gly">key container</a> name. If the CSP queried does not support these queries, the function fails. If the default provider does not support these queries, a <i>pKeyProvInfo</i> value must be specified. The RSA BASE does support these queries.

If the <i>pKeyProvInfo</i> parameter is not <b>NULL</b>, the corresponding values are set in the <b>CERT_KEY_PROV_INFO_PROP_ID</b> value of the generated certificate. You must ensure that all parameters of the supplied structure are correctly specified.

### -param pSignatureAlgorithm [in, optional]

A pointer to a <a href="/windows/desktop/api/wincrypt/ns-wincrypt-crypt_algorithm_identifier">CRYPT_ALGORITHM_IDENTIFIER</a> structure. If <b>NULL</b>, the default algorithm, SHA1RSA, is used.

### -param pStartTime [in, optional]

A pointer to a <a href="/windows/desktop/api/minwinbase/ns-minwinbase-systemtime">SYSTEMTIME</a> structure. If <b>NULL</b>, the system current time is used by default.

### -param pEndTime [in, optional]

A pointer to a <a href="/windows/desktop/api/minwinbase/ns-minwinbase-systemtime">SYSTEMTIME</a> structure. If <b>NULL</b>, the <i>pStartTime</i> value plus one year will be used by default.

### -param pExtensions [optional]

A pointer to a <a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_extensions">CERT_EXTENSIONS</a> array of <a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_extension">CERT_EXTENSION</a> structures. By default, the array is empty. An alternate subject name, if desired, can be specified as one of these extensions.

## -returns

If the function succeeds, a <a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_context">PCCERT_CONTEXT</a> variable that points to the created certificate is returned. If the function fails, it returns <b>NULL</b>. For extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

As the pEndTime must be a valid date, and is automatically generated if it is not supplied by the user, unexpected failures may easily be caused when this API is called on a leap day without accompanying app logic to compensate. For more information, please see [leap year readiness](https://techcommunity.microsoft.com/t5/azure-developer-community-blog/it-s-2020-is-your-code-ready-for-leap-day/ba-p/1157279).

## -see-also

<a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_extension">CERT_EXTENSION</a>



<a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_extensions">CERT_EXTENSIONS</a>



<a href="/windows/desktop/api/wincrypt/ns-wincrypt-crypt_algorithm_identifier">CRYPT_ALGORITHM_IDENTIFIER</a>



<a href="/windows/desktop/api/wincrypt/nf-wincrypt-certstrtonamea">CertStrToName</a>



<a href="/windows/desktop/api/wincrypt/nf-wincrypt-cryptencodeobject">CryptEncodeObject</a>



<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>



<a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_context">PCCERT_CONTEXT</a>



<a href="/windows/desktop/api/minwinbase/ns-minwinbase-systemtime">SYSTEMTIME</a>