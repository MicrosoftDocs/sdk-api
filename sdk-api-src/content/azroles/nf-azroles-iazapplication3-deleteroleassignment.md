---
UID: NF:azroles.IAzApplication3.DeleteRoleAssignment
title: IAzApplication3::DeleteRoleAssignment (azroles.h)
description: Removes the specified IAzRoleAssignment object from the IAzApplication3 object.
helpviewer_keywords: ["DeleteRoleAssignment","DeleteRoleAssignment method [Security]","DeleteRoleAssignment method [Security]","IAzApplication3 interface","IAzApplication3 interface [Security]","DeleteRoleAssignment method","IAzApplication3.DeleteRoleAssignment","IAzApplication3::DeleteRoleAssignment","azroles/IAzApplication3::DeleteRoleAssignment","security.iazapplication3_deleteroleassignment"]
old-location: security\iazapplication3_deleteroleassignment.htm
tech.root: security
ms.assetid: 1844e7c5-91ad-4f6d-8f5b-1a174e9653dd
ms.date: 12/05/2018
ms.keywords: DeleteRoleAssignment, DeleteRoleAssignment method [Security], DeleteRoleAssignment method [Security],IAzApplication3 interface, IAzApplication3 interface [Security],DeleteRoleAssignment method, IAzApplication3.DeleteRoleAssignment, IAzApplication3::DeleteRoleAssignment, azroles/IAzApplication3::DeleteRoleAssignment, security.iazapplication3_deleteroleassignment
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
 - IAzApplication3::DeleteRoleAssignment
 - azroles/IAzApplication3::DeleteRoleAssignment
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
 - IAzApplication3.DeleteRoleAssignment
---

# IAzApplication3::DeleteRoleAssignment


## -description

The <b>DeleteRoleAssignment</b> method removes the specified <a href="/windows/desktop/api/azroles/nn-azroles-iazroleassignment">IAzRoleAssignment</a> object from the <a href="/windows/desktop/api/azroles/nn-azroles-iazapplication3">IAzApplication3</a> object.

## -parameters

### -param bstrRoleAssignmentName [in]

A string that contains the name of the <a href="/windows/desktop/api/azroles/nn-azroles-iazroleassignment">IAzRoleAssignment</a> object to remove.

## -returns

 If the method succeeds, it returns <b>S_OK</b>.

If the method fails, it returns an error code. For a list of common error codes, see <a href="/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.

## -remarks

If any references to an <a href="/windows/desktop/api/azroles/nn-azroles-iazroleassignment">IAzRoleAssignment</a> object have been deleted from the cache, you can no longer use that object. In C++, you must release references to deleted <b>IAzRoleAssignment</b> objects by calling the <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-release">IUnknown::Release</a> method. In Visual Basic, references to deleted objects are automatically released.