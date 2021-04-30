---
UID: NF:certenroll.IX509ExtensionTemplate.get_MinorVersion
title: IX509ExtensionTemplate::get_MinorVersion (certenroll.h)
description: Retrieves the minimum minor version number of the certificate template.
helpviewer_keywords: ["IX509ExtensionTemplate interface [Security]","MinorVersion property","IX509ExtensionTemplate.MinorVersion","IX509ExtensionTemplate.get_MinorVersion","IX509ExtensionTemplate::MinorVersion","IX509ExtensionTemplate::get_MinorVersion","MinorVersion property [Security]","MinorVersion property [Security]","IX509ExtensionTemplate interface","certenroll/IX509ExtensionTemplate::MinorVersion","certenroll/IX509ExtensionTemplate::get_MinorVersion","get_MinorVersion","security.ix509extensiontemplate_minorversion_property"]
old-location: security\ix509extensiontemplate_minorversion_property.htm
tech.root: security
ms.assetid: 0fb17099-4bf6-405c-8b54-4280a8023256
ms.date: 12/05/2018
ms.keywords: IX509ExtensionTemplate interface [Security],MinorVersion property, IX509ExtensionTemplate.MinorVersion, IX509ExtensionTemplate.get_MinorVersion, IX509ExtensionTemplate::MinorVersion, IX509ExtensionTemplate::get_MinorVersion, MinorVersion property [Security], MinorVersion property [Security],IX509ExtensionTemplate interface, certenroll/IX509ExtensionTemplate::MinorVersion, certenroll/IX509ExtensionTemplate::get_MinorVersion, get_MinorVersion, security.ix509extensiontemplate_minorversion_property
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
 - IX509ExtensionTemplate::get_MinorVersion
 - certenroll/IX509ExtensionTemplate::get_MinorVersion
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
 - IX509ExtensionTemplate.MinorVersion
 - IX509ExtensionTemplate.get_MinorVersion
---

# IX509ExtensionTemplate::get_MinorVersion


## -description

The <b>MinorVersion</b> property retrieves the minimum minor version number of the certificate template.

This property is read-only.

## -parameters

## -remarks

You must call either <a href="/windows/desktop/api/certenroll/nf-certenroll-ix509extensiontemplate-initializeencode">InitializeEncode</a> or <a href="/windows/desktop/api/certenroll/nf-certenroll-ix509extensiontemplate-initializedecode">InitializeDecode</a> before you can use an  <a href="/windows/desktop/api/certenroll/nn-certenroll-ix509extensiontemplate">IX509ExtensionTemplate</a> object. You can retrieve the following additional properties for this extension:<ul>
<li>The <a href="/windows/desktop/api/certenroll/nf-certenroll-ix509extension-get_critical">Critical</a> property identifies whether the extension is critical. You can also specify this property.</li>
<li>The <a href="/windows/desktop/api/certenroll/nf-certenroll-ix509extension-get_objectid">ObjectId</a> property retrieves the <a href="/windows/desktop/SecGloss/o-gly">object identifier</a> (OID).</li>
<li>The <a href="/windows/desktop/api/certenroll/nf-certenroll-ix509extensiontemplate-get_majorversion">MajorVersion</a> property retrieves version information.</li>
<li>The <a href="/windows/desktop/api/certenroll/nf-certenroll-ix509extensiontemplate-get_templateoid">TemplateOid</a> property retrieves the OID of the template.</li>
</ul>

## -see-also

<a href="/windows/desktop/api/certenroll/nn-certenroll-ix509extensiontemplate">IX509ExtensionTemplate</a>