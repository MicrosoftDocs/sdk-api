---
UID: NE:authz.__unnamed_enum_0
title: AUTHZ_SECURITY_ATTRIBUTE_OPERATION (authz.h)
description: Indicates the type of modification to be made to security attributes by a call to the AuthzModifySecurityAttributes function.
helpviewer_keywords: ["*PAUTHZ_SECURITY_ATTRIBUTE_OPERATION","AUTHZ_SECURITY_ATTRIBUTE_OPERATION","AUTHZ_SECURITY_ATTRIBUTE_OPERATION enumeration [Security]","AUTHZ_SECURITY_ATTRIBUTE_OPERATION_ADD","AUTHZ_SECURITY_ATTRIBUTE_OPERATION_DELETE","AUTHZ_SECURITY_ATTRIBUTE_OPERATION_NONE","AUTHZ_SECURITY_ATTRIBUTE_OPERATION_REPLACE","AUTHZ_SECURITY_ATTRIBUTE_OPERATION_REPLACE_ALL","PAUTHZ_SECURITY_ATTRIBUTE_OPERATION","PAUTHZ_SECURITY_ATTRIBUTE_OPERATION enumeration pointer [Security]","authz/AUTHZ_SECURITY_ATTRIBUTE_OPERATION","authz/AUTHZ_SECURITY_ATTRIBUTE_OPERATION_ADD","authz/AUTHZ_SECURITY_ATTRIBUTE_OPERATION_DELETE","authz/AUTHZ_SECURITY_ATTRIBUTE_OPERATION_NONE","authz/AUTHZ_SECURITY_ATTRIBUTE_OPERATION_REPLACE","authz/AUTHZ_SECURITY_ATTRIBUTE_OPERATION_REPLACE_ALL","authz/PAUTHZ_SECURITY_ATTRIBUTE_OPERATION","security.authz_security_attribute_operation"]
old-location: security\authz_security_attribute_operation.htm
tech.root: security
ms.assetid: c1716cdb-87f9-47d6-bfc3-ae6cc043e917
ms.date: 12/05/2018
ms.keywords: '*PAUTHZ_SECURITY_ATTRIBUTE_OPERATION, AUTHZ_SECURITY_ATTRIBUTE_OPERATION, AUTHZ_SECURITY_ATTRIBUTE_OPERATION enumeration [Security], AUTHZ_SECURITY_ATTRIBUTE_OPERATION_ADD, AUTHZ_SECURITY_ATTRIBUTE_OPERATION_DELETE, AUTHZ_SECURITY_ATTRIBUTE_OPERATION_NONE, AUTHZ_SECURITY_ATTRIBUTE_OPERATION_REPLACE, AUTHZ_SECURITY_ATTRIBUTE_OPERATION_REPLACE_ALL, PAUTHZ_SECURITY_ATTRIBUTE_OPERATION, PAUTHZ_SECURITY_ATTRIBUTE_OPERATION enumeration pointer [Security], authz/AUTHZ_SECURITY_ATTRIBUTE_OPERATION, authz/AUTHZ_SECURITY_ATTRIBUTE_OPERATION_ADD, authz/AUTHZ_SECURITY_ATTRIBUTE_OPERATION_DELETE, authz/AUTHZ_SECURITY_ATTRIBUTE_OPERATION_NONE, authz/AUTHZ_SECURITY_ATTRIBUTE_OPERATION_REPLACE, authz/AUTHZ_SECURITY_ATTRIBUTE_OPERATION_REPLACE_ALL, authz/PAUTHZ_SECURITY_ATTRIBUTE_OPERATION, security.authz_security_attribute_operation'
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
req.typenames: AUTHZ_SECURITY_ATTRIBUTE_OPERATION, *PAUTHZ_SECURITY_ATTRIBUTE_OPERATION
req.redist: 
ms.custom: 19H1
f1_keywords:
 - PAUTHZ_SECURITY_ATTRIBUTE_OPERATION
 - authz/PAUTHZ_SECURITY_ATTRIBUTE_OPERATION
 - AUTHZ_SECURITY_ATTRIBUTE_OPERATION
 - authz/AUTHZ_SECURITY_ATTRIBUTE_OPERATION
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
 - AUTHZ_SECURITY_ATTRIBUTE_OPERATION
---

# AUTHZ_SECURITY_ATTRIBUTE_OPERATION enumeration


## -description

The <b>AUTHZ_SECURITY_ATTRIBUTE_OPERATION</b> enumeration indicates the type of modification to be made to security attributes by a call to the <a href="/windows/desktop/api/authz/nf-authz-authzmodifysecurityattributes">AuthzModifySecurityAttributes</a> function.

## -enum-fields

### -field AUTHZ_SECURITY_ATTRIBUTE_OPERATION_NONE:0

Do not perform any modification.

### -field AUTHZ_SECURITY_ATTRIBUTE_OPERATION_REPLACE_ALL

Delete all existing security attributes and their values in the token and replace them with the specified attributes and values.

If no new attributes are specified, all existing attributes and values are deleted.

This operation must be the only operation specified and can be specified only once in a single call to <a href="/windows/desktop/api/authz/nf-authz-authzmodifysecurityattributes">AuthzModifySecurityAttributes</a>. If the operation is not specified as the first in the list of operations, the call to <b>AuthzModifySecurityAttributes</b> fails. If the operation is specified as the first in the array of operations performed, the rest of the operations are ignored.

### -field AUTHZ_SECURITY_ATTRIBUTE_OPERATION_ADD

Add a new attribute or a new value to an existing attribute.

If the value specified for any attribute already exists for that attribute, the call to <a href="/windows/desktop/api/authz/nf-authz-authzmodifysecurityattributes">AuthzModifySecurityAttributes</a> fails.

### -field AUTHZ_SECURITY_ATTRIBUTE_OPERATION_DELETE

Delete the specified values of the specified attributes. If an attribute is specified without a value, that attribute is deleted.

If this operation results in an attribute that does not contain any values, that attribute is deleted.

If a value is specified that does not match an existing attribute, no modifications are performed and the call to <a href="/windows/desktop/api/authz/nf-authz-authzmodifysecurityattributes">AuthzModifySecurityAttributes</a> fails.

### -field AUTHZ_SECURITY_ATTRIBUTE_OPERATION_REPLACE

The existing values of the specified security attributes are replaced by the specified new values.

If any of the specified attributes does not already exist, they are added.

When no value is specified for an attribute, that attribute is deleted. Otherwise, the operation is simply ignored and no failure is reported.

## -see-also

<a href="/windows/desktop/api/authz/nf-authz-authzmodifysecurityattributes">AuthzModifySecurityAttributes</a>
