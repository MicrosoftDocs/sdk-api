---
UID: NF:azroles.IAzApplication.DeleteTask
title: IAzApplication::DeleteTask (azroles.h)
description: Removes the IAzTask object with the specified name from the IAzApplication object.
helpviewer_keywords: ["AzApplication object [Security]","DeleteTask method","DeleteTask","DeleteTask method [Security]","DeleteTask method [Security]","AzApplication object","DeleteTask method [Security]","IAzApplication interface","IAzApplication interface [Security]","DeleteTask method","IAzApplication.DeleteTask","IAzApplication::DeleteTask","azroles/IAzApplication::DeleteTask","security.iazapplication_deletetask"]
old-location: security\iazapplication_deletetask.htm
tech.root: security
ms.assetid: b97015d7-00c3-445c-a445-07c52ef6ff29
ms.date: 03/20/2023
ms.keywords: AzApplication object [Security],DeleteTask method, DeleteTask, DeleteTask method [Security], DeleteTask method [Security],AzApplication object, DeleteTask method [Security],IAzApplication interface, IAzApplication interface [Security],DeleteTask method, IAzApplication.DeleteTask, IAzApplication::DeleteTask, azroles/IAzApplication::DeleteTask, security.iazapplication_deletetask
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
 - IAzApplication::DeleteTask
 - azroles/IAzApplication::DeleteTask
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
 - IAzApplication.DeleteTask
 - AzApplication.DeleteTask
---

# IAzApplication::DeleteTask

## -description

The **DeleteTask** method removes the [IAzTask](nn-azroles-iaztask.md) object with the specified name from the [IAzApplication](nn-azroles-iazapplication.md) object.

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

[IAzApplication](nn-azroles-iazapplication.md)
