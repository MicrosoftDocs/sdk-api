---
UID: NF:azroles.IAzScope2.DeleteRoleDefinition
title: IAzScope2::DeleteRoleDefinition
author: windows-sdk-content
description: Removes the specified IAzRoleDefinition object from this scope.
old-location: security\iazscope2_deleteroledefinition.htm
old-project: secauthz
ms.assetid: 12eddceb-15e2-4c9a-8372-749b0eccdd79
ms.author: windowssdkdev
ms.date: 08/10/2018
ms.keywords: DeleteRoleDefinition, DeleteRoleDefinition method [Security], DeleteRoleDefinition method [Security],IAzScope2 interface, IAzScope2 interface [Security],DeleteRoleDefinition method, IAzScope2.DeleteRoleDefinition, IAzScope2::DeleteRoleDefinition, azroles/IAzScope2::DeleteRoleDefinition, security.iazscope2_deleteroledefinition
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: azroles.h
req.include-header: 
req.redist: 
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
 - IAzScope2.DeleteRoleDefinition
product: Windows
targetos: Windows
req.lib: 
req.dll: Azroles.dll
req.irql: 
---

# IAzScope2::DeleteRoleDefinition


## -description


The <b>DeleteRoleDefinition</b> method removes the specified <a href="https://msdn.microsoft.com/d951f5cc-85da-4898-a70f-9e50ab66ade5">IAzRoleDefinition</a> object from this scope.


## -parameters




### -param bstrRoleDefinitionName [in]

A string that contains the name of the <a href="https://msdn.microsoft.com/d951f5cc-85da-4898-a70f-9e50ab66ade5">IAzRoleDefinition</a> object to remove.


## -returns



 If the method succeeds, it returns <b>S_OK</b>.

If the method fails, it returns an error code. For a list of common error codes, see <a href="https://msdn.microsoft.com/ce52efc3-92c7-40e4-ac49-0c54049e169f">Common HRESULT Values</a>.




## -remarks



If any references to an <a href="https://msdn.microsoft.com/d951f5cc-85da-4898-a70f-9e50ab66ade5">IAzRoleDefinition</a> object have been deleted from the cache, that object can no longer be used. In C++, you must release references to deleted <b>IAzRoleDefinition</b> objects by calling the <a href="_com_iunknown_release">IUnknown::Release</a> method. In Visual Basic, references to deleted objects are automatically released.



