---
UID: NF:certenroll.IX509ExtensionTemplate.get_MajorVersion
title: IX509ExtensionTemplate::get_MajorVersion (certenroll.h)
description: Retrieves the minimum major version number of the certificate template.
helpviewer_keywords: ["IX509ExtensionTemplate interface [Security]","MajorVersion property","IX509ExtensionTemplate.MajorVersion","IX509ExtensionTemplate.get_MajorVersion","IX509ExtensionTemplate::MajorVersion","IX509ExtensionTemplate::get_MajorVersion","MajorVersion property [Security]","MajorVersion property [Security]","IX509ExtensionTemplate interface","certenroll/IX509ExtensionTemplate::MajorVersion","certenroll/IX509ExtensionTemplate::get_MajorVersion","get_MajorVersion","security.ix509extensiontemplate_majorversion_property"]
old-location: security\ix509extensiontemplate_majorversion_property.htm
tech.root: security
ms.assetid: 35057dbc-4518-4f76-bf82-9d9a8abe5525
ms.date: 12/05/2018
ms.keywords: IX509ExtensionTemplate interface [Security],MajorVersion property, IX509ExtensionTemplate.MajorVersion, IX509ExtensionTemplate.get_MajorVersion, IX509ExtensionTemplate::MajorVersion, IX509ExtensionTemplate::get_MajorVersion, MajorVersion property [Security], MajorVersion property [Security],IX509ExtensionTemplate interface, certenroll/IX509ExtensionTemplate::MajorVersion, certenroll/IX509ExtensionTemplate::get_MajorVersion, get_MajorVersion, security.ix509extensiontemplate_majorversion_property
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
 - IX509ExtensionTemplate::get_MajorVersion
 - certenroll/IX509ExtensionTemplate::get_MajorVersion
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
 - IX509ExtensionTemplate.MajorVersion
 - IX509ExtensionTemplate.get_MajorVersion
---

# IX509ExtensionTemplate::get_MajorVersion


## -description

The <b>MajorVersion</b> property retrieves the minimum major version number of the <a href="/windows/desktop/SecGloss/c-gly">certificate template</a>.

This property is read-only.

## -parameters

## -remarks

You must call either <a href="/windows/desktop/api/certenroll/nf-certenroll-ix509extensiontemplate-initializeencode">InitializeEncode</a> or <a href="/windows/desktop/api/certenroll/nf-certenroll-ix509extensiontemplate-initializedecode">InitializeDecode</a> before you can use an  <a href="/windows/desktop/api/certenroll/nn-certenroll-ix509extensiontemplate">IX509ExtensionTemplate</a> object. You can retrieve the following additional properties for this extension:<ul>
<li>The <a href="/windows/desktop/api/certenroll/nf-certenroll-ix509extension-get_critical">Critical</a> property identifies whether the extension is critical. You can also specify this property.</li>
<li>The <a href="/windows/desktop/api/certenroll/nf-certenroll-ix509extension-get_objectid">ObjectId</a> property retrieves the <a href="/windows/desktop/SecGloss/o-gly">object identifier</a> (OID).</li>
<li>The <a href="/windows/desktop/api/certenroll/nf-certenroll-ix509extensiontemplate-get_minorversion">MinorVersion</a> property retrieves version information.</li>
<li>The <a href="/windows/desktop/api/certenroll/nf-certenroll-ix509extensiontemplate-get_templateoid">TemplateOid</a> property retrieves the OID of the template.</li>
</ul>

## -see-also

<a href="/windows/desktop/api/certenroll/nn-certenroll-ix509extensiontemplate">IX509ExtensionTemplate</a>