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

# AUTHZ_SECURITY_ATTRIBUTE_OPERATION enumeration


## -description


The <b>AUTHZ_SECURITY_ATTRIBUTE_OPERATION</b> enumeration indicates the type of modification to be made to security attributes by a call to the <a href="https://msdn.microsoft.com/d84873e2-ecfe-45cf-9048-7ed173117efa">AuthzModifySecurityAttributes</a> function.


## -enum-fields




### -field AUTHZ_SECURITY_ATTRIBUTE_OPERATION_NONE

Do not perform any modification.


### -field AUTHZ_SECURITY_ATTRIBUTE_OPERATION_REPLACE_ALL

Delete all existing security attributes and their values in the token and replace them with the specified attributes and values.

If no new attributes are specified, all existing attributes and values are deleted.

This operation must be the only operation specified and can be specified only once in a single call to <a href="https://msdn.microsoft.com/d84873e2-ecfe-45cf-9048-7ed173117efa">AuthzModifySecurityAttributes</a>. If the operation is not specified as the first in the list of operations, the call to <b>AuthzModifySecurityAttributes</b> fails. If the operation is specified as the first in the array of operations performed, the rest of the operations are ignored.


### -field AUTHZ_SECURITY_ATTRIBUTE_OPERATION_ADD

Add a new attribute or a new value to an existing attribute.

If the value specified for any attribute already exists for that attribute, the call to <a href="https://msdn.microsoft.com/d84873e2-ecfe-45cf-9048-7ed173117efa">AuthzModifySecurityAttributes</a> fails.


### -field AUTHZ_SECURITY_ATTRIBUTE_OPERATION_DELETE

Delete the specified values of the specified attributes. If an attribute is specified without a value, that attribute is deleted.

If this operation results in an attribute that does not contain any values, that attribute is deleted.

If a value is specified that does not match an existing attribute, no modifications are performed and the call to <a href="https://msdn.microsoft.com/d84873e2-ecfe-45cf-9048-7ed173117efa">AuthzModifySecurityAttributes</a> fails.


### -field AUTHZ_SECURITY_ATTRIBUTE_OPERATION_REPLACE

The existing values of the specified security attributes are replaced by the specified new values.

If any of the specified attributes does not already exist, they are added.

When no value is specified for an attribute, that attribute is deleted. Otherwise, the operation is simply ignored and no failure is reported.


## -see-also




<a href="https://msdn.microsoft.com/d84873e2-ecfe-45cf-9048-7ed173117efa">AuthzModifySecurityAttributes</a>
 

 

