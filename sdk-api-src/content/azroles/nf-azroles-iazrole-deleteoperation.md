---
UID: NF:azroles.IAzRole.DeleteOperation
title: IAzRole::DeleteOperation (azroles.h)
description: Removes the IAzOperation object with the specified name from the role.
helpviewer_keywords: ["AzRole object [Security]","DeleteOperation method","DeleteOperation","DeleteOperation method [Security]","DeleteOperation method [Security]","AzRole object","DeleteOperation method [Security]","IAzRole interface","IAzRole interface [Security]","DeleteOperation method","IAzRole.DeleteOperation","IAzRole::DeleteOperation","azroles/IAzRole::DeleteOperation","security.iazrole_deleteoperation"]
old-location: security\iazrole_deleteoperation.htm
tech.root: security
ms.assetid: d3486a12-7059-47b8-9f06-a025d5756b70
ms.date: 03/20/2023
ms.keywords: AzRole object [Security],DeleteOperation method, DeleteOperation, DeleteOperation method [Security], DeleteOperation method [Security],AzRole object, DeleteOperation method [Security],IAzRole interface, IAzRole interface [Security],DeleteOperation method, IAzRole.DeleteOperation, IAzRole::DeleteOperation, azroles/IAzRole::DeleteOperation, security.iazrole_deleteoperation
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
 - IAzRole::DeleteOperation
 - azroles/IAzRole::DeleteOperation
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
 - IAzRole.DeleteOperation
 - AzRole.DeleteOperation
---

# IAzRole::DeleteOperation

## -description

The **DeleteOperation** method removes the [IAzOperation](nn-azroles-iazoperation.md) object with the specified name from the role.

## -parameters

### -param bstrProp [in]

Name of the [IAzOperation](nn-azroles-iazoperation.md) object to remove from the role.

### -param varReserved [in, optional]

Reserved for future use.

## -returns

If the method succeeds, it will return `S_OK`. Any other **HRESULT** value indicates that the operation failed.

## -remarks

If there are any [IAzOperation](nn-azroles-iazoperation.md) references to an **IAzOperation** object that has been deleted from the cache, the **IAzOperation** object can no longer be used. In C++, you must release references to deleted **IAzOperation** objects by calling the [IUnknown::Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) method. In C# and Visual Basic, references to deleted objects are automatically released.

## -see-also

[IAzOperation](nn-azroles-iazoperation.md)
