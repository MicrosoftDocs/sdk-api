---
UID: NF:certenroll.IX509ExtensionTemplate.get_TemplateOid
title: IX509ExtensionTemplate::get_TemplateOid
author: windows-sdk-content
description: Retrieves the template object identifier (OID).
old-location: security\ix509extensiontemplate_templateoid_property.htm
tech.root: seccertenroll
ms.assetid: 9106f995-4d74-464a-8ca3-aec056199ace
ms.author: windowssdkdev
ms.date: 08/31/2018
ms.keywords: IX509ExtensionTemplate interface [Security],TemplateOid property, IX509ExtensionTemplate.TemplateOid, IX509ExtensionTemplate.get_TemplateOid, IX509ExtensionTemplate::TemplateOid, IX509ExtensionTemplate::get_TemplateOid, TemplateOid property [Security], TemplateOid property [Security],IX509ExtensionTemplate interface, certenroll/IX509ExtensionTemplate::TemplateOid, certenroll/IX509ExtensionTemplate::get_TemplateOid, get_TemplateOid, security.ix509extensiontemplate_templateoid_property
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
 - IX509ExtensionTemplate.TemplateOid
 - IX509ExtensionTemplate.get_TemplateOid
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IX509ExtensionTemplate::get_TemplateOid


## -description


The <b>TemplateOid</b> property retrieves the template <a href="https://msdn.microsoft.com/en-us/library/ms721599(v=VS.85).aspx">object identifier</a> (OID).

This property is read-only.


## -parameters


## -remarks



You must call either <a href="https://msdn.microsoft.com/en-us/library/Aa378310(v=VS.85).aspx">InitializeEncode</a> or <a href="https://msdn.microsoft.com/en-us/library/Aa378307(v=VS.85).aspx">InitializeDecode</a> before you can use an  <a href="https://msdn.microsoft.com/en-us/library/Aa378274(v=VS.85).aspx">IX509ExtensionTemplate</a> object. You can retrieve the following additional properties for this extension:<ul>
<li>The <a href="https://msdn.microsoft.com/en-us/library/Aa378409(v=VS.85).aspx">Critical</a> property identifies whether the extension is critical. You can also specify this property.</li>
<li>The <a href="https://msdn.microsoft.com/en-us/library/Aa378518(v=VS.85).aspx">ObjectId</a> property retrieves the OID.</li>
<li>The <a href="https://msdn.microsoft.com/en-us/library/Aa378314(v=VS.85).aspx">MajorVersion</a> and <a href="https://msdn.microsoft.com/en-us/library/Aa378343(v=VS.85).aspx">MinorVersion</a> properties retrieve the version information.</li>
</ul>





## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Aa378274(v=VS.85).aspx">IX509ExtensionTemplate</a>
 

 

