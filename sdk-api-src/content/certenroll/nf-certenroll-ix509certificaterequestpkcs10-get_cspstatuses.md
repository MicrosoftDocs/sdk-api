---
UID: NF:certenroll.IX509CertificateRequestPkcs10.get_CspStatuses
title: IX509CertificateRequestPkcs10::get_CspStatuses
author: windows-sdk-content
description: Retrieves a collection of ICspStatus objects that matches the intended use of the private key associated with the certificate request.
old-location: security\ix509certificaterequestpkcs10_cspstatuses_property.htm
old-project: SecCertEnroll
ms.assetid: cad6d8f0-f7d6-4ede-96a2-b00159962a1b
ms.author: windowssdkdev
ms.date: 05/10/2018
ms.keywords: CspStatuses property [Security], CspStatuses property [Security],IX509CertificateRequestPkcs10 interface, IX509CertificateRequestPkcs10 interface [Security],CspStatuses property, IX509CertificateRequestPkcs10.CspStatuses, IX509CertificateRequestPkcs10.get_CspStatuses, IX509CertificateRequestPkcs10::CspStatuses, IX509CertificateRequestPkcs10::get_CspStatuses, certenroll/IX509CertificateRequestPkcs10::CspStatuses, certenroll/IX509CertificateRequestPkcs10::get_CspStatuses, get_CspStatuses, security.ix509certificaterequestpkcs10_cspstatuses_property
ms.prod: windows
ms.technology: windows-sdk
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
-	IX509CertificateRequestPkcs10.CspStatuses
-	IX509CertificateRequestPkcs10.get_CspStatuses
product: Windows
targetos: Windows
req.lib: 
req.dll: CertEnroll.dll
req.irql: 
---

# IX509CertificateRequestPkcs10::get_CspStatuses


## -description


The <b>CspStatuses</b> property retrieves a collection of <a href="https://msdn.microsoft.com/30cc43c8-6ef3-49ad-8cff-9a5b7389ff68">ICspStatus</a> objects that matches the intended use of the private key associated with the certificate request.

This property is read-only.


## -parameters


## -remarks



This property retrieves a collection of <a href="https://msdn.microsoft.com/30cc43c8-6ef3-49ad-8cff-9a5b7389ff68">ICspStatus</a> objects. Each object represents a single provider/algorithm pair. The <b>CspStatuses</b> property differs from the <a href="https://msdn.microsoft.com/50dc8cc5-21ee-4347-a12a-0d6e62901fbb">GetCspStatuses</a> method. The method enables you to set a <i>KeySpec</i> parameter, but <b>CspStatuses</b> uses the  <a href="https://msdn.microsoft.com/163e0fb5-e5b1-48db-a90f-66984530f92f">KeySpec</a> property set on the private key associated with the <a href="https://msdn.microsoft.com/5b3764dc-fc63-45cc-8c35-65539c461e81">IX509CertificateRequestPkcs10</a> object. This can be one of the following values. <table>
<tr>
<th>Value</th>
<th>Description</th>
</tr>
<tr>
<td>XCN_AT_NONE</td>
<td>Only Cryptography API: Next Generation (CNG) providers are selected.</td>
</tr>
<tr>
<td>XCN_AT_KEYEXCHANGE</td>
<td>Only CryptoAPI cryptographic service providers (CSPs) with encryption algorithms (including key exchange) are selected.</td>
</tr>
<tr>
<td>XCN_AT_SIGNATURE</td>
<td>Only CryptoAPI cryptographic service providers (CSPs) with signature algorithms are selected.</td>
</tr>
</table>
 



 If you specify a template when initializing the request object, template attributes  such as the  <b>pKIDefaultCSPs</b> and <b>pKIDefaultKeySpec</b> affect which provider/algorithm pairs are initially enabled in the collection. You can call the following properties on each <a href="https://msdn.microsoft.com/30cc43c8-6ef3-49ad-8cff-9a5b7389ff68">ICspStatus</a> object to retrieve information about a pair:<ul>
<li>The <a href="https://msdn.microsoft.com/9e9202ad-086e-493b-8830-0a0f8980cec5">CspInformation</a> property retrieves provider information.</li>
<li>The <a href="https://msdn.microsoft.com/fc86ff4a-98f4-4e14-8d24-132926c9b41d">CspAlgorithm</a> property retrieves algorithm information.</li>
<li>The <a href="https://msdn.microsoft.com/56798477-ec12-47b6-a226-d20258677033">EnrollmentStatus</a> property retrieves an <a href="https://msdn.microsoft.com/fa5e3a10-7f00-46b6-b740-b72d78745bf7">IX509EnrollmentStatus</a> object. Call the <a href="https://msdn.microsoft.com/library/windows/hardware/hh973228">Selected</a> property on the status object to determine whether the provider/algorithm pair is enabled for this request.</li>
<li>The <a href="https://msdn.microsoft.com/e392e28f-084e-43a7-8a5e-14bea0ed8d58">Ordinal</a> property retrieves the position in the collection of the provider/algorithm pair.</li>
</ul>


The collection retrieved by this method is saved internally on the request object. The collection exists as long as the PKCS #10 object continues to exist.

Assume, for example, that the <a href="https://msdn.microsoft.com/163e0fb5-e5b1-48db-a90f-66984530f92f">KeySpec</a> property on the private key associated with the request object is set to XCN_AT_SIGNATURE and that a template is used to initialize the request. The following statements will be true:<ul>
<li>A collection of <a href="https://msdn.microsoft.com/30cc43c8-6ef3-49ad-8cff-9a5b7389ff68">ICspStatus</a> objects is created and saved on the <a href="https://msdn.microsoft.com/5b3764dc-fc63-45cc-8c35-65539c461e81">IX509CertificateRequestPkcs10</a> object. The collection contains all valid provider/algorithm pairs installed on the computer.</li>
<li>Because the <a href="https://msdn.microsoft.com/163e0fb5-e5b1-48db-a90f-66984530f92f">KeySpec</a> property is not set to XCN_AT_NONE, the <a href="https://msdn.microsoft.com/library/windows/hardware/hh973228">Selected</a> property is set to SelectedNo for each Cryptography API: Next Generation (CNG) provider/algorithm pair in the collection.</li>
<li>Because the <a href="https://msdn.microsoft.com/163e0fb5-e5b1-48db-a90f-66984530f92f">KeySpec</a> property is not set to XCN_AT_KEYEXCHANGE, the <a href="https://msdn.microsoft.com/library/windows/hardware/hh973228">Selected</a> property is set to SelectedNo for each CryptoAPI CSP/algorithm pair in the collection where the algorithm can be used only to encrypt data or archive a key.</li>
<li>For each provider referenced by the template or private key but not supported on the computer, a placeholder <a href="https://msdn.microsoft.com/30cc43c8-6ef3-49ad-8cff-9a5b7389ff68">ICspStatus</a> object is created and added to the collection and the <a href="https://msdn.microsoft.com/library/windows/hardware/hh973228">Selected</a> property is set to SelectedNo.</li>
<li>The <a href="https://msdn.microsoft.com/library/windows/hardware/hh973228">Selected</a> property is set to SelectedYes for each CryptoAPI CSP/algorithm pair where the algorithm can be used only to sign data.</li>
<li>The <a href="https://msdn.microsoft.com/e392e28f-084e-43a7-8a5e-14bea0ed8d58">Ordinal</a> property is set to reflect the CSP order, if any, identified by the <b>pKIDefaultCSPs</b> template attribute. The CSPs listed first by the attribute are ordered first in the collection. This property is used during enrollment if a private key must be created. The first selected CSP/algorithm pair is used to create the key, but if the operation fails, the next selected pair is tried.</li>
</ul>


 You must initialize the <a href="https://msdn.microsoft.com/5b3764dc-fc63-45cc-8c35-65539c461e81">IX509CertificateRequestPkcs10</a> object before calling this method. For more information, see any of the following methods:<ul>
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




<a href="https://msdn.microsoft.com/08eba616-2e96-40cd-9fda-8549de98c138">ICspAlgorithm</a>



<a href="https://msdn.microsoft.com/bbf8cff4-b1b2-480e-8c30-eb34166db143">ICspAlgorithms</a>



<a href="https://msdn.microsoft.com/e337ae2c-6f86-4025-8d31-47bc5d8a4ca8">ICspInformation</a>



<a href="https://msdn.microsoft.com/8141023c-c162-46d6-9c37-e227ce1c8761">ICspInformations</a>



<a href="https://msdn.microsoft.com/30cc43c8-6ef3-49ad-8cff-9a5b7389ff68">ICspStatus</a>



<a href="https://msdn.microsoft.com/5b3764dc-fc63-45cc-8c35-65539c461e81">IX509CertificateRequestPkcs10</a>
 

 

