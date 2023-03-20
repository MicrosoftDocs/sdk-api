---
UID: NF:azroles.IAzApplication.DeleteApplicationGroup
title: IAzApplication::DeleteApplicationGroup (azroles.h)
description: Removes the IAzApplicationGroup object with the specified name from the IAzApplication object.
helpviewer_keywords: ["AzApplication object [Security]","DeleteApplicationGroup method","DeleteApplicationGroup","DeleteApplicationGroup method [Security]","DeleteApplicationGroup method [Security]","AzApplication object","DeleteApplicationGroup method [Security]","IAzApplication interface","IAzApplication interface [Security]","DeleteApplicationGroup method","IAzApplication.DeleteApplicationGroup","IAzApplication::DeleteApplicationGroup","azroles/IAzApplication::DeleteApplicationGroup","security.iazapplication_deleteapplicationgroup"]
old-location: security\iazapplication_deleteapplicationgroup.htm
tech.root: security
ms.assetid: e2ec7ba1-5998-45bf-aacf-e519bb944d5e
ms.date: 03/20/2023
ms.keywords: AzApplication object [Security],DeleteApplicationGroup method, DeleteApplicationGroup, DeleteApplicationGroup method [Security], DeleteApplicationGroup method [Security],AzApplication object, DeleteApplicationGroup method [Security],IAzApplication interface, IAzApplication interface [Security],DeleteApplicationGroup method, IAzApplication.DeleteApplicationGroup, IAzApplication::DeleteApplicationGroup, azroles/IAzApplication::DeleteApplicationGroup, security.iazapplication_deleteapplicationgroup
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
 - IAzApplication::DeleteApplicationGroup
 - azroles/IAzApplication::DeleteApplicationGroup
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
 - IAzApplication.DeleteApplicationGroup
 - AzApplication.DeleteApplicationGroup
---

# IAzApplication::DeleteApplicationGroup

## -description

The **DeleteApplicationGroup** method removes the [IAzApplicationGroup](nn-azroles-iazapplicationgroup.md) object with the specified name from the [IAzApplication](nn-azroles-iazapplication.md) object.

## -parameters

### -param bstrGroupName [in]

Name of the [IAzApplicationGroup](nn-azroles-iazapplicationgroup.md) object to delete.

### -param varReserved [in, optional]

Reserved for future use.

## -returns

If the method succeeds, it will return `S_OK`. Any other **HRESULT** value indicates that the operation failed.

## -remarks

If there are any [IAzApplicationGroup](nn-azroles-iazapplicationgroup.md) references to an **IAzApplicationGroup** object that has been deleted from the cache, the **IAzApplicationGroup** object can no longer be used. In C++, you must release references to deleted **IAzApplicationGroup** objects by calling the [IUnknown::Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) method. In C# and Visual Basic, references to deleted objects are automatically released.

## -see-also

[IAzApplicationGroup](nn-azroles-iazapplicationgroup.md)

[IAzApplication](nn-azroles-iazapplication.md)
