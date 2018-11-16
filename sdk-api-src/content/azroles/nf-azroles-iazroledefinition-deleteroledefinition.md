---
UID: NF:azroles.IAzRoleDefinition.DeleteRoleDefinition
title: IAzRoleDefinition::DeleteRoleDefinition
author: windows-sdk-content
description: Removes the IAzRoleDefinition object with the specified name from this IAzRoleDefinition object.
old-location: security\iazroledefinition_deleteroledefinition.htm
tech.root: SecAuthZ
ms.assetid: aba2f195-ebd8-40a2-8af4-455144822588
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: DeleteRoleDefinition, DeleteRoleDefinition method [Security], DeleteRoleDefinition method [Security],IAzRoleDefinition interface, IAzRoleDefinition interface [Security],DeleteRoleDefinition method, IAzRoleDefinition.DeleteRoleDefinition, IAzRoleDefinition::DeleteRoleDefinition, azroles/IAzRoleDefinition::DeleteRoleDefinition, security.iazroledefinition_deleteroledefinition
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
 - IAzRoleDefinition.DeleteRoleDefinition
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- azroles.h
: 
- IAzRoleDefinition.DeleteRoleDefinition
: 
---

# IAzRoleDefinition::DeleteRoleDefinition


## -description


The <b>DeleteRoleDefinition</b> method removes the <a href="https://msdn.microsoft.com/d951f5cc-85da-4898-a70f-9e50ab66ade5">IAzRoleDefinition</a> object with the specified name from this <b>IAzRoleDefinition</b> object.


## -parameters




### -param bstrRoleDefinition [in]

The name of the <a href="https://msdn.microsoft.com/d951f5cc-85da-4898-a70f-9e50ab66ade5">IAzRoleDefinition</a> object to delete.


## -returns



 If the method succeeds, the method returns S_OK.

If the method fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="https://msdn.microsoft.com/ce52efc3-92c7-40e4-ac49-0c54049e169f">Common HRESULT Values</a>.




## -remarks



If there are any references to an <a href="https://msdn.microsoft.com/d951f5cc-85da-4898-a70f-9e50ab66ade5">IAzRoleDefinition</a> object that has been deleted from the cache, the <b>IAzRoleDefinition</b> object can no longer be used. In C++, you must release references to deleted <b>IAzRoleDefinition</b> objects by calling the <a href="_com_iunknown_release">IUnknown::Release</a> method. In Visual Basic, references to deleted objects are automatically released.



