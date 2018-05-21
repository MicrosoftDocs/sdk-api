---
UID: NF:certenroll.IX509CertificateRequestCertificate.CheckPublicKeySignature
title: IX509CertificateRequestCertificate::CheckPublicKeySignature
author: windows-driver-content
description: Verifies the certificate signature by using the public key of the signing certificate.
old-location: security\ix509certificaterequestcertificate_checkpublickeysignature_method.htm
old-project: SecCertEnroll
ms.assetid: b7c7becc-667a-4ee2-ae61-0a009d0c87e7
ms.author: windowsdriverdev
ms.date: 5/10/2018
ms.keywords: CheckPublicKeySignature, CheckPublicKeySignature method [Security], CheckPublicKeySignature method [Security],IX509CertificateRequestCertificate interface, IX509CertificateRequestCertificate interface [Security],CheckPublicKeySignature method, IX509CertificateRequestCertificate.CheckPublicKeySignature, IX509CertificateRequestCertificate::CheckPublicKeySignature, certenroll/IX509CertificateRequestCertificate::CheckPublicKeySignature, security.ix509certificaterequestcertificate_checkpublickeysignature_method
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: certenroll.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: X509RequestType
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	CertEnroll.dll
api_name:
-	IX509CertificateRequestCertificate.CheckPublicKeySignature
product: Windows
targetos: Windows
req.lib: 
req.dll: CertEnroll.dll
req.irql: 
---

# IX509CertificateRequestCertificate::CheckPublicKeySignature


## -description


The <b>CheckPublicKeySignature</b> method verifies the certificate signature by using the public key of the signing certificate.


## -parameters




### -param pPublicKey [in]

Pointer to an <a href="https://msdn.microsoft.com/cd6f28a3-9998-40d7-a3e8-dab0cf3991a8">IX509PublicKey</a> interface that represents the public key.


## -returns



If the function succeeds, the function returns <b>S_OK</b>.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error. Possible values include, but are not limited to, those in the following table. For a list of common error codes, see <a href="https://msdn.microsoft.com/ce52efc3-92c7-40e4-ac49-0c54049e169f">Common HRESULT Values</a>.

<table>
<tr>
<th>Return code/value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><b>CRYPT_E_NO_SIGNER</b></b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
The signature cannot be found.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><b>HRESULT_FROM_WIN32(ERROR_INVALID_STATE)</b></b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
The <a href="https://msdn.microsoft.com/cd6f28a3-9998-40d7-a3e8-dab0cf3991a8">IX509PublicKey</a> object has not been initialized.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b><b>OLE_E_BLANK</b></b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
The request object has not been initialized.

</td>
</tr>
</table>
 




## -remarks



This method decrypts the signature and compares it to a hash of the certificate, using the hash algorithm specified by the signature. You must initialize the request object before calling this property. For more information, see any of the following methods:

<ul>
<li>
<a href="https://msdn.microsoft.com/library/windows/hardware/ff550945">Initialize</a>
</li>
<li>
<a href="https://msdn.microsoft.com/10ab62c3-9c6f-4e1b-8a86-131d08282d9c">InitializeDecode</a>
</li>
<li>
<a href="https://msdn.microsoft.com/3f390abc-5c1c-4f9c-a5f4-4d6fec065acf">InitializeFromCertificate</a>
</li>
<li>
<a href="https://msdn.microsoft.com/b26e69c4-bfe4-4395-aaf6-bc1d045f59cc">InitializeFromPrivateKey</a>
</li>
<li>
<a href="https://msdn.microsoft.com/7b7e00dc-649b-4bcb-a9b6-5745b33ea48b">InitializeFromPublicKey</a>
</li>
<li>
<a href="https://msdn.microsoft.com/4ea746c3-b967-41b4-94ae-7b16b93ca4e4">InitializeFromTemplateName</a>
</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/7197a225-b2dc-47bb-8843-d3fb4bf95811">IX509CertificateRequestCertificate</a>
 

 

