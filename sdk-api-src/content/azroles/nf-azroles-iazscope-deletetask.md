---
UID: NF:azroles.IAzScope.DeleteTask
title: IAzScope::DeleteTask (azroles.h)
description: Removes the IAzTask object with the specified name from the IAzScope object.
helpviewer_keywords: ["AzScope object [Security]","DeleteTask method","DeleteTask","DeleteTask method [Security]","DeleteTask method [Security]","AzScope object","DeleteTask method [Security]","IAzScope interface","IAzScope interface [Security]","DeleteTask method","IAzScope.DeleteTask","IAzScope::DeleteTask","azroles/IAzScope::DeleteTask","security.iazscope_deletetask"]
old-location: security\iazscope_deletetask.htm
tech.root: security
ms.assetid: de72b944-2796-4445-9fdd-4d56526dc903
ms.date: 03/20/2023
ms.keywords: AzScope object [Security],DeleteTask method, DeleteTask, DeleteTask method [Security], DeleteTask method [Security],AzScope object, DeleteTask method [Security],IAzScope interface, IAzScope interface [Security],DeleteTask method, IAzScope.DeleteTask, IAzScope::DeleteTask, azroles/IAzScope::DeleteTask, security.iazscope_deletetask
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
 - IAzScope::DeleteTask
 - azroles/IAzScope::DeleteTask
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
 - IAzScope.DeleteTask
 - AzScope.DeleteTask
---

# IAzScope::DeleteTask

## -description

The **DeleteTask** method removes the [IAzTask](nn-azroles-iaztask.md) object with the specified name from the [IAzScope](nn-azroles-iazscope.md) object.

## -parameters

### -param bstrTaskName [in]

Name of the [IAzTask](nn-azroles-iaztask.md) object to delete.

### -param varReserved [in, optional]

Reserved for future use.

## -returns

If the method succeeds, it will return `S_OK`. Any other **HRESULT** value indicates that the operation failed.

## -remarks

If there are any [IAzTask](nn-azroles-iaztask.md) references to an **IAzTask** object that has been deleted from the cache, the **IAzTask** object can no longer be used. In C++, you must release references to deleted **IAzTask** objects by calling the [IUnknown::Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) method. In C# and Visual Basic, references to deleted objects are automatically released.

## -see-also

[IAzTask](nn-azroles-iaztask.md)

[IAzScope](nn-azroles-iazscope.md)
