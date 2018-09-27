---
UID: NF:certenroll.IX509CertificateRequestPkcs10.get_CspStatuses
title: IX509CertificateRequestPkcs10::get_CspStatuses
author: windows-sdk-content
description: Retrieves a collection of ICspStatus objects that matches the intended use of the private key associated with the certificate request.
old-location: security\ix509certificaterequestpkcs10_cspstatuses_property.htm
tech.root: seccertenroll
ms.assetid: cad6d8f0-f7d6-4ede-96a2-b00159962a1b
ms.author: windowssdkdev
ms.date: 08/31/2018
ms.keywords: CspStatuses property [Security], CspStatuses property [Security],IX509CertificateRequestPkcs10 interface, IX509CertificateRequestPkcs10 interface [Security],CspStatuses property, IX509CertificateRequestPkcs10.CspStatuses, IX509CertificateRequestPkcs10.get_CspStatuses, IX509CertificateRequestPkcs10::CspStatuses, IX509CertificateRequestPkcs10::get_CspStatuses, certenroll/IX509CertificateRequestPkcs10::CspStatuses, certenroll/IX509CertificateRequestPkcs10::get_CspStatuses, get_CspStatuses, security.ix509certificaterequestpkcs10_cspstatuses_property
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
req.lib: 
req.dll: CertEnroll.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - CertEnroll.dll
api_name:
 - IX509CertificateRequestPkcs10.CspStatuses
 - IX509CertificateRequestPkcs10.get_CspStatuses
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IX509CertificateRequestPkcs10::get_CspStatuses


## -description


The <b>CspStatuses</b> property retrieves a collection of <a href="https://msdn.microsoft.com/en-us/library/Aa376760(v=VS.85).aspx">ICspStatus</a> objects that matches the intended use of the private key associated with the certificate request.

This property is read-only.


## -parameters


## -remarks



This property retrieves a collection of <a href="https://msdn.microsoft.com/en-us/library/Aa376760(v=VS.85).aspx">ICspStatus</a> objects. Each object represents a single provider/algorithm pair. The <b>CspStatuses</b> property differs from the <a href="https://msdn.microsoft.com/en-us/library/Aa965815(v=VS.85).aspx">GetCspStatuses</a> method. The method enables you to set a <i>KeySpec</i> parameter, but <b>CspStatuses</b> uses the  <a href="https://msdn.microsoft.com/en-us/library/Aa379020(v=VS.85).aspx">KeySpec</a> property set on the private key associated with the <a href="https://msdn.microsoft.com/en-us/library/Aa377505(v=VS.85).aspx">IX509CertificateRequestPkcs10</a> object. This can be one of the following values. <table>
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
 



 If you specify a template when initializing the request object, template attributes  such as the  <b>pKIDefaultCSPs</b> and <b>pKIDefaultKeySpec</b> affect which provider/algorithm pairs are initially enabled in the collection. You can call the following properties on each <a href="https://msdn.microsoft.com/en-us/library/Aa376760(v=VS.85).aspx">ICspStatus</a> object to retrieve information about a pair:<ul>
<li>The <a href="https://msdn.microsoft.com/en-us/library/Aa376773(v=VS.85).aspx">CspInformation</a> property retrieves provider information.</li>
<li>The <a href="https://msdn.microsoft.com/en-us/library/Aa376772(v=VS.85).aspx">CspAlgorithm</a> property retrieves algorithm information.</li>
<li>The <a href="https://msdn.microsoft.com/en-us/library/Aa376775(v=VS.85).aspx">EnrollmentStatus</a> property retrieves an <a href="https://msdn.microsoft.com/en-us/library/Aa377818(v=VS.85).aspx">IX509EnrollmentStatus</a> object. Call the <a href="https://msdn.microsoft.com/en-us/library/Aa377841(v=VS.85).aspx">Selected</a> property on the status object to determine whether the provider/algorithm pair is enabled for this request.</li>
<li>The <a href="https://msdn.microsoft.com/en-us/library/Aa376779(v=VS.85).aspx">Ordinal</a> property retrieves the position in the collection of the provider/algorithm pair.</li>
</ul>


The collection retrieved by this method is saved internally on the request object. The collection exists as long as the PKCS #10 object continues to exist.

Assume, for example, that the <a href="https://msdn.microsoft.com/en-us/library/Aa379020(v=VS.85).aspx">KeySpec</a> property on the private key associated with the request object is set to XCN_AT_SIGNATURE and that a template is used to initialize the request. The following statements will be true:<ul>
<li>A collection of <a href="https://msdn.microsoft.com/en-us/library/Aa376760(v=VS.85).aspx">ICspStatus</a> objects is created and saved on the <a href="https://msdn.microsoft.com/en-us/library/Aa377505(v=VS.85).aspx">IX509CertificateRequestPkcs10</a> object. The collection contains all valid provider/algorithm pairs installed on the computer.</li>
<li>Because the <a href="https://msdn.microsoft.com/en-us/library/Aa379020(v=VS.85).aspx">KeySpec</a> property is not set to XCN_AT_NONE, the <a href="https://msdn.microsoft.com/en-us/library/Aa377841(v=VS.85).aspx">Selected</a> property is set to SelectedNo for each Cryptography API: Next Generation (CNG) provider/algorithm pair in the collection.</li>
<li>Because the <a href="https://msdn.microsoft.com/en-us/library/Aa379020(v=VS.85).aspx">KeySpec</a> property is not set to XCN_AT_KEYEXCHANGE, the <a href="https://msdn.microsoft.com/en-us/library/Aa377841(v=VS.85).aspx">Selected</a> property is set to SelectedNo for each CryptoAPI CSP/algorithm pair in the collection where the algorithm can be used only to encrypt data or archive a key.</li>
<li>For each provider referenced by the template or private key but not supported on the computer, a placeholder <a href="https://msdn.microsoft.com/en-us/library/Aa376760(v=VS.85).aspx">ICspStatus</a> object is created and added to the collection and the <a href="https://msdn.microsoft.com/en-us/library/Aa377841(v=VS.85).aspx">Selected</a> property is set to SelectedNo.</li>
<li>The <a href="https://msdn.microsoft.com/en-us/library/Aa377841(v=VS.85).aspx">Selected</a> property is set to SelectedYes for each CryptoAPI CSP/algorithm pair where the algorithm can be used only to sign data.</li>
<li>The <a href="https://msdn.microsoft.com/en-us/library/Aa376779(v=VS.85).aspx">Ordinal</a> property is set to reflect the CSP order, if any, identified by the <b>pKIDefaultCSPs</b> template attribute. The CSPs listed first by the attribute are ordered first in the collection. This property is used during enrollment if a private key must be created. The first selected CSP/algorithm pair is used to create the key, but if the operation fails, the next selected pair is tried.</li>
</ul>


 You must initialize the <a href="https://msdn.microsoft.com/en-us/library/Aa377505(v=VS.85).aspx">IX509CertificateRequestPkcs10</a> object before calling this method. For more information, see any of the following methods:<ul>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa377520(v=VS.85).aspx">InitializeDecode</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa377523(v=VS.85).aspx">InitializeFromCertificate</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa377527(v=VS.85).aspx">InitializeFromPrivateKey</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa377531(v=VS.85).aspx">InitializeFromPublicKey</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa377533(v=VS.85).aspx">InitializeFromTemplateName</a>
</li>
</ul>





## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Aa375947(v=VS.85).aspx">ICspAlgorithm</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa375948(v=VS.85).aspx">ICspAlgorithms</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa375967(v=VS.85).aspx">ICspInformation</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa375968(v=VS.85).aspx">ICspInformations</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa376760(v=VS.85).aspx">ICspStatus</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa377505(v=VS.85).aspx">IX509CertificateRequestPkcs10</a>
 

 

