---
UID: NF:azroles.IAzClientContext3.IsInRoleAssignment
title: IAzClientContext3::IsInRoleAssignment (azroles.h)
description: Checks whether the principal represented by the current client context is a member of the specified role in the specified scope.
helpviewer_keywords: ["IAzClientContext3 interface [Security]","IsInRoleAssignment method","IAzClientContext3.IsInRoleAssignment","IAzClientContext3::IsInRoleAssignment","IsInRoleAssignment","IsInRoleAssignment method [Security]","IsInRoleAssignment method [Security]","IAzClientContext3 interface","azroles/IAzClientContext3::IsInRoleAssignment","security.iazclientcontext3_isinroleassignment_method"]
old-location: security\iazclientcontext3_isinroleassignment_method.htm
tech.root: security
ms.assetid: 20e19ee7-3b65-4f0f-ba19-7fb6cbbaea7b
ms.date: 12/05/2018
ms.keywords: IAzClientContext3 interface [Security],IsInRoleAssignment method, IAzClientContext3.IsInRoleAssignment, IAzClientContext3::IsInRoleAssignment, IsInRoleAssignment, IsInRoleAssignment method [Security], IsInRoleAssignment method [Security],IAzClientContext3 interface, azroles/IAzClientContext3::IsInRoleAssignment, security.iazclientcontext3_isinroleassignment_method
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
 - IAzClientContext3::IsInRoleAssignment
 - azroles/IAzClientContext3::IsInRoleAssignment
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
 - IAzClientContext3.IsInRoleAssignment
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

If the method fails, it returns an error code. For a list of common error codes, see <a href="/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.