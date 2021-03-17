---
UID: NF:azroles.IAzOperation2.RoleAssignments
title: IAzOperation2::RoleAssignments (azroles.h)
description: Returns a collection of the role assignments associated with this operation.
helpviewer_keywords: ["IAzOperation2 interface [Security]","RoleAssignments method","IAzOperation2.RoleAssignments","IAzOperation2::RoleAssignments","RoleAssignments","RoleAssignments method [Security]","RoleAssignments method [Security]","IAzOperation2 interface","azroles/IAzOperation2::RoleAssignments","security.iazoperation2_roleassignments_method"]
old-location: security\iazoperation2_roleassignments_method.htm
tech.root: security
ms.assetid: 99f1d60a-69c2-4736-a328-19796f4d37f0
ms.date: 12/05/2018
ms.keywords: IAzOperation2 interface [Security],RoleAssignments method, IAzOperation2.RoleAssignments, IAzOperation2::RoleAssignments, RoleAssignments, RoleAssignments method [Security], RoleAssignments method [Security],IAzOperation2 interface, azroles/IAzOperation2::RoleAssignments, security.iazoperation2_roleassignments_method
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
 - IAzOperation2::RoleAssignments
 - azroles/IAzOperation2::RoleAssignments
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
 - IAzOperation2.RoleAssignments
---

# IAzOperation2::RoleAssignments


## -description

The <b>RoleAssignments</b> method returns a collection of the role assignments associated with this operation.

## -parameters

### -param bstrScopeName [in]

The name of the scope in which to check for role assignments. If the value of this parameter is an empty string, the method checks for role assignments at the application level.

### -param bRecursive [in]

<b>TRUE</b> if the method checks all scopes within the application; otherwise, <b>FALSE</b>. This parameter is ignored if the value of the <i>bstrScopeName</i> parameter is not <b>NULL</b>.

### -param ppRoleAssignments [out]

The address of a pointer to an <a href="/windows/desktop/api/azroles/nn-azroles-iazroleassignments">IAzRoleAssignments</a> interface that represents the collection of <a href="/windows/desktop/api/azroles/nn-azroles-iazroleassignment">IAzRoleAssignment</a> objects associated with this operation.

## -returns

 If the method succeeds, it returns <b>S_OK</b>.

If the method fails, it returns an error code. For a list of common error codes, see <a href="/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.