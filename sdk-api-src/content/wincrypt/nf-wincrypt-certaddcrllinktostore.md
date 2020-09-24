---
UID: NF:wincrypt.CertAddCRLLinkToStore
title: CertAddCRLLinkToStore function (wincrypt.h)
description: Adds a link in a store to a certificate revocation list (CRL) context in a different store.
helpviewer_keywords: ["CERT_STORE_ADD_ALWAYS","CERT_STORE_ADD_NEW","CERT_STORE_ADD_NEWER","CERT_STORE_ADD_REPLACE_EXISTING","CERT_STORE_ADD_USE_EXISTING","CertAddCRLLinkToStore","CertAddCRLLinkToStore function [Security]","_crypto2_certaddcrllinktostore","security.certaddcrllinktostore","wincrypt/CertAddCRLLinkToStore"]
old-location: security\certaddcrllinktostore.htm
tech.root: security
ms.assetid: 2fde63ed-7522-4400-a16b-059a001e7c26
ms.date: 12/05/2018
ms.keywords: CERT_STORE_ADD_ALWAYS, CERT_STORE_ADD_NEW, CERT_STORE_ADD_NEWER, CERT_STORE_ADD_REPLACE_EXISTING, CERT_STORE_ADD_USE_EXISTING, CertAddCRLLinkToStore, CertAddCRLLinkToStore function [Security], _crypto2_certaddcrllinktostore, security.certaddcrllinktostore, wincrypt/CertAddCRLLinkToStore
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
 - CertAddCRLLinkToStore
 - wincrypt/CertAddCRLLinkToStore
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
 - CertAddCRLLinkToStore
---

# CertAddCRLLinkToStore function


## -description

The <b>CertAddCRLLinkToStore</b> function adds a link in a store to a <a href="/windows/desktop/SecGloss/c-gly">certificate revocation list</a> (CRL) context in a different store. Instead of creating and adding a duplicate of the CRL, this function adds a link to the original CRL context.

## -parameters

### -param hCertStore [in]

Handle of a certificate store where the link is to be added.

### -param pCrlContext [in]

A pointer to the 
<a href="/windows/desktop/api/wincrypt/ns-wincrypt-crl_context">CRL_CONTEXT</a> structure to be linked.

### -param dwAddDisposition [in]

Specifies the action to take if a matching CRL or a link to a matching CRL exists in the store. Currently defined disposition values and their uses are as follows.

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
Makes no check for an existing matching CRL or link to a matching CRL. A new link is always added to the store. This can lead to duplicates in a store.

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
If a matching CRL or a link to a matching CRL exists, the <b>ThisUpdate</b> times on the CRLs are compared. If the existing CRL has a <b>ThisUpdate</b> time less than the <b>ThisUpdate</b> time on the new CRL, the old link is replaced just as with CERT_STORE_ADD_REPLACE_EXISTING. If the existing CRL has a <b>ThisUpdate</b> time greater than or equal to the <b>ThisUpdate</b> time on the CRL to be added, the function fails with 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> returning the CRYPT_E_EXISTS code. 




If a matching CRL or a link to a matching CRL is not found in the store, a new link is added to the store.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_STORE_ADD_REPLACE_EXISTING"></a><a id="cert_store_add_replace_existing"></a><dl>
<dt><b>CERT_STORE_ADD_REPLACE_EXISTING</b></dt>
</dl>
</td>
<td width="60%">
If a link to the matching CRL exists, that existing link is deleted and a new link is created and added to the store. If a matching CRL or a link to a matching CRL does not exist, a new link is added.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_STORE_ADD_USE_EXISTING"></a><a id="cert_store_add_use_existing"></a><dl>
<dt><b>CERT_STORE_ADD_USE_EXISTING</b></dt>
</dl>
</td>
<td width="60%">
If a matching CRL or a link to a matching CRL exists, that existing link is used. The function does not fail, but no new link is added. If a matching CRL or link to a CRL does not exist, a new link is added.

</td>
</tr>
</table>

### -param ppStoreContext [out, optional]

A pointer to a pointer of a copy of the link created. The <i>ppStoreContext</i> parameter can be <b>NULL</b> to indicate that a copy of the link is not needed. If a copy of the link is created, that copy must be freed using 
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
A disposition value that is not valid was specified in the <i>dwAddDisposition</i> parameter.

</td>
</tr>
</table>

## -remarks

Because the link provides access to an original CRL context, setting an extended property in the linked CRL context changes that extended property in the CRL's original location and in any other links to that CRL.

Links cannot be added to a store that is opened as a collection. Stores opened as collections include all stores opened with 
<a href="/windows/desktop/api/wincrypt/nf-wincrypt-certopensystemstorea">CertOpenSystemStore</a> or 
<a href="/windows/desktop/api/wincrypt/nf-wincrypt-certopenstore">CertOpenStore</a> using CERT_STORE_PROV_SYSTEM or CERT_STORE_PROV_COLLECTION. For more information, see 
<a href="/windows/desktop/api/wincrypt/nf-wincrypt-certaddstoretocollection">CertAddStoreToCollection</a>.

If links are used and 
<a href="/windows/desktop/api/wincrypt/nf-wincrypt-certclosestore">CertCloseStore</a> is called with CERT_CLOSE_STORE_FORCE_FLAG, the store using links must be closed before the store containing the original contexts can be closed. If CERT_CLOSE_STORE_FORCE_FLAG is not used, the two stores can be closed in either order.

To remove the CRL context link from the certificate store, use the  <a href="/windows/desktop/api/wincrypt/nf-wincrypt-certdeletecrlfromstore">CertDeleteCRLFromStore</a> function.

## -see-also

<a href="/windows/desktop/api/wincrypt/nf-wincrypt-certaddctllinktostore">CertAddCTLLinkToStore</a>



<a href="/windows/desktop/api/wincrypt/nf-wincrypt-certaddcertificatelinktostore">CertAddCertificateLinkToStore</a>



<a href="/windows/desktop/api/wincrypt/nf-wincrypt-certaddstoretocollection">CertAddStoreToCollection</a>



<a href="/windows/desktop/api/wincrypt/nf-wincrypt-certclosestore">CertCloseStore</a>



<a href="/windows/desktop/api/wincrypt/nf-wincrypt-certfreecrlcontext">CertFreeCRLContext</a>



<a href="/windows/desktop/api/wincrypt/nf-wincrypt-certopenstore">CertOpenStore</a>



<a href="/windows/desktop/api/wincrypt/nf-wincrypt-certopensystemstorea">CertOpenSystemStore</a>



<a href="/windows/desktop/SecCrypto/cryptography-functions">Certificate Revocation List Functions</a>