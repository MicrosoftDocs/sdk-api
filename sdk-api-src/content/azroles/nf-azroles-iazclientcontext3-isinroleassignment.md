---
UID: NF:azroles.IAzClientContext3.IsInRoleAssignment
title: IAzClientContext3::IsInRoleAssignment
author: windows-sdk-content
description: Checks whether the principal represented by the current client context is a member of the specified role in the specified scope.
old-location: security\iazclientcontext3_isinroleassignment_method.htm
old-project: secauthz
ms.assetid: 20e19ee7-3b65-4f0f-ba19-7fb6cbbaea7b
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: IAzClientContext3 interface [Security],IsInRoleAssignment method, IAzClientContext3.IsInRoleAssignment, IAzClientContext3::IsInRoleAssignment, IsInRoleAssignment, IsInRoleAssignment method [Security], IsInRoleAssignment method [Security],IAzClientContext3 interface, azroles/IAzClientContext3::IsInRoleAssignment, security.iazclientcontext3_isinroleassignment_method
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: AZ_PROP_CONSTANTS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Azroles.h
api_name:
 - IAzClientContext3.IsInRoleAssignment
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# IAzClientContext3::IsInRoleAssignment


## -description


The <b>IsInRoleAssignment</b> method checks whether the principal represented by the current client context is a member of the specified role in the specified scope.


## -parameters




### -param bstrScopeName [in]

The name of the scope to check.


### -param bstrRoleName [in]

The name of the role to check.


### -param pbIsInRole [out]

<b>VARIANT_TRUE</b> if the principal represented by the current client context is a member of the role specified by the <i>bstrRoleName</i> parameter in the scope specified by the <i>bstrScopeName</i> parameter; otherwise, <b>VARIANT_FALSE</b>.


## -returns



 If the method succeeds, it returns <b>S_OK</b>.

If the method fails, it returns an error code. For a list of common error codes, see <a href="https://msdn.microsoft.com/ce52efc3-92c7-40e4-ac49-0c54049e169f">Common HRESULT Values</a>.



