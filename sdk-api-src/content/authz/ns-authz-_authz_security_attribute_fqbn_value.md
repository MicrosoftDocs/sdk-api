---
UID: NS:authz._AUTHZ_SECURITY_ATTRIBUTE_FQBN_VALUE
title: "_AUTHZ_SECURITY_ATTRIBUTE_FQBN_VALUE"
author: windows-sdk-content
description: Specifies a fully qualified binary name value associated with a security attribute.
old-location: security\authz_security_attribute_fqbn_value.htm
tech.root: secauthz
ms.assetid: 05b4bf7d-a0d9-473c-b215-9cf566b2a996
ms.author: windowssdkdev
ms.date: 08/31/2018
ms.keywords: "*PAUTHZ_SECURITY_ATTRIBUTE_FQBN_VALUE, AUTHZ_SECURITY_ATTRIBUTE_FQBN_VALUE, AUTHZ_SECURITY_ATTRIBUTE_FQBN_VALUE structure [Security], PAUTHZ_SECURITY_ATTRIBUTE_FQBN_VALUE, PAUTHZ_SECURITY_ATTRIBUTE_FQBN_VALUE structure pointer [Security], _AUTHZ_SECURITY_ATTRIBUTE_FQBN_VALUE, authz/AUTHZ_SECURITY_ATTRIBUTE_FQBN_VALUE, authz/PAUTHZ_SECURITY_ATTRIBUTE_FQBN_VALUE, security.authz_security_attribute_fqbn_value"
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Authz.h
api_name:
 - AUTHZ_SECURITY_ATTRIBUTE_FQBN_VALUE
product: Windows
targetos: Windows
req.typenames: AUTHZ_SECURITY_ATTRIBUTE_FQBN_VALUE, *PAUTHZ_SECURITY_ATTRIBUTE_FQBN_VALUE
req.redist: 
---

# _AUTHZ_SECURITY_ATTRIBUTE_FQBN_VALUE structure


## -description


The <b>AUTHZ_SECURITY_ATTRIBUTE_FQBN_VALUE</b> structure specifies a fully qualified binary name value associated with a security attribute.


## -struct-fields




### -field Version

The version number of the structure.


### -field pName

A pointer to strings that specify the names of the publisher, the product, and the original binary file of the value.


## -see-also




<a href="https://msdn.microsoft.com/0c4778bb-1b5d-4422-b066-d2a6aaa1f351">AUTHZ_SECURITY_ATTRIBUTE_V1</a>



<a href="https://msdn.microsoft.com/1db95ab0-951f-488c-b522-b3f38fc74c7c">AUTHZ_SECURITY_ATTRUBUTES_INFORMATION</a>



<a href="https://msdn.microsoft.com/d84873e2-ecfe-45cf-9048-7ed173117efa">AuthzModifySecurityAttributes</a>
 

 

