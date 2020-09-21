---
UID: NF:wincrypt.CertAddCertificateContextToStore
title: CertAddCertificateContextToStore function (wincrypt.h)
description: Adds a certificate context to the certificate store.
helpviewer_keywords: ["CERT_STORE_ADD_ALWAYS","CERT_STORE_ADD_NEW","CERT_STORE_ADD_NEWER","CERT_STORE_ADD_NEWER_INHERIT_PROPERTIES","CERT_STORE_ADD_REPLACE_EXISTING","CERT_STORE_ADD_REPLACE_EXISTING_INHERIT_PROPERTIES","CERT_STORE_ADD_USE_EXISTING","CertAddCertificateContextToStore","CertAddCertificateContextToStore function [Security]","_crypto2_certaddcertificatecontexttostore","security.certaddcertificatecontexttostore","wincrypt/CertAddCertificateContextToStore"]
old-location: security\certaddcertificatecontexttostore.htm
tech.root: security
ms.assetid: 5e4d8cae-1096-491f-9a04-92b7e9c020bb
ms.date: 12/05/2018
ms.keywords: CERT_STORE_ADD_ALWAYS, CERT_STORE_ADD_NEW, CERT_STORE_ADD_NEWER, CERT_STORE_ADD_NEWER_INHERIT_PROPERTIES, CERT_STORE_ADD_REPLACE_EXISTING, CERT_STORE_ADD_REPLACE_EXISTING_INHERIT_PROPERTIES, CERT_STORE_ADD_USE_EXISTING, CertAddCertificateContextToStore, CertAddCertificateContextToStore function [Security], _crypto2_certaddcertificatecontexttostore, security.certaddcertificatecontexttostore, wincrypt/CertAddCertificateContextToStore
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
 - CertAddCertificateContextToStore
 - wincrypt/CertAddCertificateContextToStore
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
 - CertAddCertificateContextToStore
---

# CertAddCertificateContextToStore function


## -description

The <b>CertAddCertificateContextToStore</b> function adds a certificate <a href="/windows/desktop/SecGloss/c-gly">context</a> to the <a href="/windows/desktop/SecGloss/c-gly">certificate store</a>.

## -parameters

### -param hCertStore [in]

Handle of a certificate store.

### -param pCertContext [in]

A pointer to the 
<a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_context">CERT_CONTEXT</a> structure to be added to the store.

### -param dwAddDisposition [in]

Specifies the action to take if a matching certificate or a link to a matching certificate already exists in the store. Currently defined disposition values and their uses are as follows. 




					

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
If a matching certificate or a link to a matching certificate exists, the operation fails. 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> returns the CRYPT_E_EXISTS code.

</td>
</tr>
<tr>
<td width="40%"><a id="___CERT_STORE_ADD_NEWER"></a><a id="___cert_store_add_newer"></a><dl>
<dt><b>   CERT_STORE_ADD_NEWER</b></dt>
</dl>
</td>
<td width="60%">
If a matching certificate or a link to a matching certificate exists  and the NotBefore
time of the existing context is equal to or greater than the
NotBefore time of the new context being added, the operation fails and <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> returns the CRYPT_E_EXISTS code. 

If the NotBefore
time of the existing context is less than the
NotBefore time of the new context being added, the existing certificate or link is deleted and a new certificate is created and added to the store. If a matching certificate or a link to a matching certificate does not exist, a new link is added.      

If <a href="/windows/desktop/SecGloss/c-gly">certificate revocation lists</a> (CRLs) or <a href="/windows/desktop/SecGloss/c-gly">certificate trust list</a> (CTLs) are being compared, the ThisUpdate time is  used.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_STORE_ADD_NEWER_INHERIT_PROPERTIES"></a><a id="cert_store_add_newer_inherit_properties"></a><dl>
<dt><b>CERT_STORE_ADD_NEWER_INHERIT_PROPERTIES</b></dt>
</dl>
</td>
<td width="60%">
If a matching certificate or a link to a matching certificate exists and the NotBefore
time of the existing context is equal to or greater than the
NotBefore time of the new context being added, the operation fails and <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> returns the CRYPT_E_EXISTS code. 

If the NotBefore
time of the existing context is less than the
NotBefore time of the new context being added, the existing context is deleted before creating and adding the new context. The new added context inherits properties from the existing certificate.

If CRLs or CTLs are being compared, the ThisUpdate time is  used.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_STORE_ADD_REPLACE_EXISTING"></a><a id="cert_store_add_replace_existing"></a><dl>
<dt><b>CERT_STORE_ADD_REPLACE_EXISTING</b></dt>
</dl>
</td>
<td width="60%">
If a link to a matching certificate exists, that existing certificate or link is deleted and a new certificate is created and added to the store. If a matching certificate or a link to a matching certificate does not exist, a new link is added.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_STORE_ADD_REPLACE_EXISTING_INHERIT_PROPERTIES"></a><a id="cert_store_add_replace_existing_inherit_properties"></a><dl>
<dt><b>CERT_STORE_ADD_REPLACE_EXISTING_INHERIT_PROPERTIES</b></dt>
</dl>
</td>
<td width="60%">
If a matching certificate exists in the store, the existing context is not replaced. The existing context inherits properties from the new certificate.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_STORE_ADD_USE_EXISTING"></a><a id="cert_store_add_use_existing"></a><dl>
<dt><b>CERT_STORE_ADD_USE_EXISTING</b></dt>
</dl>
</td>
<td width="60%">
If a matching certificate or a link to a matching certificate exists, that existing certificate or link is used and properties from the new certificate are added. The function does not fail, but it does not add a new context. If <i>pCertContext</i> is not <b>NULL</b>, the existing context is duplicated. 




If a matching certificate or a link to a matching certificate does not exist, a new certificate is added.

</td>
</tr>
</table>

### -param ppStoreContext [out, optional]

A pointer to a pointer to the copy to be made of the certificate that was added to the store. 




The <i>ppStoreContext</i> parameter can be <b>NULL</b>, indicating that the calling application does not require a copy of the added certificate. If a copy is made, it must be freed by using 
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
This value is returned if CERT_STORE_ADD_NEW is set and the certificate already exists in the store, or if CERT_STORE_ADD_NEWER is set and a certificate exists in the store with a <b>NotBefore</b> date greater than or equal to the <b>NotBefore</b> date on the certificate to be added.

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
 

Errors from the called functions, 
<a href="/windows/desktop/api/wincrypt/nf-wincrypt-certaddencodedcertificatetostore">CertAddEncodedCertificateToStore</a> and 
<a href="/windows/desktop/api/wincrypt/nf-wincrypt-certsetcertificatecontextproperty">CertSetCertificateContextProperty</a>, can be propagated to this function.

## -remarks

The certificate <a href="/windows/desktop/SecGloss/c-gly">context</a> is not duplicated using <a href="/windows/desktop/api/wincrypt/nf-wincrypt-certduplicatecertificatecontext">CertDuplicateCertificateContext</a>. Instead, the function creates a new copy of the context and adds it to the <a href="/windows/desktop/SecGloss/c-gly">store</a>.

In addition to the encoded certificate, <a href="/windows/desktop/api/wincrypt/nf-wincrypt-certduplicatecertificatecontext">CertDuplicateCertificateContext</a> also copies the context's properties, with the exception of the CERT_KEY_PROV_HANDLE_PROP_ID and CERT_KEY_CONTEXT_PROP_ID properties.

To remove the certificate context from the certificate store, use the  <a href="/windows/desktop/api/wincrypt/nf-wincrypt-certdeletecertificatefromstore">CertDeleteCertificateFromStore</a> function.

<div class="alert"><b>Note</b>  The order of the certificate context may not be preserved within the store. 
To access a specific certificate you must iterate across the certificates in the store.</div>
<div> </div>

## -see-also

<a href="/windows/desktop/api/wincrypt/nf-wincrypt-certaddencodedcertificatetostore">CertAddEncodedCertificateToStore</a>



<a href="/windows/desktop/api/wincrypt/nf-wincrypt-certsetcertificatecontextproperty">CertSetCertificateContextProperty</a>



<a href="/windows/desktop/SecCrypto/cryptography-functions">Certificate Functions</a>