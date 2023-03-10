---
UID: NF:wincrypt.CertAddCRLContextToStore
title: CertAddCRLContextToStore function (wincrypt.h)
description: Adds a certificate revocation list (CRL) context to the specified certificate store.
helpviewer_keywords: ["CERT_STORE_ADD_ALWAYS","CERT_STORE_ADD_NEW","CERT_STORE_ADD_NEWER","CERT_STORE_ADD_NEWER_INHERIT_PROPERTIES","CERT_STORE_ADD_REPLACE_EXISTING","CERT_STORE_ADD_REPLACE_EXISTING_INHERIT_PROPERTIES","CERT_STORE_ADD_USE_EXISTING","CertAddCRLContextToStore","CertAddCRLContextToStore function [Security]","_crypto2_certaddcrlcontexttostore","security.certaddcrlcontexttostore","wincrypt/CertAddCRLContextToStore"]
old-location: security\certaddcrlcontexttostore.htm
tech.root: security
ms.assetid: 5dfa1c08-5d75-4ee4-bd65-ce56eb61ecce
ms.date: 12/05/2018
ms.keywords: CERT_STORE_ADD_ALWAYS, CERT_STORE_ADD_NEW, CERT_STORE_ADD_NEWER, CERT_STORE_ADD_NEWER_INHERIT_PROPERTIES, CERT_STORE_ADD_REPLACE_EXISTING, CERT_STORE_ADD_REPLACE_EXISTING_INHERIT_PROPERTIES, CERT_STORE_ADD_USE_EXISTING, CertAddCRLContextToStore, CertAddCRLContextToStore function [Security], _crypto2_certaddcrlcontexttostore, security.certaddcrlcontexttostore, wincrypt/CertAddCRLContextToStore
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
 - CertAddCRLContextToStore
 - wincrypt/CertAddCRLContextToStore
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
 - CertAddCRLContextToStore
---

# CertAddCRLContextToStore function


## -description

The <b>CertAddCRLContextToStore</b> function adds a <a href="/windows/desktop/SecGloss/c-gly">certificate revocation list</a> (CRL) context to the specified <a href="/windows/desktop/SecGloss/c-gly">certificate store</a>.

## -parameters

### -param hCertStore [in]

Handle of a certificate store.

### -param pCrlContext [in]

A pointer to the 
<a href="/windows/desktop/api/wincrypt/ns-wincrypt-crl_context">CRL_CONTEXT</a> structure to be added.

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
If a matching CRL or a link to a matching CRL exists, the function compares the <b>ThisUpdate</b> times on the CRLs. If the existing CRL has a <b>ThisUpdate</b> time less than the <b>ThisUpdate</b> time on the new CRL, the old CRL or link is replaced just as with CERT_STORE_ADD_REPLACE_EXISTING. If the existing CRL has a <b>ThisUpdate</b> time greater than or equal to the <b>ThisUpdate</b> time on the CRL to be added, the function fails with 
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
If a matching CRL or a link to a matching CRL exists, the existing CRL or link is deleted and a new CRL is created and added to the store. If a matching CRL or a link to a matching CRL does not exist, one is added.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_STORE_ADD_REPLACE_EXISTING_INHERIT_PROPERTIES"></a><a id="cert_store_add_replace_existing_inherit_properties"></a><dl>
<dt><b>CERT_STORE_ADD_REPLACE_EXISTING_INHERIT_PROPERTIES</b></dt>
</dl>
</td>
<td width="60%">
If a matching CRL exists in the store, the existing context is deleted before creating and adding the new context. The added context inherits properties from the existing CRL.

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

### -param ppStoreContext [out, optional]

A pointer to a pointer to the decoded CRL context. This is an optional parameter and can be <b>NULL</b>, indicating that the calling application does not require a copy of the added or existing CRL. If a copy is made, that context must be freed by using 
<a href="/windows/desktop/api/wincrypt/nf-wincrypt-certfreecrlcontext">CertFreeCRLContext</a>.

## -returns

If the function succeeds, the return value is <b>TRUE</b>.

If the function fails, the return value is <b>FALSE</b>. Errors from the called functions 
<a href="/windows/desktop/api/wincrypt/nf-wincrypt-certaddencodedcrltostore">CertAddEncodedCRLToStore</a> and 
<a href="/windows/desktop/api/wincrypt/nf-wincrypt-certsetcrlcontextproperty">CertSetCRLContextProperty</a> can be propagated to this function.

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
<dt><b>CRYPT_E_EXISTS</b></dt>
</dl>
</td>
<td width="60%">
This error is returned if CERT_STORE_ADD_NEW is set and the CRL already exists in the store or if CERT_STORE_ADD_NEWER is set and a CRL exists in the store with a <b>ThisUpdate</b> date greater than or equal to the <b>ThisUpdate</b> date on the CRL to be added.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The <i>dwAddDisposition</i> parameter specified a disposition value that is not valid.

</td>
</tr>
</table>

## -remarks

The CRL context is not duplicated using 
<a href="/windows/desktop/api/wincrypt/nf-wincrypt-certduplicatecrlcontext">CertDuplicateCRLContext</a>. Instead, a new copy is created and added to the store. In addition to copying the encoded CRL, the function copies the context's properties.

To remove the CRL context from the certificate store, use the  <a href="/windows/desktop/api/wincrypt/nf-wincrypt-certdeletecrlfromstore">CertDeleteCRLFromStore</a> function.

## -see-also

<a href="/windows/desktop/api/wincrypt/nf-wincrypt-certaddencodedcrltostore">CertAddEncodedCRLToStore</a>



<a href="/windows/desktop/api/wincrypt/nf-wincrypt-certduplicatecrlcontext">CertDuplicateCRLContext</a>



<a href="/windows/desktop/api/wincrypt/nf-wincrypt-certfreecrlcontext">CertFreeCRLContext</a>



<a href="/windows/desktop/api/wincrypt/nf-wincrypt-certsetcrlcontextproperty">CertSetCRLContextProperty</a>



<a href="/windows/desktop/SecCrypto/cryptography-functions">Certificate Revocation List Functions</a>