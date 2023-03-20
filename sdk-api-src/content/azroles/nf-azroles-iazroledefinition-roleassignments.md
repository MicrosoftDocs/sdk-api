---
UID: NF:azroles.IAzRoleDefinition.RoleAssignments
title: IAzRoleDefinition::RoleAssignments (azroles.h)
description: Retrieves a collection of IAzRoleAssignment objects that represent the role assignments associated with this IAzRoleDefinition object.
helpviewer_keywords: ["IAzRoleDefinition interface [Security]","RoleAssignments property","IAzRoleDefinition.RoleAssignments","IAzRoleDefinition::RoleAssignments","IAzRoleDefinition::get_RoleAssignments","RoleAssignments","RoleAssignments property [Security]","RoleAssignments property [Security]","IAzRoleDefinition interface","azroles/IAzRoleDefinition::RoleAssignments","azroles/IAzRoleDefinition::get_RoleAssignments","security.iazroledefinition_roleassignments"]
old-location: security\iazroledefinition_roleassignments.htm
tech.root: security
ms.assetid: 1b8c3aaf-ed33-4253-b15f-06e5d3415d58
ms.date: 03/20/2023
ms.keywords: IAzRoleDefinition interface [Security],RoleAssignments property, IAzRoleDefinition.RoleAssignments, IAzRoleDefinition::RoleAssignments, IAzRoleDefinition::get_RoleAssignments, RoleAssignments, RoleAssignments property [Security], RoleAssignments property [Security],IAzRoleDefinition interface, azroles/IAzRoleDefinition::RoleAssignments, azroles/IAzRoleDefinition::get_RoleAssignments, security.iazroledefinition_roleassignments
req.header: azroles.h
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
req.dll: Azroles.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IAzRoleDefinition::RoleAssignments
 - azroles/IAzRoleDefinition::RoleAssignments
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Azroles.dll
api_name:
 - IAzRoleDefinition.RoleAssignments
 - IAzRoleDefinition.get_RoleAssignments
---

# IAzRoleDefinition::RoleAssignments

## -description

The **RoleAssignments** function retrieves a collection of [IAzRoleAssignment](nn-azroles-iazroleassignment.md) objects that represent the role assignments associated with this [IAzRoleDefinition](nn-azroles-iazroledefinition.md) object.

This property is read-only.

## -parameters

### -param bstrScopeName

Provides a scope name to include in the search for **IAzRoleAssignment** objects. If this parameter is **NULL**, the search is performed in the global scope.

### -param bRecursive

Indicates if the search for **IAzRoleAssignment** objects should be performed recursively.

### -param ppRoleAssignments

The collection of **IAzRoleAssignment** objects that represent the role assignments associated with this **IAzRoleDefinition** object.

## -returns

If the method succeeds, it will return `S_OK`. Any other **HRESULT** value indicates that the operation failed.

## -see-also

[IAzRoleAssignment](nn-azroles-iazroleassignment.md)

[IAzRoleDefinition](nn-azroles-iazroledefinition.md)
