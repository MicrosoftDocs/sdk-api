---
UID: NF:certenroll.IX509CertificateTemplateWritable.get_Property
title: IX509CertificateTemplateWritable::get_Property
author: windows-sdk-content
description: Specifies or retrieves a property value for the IX509CertificateTemplateWritable object.
old-location: security\ix509certificatetemplatewritable_property.htm
old-project: SecCertEnroll
ms.assetid: df665957-c276-4e46-8838-76010146e4d7
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: IX509CertificateTemplateWritable interface [Security],Property property, IX509CertificateTemplateWritable.Property, IX509CertificateTemplateWritable.get_Property, IX509CertificateTemplateWritable::Property, IX509CertificateTemplateWritable::get_Property, IX509CertificateTemplateWritable::put_Property, Property property [Security], Property property [Security],IX509CertificateTemplateWritable interface, certenroll/IX509CertificateTemplateWritable::Property, certenroll/IX509CertificateTemplateWritable::get_Property, certenroll/IX509CertificateTemplateWritable::put_Property, get_Property, security.ix509certificatetemplatewritable_property
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: certenroll.h
req.include-header: 
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Certenroll.idl
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
 - Certenroll.h
api_name:
 - IX509CertificateTemplateWritable.Property
 - IX509CertificateTemplateWritable.get_Property
 - IX509CertificateTemplateWritable.put_Property
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IX509CertificateTemplateWritable::get_Property


## -description


The <b>Property</b> property specifies or retrieves a property value for the <a href="https://msdn.microsoft.com/87660b16-06a8-4a71-8669-24521f1399e4">IX509CertificateTemplateWritable</a> object.

This property is read/write.


## -parameters


## -remarks



Currently, TemplatePropSecurityDescriptor is the only property that you can set. The property value must be a <b>VARIANT</b> of type <b>VT_BSTR</b> or <b>VT_BYREF|VT_BSTR</b> and must be a valid SDDL string.




## -see-also




<a href="https://msdn.microsoft.com/87660b16-06a8-4a71-8669-24521f1399e4">IX509CertificateTemplateWritable</a>
 

 

