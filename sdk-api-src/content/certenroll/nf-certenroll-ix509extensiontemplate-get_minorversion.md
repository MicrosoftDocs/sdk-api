---
UID: NF:certenroll.IX509ExtensionTemplate.get_MinorVersion
title: IX509ExtensionTemplate::get_MinorVersion (certenroll.h)
author: windows-sdk-content
description: Retrieves the minimum minor version number of the certificate template.
old-location: security\ix509extensiontemplate_minorversion_property.htm
tech.root: seccertenroll
ms.assetid: 0fb17099-4bf6-405c-8b54-4280a8023256
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IX509ExtensionTemplate interface [Security],MinorVersion property, IX509ExtensionTemplate.MinorVersion, IX509ExtensionTemplate.get_MinorVersion, IX509ExtensionTemplate::MinorVersion, IX509ExtensionTemplate::get_MinorVersion, MinorVersion property [Security], MinorVersion property [Security],IX509ExtensionTemplate interface, certenroll/IX509ExtensionTemplate::MinorVersion, certenroll/IX509ExtensionTemplate::get_MinorVersion, get_MinorVersion, security.ix509extensiontemplate_minorversion_property
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
 - IX509ExtensionTemplate.MinorVersion
 - IX509ExtensionTemplate.get_MinorVersion
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IX509ExtensionTemplate::get_MinorVersion


## -description


The <b>MinorVersion</b> property retrieves the minimum minor version number of the certificate template.

This property is read-only.


## -parameters


## -remarks



You must call either <a href="https://msdn.microsoft.com/93590649-78b4-4f78-81b8-5c21cf91608d">InitializeEncode</a> or <a href="https://msdn.microsoft.com/c35a6108-9f5e-4876-9ea1-ce8b568abfde">InitializeDecode</a> before you can use an  <a href="https://msdn.microsoft.com/2ac24ee9-f31f-4501-a4f0-321580ec2fa9">IX509ExtensionTemplate</a> object. You can retrieve the following additional properties for this extension:<ul>
<li>The <a href="https://msdn.microsoft.com/b03ec7fe-78e9-4a8a-81b8-eaa91aa8d072">Critical</a> property identifies whether the extension is critical. You can also specify this property.</li>
<li>The <a href="https://msdn.microsoft.com/d3508bfe-e323-4075-9c82-d9b53b8f54aa">ObjectId</a> property retrieves the <a href="https://msdn.microsoft.com/e6be8932-015e-4058-b249-1671b3fea521">object identifier</a> (OID).</li>
<li>The <a href="https://msdn.microsoft.com/35057dbc-4518-4f76-bf82-9d9a8abe5525">MajorVersion</a> property retrieves version information.</li>
<li>The <a href="https://msdn.microsoft.com/9106f995-4d74-464a-8ca3-aec056199ace">TemplateOid</a> property retrieves the OID of the template.</li>
</ul>





## -see-also




<a href="https://msdn.microsoft.com/2ac24ee9-f31f-4501-a4f0-321580ec2fa9">IX509ExtensionTemplate</a>
 

 

