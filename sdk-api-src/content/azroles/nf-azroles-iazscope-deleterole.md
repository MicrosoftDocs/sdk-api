---
UID: NF:azroles.IAzScope.DeleteRole
title: IAzScope::DeleteRole (azroles.h)
description: Removes the IAzRole object with the specified name from the IAzScope object.
helpviewer_keywords: ["AzScope object [Security]","DeleteRole method","DeleteRole","DeleteRole method [Security]","DeleteRole method [Security]","AzScope object","DeleteRole method [Security]","IAzScope interface","IAzScope interface [Security]","DeleteRole method","IAzScope.DeleteRole","IAzScope::DeleteRole","azroles/IAzScope::DeleteRole","security.iazscope_deleterole"]
old-location: security\iazscope_deleterole.htm
tech.root: security
ms.assetid: 9155c4f8-ad17-402e-80a1-3dcee044d2c4
ms.date: 03/20/2023
ms.keywords: AzScope object [Security],DeleteRole method, DeleteRole, DeleteRole method [Security], DeleteRole method [Security],AzScope object, DeleteRole method [Security],IAzScope interface, IAzScope interface [Security],DeleteRole method, IAzScope.DeleteRole, IAzScope::DeleteRole, azroles/IAzScope::DeleteRole, security.iazscope_deleterole
req.header: azroles.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Azroles.lib
req.dll: Azroles.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: Windows Server 2003 Administration Tools Pack on Windows XP
ms.custom: 19H1
f1_keywords:
 - IAzScope::DeleteRole
 - azroles/IAzScope::DeleteRole
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
 - IAzScope.DeleteRole
 - AzScope.DeleteRole
---

# IAzScope::DeleteRole

## -description

The **DeleteRole** method removes the [IAzRole](nn-azroles-iazrole.md) object with the specified name from the [IAzScope](nn-azroles-iazscope.md) object.

## -parameters

### -param bstrRoleName [in]

Name of the [IAzRole](nn-azroles-iazrole.md) object to delete.

### -param varReserved [in, optional]

Reserved for future use.

## -returns

If the method succeeds, it will return `S_OK`. Any other **HRESULT** value indicates that the operation failed.

## -remarks

If there are any [IAzRole](nn-azroles-iazrole.md) references to an **IAzRole** object that has been deleted from the cache, the **IAzRole** object can no longer be used. In C++, you must release references to deleted **IAzRole** objects by calling the [IUnknown::Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) method. In C# and Visual Basic, references to deleted objects are automatically released.

## -see-also

[IAzRole](nn-azroles-iazrole.md)
