---
UID: NN:certenroll.ICertProperty
title: ICertProperty
author: windows-sdk-content
description: Can be used to associate an external property with a certificate.
old-location: security\icertproperty.htm
tech.root: seccertenroll
ms.assetid: 947c2f09-993d-4ced-8b76-66b79d96e3bc
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: ICertProperty, ICertProperty interface [Security], ICertProperty interface [Security],described, certenroll/ICertProperty, security.icertproperty
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - ICertProperty
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ICertProperty interface


## -description


The <b>ICertProperty</b> interface can be used to associate an external property with a <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">certificate</a>. Properties are never sent to or processed by a <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">certification authority</a>, and they are not stored inside a certificate. Typically, they are associated with a  certificate after the certificate is received from the certification authority and before it is saved in a store. The properties are saved in the store along with the certificate. A collection of properties is contained in an <a href="https://msdn.microsoft.com/b830c0af-0a38-419d-8a33-8e3626c4e8f1">ICertProperties</a> object. You can initialize the collection by using an existing certificate.

The <a href="https://msdn.microsoft.com/e7ad0ec5-a568-4506-ba54-908e00083c2b">CERTENROLL_PROPERTYID</a> enumeration identifies the properties that you can specify or retrieve. Also, the following interfaces, which inherit from <b>ICertProperty</b>, can be used to specify the most commonly used properties:<ul>
<li>
<a href="https://msdn.microsoft.com/81219ad9-4717-40e5-9ecd-d3df980e23c6">ICertPropertyArchived</a>
</li>
<li>
<a href="https://msdn.microsoft.com/06696346-b9d1-4229-991e-539862cff3c9">ICertPropertyArchivedKeyHash</a>
</li>
<li>
<a href="https://msdn.microsoft.com/25eab0e9-4980-49ad-9d3b-35ad47c20bcb">ICertPropertyAutoEnroll</a>
</li>
<li>
<a href="https://msdn.microsoft.com/9c694991-6f2d-420e-9f9f-5a36b10c39aa">ICertPropertyBackedUp</a>
</li>
<li>
<a href="https://msdn.microsoft.com/229e8ce9-fe18-45f4-8f91-cd741052a134">ICertPropertyDescription</a>
</li>
<li>
<a href="https://msdn.microsoft.com/7530998b-b59c-426b-a74a-ead4bca55c3b">ICertPropertyEnrollment</a>
</li>
<li>
<a href="https://msdn.microsoft.com/d2bfe2f2-423e-4620-8933-bbae4f98c62a">ICertPropertyFriendlyName</a>
</li>
<li>
<a href="https://msdn.microsoft.com/1c35c2f0-8e79-4031-bae2-2be081f3c8dd">ICertPropertyKeyProvInfo</a>
</li>
<li>
<a href="https://msdn.microsoft.com/c87a391a-aec9-4b42-8084-c593ecbb0bc6">ICertPropertyRenewal</a>
</li>
<li>
<a href="https://msdn.microsoft.com/ce33605e-c3ae-4b96-a13e-6f06e8d5ffee">ICertPropertyRequestOriginator</a>
</li>
<li>
<a href="https://msdn.microsoft.com/0946827b-c933-472c-9466-aaa3495ab202">ICertPropertySHA1Hash</a>
</li>
</ul>

<div class="alert"><b>Note</b>  We recommend that you use the interfaces in the preceding list when appropriate. Enrollment behavior is not defined when you use an <b>ICertProperty</b> base interface to represent any of these common properties.</div><div> </div>

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ICertProperty</b> interface inherits from the <a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a> interface. <b>ICertProperty</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>ICertProperty</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/38b51242-cd4a-402e-b7ff-286f7bf66953">InitializeDecode</a>
</td>
<td align="left" width="63%">
Initializes the object from a byte array that contains the property value.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5d23bacc-bbe5-42fa-b4c5-57a6767f79ba">InitializeFromCertificate</a>
</td>
<td align="left" width="63%">
Initializes the object by using a property value associated with an existing certificate.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9f3e21ec-f537-40ba-84a3-b71c7aa50e84">RemoveFromCertificate</a>
</td>
<td align="left" width="63%">
Disassociates a property from a certificate.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/46c409c4-46bd-4349-8363-1983f4411bc2">SetValueOnCertificate</a>
</td>
<td align="left" width="63%">
Associates a property value with an existing certificate.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ICertProperty</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/2829dab5-253d-4ade-bba5-d399afe87a28">PropertyId</a>


</td>
<td align="left" width="63%">
Specifies or retrieves a value of the <a href="https://msdn.microsoft.com/e7ad0ec5-a568-4506-ba54-908e00083c2b">CERTENROLL_PROPERTYID</a> enumeration that identifies an external  certificate property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/1413f6da-0fcf-42ca-a79f-43f164368407">RawData</a>


</td>
<td align="left" width="63%">
Retrieves the value of the  certificate property.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/d49511ed-8651-457e-a102-0bea4edde24c">CertEnroll Interfaces</a>



<a href="https://msdn.microsoft.com/b830c0af-0a38-419d-8a33-8e3626c4e8f1">ICertProperties</a>



<a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a>
 

 

