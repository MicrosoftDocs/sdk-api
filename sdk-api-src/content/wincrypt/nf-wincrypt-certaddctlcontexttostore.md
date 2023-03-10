---
UID: NF:wincrypt.CertAddCTLContextToStore
title: CertAddCTLContextToStore function (wincrypt.h)
description: Adds a certificate trust list (CTL) context to a certificate store.
helpviewer_keywords: ["CERT_STORE_ADD_ALWAYS","CERT_STORE_ADD_NEW","CERT_STORE_ADD_NEWER","CERT_STORE_ADD_NEWER_INHERIT_PROPERTIES","CERT_STORE_ADD_REPLACE_EXISTING","CERT_STORE_ADD_REPLACE_EXISTING_INHERIT_PROPERTIES","CERT_STORE_ADD_USE_EXISTING","CertAddCTLContextToStore","CertAddCTLContextToStore function [Security]","_crypto2_certaddctlcontexttostore","security.certaddctlcontexttostore","wincrypt/CertAddCTLContextToStore"]
old-location: security\certaddctlcontexttostore.htm
tech.root: security
ms.assetid: e8858f75-77a1-4c5f-a3e3-a645c5e0f053
ms.date: 12/05/2018
ms.keywords: CERT_STORE_ADD_ALWAYS, CERT_STORE_ADD_NEW, CERT_STORE_ADD_NEWER, CERT_STORE_ADD_NEWER_INHERIT_PROPERTIES, CERT_STORE_ADD_REPLACE_EXISTING, CERT_STORE_ADD_REPLACE_EXISTING_INHERIT_PROPERTIES, CERT_STORE_ADD_USE_EXISTING, CertAddCTLContextToStore, CertAddCTLContextToStore function [Security], _crypto2_certaddctlcontexttostore, security.certaddctlcontexttostore, wincrypt/CertAddCTLContextToStore
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
 - CertAddCTLContextToStore
 - wincrypt/CertAddCTLContextToStore
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
 - CertAddCTLContextToStore
---

# CertAddCTLContextToStore function


## -description

The <b>CertAddCTLContextToStore</b> function adds a <a href="/windows/desktop/SecGloss/c-gly">certificate trust list</a> (CTL) context to a <a href="/windows/desktop/SecGloss/c-gly">certificate store</a>.

## -parameters

### -param hCertStore [in]

Handle of a certificate store.

### -param pCtlContext [in]

A pointer to the 
<a href="/windows/desktop/api/wincrypt/ns-wincrypt-ctl_context">CTL_CONTEXT</a> structure to be added to the store.

### -param dwAddDisposition [in]

Specifies the action to take if a matching CTL or a link to a matching CTL already exists in the store. Currently defined disposition values and their uses are as follows.

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
Makes no check for an existing matching CTL or link to a matching CTL. A new CTL is always added to the store. This can lead to duplicates in a store.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_STORE_ADD_NEW"></a><a id="cert_store_add_new"></a><dl>
<dt><b>CERT_STORE_ADD_NEW</b></dt>
</dl>
</td>
<td width="60%">
If a matching CTL or a link to a matching CTL exists, the operation fails. 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> returns the CRYPT_E_EXISTS code.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_STORE_ADD_NEWER"></a><a id="cert_store_add_newer"></a><dl>
<dt><b>CERT_STORE_ADD_NEWER</b></dt>
</dl>
</td>
<td width="60%">
If a matching CTL or a link to a matching CTL exists, the <b>ThisUpdate</b> times on the CTLs are compared. If the existing CTL has a <b>ThisUpdate</b> time less than the <b>ThisUpdate</b> time on the new CTL, the old CTL or link is replaced just as with CERT_STORE_ADD_REPLACE_EXISTING. If the existing CTL has a <b>ThisUpdate</b> time greater than or equal to the <b>ThisUpdate</b> time on the CTL to be added, the function fails with 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> returning the CRYPT_E_EXISTS code.

If a matching CTL or a link to a matching CTL is not found in the store, a new CTL is added to the store.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_STORE_ADD_NEWER_INHERIT_PROPERTIES"></a><a id="cert_store_add_newer_inherit_properties"></a><dl>
<dt><b>CERT_STORE_ADD_NEWER_INHERIT_PROPERTIES</b></dt>
</dl>
</td>
<td width="60%">
The action is the same as for CERT_STORE_ADD_NEWER, except that if an older CTL is replaced, the properties of the older CTL are incorporated into the replacement CTL.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_STORE_ADD_REPLACE_EXISTING"></a><a id="cert_store_add_replace_existing"></a><dl>
<dt><b>CERT_STORE_ADD_REPLACE_EXISTING</b></dt>
</dl>
</td>
<td width="60%">
If a matching CTL or a link to a matching CTL exists, the existing CTL or link is deleted and a new CTL is created and added to the store. If a matching CTL or a link to a matching CTL does not exist, one is added.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_STORE_ADD_REPLACE_EXISTING_INHERIT_PROPERTIES"></a><a id="cert_store_add_replace_existing_inherit_properties"></a><dl>
<dt><b>CERT_STORE_ADD_REPLACE_EXISTING_INHERIT_PROPERTIES</b></dt>
</dl>
</td>
<td width="60%">
If a matching CTL exists in the store, that existing context is deleted before creating and adding the new context. The added context inherits properties from the existing CTL.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_STORE_ADD_USE_EXISTING"></a><a id="cert_store_add_use_existing"></a><dl>
<dt><b>CERT_STORE_ADD_USE_EXISTING</b></dt>
</dl>
</td>
<td width="60%">
If a matching CTL or a link to a matching CTL exists, that existing CTL is used and properties from the new CTL are added. The function does not fail, but no new CTL is added. If <i>ppCertContext</i> is not <b>NULL</b>, the existing context is duplicated.

If a matching CTL or a link to a matching CTL does not exist, a new CTL is added.

</td>
</tr>
</table>

### -param ppStoreContext [out, optional]

Pointer to a pointer to the decoded CTL <a href="/windows/desktop/SecGloss/c-gly">context</a>. This optional parameter can be <b>NULL</b> indicating that the calling application does not require a copy of the added or existing CTL. If a copy is made, that context must be freed using 
<a href="/windows/desktop/api/wincrypt/nf-wincrypt-certfreectlcontext">CertFreeCTLContext</a>.

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
This error is returned if CERT_STORE_ADD_NEW is set and the CTL exists in the store or if CERT_STORE_ADD_NEWER is set and a CTL exists in the store with a <b>ThisUpdate</b> date greater than or equal to the <b>ThisUpdate</b> date on the CTL to be added.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
An add disposition that is not valid was specified by the <i>dwAddDisposition</i> parameter.

</td>
</tr>
</table>

## -remarks

The CTL context is not duplicated using 
<a href="/windows/desktop/api/wincrypt/nf-wincrypt-certduplicatectlcontext">CertDuplicateCTLContext</a>. Instead, a new copy is created and added to the store. In addition to the encoded CTL, the context's properties are copied.

To remove the CTL context from the certificate store, use the  <a href="/windows/desktop/api/wincrypt/nf-wincrypt-certdeletectlfromstore">CertDeleteCTLFromStore</a> function.

## -see-also

<a href="/windows/desktop/api/wincrypt/nf-wincrypt-certaddencodedctltostore">CertAddEncodedCTLToStore</a>



<a href="/windows/desktop/api/wincrypt/nf-wincrypt-certsetctlcontextproperty">CertSetCTLContextProperty</a>



<a href="/windows/desktop/SecCrypto/cryptography-functions">Certificate Trust List Functions</a>