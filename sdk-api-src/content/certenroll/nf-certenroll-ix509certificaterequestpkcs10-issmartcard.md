---
UID: NF:certenroll.IX509CertificateRequestPkcs10.IsSmartCard
title: IX509CertificateRequestPkcs10::IsSmartCard
author: windows-driver-content
description: Retrieves a Boolean value that indicates whether any of the cryptographic providers associated with the request object is a smart card provider.
old-location: security\ix509certificaterequestpkcs10_issmartcard_method.htm
old-project: SecCertEnroll
ms.assetid: 663ca7dd-f108-46bf-9564-cd2d7ec2bb1f
ms.author: windowsdriverdev
ms.date: 5/10/2018
ms.keywords: IX509CertificateRequestPkcs10 interface [Security],IsSmartCard method, IX509CertificateRequestPkcs10.IsSmartCard, IX509CertificateRequestPkcs10::IsSmartCard, IsSmartCard, IsSmartCard method [Security], IsSmartCard method [Security],IX509CertificateRequestPkcs10 interface, certenroll/IX509CertificateRequestPkcs10::IsSmartCard, security.ix509certificaterequestpkcs10_issmartcard_method
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
-	IX509CertificateRequestPkcs10.IsSmartCard
product: Windows
targetos: Windows
req.lib: 
req.dll: CertEnroll.dll
req.irql: 
---

# IX509CertificateRequestPkcs10::IsSmartCard


## -description


The <b>IsSmartCard</b> method retrieves a Boolean value that indicates whether any of the cryptographic providers associated with the request object is a smart card provider.


## -parameters




### -param pValue [out]

Pointer to a <b>VARIANT_BOOL</b> variable that indicates whether any of the enumerated and selected providers is  a smart card provider.


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
<dt><b><b>CERTSRV_E_PROPERTY_EMPTY</b></b></dt>
<dt></dt>
</dl>
</td>
<td width="60%">
The private key cannot be found, or the <a href="https://msdn.microsoft.com/e337ae2c-6f86-4025-8d31-47bc5d8a4ca8">ICspInformation</a> object associated with the private key cannot be found.

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
The object is not initialized.

</td>
</tr>
</table>
 




## -remarks



The <b>IsSmartCard</b> method first checks the provider associated with the private key. If that provider is not for a smart card, the method iterates through the <a href="https://msdn.microsoft.com/cad6d8f0-f7d6-4ede-96a2-b00159962a1b">CspStatuses</a> collection until it finds a selected provider that is. If no selected smart card providers are found, the method returns <b>False</b>. You must initialize the <a href="https://msdn.microsoft.com/5b3764dc-fc63-45cc-8c35-65539c461e81">IX509CertificateRequestPkcs10</a> object before calling this method. For more information, see any of the following methods:

<ul>
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




<a href="https://msdn.microsoft.com/5b3764dc-fc63-45cc-8c35-65539c461e81">IX509CertificateRequestPkcs10</a>
 

 

