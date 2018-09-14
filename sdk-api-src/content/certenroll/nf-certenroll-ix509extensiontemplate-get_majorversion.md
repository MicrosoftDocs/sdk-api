---
UID: NF:certenroll.IX509ExtensionTemplate.get_MajorVersion
title: IX509ExtensionTemplate::get_MajorVersion
author: windows-sdk-content
description: Retrieves the minimum major version number of the certificate template.
old-location: security\ix509extensiontemplate_majorversion_property.htm
tech.root: seccertenroll
ms.assetid: 35057dbc-4518-4f76-bf82-9d9a8abe5525
ms.author: windowssdkdev
ms.date: 08/31/2018
ms.keywords: IX509ExtensionTemplate interface [Security],MajorVersion property, IX509ExtensionTemplate.MajorVersion, IX509ExtensionTemplate.get_MajorVersion, IX509ExtensionTemplate::MajorVersion, IX509ExtensionTemplate::get_MajorVersion, MajorVersion property [Security], MajorVersion property [Security],IX509ExtensionTemplate interface, certenroll/IX509ExtensionTemplate::MajorVersion, certenroll/IX509ExtensionTemplate::get_MajorVersion, get_MajorVersion, security.ix509extensiontemplate_majorversion_property
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
 - IX509ExtensionTemplate.MajorVersion
 - IX509ExtensionTemplate.get_MajorVersion
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IX509ExtensionTemplate::get_MajorVersion


## -description


The <b>MajorVersion</b> property retrieves the minimum major version number of the <a href="https://msdn.microsoft.com/en-us/library/ms721572(v=VS.85).aspx">certificate template</a>.

This property is read-only.


## -parameters


## -remarks



You must call either <a href="https://msdn.microsoft.com/en-us/library/Aa378310(v=VS.85).aspx">InitializeEncode</a> or <a href="https://msdn.microsoft.com/en-us/library/Aa378307(v=VS.85).aspx">InitializeDecode</a> before you can use an  <a href="https://msdn.microsoft.com/en-us/library/Aa378274(v=VS.85).aspx">IX509ExtensionTemplate</a> object. You can retrieve the following additional properties for this extension:<ul>
<li>The <a href="https://msdn.microsoft.com/en-us/library/Aa378409(v=VS.85).aspx">Critical</a> property identifies whether the extension is critical. You can also specify this property.</li>
<li>The <a href="https://msdn.microsoft.com/en-us/library/Aa378518(v=VS.85).aspx">ObjectId</a> property retrieves the <a href="https://msdn.microsoft.com/en-us/library/ms721599(v=VS.85).aspx">object identifier</a> (OID).</li>
<li>The <a href="https://msdn.microsoft.com/en-us/library/Aa378343(v=VS.85).aspx">MinorVersion</a> property retrieves version information.</li>
<li>The <a href="https://msdn.microsoft.com/en-us/library/Aa378403(v=VS.85).aspx">TemplateOid</a> property retrieves the OID of the template.</li>
</ul>





## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Aa378274(v=VS.85).aspx">IX509ExtensionTemplate</a>
 

 

