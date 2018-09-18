---
UID: NN:certenroll.IX509CertificateRequest
title: IX509CertificateRequest
author: windows-sdk-content
description: The IX509CertificateRequest interface represents an abstract base certificate request that identifies methods and properties common to and inherited by each of the request objects implemented by the Certificate Enrollment API.
old-location: security\ix509certificaterequest.htm
tech.root: seccertenroll
ms.assetid: 5425c9ab-565d-449d-87e1-e5765868acfb
ms.author: windowssdkdev
ms.date: 08/31/2018
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
 - IX509CertificateRequest
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IX509CertificateRequest interface


## -description


The <b>IX509CertificateRequest</b> interface   represents an abstract base certificate request that identifies methods and properties common to and inherited by each of the request objects implemented by the Certificate Enrollment API. The following list discusses the inheritance structure of these objects:<ul>
<li>
A PKCS #10 certificate request implements the <b>IX509CertificateRequest</b> and <a href="https://msdn.microsoft.com/en-us/library/Aa377505(v=VS.85).aspx">IX509CertificateRequestPkcs10</a> interfaces. 

<img alt="Inheritance diagram for a PKCS #10 request object" src="./images/X509Inherit_RequestPkcs10.png"/>

</li>
<li>
 PKCS #7 certificate request implements the <b>IX509CertificateRequest</b> and <a href="https://msdn.microsoft.com/en-us/library/Aa377608(v=VS.85).aspx">IX509CertificateRequestPkcs7</a> interfaces.

<img alt="Inheritance diagram for a PKCS #7 request object" src="./images/X509Inherit_RequestPkcs7.png"/>

Although the PKCS #7 specification defines a secure message syntax rather than a type of certificate request, the implementation of the <a href="https://msdn.microsoft.com/en-us/library/Aa377608(v=VS.85).aspx">IX509CertificateRequestPkcs7</a> interface in this SDK requires that it contain a PKCS #10 request. Therefore, this documentation refers to a PKCS #7 object as a certificate request.

</li>
<li>
A CMC (Certificate Management Message over CMS) certificate request implements the <b>IX509CertificateRequest</b>, <a href="https://msdn.microsoft.com/en-us/library/Aa377608(v=VS.85).aspx">IX509CertificateRequestPkcs7</a>, and <a href="https://msdn.microsoft.com/en-us/library/Aa377133(v=VS.85).aspx">IX509CertificateRequestCmc</a> interfaces.

<img alt="Inheritance diagram for a CMC request object" src="./images/X509Inherit_RequestCMC.png"/>

</li>
<li>
An object that can be used to represent a self-generated certificate (a certificate not issued by a certification authority) implements the <b>IX509CertificateRequest</b>, <a href="https://msdn.microsoft.com/en-us/library/Aa377505(v=VS.85).aspx">IX509CertificateRequestPkcs10</a>, and <a href="https://msdn.microsoft.com/en-us/library/Aa377124(v=VS.85).aspx">IX509CertificateRequestCertificate</a> interfaces.

<img alt="Inheritance diagram for a self-generated certificate" src="./images/X509Inherit_Requestcertificate.png"/>

</li>
</ul>



## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IX509CertificateRequest</b> interface inherits from the <a href="https://msdn.microsoft.com/en-us/library/ms221608(v=VS.85).aspx">IDispatch</a> interface. <b>IX509CertificateRequest</b> also has these types of members:
<ul>
<li><a href="https://msdn.microsoft.com/en-us/library/ms684591(v=VS.85).aspx">Methods</a></li>
<li><a href="https://msdn.microsoft.com/en-us/library/ms684591(v=VS.85).aspx">Properties</a></li>
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
<a href="https://msdn.microsoft.com/en-us/library/Aa377650(v=VS.85).aspx">Encode</a>
</td>
<td align="left" width="63%">
Signs and encodes a certificate request and creates a key pair if one does not exist.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Aa377662(v=VS.85).aspx">GetInnerRequest</a>
</td>
<td align="left" width="63%">
Retrieves a nested request object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Aa377669(v=VS.85).aspx">Initialize</a>
</td>
<td align="left" width="63%">
Initializes the request object for a user or a computer.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Aa377692(v=VS.85).aspx">ResetForEncode</a>
</td>
<td align="left" width="63%">
Restores the state of the request object to that which existed before the <a href="https://msdn.microsoft.com/en-us/library/Aa377650(v=VS.85).aspx">Encode</a> method was called.

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

<a href="https://msdn.microsoft.com/en-us/library/Aa965816(v=VS.85).aspx">AlternateSignatureAlgorithm</a>


</td>
<td align="left" width="63%">
Specifies and retrieves a Boolean value that indicates whether the signature algorithm object identifier for a PKCS #10 certificate request is discrete or combined.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/en-us/library/Aa377640(v=VS.85).aspx">ClientId</a>


</td>
<td align="left" width="63%">
Specifies and retrieves a value that identifies the executable that created the request.

[WebEnabled]

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/en-us/library/Aa377643(v=VS.85).aspx">CspInformations</a>


</td>
<td align="left" width="63%">
Specifies and retrieves a collection of cryptographic providers available for use by the request object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/en-us/library/Aa377658(v=VS.85).aspx">EnrollmentContext</a>


</td>
<td align="left" width="63%">
Retrieves a value that specifies whether the certificate is intended for a computer or a user.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/en-us/library/Aa377667(v=VS.85).aspx">HashAlgorithm</a>


</td>
<td align="left" width="63%">
Specifies and retrieves the object identifier of the algorithm used to sign the certificate request. 

[WebEnabled]

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/en-us/library/Aa377677(v=VS.85).aspx">ParentWindow</a>


</td>
<td align="left" width="63%">
Specifies and retrieves the ID of the window used by key-related user interface dialogs.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/en-us/library/Aa377685(v=VS.85).aspx">RawData</a>


</td>
<td align="left" width="63%">
Retrieves a byte array that contains the signed, DER-encoded certificate request.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/en-us/library/Aa377689(v=VS.85).aspx">RenewalCertificate</a>


</td>
<td align="left" width="63%">
Specifies or retrieves a byte array that contains the <a href="https://msdn.microsoft.com/en-us/library/ms721573(v=VS.85).aspx">Distinguished Encoding Rules</a> (DER) encoded certificate that is being renewed.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/en-us/library/Aa377696(v=VS.85).aspx">Silent</a>


</td>
<td align="left" width="63%">
Specifies or retrieves a Boolean value that indicates whether any of the  key-related modal dialogs are displayed during the certificate enrollment process.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/en-us/library/Aa377698(v=VS.85).aspx">SuppressDefaults</a>


</td>
<td align="left" width="63%">
Specifies or retrieves a Boolean value that indicates whether the default extensions and attributes are included in the request.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/en-us/library/Aa377801(v=VS.85).aspx">Type</a>


</td>
<td align="left" width="63%">
Retrieves a  value that specifies the type of the request object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/en-us/library/Aa377806(v=VS.85).aspx">UIContextMessage</a>


</td>
<td align="left" width="63%">
Specifies or retrieves a context string to display in the user interface.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Aa374850(v=VS.85).aspx">CertEnroll Interfaces</a>



<a href="https://msdn.microsoft.com/en-us/library/ms221608(v=VS.85).aspx">IDispatch</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa377124(v=VS.85).aspx">IX509CertificateRequestCertificate</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa377133(v=VS.85).aspx">IX509CertificateRequestCmc</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa377505(v=VS.85).aspx">IX509CertificateRequestPkcs10</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa377608(v=VS.85).aspx">IX509CertificateRequestPkcs7</a>
 

 

