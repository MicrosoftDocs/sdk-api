---
UID: NF:azroles.IAzScope2.DeleteRoleAssignment
title: IAzScope2::DeleteRoleAssignment
author: windows-sdk-content
description: Removes the specified IAzRoleAssignment object from this scope.
old-location: security\iazscope2_deleteroleassignment.htm
tech.root: SecAuthZ
ms.assetid: 8e28e09a-f9a4-4e6e-bb11-cfa1145f1ba1
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: DeleteRoleAssignment, DeleteRoleAssignment method [Security], DeleteRoleAssignment method [Security],IAzScope2 interface, IAzScope2 interface [Security],DeleteRoleAssignment method, IAzScope2.DeleteRoleAssignment, IAzScope2::DeleteRoleAssignment, azroles/IAzScope2::DeleteRoleAssignment, security.iazscope2_deleteroleassignment
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IAzScope2::DeleteRoleAssignment


## -description


The <b>DeleteRoleAssignment</b> method removes the specified <a href="https://msdn.microsoft.com/3f0b926f-77f4-4477-b155-5f866822baba">IAzRoleAssignment</a> object from this scope.


## -parameters




### -param bstrRoleAssignmentName [in]

A string that contains the name of the <a href="https://msdn.microsoft.com/3f0b926f-77f4-4477-b155-5f866822baba">IAzRoleAssignment</a> object to remove.


## -returns



 If the method succeeds, it returns <b>S_OK</b>.

If the method fails, it returns an error code. For a list of common error codes, see <a href="https://msdn.microsoft.com/ce52efc3-92c7-40e4-ac49-0c54049e169f">Common HRESULT Values</a>.




## -remarks



If any references to an <a href="https://msdn.microsoft.com/3f0b926f-77f4-4477-b155-5f866822baba">IAzRoleAssignment</a> object have been deleted from the cache, the <b>IAzRoleAssignment</b> object can no longer be used. In C++, you must release references to deleted <b>IAzRoleAssignment</b> objects by calling the <a href="https://msdn.microsoft.com/en-us/library/ms682317(v=VS.85).aspx">IUnknown::Release</a> method. In Visual Basic, references to deleted objects are automatically released.



