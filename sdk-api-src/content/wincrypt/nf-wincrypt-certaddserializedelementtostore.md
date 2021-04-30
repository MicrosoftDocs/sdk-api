---
UID: NF:wincrypt.CertAddSerializedElementToStore
title: CertAddSerializedElementToStore function (wincrypt.h)
description: Adds a serialized certificate, certificate revocation list (CRL), or certificate trust list (CTL) element to the store.
helpviewer_keywords: ["CERT_STORE_ADD_ALWAYS","CERT_STORE_ADD_NEW","CERT_STORE_ADD_NEWER","CERT_STORE_ADD_NEWER_INHERIT_PROPERTIES","CERT_STORE_ADD_REPLACE_EXISTING","CERT_STORE_ADD_REPLACE_EXISTING_INHERIT_PROPERTIES","CERT_STORE_ADD_USE_EXISTING","CERT_STORE_ALL_CONTEXT_FLAG","CERT_STORE_CERTIFICATE_CONTEXT","CERT_STORE_CERTIFICATE_CONTEXT_FLAG","CERT_STORE_CRL_CONTEXT","CERT_STORE_CRL_CONTEXT_FLAG","CERT_STORE_CTL_CONTEXT","CERT_STORE_CTL_CONTEXT_FLAG","CertAddSerializedElementToStore","CertAddSerializedElementToStore function [Security]","_crypto2_certaddserializedelementtostore","security.certaddserializedelementtostore","wincrypt/CertAddSerializedElementToStore"]
old-location: security\certaddserializedelementtostore.htm
tech.root: security
ms.assetid: 2726cd34-51ba-4f68-9a3c-7cd505eb32a1
ms.date: 12/05/2018
ms.keywords: CERT_STORE_ADD_ALWAYS, CERT_STORE_ADD_NEW, CERT_STORE_ADD_NEWER, CERT_STORE_ADD_NEWER_INHERIT_PROPERTIES, CERT_STORE_ADD_REPLACE_EXISTING, CERT_STORE_ADD_REPLACE_EXISTING_INHERIT_PROPERTIES, CERT_STORE_ADD_USE_EXISTING, CERT_STORE_ALL_CONTEXT_FLAG, CERT_STORE_CERTIFICATE_CONTEXT, CERT_STORE_CERTIFICATE_CONTEXT_FLAG, CERT_STORE_CRL_CONTEXT, CERT_STORE_CRL_CONTEXT_FLAG, CERT_STORE_CTL_CONTEXT, CERT_STORE_CTL_CONTEXT_FLAG, CertAddSerializedElementToStore, CertAddSerializedElementToStore function [Security], _crypto2_certaddserializedelementtostore, security.certaddserializedelementtostore, wincrypt/CertAddSerializedElementToStore
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
 - CertAddSerializedElementToStore
 - wincrypt/CertAddSerializedElementToStore
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
 - CertAddSerializedElementToStore
---

# CertAddSerializedElementToStore function


## -description

The <b>CertAddSerializedElementToStore</b> function adds a serialized <a href="/windows/desktop/SecGloss/c-gly">certificate</a>, <a href="/windows/desktop/SecGloss/c-gly">certificate revocation list</a> (CRL), or <a href="/windows/desktop/SecGloss/c-gly">certificate trust list</a> (CTL) element to the store. The serialized element contains the encoded certificate, CRL, or CTL and its extended properties. Extended properties are associated with a certificate and are not part of a certificate as issued by a <a href="/windows/desktop/SecGloss/c-gly">certification authority</a>. Extended properties are not available on a certificate when it is used on a non-Microsoft platform.

## -parameters

### -param hCertStore [in]

The handle of a <a href="/windows/desktop/SecGloss/c-gly">certificate store</a> where the created certificate will be stored. If <i>hCertStore</i> is <b>NULL</b>, the function creates a copy of a certificate, CRL, or CTL context with its extended properties, but the certificate, CRL, or CTL is not persisted in any store.

### -param pbElement [in]

A pointer to a buffer that contains the certificate, CRL, or CTL information to be serialized and added to the certificate store.

### -param cbElement [in]

The size, in bytes, of the <i>pbElement</i> buffer.

### -param dwAddDisposition [in]

Specifies the action to take if the certificate, CRL, or CTL already exists in the store. Currently defined disposition values are shown in the following table.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="CERT_STORE_ADD_NEW"></a><a id="cert_store_add_new"></a><dl>
<dt><b>CERT_STORE_ADD_NEW</b></dt>
</dl>
</td>
<td width="60%">
If the certificate, CRL, or CTL is new, it is created and persisted to the store. The operation fails if an identical certificate, CRL, or CTL already exists in the store. The last error code is set to CRYPT_E_EXISTS.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_STORE_ADD_USE_EXISTING"></a><a id="cert_store_add_use_existing"></a><dl>
<dt><b>CERT_STORE_ADD_USE_EXISTING</b></dt>
</dl>
</td>
<td width="60%">
If the certificate, CRL, or CTL is new, it is added to the store. If an identical certificate, CRL, or CTL already exists, the existing element is used. If <i>ppvContext</i> is not <b>NULL</b>, the existing context is duplicated. The function only adds properties that do not already exist. The SHA-1 and MD5 hash properties are not copied.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_STORE_ADD_REPLACE_EXISTING"></a><a id="cert_store_add_replace_existing"></a><dl>
<dt><b>CERT_STORE_ADD_REPLACE_EXISTING</b></dt>
</dl>
</td>
<td width="60%">
If an identical certificate, CRL, or CTL already exists in the store, the existing certificate, CRL, or CTL context is deleted before creating and adding the new context.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_STORE_ADD_ALWAYS"></a><a id="cert_store_add_always"></a><dl>
<dt><b>CERT_STORE_ADD_ALWAYS</b></dt>
</dl>
</td>
<td width="60%">
No check is made to determine whether an identical certificate, CRL, or CTL already exists. A new element is always created. This can lead to duplicates in the store. To determine whether the element already exists in the store, call 
<a href="/windows/desktop/api/wincrypt/nf-wincrypt-certgetcrlfromstore">CertGetCRLFromStore</a> or 
<a href="/windows/desktop/api/wincrypt/nf-wincrypt-certgetsubjectcertificatefromstore">CertGetSubjectCertificateFromStore</a>.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_STORE_ADD_NEWER"></a><a id="cert_store_add_newer"></a><dl>
<dt><b>CERT_STORE_ADD_NEWER</b></dt>
</dl>
</td>
<td width="60%">
If a matching CRL or CTL or a link to a matching CRL or CTL exists, the function compares the <b>NotBefore</b> times on the CRL or CTL. If the existing CRL or CTL has a <b>NotBefore</b> time less than the <b>NotBefore</b> time on the new element, the old element or link is replaced just as with CERT_STORE_ADD_REPLACE_EXISTING. If the existing element has a <b>NotBefore</b> time greater than or equal to the <b>NotBefore</b> time on the element to be added, the function fails with 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> returning the CRYPT_E_EXISTS code.

If a matching CRL or CTL or a link to a matching CRL or CTL is not found in the store, a new element is added to the store.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_STORE_ADD_NEWER_INHERIT_PROPERTIES"></a><a id="cert_store_add_newer_inherit_properties"></a><dl>
<dt><b>CERT_STORE_ADD_NEWER_INHERIT_PROPERTIES</b></dt>
</dl>
</td>
<td width="60%">
The action is the same as for CERT_STORE_ADD_NEWER. However, if an older CRL or CTL is replaced, the properties of the older element are incorporated into the replacement.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_STORE_ADD_REPLACE_EXISTING_INHERIT_PROPERTIES"></a><a id="cert_store_add_replace_existing_inherit_properties"></a><dl>
<dt><b>CERT_STORE_ADD_REPLACE_EXISTING_INHERIT_PROPERTIES</b></dt>
</dl>
</td>
<td width="60%">
If a matching certificate exists in the store, the existing context is deleted before creating and adding the new context. The new added context inherits properties from the existing certificate.

</td>
</tr>
</table>

### -param dwFlags [in]

Reserved for future use and must be zero.

### -param dwContextTypeFlags [in]

Specifics the contexts that can be added. For example, to add either a certificate, CRL, or CTL, set <i>dwContextTypeFlags</i> to <b>CERT_STORE_CERTIFICATE_CONTEXT_FLAG</b> or <b>CERT_STORE_CRL_CONTEXT_FLAG</b>.
						

Currently defined context type flags are shown in the following table.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="CERT_STORE_ALL_CONTEXT_FLAG"></a><a id="cert_store_all_context_flag"></a><dl>
<dt><b>CERT_STORE_ALL_CONTEXT_FLAG</b></dt>
</dl>
</td>
<td width="60%">
Adds any context.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_STORE_CERTIFICATE_CONTEXT_FLAG"></a><a id="cert_store_certificate_context_flag"></a><dl>
<dt><b>CERT_STORE_CERTIFICATE_CONTEXT_FLAG</b></dt>
</dl>
</td>
<td width="60%">
Adds only a certificate context.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_STORE_CRL_CONTEXT_FLAG"></a><a id="cert_store_crl_context_flag"></a><dl>
<dt><b>CERT_STORE_CRL_CONTEXT_FLAG</b></dt>
</dl>
</td>
<td width="60%">
Adds only a CRL context.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_STORE_CTL_CONTEXT_FLAG"></a><a id="cert_store_ctl_context_flag"></a><dl>
<dt><b>CERT_STORE_CTL_CONTEXT_FLAG</b></dt>
</dl>
</td>
<td width="60%">
Adds only a CTL context.

</td>
</tr>
</table>

### -param pdwContextType [out]

A pointer to the context type of the added serialized element. This is an optional parameter and can be <b>NULL</b>, which indicates that the calling application does not require the <a href="/windows/desktop/SecGloss/c-gly">context</a> type.

Currently defined context types are shown in the following table.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="CERT_STORE_CERTIFICATE_CONTEXT"></a><a id="cert_store_certificate_context"></a><dl>
<dt><b>CERT_STORE_CERTIFICATE_CONTEXT</b></dt>
</dl>
</td>
<td width="60%">
Certificates

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_STORE_CRL_CONTEXT"></a><a id="cert_store_crl_context"></a><dl>
<dt><b>CERT_STORE_CRL_CONTEXT</b></dt>
</dl>
</td>
<td width="60%">
CRLs

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_STORE_CTL_CONTEXT"></a><a id="cert_store_ctl_context"></a><dl>
<dt><b>CERT_STORE_CTL_CONTEXT</b></dt>
</dl>
</td>
<td width="60%">
CTLs

</td>
</tr>
</table>

### -param ppvContext [out]

A pointer to a pointer to the decoded certificate, CRL, or CTL context. This is an optional parameter and can be <b>NULL</b>, which indicates that the calling application does not require the context of the added or existing certificate, CRL, or CTL.

If <i>ppvContext</i> is not <b>NULL</b>, it must be the address of a pointer to a 
<a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_context">CERT_CONTEXT</a>, 
<a href="/windows/desktop/api/wincrypt/ns-wincrypt-crl_context">CRL_CONTEXT</a>, or 
<a href="/windows/desktop/api/wincrypt/ns-wincrypt-ctl_context">CTL_CONTEXT</a>. When the application is finished with the context, the context must be freed by using 
<a href="/windows/desktop/api/wincrypt/nf-wincrypt-certfreecertificatecontext">CertFreeCertificateContext</a> for a certificate, 
<a href="/windows/desktop/api/wincrypt/nf-wincrypt-certfreecrlcontext">CertFreeCRLContext</a> for a CRL, or 
<a href="/windows/desktop/api/wincrypt/nf-wincrypt-certfreectlcontext">CertFreeCTLContext</a> for a CTL.

## -returns

If the function succeeds, the function returns nonzero.

If the function fails, it returns zero. For extended error information, call 
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
If the <i>dwAddDisposition</i> parameter is set to CERT_STORE_ADD_NEW, the certificate, CRL, or CTL already exists in the store.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
A disposition value that is not valid was specified in the <i>dwAddDisposition</i> parameter.

</td>
</tr>
</table>
 

If the function fails, <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> may return an <a href="/windows/desktop/SecGloss/a-gly">Abstract Syntax Notation One</a> (ASN.1) encoding/decoding error. For information about these errors, see 
<a href="/windows/desktop/SecCrypto/asn-1-encoding-decoding-return-values">ASN.1 Encoding/Decoding Return Values</a>.

## -see-also

<a href="/windows/desktop/api/wincrypt/nf-wincrypt-certserializecrlstoreelement">CertSerializeCRLStoreElement</a>



<a href="/windows/desktop/api/wincrypt/nf-wincrypt-certserializecertificatestoreelement">CertSerializeCertificateStoreElement</a>



<a href="/windows/desktop/SecCrypto/cryptography-functions">Certificate and Certificate Store Maintenance Functions</a>