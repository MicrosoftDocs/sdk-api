---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# _AUTHZ_SECURITY_ATTRIBUTES_INFORMATION structure


## -description


The <b>AUTHZ_SECURITY_ATTRIBUTES_INFORMATION</b> structure specifies one or more security attributes.


## -struct-fields




### -field Version

The  version of this structure. Currently the only value supported is 1.


### -field Reserved

Reserved. Do not use.


### -field AttributeCount

The number of attributes specified by the <b>Attribute</b> member.


### -field Attribute


### -field Attribute.pAttributeV1

An array of <a href="https://msdn.microsoft.com/0c4778bb-1b5d-4422-b066-d2a6aaa1f351">AUTHZ_SECURITY_ATTRIBUTE_V1</a> structures of the length of the <b>AttributeCount</b> member.


## -see-also




<a href="https://msdn.microsoft.com/d84873e2-ecfe-45cf-9048-7ed173117efa">AuthzModifySecurityAttributes</a>
 

 

