---
UID: NF:azroles.IAzScope2.DeleteRoleDefinition
title: IAzScope2::DeleteRoleDefinition
author: windows-sdk-content
description: Removes the specified IAzRoleDefinition object from this scope.
old-location: security\iazscope2_deleteroledefinition.htm
tech.root: secauthz
ms.assetid: 12eddceb-15e2-4c9a-8372-749b0eccdd79
ms.author: windowssdkdev
ms.date: 11/13/2018
ms.keywords: DeleteRoleDefinition, DeleteRoleDefinition method [Security], DeleteRoleDefinition method [Security],IAzScope2 interface, IAzScope2 interface [Security],DeleteRoleDefinition method, IAzScope2.DeleteRoleDefinition, IAzScope2::DeleteRoleDefinition, azroles/IAzScope2::DeleteRoleDefinition, security.iazscope2_deleteroledefinition
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
 - IAzScope2.DeleteRoleDefinition
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
- IAzScope2.DeleteRoleDefinition
: 
---

# IAzScope2::DeleteRoleDefinition


## -description


The <b>DeleteRoleDefinition</b> method removes the specified <a href="https://msdn.microsoft.com/en-us/library/Aa377927(v=VS.85).aspx">IAzRoleDefinition</a> object from this scope.


## -parameters




### -param bstrRoleDefinitionName [in]

A string that contains the name of the <a href="https://msdn.microsoft.com/en-us/library/Aa377927(v=VS.85).aspx">IAzRoleDefinition</a> object to remove.


## -returns



 If the method succeeds, it returns <b>S_OK</b>.

If the method fails, it returns an error code. For a list of common error codes, see <a href="https://msdn.microsoft.com/en-us/library/Aa378137(v=VS.85).aspx">Common HRESULT Values</a>.




## -remarks



If any references to an <a href="https://msdn.microsoft.com/en-us/library/Aa377927(v=VS.85).aspx">IAzRoleDefinition</a> object have been deleted from the cache, that object can no longer be used. In C++, you must release references to deleted <b>IAzRoleDefinition</b> objects by calling the <a href="https://msdn.microsoft.com/en-us/library/ms682317(v=VS.85).aspx">IUnknown::Release</a> method. In Visual Basic, references to deleted objects are automatically released.



