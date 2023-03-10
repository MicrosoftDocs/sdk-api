---
UID: NF:certenroll.IX509CertificateTemplateWritable.get_Template
title: IX509CertificateTemplateWritable::get_Template (certenroll.h)
description: Retrieves a copy of the IX509CertificateTemplate object that was used to initialize this IX509CertificateTemplateWritable instance.
helpviewer_keywords: ["IX509CertificateTemplateWritable interface [Security]","Template property","IX509CertificateTemplateWritable.Template","IX509CertificateTemplateWritable.get_Template","IX509CertificateTemplateWritable::Template","IX509CertificateTemplateWritable::get_Template","Template property [Security]","Template property [Security]","IX509CertificateTemplateWritable interface","certenroll/IX509CertificateTemplateWritable::Template","certenroll/IX509CertificateTemplateWritable::get_Template","get_Template","security.ix509certificatetemplatewritable_template"]
old-location: security\ix509certificatetemplatewritable_template.htm
tech.root: security
ms.assetid: 35eef4e5-fcd9-4017-9d15-d8d418e063e7
ms.date: 12/05/2018
ms.keywords: IX509CertificateTemplateWritable interface [Security],Template property, IX509CertificateTemplateWritable.Template, IX509CertificateTemplateWritable.get_Template, IX509CertificateTemplateWritable::Template, IX509CertificateTemplateWritable::get_Template, Template property [Security], Template property [Security],IX509CertificateTemplateWritable interface, certenroll/IX509CertificateTemplateWritable::Template, certenroll/IX509CertificateTemplateWritable::get_Template, get_Template, security.ix509certificatetemplatewritable_template
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
 - IX509CertificateTemplateWritable::get_Template
 - certenroll/IX509CertificateTemplateWritable::get_Template
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
 - IX509CertificateTemplateWritable.Template
 - IX509CertificateTemplateWritable.get_Template
---

# IX509CertificateTemplateWritable::get_Template


## -description

The <b>Template</b> property retrieves a copy of the <a href="/windows/desktop/api/certenroll/nn-certenroll-ix509certificatetemplate">IX509CertificateTemplate</a> object that was used to initialize this <a href="/windows/desktop/api/certenroll/nn-certenroll-ix509certificatetemplatewritable">IX509CertificateTemplateWritable</a> instance.

This property is read-only.

## -parameters

## -remarks

You must call the COM <b>Release</b> method to free the interface pointer when you are finished using it.

## -see-also

<a href="/windows/desktop/api/certenroll/nn-certenroll-ix509certificatetemplatewritable">IX509CertificateTemplateWritable</a>