---
UID: NN:certenroll.ICertProperty
title: ICertProperty
author: windows-sdk-content
description: Can be used to associate an external property with a certificate.
old-location: security\icertproperty.htm
old-project: seccertenroll
ms.assetid: 947c2f09-993d-4ced-8b76-66b79d96e3bc
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: ICertProperty, ICertProperty interface [Security], ICertProperty interface [Security],described, certenroll/ICertProperty, security.icertproperty
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: certenroll.h
req.include-header: 
req.redist: 
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
 - ICertProperty
product: Windows
targetos: Windows
req.lib: 
req.dll: CertEnroll.dll
req.irql: 
---

# ICertProperty interface


## -description


The <b>ICertProperty</b> interface can be used to associate an external property with a <a href="https://msdn.microsoft.com/en-us/library/ms721572(v=VS.85).aspx">certificate</a>. Properties are never sent to or processed by a <a href="https://msdn.microsoft.com/en-us/library/ms721572(v=VS.85).aspx">certification authority</a>, and they are not stored inside a certificate. Typically, they are associated with a  certificate after the certificate is received from the certification authority and before it is saved in a store. The properties are saved in the store along with the certificate. A collection of properties is contained in an <a href="https://msdn.microsoft.com/en-us/library/Aa375231(v=VS.85).aspx">ICertProperties</a> object. You can initialize the collection by using an existing certificate.

The <a href="https://msdn.microsoft.com/en-us/library/Aa374867(v=VS.85).aspx">CERTENROLL_PROPERTYID</a> enumeration identifies the properties that you can specify or retrieve. Also, the following interfaces, which inherit from <b>ICertProperty</b>, can be used to specify the most commonly used properties:<ul>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa375240(v=VS.85).aspx">ICertPropertyArchived</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa375241(v=VS.85).aspx">ICertPropertyArchivedKeyHash</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa375250(v=VS.85).aspx">ICertPropertyAutoEnroll</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa375353(v=VS.85).aspx">ICertPropertyBackedUp</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa375646(v=VS.85).aspx">ICertPropertyDescription</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa375665(v=VS.85).aspx">ICertPropertyEnrollment</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa375715(v=VS.85).aspx">ICertPropertyFriendlyName</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa375725(v=VS.85).aspx">ICertPropertyKeyProvInfo</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa375749(v=VS.85).aspx">ICertPropertyRenewal</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa375772(v=VS.85).aspx">ICertPropertyRequestOriginator</a>
</li>
<li>
<a href="https://msdn.microsoft.com/en-us/library/Aa375792(v=VS.85).aspx">ICertPropertySHA1Hash</a>
</li>
</ul>

<div class="alert"><b>Note</b>  We recommend that you use the interfaces in the preceding list when appropriate. Enrollment behavior is not defined when you use an <b>ICertProperty</b> base interface to represent any of these common properties.</div><div> </div>

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ICertProperty</b> interface inherits from the <a href="https://msdn.microsoft.com/en-us/library/ms221608(v=VS.85).aspx">IDispatch</a> interface. <b>ICertProperty</b> also has these types of members:
<ul>
<li><a href="https://msdn.microsoft.com/en-us/library/ms684591(v=VS.85).aspx">Methods</a></li>
<li><a href="https://msdn.microsoft.com/en-us/library/ms684591(v=VS.85).aspx">Properties</a></li>
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
<a href="https://msdn.microsoft.com/en-us/library/Aa375811(v=VS.85).aspx">InitializeDecode</a>
</td>
<td align="left" width="63%">
Initializes the object from a byte array that contains the property value.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Aa375817(v=VS.85).aspx">InitializeFromCertificate</a>
</td>
<td align="left" width="63%">
Initializes the object by using a property value associated with an existing certificate.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Aa375842(v=VS.85).aspx">RemoveFromCertificate</a>
</td>
<td align="left" width="63%">
Disassociates a property from a certificate.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Aa375928(v=VS.85).aspx">SetValueOnCertificate</a>
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

<a href="https://msdn.microsoft.com/en-us/library/Aa375830(v=VS.85).aspx">PropertyId</a>


</td>
<td align="left" width="63%">
Specifies or retrieves a value of the <a href="https://msdn.microsoft.com/en-us/library/Aa374867(v=VS.85).aspx">CERTENROLL_PROPERTYID</a> enumeration that identifies an external  certificate property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/en-us/library/Aa375836(v=VS.85).aspx">RawData</a>


</td>
<td align="left" width="63%">
Retrieves the value of the  certificate property.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Aa374850(v=VS.85).aspx">CertEnroll Interfaces</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa375231(v=VS.85).aspx">ICertProperties</a>



<a href="https://msdn.microsoft.com/en-us/library/ms221608(v=VS.85).aspx">IDispatch</a>
 

 

