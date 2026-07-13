---
UID: NF:certenroll.IX509CertificateTemplateWritable.get_Property
title: IX509CertificateTemplateWritable::get_Property (certenroll.h)
description: Specifies or retrieves a property value for the IX509CertificateTemplateWritable object. (Get)
helpviewer_keywords: ["IX509CertificateTemplateWritable interface [Security]","Property property","IX509CertificateTemplateWritable.Property","IX509CertificateTemplateWritable.get_Property","IX509CertificateTemplateWritable::Property","IX509CertificateTemplateWritable::get_Property","IX509CertificateTemplateWritable::put_Property","Property property [Security]","Property property [Security]","IX509CertificateTemplateWritable interface","certenroll/IX509CertificateTemplateWritable::Property","certenroll/IX509CertificateTemplateWritable::get_Property","certenroll/IX509CertificateTemplateWritable::put_Property","get_Property","security.ix509certificatetemplatewritable_property"]
old-location: security\ix509certificatetemplatewritable_property.htm
tech.root: security
ms.assetid: df665957-c276-4e46-8838-76010146e4d7
ms.date: 12/05/2018
ms.keywords: IX509CertificateTemplateWritable interface [Security],Property property, IX509CertificateTemplateWritable.Property, IX509CertificateTemplateWritable.get_Property, IX509CertificateTemplateWritable::Property, IX509CertificateTemplateWritable::get_Property, IX509CertificateTemplateWritable::put_Property, Property property [Security], Property property [Security],IX509CertificateTemplateWritable interface, certenroll/IX509CertificateTemplateWritable::Property, certenroll/IX509CertificateTemplateWritable::get_Property, certenroll/IX509CertificateTemplateWritable::put_Property, get_Property, security.ix509certificatetemplatewritable_property
req.header: certenroll.h
req.include-header: 
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IX509CertificateTemplateWritable::get_Property
 - certenroll/IX509CertificateTemplateWritable::get_Property
dev_langs:
 - c++
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
---

# IX509CertificateTemplateWritable::get_Property


## -description

The <b>Property</b> property specifies or retrieves a property value for the <a href="/windows/desktop/api/certenroll/nn-certenroll-ix509certificatetemplatewritable">IX509CertificateTemplateWritable</a> object.

This property is read/write.

## -parameters

## -remarks

Currently, TemplatePropSecurityDescriptor is the only property that you can set. The property value must be a <b>VARIANT</b> of type <b>VT_BSTR</b> or <b>VT_BYREF|VT_BSTR</b> and must be a valid SDDL string.

## -see-also

<a href="/windows/desktop/api/certenroll/nn-certenroll-ix509certificatetemplatewritable">IX509CertificateTemplateWritable</a>
