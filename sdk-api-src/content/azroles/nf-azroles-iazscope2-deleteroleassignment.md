---
UID: NF:azroles.IAzScope2.DeleteRoleAssignment
title: IAzScope2::DeleteRoleAssignment (azroles.h)
description: Removes the specified IAzRoleAssignment object from this scope.
old-location: security\iazscope2_deleteroleassignment.htm
tech.root: SecAuthZ
ms.assetid: 8e28e09a-f9a4-4e6e-bb11-cfa1145f1ba1
ms.date: 12/05/2018
ms.keywords: DeleteRoleAssignment, DeleteRoleAssignment method [Security], DeleteRoleAssignment method [Security],IAzScope2 interface, IAzScope2 interface [Security],DeleteRoleAssignment method, IAzScope2.DeleteRoleAssignment, IAzScope2::DeleteRoleAssignment, azroles/IAzScope2::DeleteRoleAssignment, security.iazscope2_deleteroleassignment
f1_keywords:
- azroles/IAzScope2.DeleteRoleAssignment
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Azroles.dll
api_name:
- IAzScope2.DeleteRoleAssignment
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IAzScope2::DeleteRoleAssignment


## -description


The <b>DeleteRoleAssignment</b> method removes the specified <a href="https://docs.microsoft.com/windows/desktop/api/azroles/nn-azroles-iazroleassignment">IAzRoleAssignment</a> object from this scope.


## -parameters




### -param bstrRoleAssignmentName [in]

A string that contains the name of the <a href="https://docs.microsoft.com/windows/desktop/api/azroles/nn-azroles-iazroleassignment">IAzRoleAssignment</a> object to remove.


## -returns



 If the method succeeds, it returns <b>S_OK</b>.

If the method fails, it returns an error code. For a list of common error codes, see <a href="https://docs.microsoft.com/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.




## -remarks



If any references to an <a href="https://docs.microsoft.com/windows/desktop/api/azroles/nn-azroles-iazroleassignment">IAzRoleAssignment</a> object have been deleted from the cache, the <b>IAzRoleAssignment</b> object can no longer be used. In C++, you must release references to deleted <b>IAzRoleAssignment</b> objects by calling the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nf-unknwn-iunknown-release">IUnknown::Release</a> method. In Visual Basic, references to deleted objects are automatically released.



