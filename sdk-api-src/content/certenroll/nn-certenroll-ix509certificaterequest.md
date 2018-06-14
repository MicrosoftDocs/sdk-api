---
UID: NN:certenroll.IX509CertificateRequest
title: IX509CertificateRequest
author: windows-sdk-content
description: The IX509CertificateRequest interface represents an abstract base certificate request that identifies methods and properties common to and inherited by each of the request objects implemented by the Certificate Enrollment API.
old-location: security\ix509certificaterequest.htm
old-project: SecCertEnroll
ms.assetid: 5425c9ab-565d-449d-87e1-e5765868acfb
ms.author: windowssdkdev
ms.date: 05/10/2018
ms.keywords: IX509CertificateRequest, IX509CertificateRequest interface [Security], IX509CertificateRequest interface [Security],described, certenroll/IX509CertificateRequest, security.ix509certificaterequest
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
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
tech.root: 
req.typenames: X509RequestType
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - CertEnroll.dll
api_name:
 - IX509CertificateRequest
product: Windows
targetos: Windows
req.lib: 
req.dll: CertEnroll.dll
req.irql: 
---

# IX509CertificateRequest interface


## -description


The <b>IX509CertificateRequest</b> interface   represents an abstract base certificate request that identifies methods and properties common to and inherited by each of the request objects implemented by the Certificate Enrollment API. The following list discusses the inheritance structure of these objects:<ul>
<li>
A PKCS #10 certificate request implements the <b>IX509CertificateRequest</b> and <a href="https://msdn.microsoft.com/5b3764dc-fc63-45cc-8c35-65539c461e81">IX509CertificateRequestPkcs10</a> interfaces. 

<img alt="Inheritance diagram for a PKCS #10 request object" src="/images/X509Inherit_RequestPkcs10.png"/>

</li>
<li>
 PKCS #7 certificate request implements the <b>IX509CertificateRequest</b> and <a href="https://msdn.microsoft.com/ae869557-6523-4387-835e-c9631898d864">IX509CertificateRequestPkcs7</a> interfaces.

<img alt="Inheritance diagram for a PKCS #7 request object" src="/images/X509Inherit_RequestPkcs7.png"/>

Although the PKCS #7 specification defines a secure message syntax rather than a type of certificate request, the implementation of the <a href="https://msdn.microsoft.com/ae869557-6523-4387-835e-c9631898d864">IX509CertificateRequestPkcs7</a> interface in this SDK requires that it contain a PKCS #10 request. Therefore, this documentation refers to a PKCS #7 object as a certificate request.

</li>
<li>
A CMC (Certificate Management Message over CMS) certificate request implements the <b>IX509CertificateRequest</b>, <a href="https://msdn.microsoft.com/ae869557-6523-4387-835e-c9631898d864">IX509CertificateRequestPkcs7</a>, and <a href="https://msdn.microsoft.com/77059388-c442-4db5-ab27-1db25e2f63b9">IX509CertificateRequestCmc</a> interfaces.

<img alt="Inheritance diagram for a CMC request object" src="/images/X509Inherit_RequestCMC.png"/>

</li>
<li>
An object that can be used to represent a self-generated certificate (a certificate not issued by a certification authority) implements the <b>IX509CertificateRequest</b>, <a href="https://msdn.microsoft.com/5b3764dc-fc63-45cc-8c35-65539c461e81">IX509CertificateRequestPkcs10</a>, and <a href="https://msdn.microsoft.com/7197a225-b2dc-47bb-8843-d3fb4bf95811">IX509CertificateRequestCertificate</a> interfaces.

<img alt="Inheritance diagram for a self-generated certificate" src="/images/X509Inherit_Requestcertificate.png"/>

</li>
</ul>



## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IX509CertificateRequest</b> interface inherits from the <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch.md">IDispatch</a> interface. <b>IX509CertificateRequest</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>IX509CertificateRequest</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/098788f4-539f-420b-a4e1-65625dd56ca1">Encode</a>
</td>
<td align="left" width="63%">
Signs and encodes a certificate request and creates a key pair if one does not exist.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5ade7824-d95a-492d-aadf-487422386500">GetInnerRequest</a>
</td>
<td align="left" width="63%">
Retrieves a nested request object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/ff550945">Initialize</a>
</td>
<td align="left" width="63%">
Initializes the request object for a user or a computer.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/7f0bd391-c456-467a-8bc1-6f0a8bd21e24">ResetForEncode</a>
</td>
<td align="left" width="63%">
Restores the state of the request object to that which existed before the <a href="https://msdn.microsoft.com/098788f4-539f-420b-a4e1-65625dd56ca1">Encode</a> method was called.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IX509CertificateRequest</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/57a87aab-1e53-4b0b-a7b9-2fe89083819b">AlternateSignatureAlgorithm</a>


</td>
<td align="left" width="63%">
Specifies and retrieves a Boolean value that indicates whether the signature algorithm object identifier for a PKCS #10 certificate request is discrete or combined.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/728dba16-cda8-4eca-8cf0-4e6139e3808b">ClientId</a>


</td>
<td align="left" width="63%">
Specifies and retrieves a value that identifies the executable that created the request.

[WebEnabled]

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/7be532ab-0ab0-4c22-b274-c925fd5827d5">CspInformations</a>


</td>
<td align="left" width="63%">
Specifies and retrieves a collection of cryptographic providers available for use by the request object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/ea0fa54d-0de6-4578-b93a-1e399101006b">EnrollmentContext</a>


</td>
<td align="left" width="63%">
Retrieves a value that specifies whether the certificate is intended for a computer or a user.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/9f68ee54-5dea-47bb-8a90-0285d081c9b8">HashAlgorithm</a>


</td>
<td align="left" width="63%">
Specifies and retrieves the object identifier of the algorithm used to sign the certificate request. 

[WebEnabled]

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/86e82a6c-7689-4bf3-8f64-e512040abd6a">ParentWindow</a>


</td>
<td align="left" width="63%">
Specifies and retrieves the ID of the window used by key-related user interface dialogs.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/1830a569-03a4-4692-adbf-b627bf4370a1">RawData</a>


</td>
<td align="left" width="63%">
Retrieves a byte array that contains the signed, DER-encoded certificate request.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/ab046b65-a059-4b48-a6cd-7e2f0b18bc65">RenewalCertificate</a>


</td>
<td align="left" width="63%">
Specifies or retrieves a byte array that contains the <a href="https://msdn.microsoft.com/d007cbb9-b547-4dc7-bc22-b526f650f7c2">Distinguished Encoding Rules</a> (DER) encoded certificate that is being renewed.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/339c8d47-4406-4f2e-b927-b2dd5f58d1ec">Silent</a>


</td>
<td align="left" width="63%">
Specifies or retrieves a Boolean value that indicates whether any of the  key-related modal dialogs are displayed during the certificate enrollment process.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/3a7847b6-52b4-4058-8113-cbc3b9101a5b">SuppressDefaults</a>


</td>
<td align="left" width="63%">
Specifies or retrieves a Boolean value that indicates whether the default extensions and attributes are included in the request.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/library/windows/hardware/hh439450">Type</a>


</td>
<td align="left" width="63%">
Retrieves a  value that specifies the type of the request object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/0eedb520-06c3-4106-8593-1c5fb0829d5e">UIContextMessage</a>


</td>
<td align="left" width="63%">
Specifies or retrieves a context string to display in the user interface.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/d49511ed-8651-457e-a102-0bea4edde24c">CertEnroll Interfaces</a>



<a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch.md">IDispatch</a>



<a href="https://msdn.microsoft.com/7197a225-b2dc-47bb-8843-d3fb4bf95811">IX509CertificateRequestCertificate</a>



<a href="https://msdn.microsoft.com/77059388-c442-4db5-ab27-1db25e2f63b9">IX509CertificateRequestCmc</a>



<a href="https://msdn.microsoft.com/5b3764dc-fc63-45cc-8c35-65539c461e81">IX509CertificateRequestPkcs10</a>



<a href="https://msdn.microsoft.com/ae869557-6523-4387-835e-c9631898d864">IX509CertificateRequestPkcs7</a>
 

 

