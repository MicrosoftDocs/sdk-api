---
UID: NS:authz._AUTHZ_SECURITY_ATTRIBUTES_INFORMATION
title: AUTHZ_SECURITY_ATTRIBUTES_INFORMATION (authz.h)
description: Specifies one or more security attributes and values.
helpviewer_keywords: ["*PAUTHZ_SECURITY_ATTRIBUTES_INFORMATION","AUTHZ_SECURITY_ATTRIBUTES_INFORMATION","AUTHZ_SECURITY_ATTRIBUTES_INFORMATION structure [Security]","PAUTHZ_SECURITY_ATTRIBUTES_INFORMATION","PAUTHZ_SECURITY_ATTRIBUTES_INFORMATION structure pointer [Security]","authz/AUTHZ_SECURITY_ATTRIBUTES_INFORMATION","authz/PAUTHZ_SECURITY_ATTRIBUTES_INFORMATION","security.authz_security_attributes_information"]
old-location: security\authz_security_attributes_information.htm
tech.root: security
ms.assetid: 1db95ab0-951f-488c-b522-b3f38fc74c7c
ms.date: 12/05/2018
ms.keywords: '*PAUTHZ_SECURITY_ATTRIBUTES_INFORMATION, AUTHZ_SECURITY_ATTRIBUTES_INFORMATION, AUTHZ_SECURITY_ATTRIBUTES_INFORMATION structure [Security], PAUTHZ_SECURITY_ATTRIBUTES_INFORMATION, PAUTHZ_SECURITY_ATTRIBUTES_INFORMATION structure pointer [Security], authz/AUTHZ_SECURITY_ATTRIBUTES_INFORMATION, authz/PAUTHZ_SECURITY_ATTRIBUTES_INFORMATION, security.authz_security_attributes_information'
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
targetos: Windows
req.typenames: AUTHZ_SECURITY_ATTRIBUTES_INFORMATION, *PAUTHZ_SECURITY_ATTRIBUTES_INFORMATION
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _AUTHZ_SECURITY_ATTRIBUTES_INFORMATION
 - authz/_AUTHZ_SECURITY_ATTRIBUTES_INFORMATION
 - PAUTHZ_SECURITY_ATTRIBUTES_INFORMATION
 - authz/PAUTHZ_SECURITY_ATTRIBUTES_INFORMATION
 - AUTHZ_SECURITY_ATTRIBUTES_INFORMATION
 - authz/AUTHZ_SECURITY_ATTRIBUTES_INFORMATION
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
 - AUTHZ_SECURITY_ATTRIBUTES_INFORMATION
---

# AUTHZ_SECURITY_ATTRIBUTES_INFORMATION structure


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

An array of <a href="/windows/desktop/api/authz/ns-authz-authz_security_attribute_v1">AUTHZ_SECURITY_ATTRIBUTE_V1</a> structures of the length of the <b>AttributeCount</b> member.

## -see-also

<a href="/windows/desktop/api/authz/nf-authz-authzmodifysecurityattributes">AuthzModifySecurityAttributes</a>