---
UID: NS:authz._AUTHZ_REGISTRATION_OBJECT_TYPE_NAME_OFFSET
title: "_AUTHZ_REGISTRATION_OBJECT_TYPE_NAME_OFFSET"
author: windows-sdk-content
description: Specifies the offset of a registration object type name.
old-location: security\authz_registration_object_type_name_offset.htm
old-project: secauthz
ms.assetid: 2ec39edc-7819-41a5-8798-dc51c00ba85e
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: "*PAUTHZ_REGISTRATION_OBJECT_TYPE_NAME_OFFSET, AUTHZ_REGISTRATION_OBJECT_TYPE_NAME_OFFSET, AUTHZ_REGISTRATION_OBJECT_TYPE_NAME_OFFSET structure [Security], PAUTHZ_REGISTRATION_OBJECT_TYPE_NAME_OFFSET, PAUTHZ_REGISTRATION_OBJECT_TYPE_NAME_OFFSET structure pointer [Security], _AUTHZ_REGISTRATION_OBJECT_TYPE_NAME_OFFSET, authz/AUTHZ_REGISTRATION_OBJECT_TYPE_NAME_OFFSET, authz/PAUTHZ_REGISTRATION_OBJECT_TYPE_NAME_OFFSET, security.authz_registration_object_type_name_offset"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: authz.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
req.typenames: AUTHZ_REGISTRATION_OBJECT_TYPE_NAME_OFFSET, *PAUTHZ_REGISTRATION_OBJECT_TYPE_NAME_OFFSET
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Authz.h
api_name:
 - AUTHZ_REGISTRATION_OBJECT_TYPE_NAME_OFFSET
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# _AUTHZ_REGISTRATION_OBJECT_TYPE_NAME_OFFSET structure


## -description


The <b>AUTHZ_REGISTRATION_OBJECT_TYPE_NAME_OFFSET</b> structure specifies the offset of a registration object type name.


## -struct-fields




### -field szObjectTypeName

A pointer to a wide character string that represents the name of the object type.


### -field dwOffset

Offset of the object type name in an object types message DLL.


## -see-also




<a href="https://msdn.microsoft.com/8b4d6e14-fb9c-428a-bd94-34eba668edc6">AUTHZ_SOURCE_SCHEMA_REGISTRATION</a>
 

 

