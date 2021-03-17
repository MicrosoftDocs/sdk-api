---
UID: NF:wincrypt.CertAddEncodedCRLToStore
title: CertAddEncodedCRLToStore function (wincrypt.h)
description: Creates a certificate revocation list (CRL) context from an encoded CRL and adds it to the certificate store.
helpviewer_keywords: ["CERT_STORE_ADD_ALWAYS","CERT_STORE_ADD_NEW","CERT_STORE_ADD_NEWER","CERT_STORE_ADD_NEWER_INHERIT_PROPERTIES","CERT_STORE_ADD_REPLACE_EXISTING","CERT_STORE_ADD_REPLACE_EXISTING_INHERIT_PROPERTIES","CERT_STORE_ADD_USE_EXISTING","CertAddEncodedCRLToStore","CertAddEncodedCRLToStore function [Security]","_crypto2_certaddencodedcrltostore","security.certaddencodedcrltostore","wincrypt/CertAddEncodedCRLToStore"]
old-location: security\certaddencodedcrltostore.htm
tech.root: security
ms.assetid: ec2361e6-a1e6-413a-828e-d543a09c88f8
ms.date: 12/05/2018
ms.keywords: CERT_STORE_ADD_ALWAYS, CERT_STORE_ADD_NEW, CERT_STORE_ADD_NEWER, CERT_STORE_ADD_NEWER_INHERIT_PROPERTIES, CERT_STORE_ADD_REPLACE_EXISTING, CERT_STORE_ADD_REPLACE_EXISTING_INHERIT_PROPERTIES, CERT_STORE_ADD_USE_EXISTING, CertAddEncodedCRLToStore, CertAddEncodedCRLToStore function [Security], _crypto2_certaddencodedcrltostore, security.certaddencodedcrltostore, wincrypt/CertAddEncodedCRLToStore
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
 - CertAddEncodedCRLToStore
 - wincrypt/CertAddEncodedCRLToStore
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
 - CertAddEncodedCRLToStore
---

# CertAddEncodedCRLToStore function


## -description

The <b>CertAddEncodedCRLToStore</b> function creates a <a href="/windows/desktop/SecGloss/c-gly">certificate revocation list</a> (CRL) context from an encoded CRL and adds it to the certificate store. The function makes a copy of the CRL context before adding it to the store.

## -parameters

### -param hCertStore [in]

Handle of a certificate store.

### -param dwCertEncodingType [in]

Specifies the type of encoding used. It is always acceptable to specify both the certificate and <a href="/windows/desktop/SecGloss/m-gly">message encoding types</a> by combining them with a bitwise-<b>OR</b> operation as shown in the following example:

X509_ASN_ENCODING | PKCS_7_ASN_ENCODING Currently defined encoding types are:

<ul>
<li>X509_ASN_ENCODING</li>
<li>PKCS_7_ASN_ENCODING</li>
</ul>

### -param pbCrlEncoded [in]

A pointer to a buffer containing the encoded CRL to be added to the <a href="/windows/desktop/SecGloss/c-gly">certificate store</a>.

### -param cbCrlEncoded [in]

The size, in bytes, of the <i>pbCrlEncoded</i> buffer.

### -param dwAddDisposition [in]

Specifies the action to take if a matching CRL or a link to a matching CRL already exists in the store. Currently defined disposition values and their uses are as follows.

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
Makes no check for an existing matching CRL or link to a matching CRL. A new CRL is always added to the store. This can lead to duplicates in a store.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_STORE_ADD_NEW"></a><a id="cert_store_add_new"></a><dl>
<dt><b>CERT_STORE_ADD_NEW</b></dt>
</dl>
</td>
<td width="60%">
If a matching CRL or a link to a matching CRL exists, the operation fails. 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> returns the CRYPT_E_EXISTS code.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_STORE_ADD_NEWER"></a><a id="cert_store_add_newer"></a><dl>
<dt><b>CERT_STORE_ADD_NEWER</b></dt>
</dl>
</td>
<td width="60%">
If a matching CRL or a link to a matching CRL exists, the <b>ThisUpdate</b> times on the CRLs are compared. If the existing CRL has a <b>ThisUpdate</b> time less than the <b>ThisUpdate</b> time on the new CRL, the old CRL or link is replaced just as with CERT_STORE_ADD_REPLACE_EXISTING. If the existing CRL has a <b>ThisUpdate</b> time greater than or equal to the <b>ThisUpdate</b> time on the CRL to be added, the function fails with 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> returning the CRYPT_E_EXISTS code.

If a matching CRL or a link to a matching CRL is not found in the store, a new CRL is added to the store.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_STORE_ADD_NEWER_INHERIT_PROPERTIES"></a><a id="cert_store_add_newer_inherit_properties"></a><dl>
<dt><b>CERT_STORE_ADD_NEWER_INHERIT_PROPERTIES</b></dt>
</dl>
</td>
<td width="60%">
The action is the same as for CERT_STORE_ADD_NEWER, except that if an older CRL is replaced, the properties of the older CRL are incorporated into the replacement CRL.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_STORE_ADD_REPLACE_EXISTING"></a><a id="cert_store_add_replace_existing"></a><dl>
<dt><b>CERT_STORE_ADD_REPLACE_EXISTING</b></dt>
</dl>
</td>
<td width="60%">
If a matching CRL or a link to a matching CRL exists, that existing CRL or link is deleted and a new CRL is created and added to the store. If a matching CRL or a link to a matching CRL does not exist, one is added.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_STORE_ADD_REPLACE_EXISTING_INHERIT_PROPERTIES"></a><a id="cert_store_add_replace_existing_inherit_properties"></a><dl>
<dt><b>CERT_STORE_ADD_REPLACE_EXISTING_INHERIT_PROPERTIES</b></dt>
</dl>
</td>
<td width="60%">
If a matching CRL exists in the store, that existing context is deleted before creating and adding the new context. The new context inherits properties from the existing CRL.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_STORE_ADD_USE_EXISTING"></a><a id="cert_store_add_use_existing"></a><dl>
<dt><b>CERT_STORE_ADD_USE_EXISTING</b></dt>
</dl>
</td>
<td width="60%">
If a matching CRL or a link to a matching CRL exists, that existing CRL is used and properties from the new CRL are added. The function does not fail, but no new CRL is added. If <i>ppCertContext</i> is not <b>NULL</b>, the existing context is duplicated. 




If a matching CRL or a link to a matching CRL does not exist, a new CRL is added.

</td>
</tr>
</table>

### -param ppCrlContext [out, optional]

A pointer to a pointer to the decoded 
<a href="/windows/desktop/api/wincrypt/ns-wincrypt-crl_context">CRL_CONTEXT</a> structure. This is an optional parameter that can be <b>NULL</b>, indicating that the calling application does not require a copy of the new or existing CRL. If a copy is made, that context must be freed using 
<a href="/windows/desktop/api/wincrypt/nf-wincrypt-certfreecrlcontext">CertFreeCRLContext</a>.

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
CERT_STORE_ADD_NEW is set and the CRL already exists in the store, or CERT_STORE_ADD_NEWER is set and there is a CRL in the store with a <b>ThisUpdate</b> time greater than or equal to the <b>ThisUpdate</b> time for the CRL to be added.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
A disposition value that is not valid was specified in the <i>dwAddDisposition</i> parameter, or an encoding type that is not valid was specified. Currently, only the encoding type X509_ASN_ENCODING is supported.

</td>
</tr>
</table>
 

If the function fails, <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> may return an <a href="/windows/desktop/SecGloss/a-gly">Abstract Syntax Notation One</a> (ASN.1) encoding/decoding error. For information about these errors, see 
<a href="/windows/desktop/SecCrypto/asn-1-encoding-decoding-return-values">ASN.1 Encoding/Decoding Return Values</a>.

## -see-also

<a href="/windows/desktop/api/wincrypt/nf-wincrypt-certaddcrlcontexttostore">CertAddCRLContextToStore</a>



<a href="/windows/desktop/api/wincrypt/nf-wincrypt-certfreecrlcontext">CertFreeCRLContext</a>



<a href="/windows/desktop/SecCrypto/cryptography-functions">Certificate Revocation List Functions</a>