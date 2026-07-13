---
UID: NN:certenroll.ICertProperty
title: ICertProperty (certenroll.h)
description: Can be used to associate an external property with a certificate.
helpviewer_keywords: ["ICertProperty","ICertProperty interface [Security]","ICertProperty interface [Security]","described","certenroll/ICertProperty","security.icertproperty"]
old-location: security\icertproperty.htm
tech.root: security
ms.assetid: 947c2f09-993d-4ced-8b76-66b79d96e3bc
ms.date: 12/05/2018
ms.keywords: ICertProperty, ICertProperty interface [Security], ICertProperty interface [Security],described, certenroll/ICertProperty, security.icertproperty
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ICertProperty
 - certenroll/ICertProperty
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - CertEnroll.dll
api_name:
 - ICertProperty
---

# ICertProperty interface


## -description

The <b>ICertProperty</b> interface can be used to associate an external property with a <a href="/windows/desktop/SecGloss/c-gly">certificate</a>. Properties are never sent to or processed by a <a href="/windows/desktop/SecGloss/c-gly">certification authority</a>, and they are not stored inside a certificate. Typically, they are associated with a  certificate after the certificate is received from the certification authority and before it is saved in a store. The properties are saved in the store along with the certificate. A collection of properties is contained in an <a href="/windows/desktop/api/certenroll/nn-certenroll-icertproperties">ICertProperties</a> object. You can initialize the collection by using an existing certificate.

The <a href="/windows/desktop/api/certenroll/ne-certenroll-certenroll_propertyid">CERTENROLL_PROPERTYID</a> enumeration identifies the properties that you can specify or retrieve. Also, the following interfaces, which inherit from <b>ICertProperty</b>, can be used to specify the most commonly used properties:<ul>
<li>
<a href="/windows/desktop/api/certenroll/nn-certenroll-icertpropertyarchived">ICertPropertyArchived</a>
</li>
<li>
<a href="/windows/desktop/api/certenroll/nn-certenroll-icertpropertyarchivedkeyhash">ICertPropertyArchivedKeyHash</a>
</li>
<li>
<a href="/windows/desktop/api/certenroll/nn-certenroll-icertpropertyautoenroll">ICertPropertyAutoEnroll</a>
</li>
<li>
<a href="/windows/desktop/api/certenroll/nn-certenroll-icertpropertybackedup">ICertPropertyBackedUp</a>
</li>
<li>
<a href="/windows/desktop/api/certenroll/nn-certenroll-icertpropertydescription">ICertPropertyDescription</a>
</li>
<li>
<a href="/windows/desktop/api/certenroll/nn-certenroll-icertpropertyenrollment">ICertPropertyEnrollment</a>
</li>
<li>
<a href="/windows/desktop/api/certenroll/nn-certenroll-icertpropertyfriendlyname">ICertPropertyFriendlyName</a>
</li>
<li>
<a href="/windows/desktop/api/certenroll/nn-certenroll-icertpropertykeyprovinfo">ICertPropertyKeyProvInfo</a>
</li>
<li>
<a href="/windows/desktop/api/certenroll/nn-certenroll-icertpropertyrenewal">ICertPropertyRenewal</a>
</li>
<li>
<a href="/windows/desktop/api/certenroll/nn-certenroll-icertpropertyrequestoriginator">ICertPropertyRequestOriginator</a>
</li>
<li>
<a href="/windows/desktop/api/certenroll/nn-certenroll-icertpropertysha1hash">ICertPropertySHA1Hash</a>
</li>
</ul>

<div class="alert"><b>Note</b>  We recommend that you use the interfaces in the preceding list when appropriate. Enrollment behavior is not defined when you use an <b>ICertProperty</b> base interface to represent any of these common properties.</div><div> </div>

## -inheritance

The <b>ICertProperty</b> interface inherits from the <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>ICertProperty</b> also has these types of members:

## -see-also

<a href="/windows/desktop/SecCertEnroll/certenroll-interfaces">CertEnroll Interfaces</a>



<a href="/windows/desktop/api/certenroll/nn-certenroll-icertproperties">ICertProperties</a>



<a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a>
