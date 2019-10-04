---
UID: NF:wincrypt.CertDeleteCertificateFromStore
title: CertDeleteCertificateFromStore function (wincrypt.h)
author: windows-sdk-content
description: The CertDeleteCertificateFromStore function deletes the specified certificate context from the certificate store.
old-location: security\certdeletecertificatefromstore.htm
tech.root: SecCrypto
ms.assetid: 4390c8da-9c4d-47a4-9af4-d179829f77f3
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: CertDeleteCertificateFromStore, CertDeleteCertificateFromStore function [Security], _crypto2_certdeletecertificatefromstore, security.certdeletecertificatefromstore, wincrypt/CertDeleteCertificateFromStore
ms.topic: function
f1_keywords:
- wincrypt/CertDeleteCertificateFromStore
dev_langs:
 - c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- DllExport
api_location:
- Crypt32.dll
api_name:
- CertDeleteCertificateFromStore
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# CertDeleteCertificateFromStore function


## -description


The <b>CertDeleteCertificateFromStore</b> function deletes the specified certificate <a href="https://docs.microsoft.com/windows/desktop/SecGloss/c-gly">context</a> from the <a href="https://docs.microsoft.com/windows/desktop/SecGloss/c-gly">certificate store</a>.
		


## -parameters




### -param pCertContext [in]

A pointer to the 
<a href="https://docs.microsoft.com/windows/desktop/api/wincrypt/ns-wincrypt-cert_context">CERT_CONTEXT</a> structure to be deleted.


## -returns



If the function succeeds, the return value is <b>TRUE</b>.
						

If the function fails, the return value is <b>FALSE</b>. For extended error information, call 
<a href="https://docs.microsoft.com/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>. One possible error code is the following.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_ACCESSDENIED</b></dt>
</dl>
</td>
<td width="60%">
Indicates the store was opened as read-only and a delete operation is not allowed.

</td>
</tr>
</table>
 




## -remarks



After a certificate is deleted from a <a href="https://docs.microsoft.com/windows/desktop/SecGloss/c-gly">store</a>, all subsequent attempts to get or find that certificate in that store will fail. However, memory allocated for the certificate is not freed until all duplicated contexts have also been freed.

The <b>CertDeleteCertificateFromStore</b> function always frees <i>pCertContext</i> by calling the <a href="https://docs.microsoft.com/windows/desktop/api/wincrypt/nf-wincrypt-certfreecertificatecontext">CertFreeCertificateContext</a> function, even if an error is encountered. Freeing the <a href="https://docs.microsoft.com/windows/desktop/SecGloss/c-gly">context</a> reduces the context's <a href="https://docs.microsoft.com/windows/desktop/SecGloss/r-gly">reference count</a> by one. If the reference count reaches zero, memory allocated for the certificate is freed.


#### Examples

For an example that uses this function, see <a href="https://docs.microsoft.com/windows/desktop/SecCrypto/example-c-program-deleting-certificates-from-a-certificate-store">Example C Program: Deleting Certificates from a Certificate Store</a>.

<div class="code"></div>



## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/wincrypt/nf-wincrypt-certdeletecrlfromstore">CertDeleteCRLFromStore</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wincrypt/nf-wincrypt-certfreecertificatecontext">CertFreeCertificateContext</a>



<a href="https://docs.microsoft.com/windows/desktop/SecCrypto/cryptography-functions">Certificate Functions</a>
 

 

