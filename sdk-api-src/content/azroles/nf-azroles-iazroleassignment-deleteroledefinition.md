---
UID: NF:azroles.IAzRoleAssignment.DeleteRoleDefinition
title: IAzRoleAssignment::DeleteRoleDefinition
author: windows-sdk-content
description: Removes the IAzRoleDefinition object with the specified name from this IAzRoleAssignment object.
old-location: security\iazroleassignment_deleteroledefinition.htm
old-project: SecAuthZ
ms.assetid: 17af80d0-d9b4-4e20-b7a8-72e8dc42b69d
ms.author: windowssdkdev
ms.date: 05/22/2018
ms.keywords: DeleteRoleDefinition, DeleteRoleDefinition method [Security], DeleteRoleDefinition method [Security],IAzRoleAssignment interface, IAzRoleAssignment interface [Security],DeleteRoleDefinition method, IAzRoleAssignment.DeleteRoleDefinition, IAzRoleAssignment::DeleteRoleDefinition, azroles/IAzRoleAssignment::DeleteRoleDefinition, security.iazroleassignment_deleteroledefinition
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
req.idl: 
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
 - Azroles.dll
api_name:
 - IAzRoleAssignment.DeleteRoleDefinition
product: Windows
targetos: Windows
req.lib: 
req.dll: Azroles.dll
req.irql: 
---

# IAzRoleAssignment::DeleteRoleDefinition


## -description


The <b>DeleteRoleDefinition</b> method removes the <a href="https://msdn.microsoft.com/d951f5cc-85da-4898-a70f-9e50ab66ade5">IAzRoleDefinition</a> object with the specified name from this <a href="https://msdn.microsoft.com/3f0b926f-77f4-4477-b155-5f866822baba">IAzRoleAssignment</a> object.


## -parameters




### -param bstrRoleDefinition [in]

The name of the <a href="https://msdn.microsoft.com/d951f5cc-85da-4898-a70f-9e50ab66ade5">IAzRoleDefinition</a> object to delete.


## -returns



 If the method succeeds, the method returns S_OK.

If the method fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="https://msdn.microsoft.com/ce52efc3-92c7-40e4-ac49-0c54049e169f">Common HRESULT Values</a>.




## -remarks



If there are any references to an <a href="https://msdn.microsoft.com/d951f5cc-85da-4898-a70f-9e50ab66ade5">IAzRoleDefinition</a> object that has been deleted from the cache, the <b>IAzRoleDefinition</b> object can no longer be used. In C++, you must release references to deleted <b>IAzRoleDefinition</b> objects by calling the <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-release.md">IUnknown::Release</a> method. In Visual Basic, references to deleted objects are automatically released.



