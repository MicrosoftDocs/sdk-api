---
UID: NN:certenroll.ICertProperty
title: ICertProperty (certenroll.h)
author: windows-sdk-content
description: Can be used to associate an external property with a certificate.
old-location: security\icertproperty.htm
tech.root: seccertenroll
ms.assetid: 947c2f09-993d-4ced-8b76-66b79d96e3bc
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ICertProperty, ICertProperty interface [Security], ICertProperty interface [Security],described, certenroll/ICertProperty, security.icertproperty
ms.topic: interface
f1_keywords: 
 - "certenroll/ICertProperty"
dev_langs:
 - c++
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ICertProperty interface


## -description


The <b>ICertProperty</b> interface can be used to associate an external property with a <a href="https://docs.microsoft.com/windows/desktop/SecGloss/c-gly">certificate</a>. Properties are never sent to or processed by a <a href="https://docs.microsoft.com/windows/desktop/SecGloss/c-gly">certification authority</a>, and they are not stored inside a certificate. Typically, they are associated with a  certificate after the certificate is received from the certification authority and before it is saved in a store. The properties are saved in the store along with the certificate. A collection of properties is contained in an <a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nn-certenroll-icertproperties">ICertProperties</a> object. You can initialize the collection by using an existing certificate.

The <a href="https://docs.microsoft.com/windows/desktop/api/certenroll/ne-certenroll-certenroll_propertyid">CERTENROLL_PROPERTYID</a> enumeration identifies the properties that you can specify or retrieve. Also, the following interfaces, which inherit from <b>ICertProperty</b>, can be used to specify the most commonly used properties:<ul>
<li>
<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nn-certenroll-icertpropertyarchived">ICertPropertyArchived</a>
</li>
<li>
<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nn-certenroll-icertpropertyarchivedkeyhash">ICertPropertyArchivedKeyHash</a>
</li>
<li>
<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nn-certenroll-icertpropertyautoenroll">ICertPropertyAutoEnroll</a>
</li>
<li>
<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nn-certenroll-icertpropertybackedup">ICertPropertyBackedUp</a>
</li>
<li>
<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nn-certenroll-icertpropertydescription">ICertPropertyDescription</a>
</li>
<li>
<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nn-certenroll-icertpropertyenrollment">ICertPropertyEnrollment</a>
</li>
<li>
<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nn-certenroll-icertpropertyfriendlyname">ICertPropertyFriendlyName</a>
</li>
<li>
<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nn-certenroll-icertpropertykeyprovinfo">ICertPropertyKeyProvInfo</a>
</li>
<li>
<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nn-certenroll-icertpropertyrenewal">ICertPropertyRenewal</a>
</li>
<li>
<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nn-certenroll-icertpropertyrequestoriginator">ICertPropertyRequestOriginator</a>
</li>
<li>
<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nn-certenroll-icertpropertysha1hash">ICertPropertySHA1Hash</a>
</li>
</ul>

<div class="alert"><b>Note</b>  We recommend that you use the interfaces in the preceding list when appropriate. Enrollment behavior is not defined when you use an <b>ICertProperty</b> base interface to represent any of these common properties.</div><div> </div>

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ICertProperty</b> interface inherits from the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>ICertProperty</b> also has these types of members:
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
<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-icertproperty-initializedecode">InitializeDecode</a>
</td>
<td align="left" width="63%">
Initializes the object from a byte array that contains the property value.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-icertproperty-initializefromcertificate">InitializeFromCertificate</a>
</td>
<td align="left" width="63%">
Initializes the object by using a property value associated with an existing certificate.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-icertproperty-removefromcertificate">RemoveFromCertificate</a>
</td>
<td align="left" width="63%">
Disassociates a property from a certificate.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-icertproperty-setvalueoncertificate">SetValueOnCertificate</a>
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

<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-icertproperty-get_propertyid">PropertyId</a>


</td>
<td align="left" width="63%">
Specifies or retrieves a value of the <a href="https://docs.microsoft.com/windows/desktop/api/certenroll/ne-certenroll-certenroll_propertyid">CERTENROLL_PROPERTYID</a> enumeration that identifies an external  certificate property.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nf-certenroll-icertproperty-get_rawdata">RawData</a>


</td>
<td align="left" width="63%">
Retrieves the value of the  certificate property.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/windows/desktop/SecCertEnroll/certenroll-interfaces">CertEnroll Interfaces</a>



<a href="https://docs.microsoft.com/windows/desktop/api/certenroll/nn-certenroll-icertproperties">ICertProperties</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a>
 

 

