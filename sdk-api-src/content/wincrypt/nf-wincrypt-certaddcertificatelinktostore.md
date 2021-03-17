---
UID: NF:wincrypt.CertAddCertificateLinkToStore
title: CertAddCertificateLinkToStore function (wincrypt.h)
description: Adds a link in a certificate store to a certificate context in a different store.
helpviewer_keywords: ["CERT_STORE_ADD_ALWAYS","CERT_STORE_ADD_NEW","CERT_STORE_ADD_REPLACE_EXISTING","CERT_STORE_ADD_USE_EXISTING","CertAddCertificateLinkToStore","CertAddCertificateLinkToStore function [Security]","_crypto2_certaddcertificatelinktostore","security.certaddcertificatelinktostore","wincrypt/CertAddCertificateLinkToStore"]
old-location: security\certaddcertificatelinktostore.htm
tech.root: security
ms.assetid: bcbf7755-d0ce-4dd5-8462-72760364fdc3
ms.date: 12/05/2018
ms.keywords: CERT_STORE_ADD_ALWAYS, CERT_STORE_ADD_NEW, CERT_STORE_ADD_REPLACE_EXISTING, CERT_STORE_ADD_USE_EXISTING, CertAddCertificateLinkToStore, CertAddCertificateLinkToStore function [Security], _crypto2_certaddcertificatelinktostore, security.certaddcertificatelinktostore, wincrypt/CertAddCertificateLinkToStore
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
 - CertAddCertificateLinkToStore
 - wincrypt/CertAddCertificateLinkToStore
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
 - CertAddCertificateLinkToStore
---

# CertAddCertificateLinkToStore function


## -description

The <b>CertAddCertificateLinkToStore</b> function adds a link in a <a href="/windows/desktop/SecGloss/c-gly">certificate store</a> to a <a href="/windows/desktop/SecGloss/c-gly">certificate context</a> in a different store. Instead of creating and adding a duplicate of the certificate context, this function adds a link to the original certificate.

## -parameters

### -param hCertStore [in]

A handle to the <a href="/windows/desktop/SecGloss/c-gly">certificate store</a> where the link is to be added.

### -param pCertContext [in]

A pointer to the 
<a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_context">CERT_CONTEXT</a> structure to be linked.

### -param dwAddDisposition [in]

Specifies the action if a matching certificate or a link to a matching certificate already exists in the store. Currently defined disposition values and their uses are as follows. 




					

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
<td width="40%"><a id="CERT_STORE_ADD_REPLACE_EXISTING"></a><a id="cert_store_add_replace_existing"></a><dl>
<dt><b>CERT_STORE_ADD_REPLACE_EXISTING</b></dt>
</dl>
</td>
<td width="60%">
If a link to a matching certificate exists, that existing link is deleted and a new link is created and added to the store. If no matching certificate or link to a matching certificate exists, one is added.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_STORE_ADD_USE_EXISTING"></a><a id="cert_store_add_use_existing"></a><dl>
<dt><b>CERT_STORE_ADD_USE_EXISTING</b></dt>
</dl>
</td>
<td width="60%">
If a matching certificate or a link to a matching certificate exists, the existing certificate is used. The function does not fail, but no new link is added. If no matching certificate or link to a matching certificate exists, a new link is added.

</td>
</tr>
</table>

### -param ppStoreContext [out, optional]

A pointer to a pointer to a copy of the link created. The <i>ppStoreContext</i> parameter can be <b>NULL</b> to indicate that a copy of the link is not needed. If a copy of the link is created, that copy must be freed using 
the <a href="/windows/desktop/api/wincrypt/nf-wincrypt-certfreecertificatecontext">CertFreeCertificateContext</a> function.

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
For a <i>dwAddDisposition</i> parameter of CERT_STORE_ADD_NEW, the certificate already exists in the store.

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

Because the link provides access to the original certificate <a href="/windows/desktop/SecGloss/c-gly">context</a>, setting an extended property in the linked <a href="/windows/desktop/SecGloss/c-gly">certificate context</a> changes that extended property in the certificate's original location and in any other links to that certificate.

Links cannot be added to a store opened as a collection. Stores opened as collections include all stores opened with 
<a href="/windows/desktop/api/wincrypt/nf-wincrypt-certopensystemstorea">CertOpenSystemStore</a> or 
<a href="/windows/desktop/api/wincrypt/nf-wincrypt-certopenstore">CertOpenStore</a> using CERT_STORE_PROV_SYSTEM or CERT_STORE_PROV_COLLECTION. For more information, see 
<a href="/windows/desktop/api/wincrypt/nf-wincrypt-certaddstoretocollection">CertAddStoreToCollection</a>.

If links are used and 
<a href="/windows/desktop/api/wincrypt/nf-wincrypt-certclosestore">CertCloseStore</a> is called with CERT_CLOSE_STORE_FORCE_FLAG, the store that uses links must be closed before the store that contains the original contexts is closed. If CERT_CLOSE_STORE_FORCE_FLAG is not used, the two stores can be closed in either order.

To remove the certificate context link from the certificate store, use the  <a href="/windows/desktop/api/wincrypt/nf-wincrypt-certdeletecertificatefromstore">CertDeleteCertificateFromStore</a> function.


#### Examples

For an example that uses this function, see <a href="/windows/desktop/SecCrypto/example-c-program-certificate-store-operations">Example C Program: Certificate Store Operations</a>. For additional code that uses this function, see <a href="/windows/desktop/SecCrypto/example-c-program-collection-and-sibling-certificate-store-operations">Example C Program: Collection and Sibling Certificate Store Operations</a>.

<div class="code"></div>

## -see-also

<a href="/windows/desktop/api/wincrypt/nf-wincrypt-certaddcrllinktostore">CertAddCRLLinkToStore</a>



<a href="/windows/desktop/api/wincrypt/nf-wincrypt-certaddctllinktostore">CertAddCTLLinkToStore</a>



<a href="/windows/desktop/api/wincrypt/nf-wincrypt-certaddstoretocollection">CertAddStoreToCollection</a>



<a href="/windows/desktop/api/wincrypt/nf-wincrypt-certclosestore">CertCloseStore</a>



<a href="/windows/desktop/api/wincrypt/nf-wincrypt-certfreecertificatecontext">CertFreeCertificateContext</a>



<a href="/windows/desktop/api/wincrypt/nf-wincrypt-certopenstore">CertOpenStore</a>



<a href="/windows/desktop/api/wincrypt/nf-wincrypt-certopensystemstorea">CertOpenSystemStore</a>



<a href="/windows/desktop/SecCrypto/cryptography-functions">Certificate Functions</a>