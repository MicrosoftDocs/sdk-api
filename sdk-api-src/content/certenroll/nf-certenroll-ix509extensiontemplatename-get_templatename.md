---
UID: NF:certenroll.IX509ExtensionTemplateName.get_TemplateName
title: IX509ExtensionTemplateName::get_TemplateName (certenroll.h)
description: Retrieves the name of the template.
helpviewer_keywords: ["IX509ExtensionTemplateName interface [Security]","TemplateName property","IX509ExtensionTemplateName.TemplateName","IX509ExtensionTemplateName.get_TemplateName","IX509ExtensionTemplateName::TemplateName","IX509ExtensionTemplateName::get_TemplateName","TemplateName property [Security]","TemplateName property [Security]","IX509ExtensionTemplateName interface","certenroll/IX509ExtensionTemplateName::TemplateName","certenroll/IX509ExtensionTemplateName::get_TemplateName","get_TemplateName","security.ix509extensiontemplatename_templatename_property"]
old-location: security\ix509extensiontemplatename_templatename_property.htm
tech.root: security
ms.assetid: b403a27f-e477-4445-adcb-5fce58453727
ms.date: 12/05/2018
ms.keywords: IX509ExtensionTemplateName interface [Security],TemplateName property, IX509ExtensionTemplateName.TemplateName, IX509ExtensionTemplateName.get_TemplateName, IX509ExtensionTemplateName::TemplateName, IX509ExtensionTemplateName::get_TemplateName, TemplateName property [Security], TemplateName property [Security],IX509ExtensionTemplateName interface, certenroll/IX509ExtensionTemplateName::TemplateName, certenroll/IX509ExtensionTemplateName::get_TemplateName, get_TemplateName, security.ix509extensiontemplatename_templatename_property
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
 - IX509ExtensionTemplateName::get_TemplateName
 - certenroll/IX509ExtensionTemplateName::get_TemplateName
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
 - IX509ExtensionTemplateName.TemplateName
 - IX509ExtensionTemplateName.get_TemplateName
---

# IX509ExtensionTemplateName::get_TemplateName


## -description

The <b>TemplateName</b> property retrieves the name of the template.

This property is read-only.

## -parameters

## -remarks

You must call either <a href="/windows/desktop/api/certenroll/nf-certenroll-ix509extensiontemplatename-initializeencode">InitializeEncode</a> or <a href="/windows/desktop/api/certenroll/nf-certenroll-ix509extensiontemplatename-initializedecode">InitializeDecode</a> before you can use an  <a href="/windows/desktop/api/certenroll/nn-certenroll-ix509extensiontemplatename">IX509ExtensionTemplateName</a> object. You can retrieve the following additional properties for this extension:<ul>
<li>The <a href="/windows/desktop/api/certenroll/nf-certenroll-ix509extension-get_critical">Critical</a> property identifies whether the extension is critical. You can also specify this property.</li>
<li>The <a href="/windows/desktop/api/certenroll/nf-certenroll-ix509extension-get_objectid">ObjectId</a> property retrieves the <a href="/windows/desktop/SecGloss/o-gly">object identifier</a> (OID).</li>
</ul>

## -see-also

<a href="/windows/desktop/api/certenroll/nn-certenroll-ix509extensiontemplatename">IX509ExtensionTemplateName</a>