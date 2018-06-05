---
UID: NS:authz._AUTHZ_SECURITY_ATTRIBUTES_INFORMATION
title: "_AUTHZ_SECURITY_ATTRIBUTES_INFORMATION"
author: windows-sdk-content
description: Specifies one or more security attributes and values.
old-location: security\authz_security_attributes_information.htm
old-project: SecAuthZ
ms.assetid: 1db95ab0-951f-488c-b522-b3f38fc74c7c
ms.author: windowssdkdev
ms.date: 05/22/2018
ms.keywords: "*PAUTHZ_SECURITY_ATTRIBUTES_INFORMATION, AUTHZ_SECURITY_ATTRIBUTES_INFORMATION, AUTHZ_SECURITY_ATTRIBUTES_INFORMATION structure [Security], PAUTHZ_SECURITY_ATTRIBUTES_INFORMATION, PAUTHZ_SECURITY_ATTRIBUTES_INFORMATION structure pointer [Security], _AUTHZ_SECURITY_ATTRIBUTES_INFORMATION, authz/AUTHZ_SECURITY_ATTRIBUTES_INFORMATION, authz/PAUTHZ_SECURITY_ATTRIBUTES_INFORMATION, security.authz_security_attributes_information"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: authz.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
req.typenames: AUTHZ_SECURITY_ATTRIBUTES_INFORMATION, *PAUTHZ_SECURITY_ATTRIBUTES_INFORMATION
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Authz.h
api_name:
-	AUTHZ_SECURITY_ATTRIBUTES_INFORMATION
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
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
 

 

