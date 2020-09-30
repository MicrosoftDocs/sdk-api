---
UID: NF:wincrypt.CertAddEncodedCertificateToStore
title: CertAddEncodedCertificateToStore function (wincrypt.h)
description: Creates a certificate context from an encoded certificate and adds it to the certificate store.
helpviewer_keywords: ["CERT_STORE_ADD_ALWAYS","CERT_STORE_ADD_NEW","CERT_STORE_ADD_REPLACE_EXISTING","CERT_STORE_ADD_REPLACE_EXISTING_INHERIT_PROPERTIES","CERT_STORE_ADD_USE_EXISTING","CertAddEncodedCertificateToStore","CertAddEncodedCertificateToStore function [Security]","_crypto2_certaddencodedcertificatetostore","security.certaddencodedcertificatetostore","wincrypt/CertAddEncodedCertificateToStore"]
old-location: security\certaddencodedcertificatetostore.htm
tech.root: security
ms.assetid: 7c092bf5-f8b2-47d0-94ee-c8e0f4bca62d
ms.date: 12/05/2018
ms.keywords: CERT_STORE_ADD_ALWAYS, CERT_STORE_ADD_NEW, CERT_STORE_ADD_REPLACE_EXISTING, CERT_STORE_ADD_REPLACE_EXISTING_INHERIT_PROPERTIES, CERT_STORE_ADD_USE_EXISTING, CertAddEncodedCertificateToStore, CertAddEncodedCertificateToStore function [Security], _crypto2_certaddencodedcertificatetostore, security.certaddencodedcertificatetostore, wincrypt/CertAddEncodedCertificateToStore
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
 - CertAddEncodedCertificateToStore
 - wincrypt/CertAddEncodedCertificateToStore
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
 - CertAddEncodedCertificateToStore
---

# CertAddEncodedCertificateToStore function


## -description

The <b>CertAddEncodedCertificateToStore</b> function creates a certificate <a href="/windows/desktop/SecGloss/c-gly">context</a> from an encoded certificate and adds it to the <a href="/windows/desktop/SecGloss/c-gly">certificate store</a>. The context created does not include any extended properties.

The <b>CertAddEncodedCertificateToStore</b> function also makes a copy of the encoded certificate before adding the certificate to the store.

## -parameters

### -param hCertStore [in]

A handle to the certificate store.

### -param dwCertEncodingType [in]

Specifies the type of encoding used. It is always acceptable to specify both the certificate and <a href="/windows/desktop/SecGloss/m-gly">message encoding types</a> by combining them with a bitwise-<b>OR</b> operation as shown in the following example:

X509_ASN_ENCODING | PKCS_7_ASN_ENCODING Currently defined encoding types are:

<ul>
<li>X509_ASN_ENCODING</li>
<li>PKCS_7_ASN_ENCODING</li>
</ul>

### -param pbCertEncoded [in]

A pointer to a buffer containing the encoded certificate that is to be added to the certificate store.

### -param cbCertEncoded [in]

The size, in bytes, of the <i>pbCertEncoded</i> buffer.

### -param dwAddDisposition [in]

Specifies the action to take if a matching certificate or link to a matching certificate exists in the store. Currently defined disposition values and their uses are as follows.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="CERT_STORE_ADD_ALWAYS"></a><a id="cert_store_add_always"></a><dl>
<dt><b>CERT_STORE_ADD_ALWAYS</b></dt>
</dl>
</td>
<td width="60%">
The function makes no check for an existing matching certificate or link to a matching certificate. A new certificate is always added to the store. This can lead to duplicates in a store.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_STORE_ADD_NEW"></a><a id="cert_store_add_new"></a><dl>
<dt><b>CERT_STORE_ADD_NEW</b></dt>
</dl>
</td>
<td width="60%">
If a matching certificate or a link to a matching certificate exists in the store, the operation fails. 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> returns the CRYPT_E_EXISTS code.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_STORE_ADD_REPLACE_EXISTING"></a><a id="cert_store_add_replace_existing"></a><dl>
<dt><b>CERT_STORE_ADD_REPLACE_EXISTING</b></dt>
</dl>
</td>
<td width="60%">
If a matching certificate or link to a matching certificate exists in the store, the existing certificate or link is deleted and a new certificate is created and added to the store. If a matching certificate or link to a matching certificate does not exist, a new certificate is created and added to the store.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_STORE_ADD_REPLACE_EXISTING_INHERIT_PROPERTIES"></a><a id="cert_store_add_replace_existing_inherit_properties"></a><dl>
<dt><b>CERT_STORE_ADD_REPLACE_EXISTING_INHERIT_PROPERTIES</b></dt>
</dl>
</td>
<td width="60%">
If a matching certificate exists in the store, that existing context is deleted before creating and adding the new context. The new context inherits properties from the existing certificate.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_STORE_ADD_USE_EXISTING"></a><a id="cert_store_add_use_existing"></a><dl>
<dt><b>CERT_STORE_ADD_USE_EXISTING</b></dt>
</dl>
</td>
<td width="60%">
If a matching certificate or a link to a matching certificate exists, that existing certificate or link is used and properties from the new certificate are added. The function does not fail, but it does not add a new context. If <i>ppCertContext</i> is not <b>NULL</b>, the existing context is duplicated.

If a matching certificate or link to a matching certificate does not exist, a new certificate is added.

</td>
</tr>
</table>

### -param ppCertContext [out, optional]

A pointer to a pointer to the decoded <a href="/windows/desktop/SecGloss/c-gly">certificate context</a>. This is an optional parameter that can be <b>NULL</b>, indicating that the calling application does not require a copy of the new or existing certificate. When a copy is made, its context must be freed by using 
<a href="/windows/desktop/api/wincrypt/nf-wincrypt-certfreecertificatecontext">CertFreeCertificateContext</a>.

## -returns

If the function succeeds, the return value is <b>TRUE</b>.

If the function fails, the return value is <b>FALSE</b>. For extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>. Some possible error codes follow.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>CRYPT_E_EXISTS</b></dt>
</dl>
</td>
<td width="60%">
This code is returned if CERT_STORE_ADD_NEW is set and the certificate already exists in the store, or if CERT_STORE_ADD_NEWER is set and there is a certificate in the store with a <b>NotBefore</b> date greater than or equal to the <b>NotBefore</b> date on the certificate to be added.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
A disposition value that is not valid was specified in the <i>dwAddDisposition</i> parameter, or a certificate encoding type that is not valid was specified. Currently, only the X509_ASN_ENCODING type is supported.

</td>
</tr>
</table>
 

If the function fails, <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>  returns an <a href="/windows/desktop/SecGloss/a-gly">Abstract Syntax Notation One</a> (ASN.1) encoding/decoding error. For information about these errors, see 
<a href="/windows/desktop/SecCrypto/asn-1-encoding-decoding-return-values">ASN.1 Encoding/Decoding Return Values</a>.

## -see-also

<a href="/windows/desktop/api/wincrypt/nf-wincrypt-certaddcertificatecontexttostore">CertAddCertificateContextToStore</a>



<a href="/windows/desktop/api/wincrypt/nf-wincrypt-certfreecertificatecontext">CertFreeCertificateContext</a>



<a href="/windows/desktop/SecCrypto/cryptography-functions">Certificate Functions</a>