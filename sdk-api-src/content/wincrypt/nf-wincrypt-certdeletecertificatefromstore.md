---
UID: NF:wincrypt.CertDeleteCertificateFromStore
title: CertDeleteCertificateFromStore function
author: windows-sdk-content
description: The CertDeleteCertificateFromStore function deletes the specified certificate context from the certificate store.
old-location: security\certdeletecertificatefromstore.htm
tech.root: seccrypto
ms.assetid: 4390c8da-9c4d-47a4-9af4-d179829f77f3
ms.author: windowssdkdev
ms.date: 12/04/2018
ms.keywords: CertDeleteCertificateFromStore, CertDeleteCertificateFromStore function [Security], _crypto2_certdeletecertificatefromstore, security.certdeletecertificatefromstore, wincrypt/CertDeleteCertificateFromStore
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# CertDeleteCertificateFromStore function


## -description


The <b>CertDeleteCertificateFromStore</b> function deletes the specified certificate <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">context</a> from the <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">certificate store</a>.
		


## -parameters




### -param pCertContext [in]

A pointer to the 
<a href="https://msdn.microsoft.com/f0a3200e-6541-423d-a4a3-595a31026eea">CERT_CONTEXT</a> structure to be deleted.


## -returns



If the function succeeds, the return value is <b>TRUE</b>.
						

If the function fails, the return value is <b>FALSE</b>. For extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>. One possible error code is the following.

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



After a certificate is deleted from a <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">store</a>, all subsequent attempts to get or find that certificate in that store will fail. However, memory allocated for the certificate is not freed until all duplicated contexts have also been freed.

The <b>CertDeleteCertificateFromStore</b> function always frees <i>pCertContext</i> by calling the <a href="https://msdn.microsoft.com/7d2f3237-3f8b-4234-b6db-3057384cd89b">CertFreeCertificateContext</a> function, even if an error is encountered. Freeing the <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">context</a> reduces the context's <a href="https://msdn.microsoft.com/ce589e18-02ac-42c2-b76b-776deb686bbd">reference count</a> by one. If the reference count reaches zero, memory allocated for the certificate is freed.


#### Examples

For an example that uses this function, see <a href="https://msdn.microsoft.com/52a0287b-7d2a-483e-8bbc-43621c4b7103">Example C Program: Deleting Certificates from a Certificate Store</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/eb542c25-8d2b-4427-8f2a-719b472613a5">CertDeleteCRLFromStore</a>



<a href="https://msdn.microsoft.com/7d2f3237-3f8b-4234-b6db-3057384cd89b">CertFreeCertificateContext</a>



<a href="cryptography_functions.htm">Certificate Functions</a>
 

 

