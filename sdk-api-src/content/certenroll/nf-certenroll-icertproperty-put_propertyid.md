---
UID: NF:certenroll.ICertProperty.put_PropertyId
title: ICertProperty::put_PropertyId
author: windows-sdk-content
description: Specifies or retrieves a value of the CERTENROLL_PROPERTYID enumeration that identifies an external certificate property.
old-location: security\icertproperty_propertyid_property.htm
tech.root: SecCertEnroll
ms.assetid: 2829dab5-253d-4ade-bba5-d399afe87a28
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: ICertProperty interface [Security],PropertyId property, ICertProperty.PropertyId, ICertProperty.put_PropertyId, ICertProperty::PropertyId, ICertProperty::get_PropertyId, ICertProperty::put_PropertyId, PropertyId property [Security], PropertyId property [Security],ICertProperty interface, certenroll/ICertProperty::PropertyId, certenroll/ICertProperty::get_PropertyId, certenroll/ICertProperty::put_PropertyId, put_PropertyId, security.icertproperty_propertyid_property
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
 - ICertProperty.PropertyId
 - ICertProperty.get_PropertyId
 - ICertProperty.put_PropertyId
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ICertProperty::put_PropertyId


## -description


The <b>PropertyId</b> property specifies or retrieves a value of the <a href="https://msdn.microsoft.com/e7ad0ec5-a568-4506-ba54-908e00083c2b">CERTENROLL_PROPERTYID</a> enumeration that identifies an external  certificate property.

This property is read/write.


## -parameters


## -remarks



 Call the <b>PropertyId</b> property before trying to initialize the <a href="https://msdn.microsoft.com/947c2f09-993d-4ced-8b76-66b79d96e3bc">ICertProperty</a> object. Call the <a href="https://msdn.microsoft.com/38b51242-cd4a-402e-b7ff-286f7bf66953">InitializeDecode</a> method or the <a href="https://msdn.microsoft.com/5d23bacc-bbe5-42fa-b4c5-57a6767f79ba">InitializeFromCertificate</a> method to create a value for the certificate property. Call the <a href="https://msdn.microsoft.com/1413f6da-0fcf-42ca-a79f-43f164368407">RawData</a> property to retrieve the property value.




## -see-also




<a href="https://msdn.microsoft.com/b830c0af-0a38-419d-8a33-8e3626c4e8f1">ICertProperties</a>



<a href="https://msdn.microsoft.com/947c2f09-993d-4ced-8b76-66b79d96e3bc">ICertProperty</a>
 

 

