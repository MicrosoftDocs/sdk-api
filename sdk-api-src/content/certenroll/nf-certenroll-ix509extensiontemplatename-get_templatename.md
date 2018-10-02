---
UID: NF:certenroll.IX509ExtensionTemplateName.get_TemplateName
title: IX509ExtensionTemplateName::get_TemplateName
author: windows-sdk-content
description: Retrieves the name of the template.
old-location: security\ix509extensiontemplatename_templatename_property.htm
tech.root: SecCertEnroll
ms.assetid: b403a27f-e477-4445-adcb-5fce58453727
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: IX509ExtensionTemplateName interface [Security],TemplateName property, IX509ExtensionTemplateName.TemplateName, IX509ExtensionTemplateName.get_TemplateName, IX509ExtensionTemplateName::TemplateName, IX509ExtensionTemplateName::get_TemplateName, TemplateName property [Security], TemplateName property [Security],IX509ExtensionTemplateName interface, certenroll/IX509ExtensionTemplateName::TemplateName, certenroll/IX509ExtensionTemplateName::get_TemplateName, get_TemplateName, security.ix509extensiontemplatename_templatename_property
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
 - IX509ExtensionTemplateName.TemplateName
 - IX509ExtensionTemplateName.get_TemplateName
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IX509ExtensionTemplateName::get_TemplateName


## -description


The <b>TemplateName</b> property retrieves the name of the template.

This property is read-only.


## -parameters


## -remarks



You must call either <a href="https://msdn.microsoft.com/en-us/library/Aa378285(v=VS.85).aspx">InitializeEncode</a> or <a href="https://msdn.microsoft.com/en-us/library/Aa378278(v=VS.85).aspx">InitializeDecode</a> before you can use an  <a href="https://msdn.microsoft.com/en-us/library/Aa378276(v=VS.85).aspx">IX509ExtensionTemplateName</a> object. You can retrieve the following additional properties for this extension:<ul>
<li>The <a href="https://msdn.microsoft.com/en-us/library/Aa378409(v=VS.85).aspx">Critical</a> property identifies whether the extension is critical. You can also specify this property.</li>
<li>The <a href="https://msdn.microsoft.com/en-us/library/Aa378518(v=VS.85).aspx">ObjectId</a> property retrieves the <a href="https://msdn.microsoft.com/en-us/library/ms721599(v=VS.85).aspx">object identifier</a> (OID).</li>
</ul>





## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Aa378276(v=VS.85).aspx">IX509ExtensionTemplateName</a>
 

 

