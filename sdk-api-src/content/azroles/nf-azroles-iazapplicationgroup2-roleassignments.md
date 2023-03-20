---
UID: NF:azroles.IAzApplicationGroup2.RoleAssignments
title: IAzApplicationGroup2::RoleAssignments (azroles.h)
description: Gets a collection of IAzRoleAssignment objects associated with this application group.
helpviewer_keywords: ["IAzApplicationGroup2 interface [Security]","RoleAssignments property","IAzApplicationGroup2.RoleAssignments","IAzApplicationGroup2::RoleAssignments","IAzApplicationGroup2::get_RoleAssignments","RoleAssignments","RoleAssignments property [Security]","RoleAssignments property [Security]","IAzApplicationGroup2 interface","azroles/IAzApplicationGroup2::RoleAssignments","azroles/IAzApplicationGroup2::get_RoleAssignments","security.iazapplicationgroup2_roleassignments_method"]
old-location: security\iazapplicationgroup2_roleassignments_method.htm
tech.root: security
ms.assetid: 4996fb10-7b46-48e4-8028-a24ae4072bec
ms.date: 03/20/2023
ms.keywords: IAzApplicationGroup2 interface [Security],RoleAssignments property, IAzApplicationGroup2.RoleAssignments, IAzApplicationGroup2::RoleAssignments, IAzApplicationGroup2::get_RoleAssignments, RoleAssignments, RoleAssignments property [Security], RoleAssignments property [Security],IAzApplicationGroup2 interface, azroles/IAzApplicationGroup2::RoleAssignments, azroles/IAzApplicationGroup2::get_RoleAssignments, security.iazapplicationgroup2_roleassignments_method
req.header: azroles.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Azroles.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IAzApplicationGroup2::RoleAssignments
 - azroles/IAzApplicationGroup2::RoleAssignments
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Azroles.h
api_name:
 - IAzApplicationGroup2.RoleAssignments
 - IAzApplicationGroup2.get_RoleAssignments
---

# IAzApplicationGroup2::RoleAssignments

## -description

The **RoleAssignments** method gets a collection of [IAzRoleAssignment](nn-azroles-iazroleassignment.md) objects associated with this application group.

This property is read-only.

## -parameters

### -param bstrScopeName

Provides a scope name to include in the search for **IAzRoleAssignment** objects. If this parameter is **NULL**, the search is performed in the global scope.

### -param bRecursive

Indicates if the search for **IAzRoleAssignment** objects should be performed recursively.

### -param ppRoleAssignments

The list of [IAzRoleAssignment](nn-azroles-iazroleassignment.md) objects associated with the specified application group.

## -returns

If the method succeeds, it will return `S_OK`. Any other **HRESULT** value indicates that the operation failed.

## -see-also

[IAzRoleAssignment](nn-azroles-iazroleassignment.md)
