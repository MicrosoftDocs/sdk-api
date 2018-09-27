---
UID: NF:azroles.IAzOperation2.RoleAssignments
title: IAzOperation2::RoleAssignments
author: windows-sdk-content
description: Returns a collection of the role assignments associated with this operation.
old-location: security\iazoperation2_roleassignments_method.htm
tech.root: secauthz
ms.assetid: 99f1d60a-69c2-4736-a328-19796f4d37f0
ms.author: windowssdkdev
ms.date: 08/31/2018
ms.keywords: IAzOperation2 interface [Security],RoleAssignments method, IAzOperation2.RoleAssignments, IAzOperation2::RoleAssignments, RoleAssignments, RoleAssignments method [Security], RoleAssignments method [Security],IAzOperation2 interface, azroles/IAzOperation2::RoleAssignments, security.iazoperation2_roleassignments_method
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Azroles.h
api_name:
 - IAzOperation2.RoleAssignments
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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

The address of a pointer to an <a href="https://msdn.microsoft.com/d38fd7e0-6d0b-4b68-b6e5-f7adc2cfef47">IAzRoleAssignments</a> interface that represents the collection of <a href="https://msdn.microsoft.com/3f0b926f-77f4-4477-b155-5f866822baba">IAzRoleAssignment</a> objects associated with this operation.


## -returns



 If the method succeeds, it returns <b>S_OK</b>.

If the method fails, it returns an error code. For a list of common error codes, see <a href="https://msdn.microsoft.com/ce52efc3-92c7-40e4-ac49-0c54049e169f">Common HRESULT Values</a>.



