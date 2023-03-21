---
UID: NF:certenroll.ICertProperty.put_PropertyId
title: ICertProperty::put_PropertyId (certenroll.h)
description: Specifies or retrieves a value of the CERTENROLL_PROPERTYID enumeration that identifies an external certificate property. (Put)
helpviewer_keywords: ["ICertProperty interface [Security]","PropertyId property","ICertProperty.PropertyId","ICertProperty.put_PropertyId","ICertProperty::PropertyId","ICertProperty::get_PropertyId","ICertProperty::put_PropertyId","PropertyId property [Security]","PropertyId property [Security]","ICertProperty interface","certenroll/ICertProperty::PropertyId","certenroll/ICertProperty::get_PropertyId","certenroll/ICertProperty::put_PropertyId","put_PropertyId","security.icertproperty_propertyid_property"]
old-location: security\icertproperty_propertyid_property.htm
tech.root: security
ms.assetid: 2829dab5-253d-4ade-bba5-d399afe87a28
ms.date: 12/05/2018
ms.keywords: ICertProperty interface [Security],PropertyId property, ICertProperty.PropertyId, ICertProperty.put_PropertyId, ICertProperty::PropertyId, ICertProperty::get_PropertyId, ICertProperty::put_PropertyId, PropertyId property [Security], PropertyId property [Security],ICertProperty interface, certenroll/ICertProperty::PropertyId, certenroll/ICertProperty::get_PropertyId, certenroll/ICertProperty::put_PropertyId, put_PropertyId, security.icertproperty_propertyid_property
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
 - ICertProperty::put_PropertyId
 - certenroll/ICertProperty::put_PropertyId
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
 - ICertProperty.PropertyId
 - ICertProperty.get_PropertyId
 - ICertProperty.put_PropertyId
---

# ICertProperty::put_PropertyId


## -description

The <b>PropertyId</b> property specifies or retrieves a value of the <a href="/windows/desktop/api/certenroll/ne-certenroll-certenroll_propertyid">CERTENROLL_PROPERTYID</a> enumeration that identifies an external  certificate property.

This property is read/write.

## -parameters

## -remarks

 Call the <b>PropertyId</b> property before trying to initialize the <a href="/windows/desktop/api/certenroll/nn-certenroll-icertproperty">ICertProperty</a> object. Call the <a href="/windows/desktop/api/certenroll/nf-certenroll-icertproperty-initializedecode">InitializeDecode</a> method or the <a href="/windows/desktop/api/certenroll/nf-certenroll-icertproperty-initializefromcertificate">InitializeFromCertificate</a> method to create a value for the certificate property. Call the <a href="/windows/desktop/api/certenroll/nf-certenroll-icertproperty-get_rawdata">RawData</a> property to retrieve the property value.

## -see-also

<a href="/windows/desktop/api/certenroll/nn-certenroll-icertproperties">ICertProperties</a>



<a href="/windows/desktop/api/certenroll/nn-certenroll-icertproperty">ICertProperty</a>
