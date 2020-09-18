---
UID: NS:authz._AUTHZ_REGISTRATION_OBJECT_TYPE_NAME_OFFSET
title: AUTHZ_REGISTRATION_OBJECT_TYPE_NAME_OFFSET (authz.h)
description: Specifies the offset of a registration object type name.
helpviewer_keywords: ["*PAUTHZ_REGISTRATION_OBJECT_TYPE_NAME_OFFSET","AUTHZ_REGISTRATION_OBJECT_TYPE_NAME_OFFSET","AUTHZ_REGISTRATION_OBJECT_TYPE_NAME_OFFSET structure [Security]","PAUTHZ_REGISTRATION_OBJECT_TYPE_NAME_OFFSET","PAUTHZ_REGISTRATION_OBJECT_TYPE_NAME_OFFSET structure pointer [Security]","authz/AUTHZ_REGISTRATION_OBJECT_TYPE_NAME_OFFSET","authz/PAUTHZ_REGISTRATION_OBJECT_TYPE_NAME_OFFSET","security.authz_registration_object_type_name_offset"]
old-location: security\authz_registration_object_type_name_offset.htm
tech.root: security
ms.assetid: 2ec39edc-7819-41a5-8798-dc51c00ba85e
ms.date: 12/05/2018
ms.keywords: '*PAUTHZ_REGISTRATION_OBJECT_TYPE_NAME_OFFSET, AUTHZ_REGISTRATION_OBJECT_TYPE_NAME_OFFSET, AUTHZ_REGISTRATION_OBJECT_TYPE_NAME_OFFSET structure [Security], PAUTHZ_REGISTRATION_OBJECT_TYPE_NAME_OFFSET, PAUTHZ_REGISTRATION_OBJECT_TYPE_NAME_OFFSET structure pointer [Security], authz/AUTHZ_REGISTRATION_OBJECT_TYPE_NAME_OFFSET, authz/PAUTHZ_REGISTRATION_OBJECT_TYPE_NAME_OFFSET, security.authz_registration_object_type_name_offset'
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: AUTHZ_REGISTRATION_OBJECT_TYPE_NAME_OFFSET, *PAUTHZ_REGISTRATION_OBJECT_TYPE_NAME_OFFSET
req.redist: Windows Server 2003 Administration Tools Pack on Windows XP
ms.custom: 19H1
f1_keywords:
 - _AUTHZ_REGISTRATION_OBJECT_TYPE_NAME_OFFSET
 - authz/_AUTHZ_REGISTRATION_OBJECT_TYPE_NAME_OFFSET
 - PAUTHZ_REGISTRATION_OBJECT_TYPE_NAME_OFFSET
 - authz/PAUTHZ_REGISTRATION_OBJECT_TYPE_NAME_OFFSET
 - AUTHZ_REGISTRATION_OBJECT_TYPE_NAME_OFFSET
 - authz/AUTHZ_REGISTRATION_OBJECT_TYPE_NAME_OFFSET
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Authz.h
api_name:
 - AUTHZ_REGISTRATION_OBJECT_TYPE_NAME_OFFSET
---

# AUTHZ_REGISTRATION_OBJECT_TYPE_NAME_OFFSET structure


## -description

The <b>AUTHZ_REGISTRATION_OBJECT_TYPE_NAME_OFFSET</b> structure specifies the offset of a registration object type name.

## -struct-fields

### -field szObjectTypeName

A pointer to a wide character string that represents the name of the object type.

### -field dwOffset

Offset of the object type name in an object types message DLL.

## -see-also

<a href="/windows/desktop/api/authz/ns-authz-authz_source_schema_registration">AUTHZ_SOURCE_SCHEMA_REGISTRATION</a>