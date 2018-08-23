---
UID: NF:certenroll.IX509ExtensionTemplateName.get_TemplateName
title: IX509ExtensionTemplateName::get_TemplateName
author: windows-sdk-content
description: Retrieves the name of the template.
old-location: security\ix509extensiontemplatename_templatename_property.htm
old-project: seccertenroll
ms.assetid: b403a27f-e477-4445-adcb-5fce58453727
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: IX509ExtensionTemplateName interface [Security],TemplateName property, IX509ExtensionTemplateName.TemplateName, IX509ExtensionTemplateName.get_TemplateName, IX509ExtensionTemplateName::TemplateName, IX509ExtensionTemplateName::get_TemplateName, TemplateName property [Security], TemplateName property [Security],IX509ExtensionTemplateName interface, certenroll/IX509ExtensionTemplateName::TemplateName, certenroll/IX509ExtensionTemplateName::get_TemplateName, get_TemplateName, security.ix509extensiontemplatename_templatename_property
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: certenroll.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: X509RequestType
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
product: Windows
targetos: Windows
req.lib: 
req.dll: CertEnroll.dll
req.irql: 
---

# IX509ExtensionTemplateName::get_TemplateName


## -description


The <b>TemplateName</b> property retrieves the name of the template.

This property is read-only.


## -parameters


## -remarks



You must call either <a href="https://msdn.microsoft.com/8b72b73a-bfd5-4a56-a106-01f2fd59e922">InitializeEncode</a> or <a href="https://msdn.microsoft.com/05fb275c-75b2-4619-8d6a-c6c9868d9765">InitializeDecode</a> before you can use an  <a href="https://msdn.microsoft.com/9a2d0219-6fe3-4a75-8d28-281c0b863a35">IX509ExtensionTemplateName</a> object. You can retrieve the following additional properties for this extension:<ul>
<li>The <a href="https://msdn.microsoft.com/b03ec7fe-78e9-4a8a-81b8-eaa91aa8d072">Critical</a> property identifies whether the extension is critical. You can also specify this property.</li>
<li>The <a href="https://msdn.microsoft.com/d3508bfe-e323-4075-9c82-d9b53b8f54aa">ObjectId</a> property retrieves the <a href="https://msdn.microsoft.com/e6be8932-015e-4058-b249-1671b3fea521">object identifier</a> (OID).</li>
</ul>





## -see-also




<a href="https://msdn.microsoft.com/9a2d0219-6fe3-4a75-8d28-281c0b863a35">IX509ExtensionTemplateName</a>
 

 

