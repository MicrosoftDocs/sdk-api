---
UID: NF:certenroll.IX509ExtensionTemplate.get_TemplateOid
title: IX509ExtensionTemplate::get_TemplateOid (certenroll.h)
description: Retrieves the template object identifier (OID).
helpviewer_keywords: ["IX509ExtensionTemplate interface [Security]","TemplateOid property","IX509ExtensionTemplate.TemplateOid","IX509ExtensionTemplate.get_TemplateOid","IX509ExtensionTemplate::TemplateOid","IX509ExtensionTemplate::get_TemplateOid","TemplateOid property [Security]","TemplateOid property [Security]","IX509ExtensionTemplate interface","certenroll/IX509ExtensionTemplate::TemplateOid","certenroll/IX509ExtensionTemplate::get_TemplateOid","get_TemplateOid","security.ix509extensiontemplate_templateoid_property"]
old-location: security\ix509extensiontemplate_templateoid_property.htm
tech.root: security
ms.assetid: 9106f995-4d74-464a-8ca3-aec056199ace
ms.date: 12/05/2018
ms.keywords: IX509ExtensionTemplate interface [Security],TemplateOid property, IX509ExtensionTemplate.TemplateOid, IX509ExtensionTemplate.get_TemplateOid, IX509ExtensionTemplate::TemplateOid, IX509ExtensionTemplate::get_TemplateOid, TemplateOid property [Security], TemplateOid property [Security],IX509ExtensionTemplate interface, certenroll/IX509ExtensionTemplate::TemplateOid, certenroll/IX509ExtensionTemplate::get_TemplateOid, get_TemplateOid, security.ix509extensiontemplate_templateoid_property
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
 - IX509ExtensionTemplate::get_TemplateOid
 - certenroll/IX509ExtensionTemplate::get_TemplateOid
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
 - IX509ExtensionTemplate.TemplateOid
 - IX509ExtensionTemplate.get_TemplateOid
---

# IX509ExtensionTemplate::get_TemplateOid


## -description

The <b>TemplateOid</b> property retrieves the template <a href="/windows/desktop/SecGloss/o-gly">object identifier</a> (OID).

This property is read-only.

## -parameters

## -remarks

You must call either <a href="/windows/desktop/api/certenroll/nf-certenroll-ix509extensiontemplate-initializeencode">InitializeEncode</a> or <a href="/windows/desktop/api/certenroll/nf-certenroll-ix509extensiontemplate-initializedecode">InitializeDecode</a> before you can use an  <a href="/windows/desktop/api/certenroll/nn-certenroll-ix509extensiontemplate">IX509ExtensionTemplate</a> object. You can retrieve the following additional properties for this extension:<ul>
<li>The <a href="/windows/desktop/api/certenroll/nf-certenroll-ix509extension-get_critical">Critical</a> property identifies whether the extension is critical. You can also specify this property.</li>
<li>The <a href="/windows/desktop/api/certenroll/nf-certenroll-ix509extension-get_objectid">ObjectId</a> property retrieves the OID.</li>
<li>The <a href="/windows/desktop/api/certenroll/nf-certenroll-ix509extensiontemplate-get_majorversion">MajorVersion</a> and <a href="/windows/desktop/api/certenroll/nf-certenroll-ix509extensiontemplate-get_minorversion">MinorVersion</a> properties retrieve the version information.</li>
</ul>

## -see-also

<a href="/windows/desktop/api/certenroll/nn-certenroll-ix509extensiontemplate">IX509ExtensionTemplate</a>