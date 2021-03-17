---
UID: NF:wincrypt.CertAddCTLLinkToStore
title: CertAddCTLLinkToStore function (wincrypt.h)
description: The CertAddCTLLinkToStore function adds a link in a store to a certificate trust list (CTL) context in a different store. Instead of creating and adding a duplicate of a CTL context, this function adds a link to the original CTL context.
helpviewer_keywords: ["CERT_STORE_ADD_ALWAYS","CERT_STORE_ADD_NEW","CERT_STORE_ADD_NEWER","CERT_STORE_ADD_NEWER_INHERIT_PROPERTIES","CERT_STORE_ADD_REPLACE_EXISTING","CERT_STORE_ADD_REPLACE_EXISTING_INHERIT_PROPERTIES","CERT_STORE_ADD_USE_EXISTING","CertAddCTLLinkToStore","CertAddCTLLinkToStore function [Security]","_crypto2_certaddctllinktostore","security.certaddctllinktostore","wincrypt/CertAddCTLLinkToStore"]
old-location: security\certaddctllinktostore.htm
tech.root: security
ms.assetid: c129aeae-69d9-440a-979d-e9e481c64538
ms.date: 12/05/2018
ms.keywords: CERT_STORE_ADD_ALWAYS, CERT_STORE_ADD_NEW, CERT_STORE_ADD_NEWER, CERT_STORE_ADD_NEWER_INHERIT_PROPERTIES, CERT_STORE_ADD_REPLACE_EXISTING, CERT_STORE_ADD_REPLACE_EXISTING_INHERIT_PROPERTIES, CERT_STORE_ADD_USE_EXISTING, CertAddCTLLinkToStore, CertAddCTLLinkToStore function [Security], _crypto2_certaddctllinktostore, security.certaddctllinktostore, wincrypt/CertAddCTLLinkToStore
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
 - CertAddCTLLinkToStore
 - wincrypt/CertAddCTLLinkToStore
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
 - CertAddCTLLinkToStore
---

# CertAddCTLLinkToStore function


## -description

The <b>CertAddCTLLinkToStore</b> function adds a link in a store to a <a href="/windows/desktop/SecGloss/c-gly">certificate trust list</a> (CTL) <a href="/windows/desktop/SecGloss/c-gly">context</a> in a different store. Instead of creating and adding a duplicate of a CTL context, this function adds a link to the original CTL context.

## -parameters

### -param hCertStore [in]

Handle of the certificate store where the link is to be added.

### -param pCtlContext [in]

A pointer to the 
<a href="/windows/desktop/api/wincrypt/ns-wincrypt-ctl_context">CTL_CONTEXT</a> structure to be linked.

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

A pointer to a pointer to a copy of the link created. <i>ppStoreContext</i> can be <b>NULL</b> to indicate that a copy of the link is not needed. If a copy of the link is created, that copy must be freed using 
<a href="/windows/desktop/api/wincrypt/nf-wincrypt-certfreectlcontext">CertFreeCTLContext</a>.

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
For a <i>dwAddDisposition</i> of CERT_STORE_ADD_NEW, the CTL already exists in the store.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The add disposition specified by the <i>dwAddDisposition</i> parameter is not valid.

</td>
</tr>
</table>

## -remarks

Because the link provides access to the original <a href="/windows/desktop/SecGloss/c-gly">CTL</a> context, setting an extended property in the linked CTL context changes that extended property in the original CTL's location and in any other links to that CTL.

Links cannot be added to a store that is opened as a collection. Stores opened as collections include all stores opened with 
<a href="/windows/desktop/api/wincrypt/nf-wincrypt-certopensystemstorea">CertOpenSystemStore</a> or 
<a href="/windows/desktop/api/wincrypt/nf-wincrypt-certopenstore">CertOpenStore</a> using CERT_STORE_PROV_SYSTEM or CERT_STORE_PROV_COLLECTION. Also see 
<a href="/windows/desktop/api/wincrypt/nf-wincrypt-certaddstoretocollection">CertAddStoreToCollection</a>.

When links are used and 
<a href="/windows/desktop/api/wincrypt/nf-wincrypt-certclosestore">CertCloseStore</a> is called with CERT_CLOSE_STORE_FORCE_FLAG, the store using links must be closed before the store containing the original contexts is closed. If CERT_CLOSE_STORE_FORCE_FLAG is not used, the two stores can be closed in either order.

To remove the CTL context link from the certificate store, use the  <a href="/windows/desktop/api/wincrypt/nf-wincrypt-certdeletectlfromstore">CertDeleteCTLFromStore</a> function.

## -see-also

<a href="/windows/desktop/api/wincrypt/nf-wincrypt-certaddcrllinktostore">CertAddCRLLinkToStore</a>



<a href="/windows/desktop/api/wincrypt/nf-wincrypt-certaddcertificatelinktostore">CertAddCertificateLinkToStore</a>



<a href="/windows/desktop/api/wincrypt/nf-wincrypt-certaddstoretocollection">CertAddStoreToCollection</a>



<a href="/windows/desktop/api/wincrypt/nf-wincrypt-certfreectlcontext">CertFreeCTLContext</a>



<a href="/windows/desktop/api/wincrypt/nf-wincrypt-certopensystemstorea">CertOpenSystemStore</a>



<a href="/windows/desktop/SecCrypto/cryptography-functions">Certificate Trust List Functions</a>