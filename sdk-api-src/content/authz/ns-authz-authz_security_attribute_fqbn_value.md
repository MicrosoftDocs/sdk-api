---
UID: NS:authz._AUTHZ_SECURITY_ATTRIBUTE_FQBN_VALUE
title: AUTHZ_SECURITY_ATTRIBUTE_FQBN_VALUE (authz.h)
description: Specifies a fully qualified binary name value associated with a security attribute.
helpviewer_keywords: ["*PAUTHZ_SECURITY_ATTRIBUTE_FQBN_VALUE","AUTHZ_SECURITY_ATTRIBUTE_FQBN_VALUE","AUTHZ_SECURITY_ATTRIBUTE_FQBN_VALUE structure [Security]","PAUTHZ_SECURITY_ATTRIBUTE_FQBN_VALUE","PAUTHZ_SECURITY_ATTRIBUTE_FQBN_VALUE structure pointer [Security]","authz/AUTHZ_SECURITY_ATTRIBUTE_FQBN_VALUE","authz/PAUTHZ_SECURITY_ATTRIBUTE_FQBN_VALUE","security.authz_security_attribute_fqbn_value"]
old-location: security\authz_security_attribute_fqbn_value.htm
tech.root: security
ms.assetid: 05b4bf7d-a0d9-473c-b215-9cf566b2a996
ms.date: 12/05/2018
ms.keywords: '*PAUTHZ_SECURITY_ATTRIBUTE_FQBN_VALUE, AUTHZ_SECURITY_ATTRIBUTE_FQBN_VALUE, AUTHZ_SECURITY_ATTRIBUTE_FQBN_VALUE structure [Security], PAUTHZ_SECURITY_ATTRIBUTE_FQBN_VALUE, PAUTHZ_SECURITY_ATTRIBUTE_FQBN_VALUE structure pointer [Security], authz/AUTHZ_SECURITY_ATTRIBUTE_FQBN_VALUE, authz/PAUTHZ_SECURITY_ATTRIBUTE_FQBN_VALUE, security.authz_security_attribute_fqbn_value'
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
req.typenames: AUTHZ_SECURITY_ATTRIBUTE_FQBN_VALUE, *PAUTHZ_SECURITY_ATTRIBUTE_FQBN_VALUE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _AUTHZ_SECURITY_ATTRIBUTE_FQBN_VALUE
 - authz/_AUTHZ_SECURITY_ATTRIBUTE_FQBN_VALUE
 - PAUTHZ_SECURITY_ATTRIBUTE_FQBN_VALUE
 - authz/PAUTHZ_SECURITY_ATTRIBUTE_FQBN_VALUE
 - AUTHZ_SECURITY_ATTRIBUTE_FQBN_VALUE
 - authz/AUTHZ_SECURITY_ATTRIBUTE_FQBN_VALUE
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
 - AUTHZ_SECURITY_ATTRIBUTE_FQBN_VALUE
---

# AUTHZ_SECURITY_ATTRIBUTE_FQBN_VALUE structure


## -description

The <b>AUTHZ_SECURITY_ATTRIBUTE_FQBN_VALUE</b> structure specifies a fully qualified binary name value associated with a security attribute.

## -struct-fields

### -field Version

The version number of the structure.

### -field pName

A pointer to strings that specify the names of the publisher, the product, and the original binary file of the value.

## -see-also

<a href="/windows/desktop/api/authz/ns-authz-authz_security_attribute_v1">AUTHZ_SECURITY_ATTRIBUTE_V1</a>



<a href="/windows/desktop/api/authz/ns-authz-authz_security_attributes_information">AUTHZ_SECURITY_ATTRUBUTES_INFORMATION</a>



<a href="/windows/desktop/api/authz/nf-authz-authzmodifysecurityattributes">AuthzModifySecurityAttributes</a>