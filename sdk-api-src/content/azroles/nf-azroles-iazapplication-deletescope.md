---
UID: NF:azroles.IAzApplication.DeleteScope
title: IAzApplication::DeleteScope (azroles.h)
description: Removes the IAzScope object with the specified name from the IAzApplication object.
helpviewer_keywords: ["AzApplication object [Security]","DeleteScope method","DeleteScope","DeleteScope method [Security]","DeleteScope method [Security]","AzApplication object","DeleteScope method [Security]","IAzApplication interface","IAzApplication interface [Security]","DeleteScope method","IAzApplication.DeleteScope","IAzApplication::DeleteScope","azroles/IAzApplication::DeleteScope","security.iazapplication_deletescope"]
old-location: security\iazapplication_deletescope.htm
tech.root: security
ms.assetid: 2a3c2e18-9264-496a-9bd3-ff9c529a2426
ms.date: 03/20/2023
ms.keywords: AzApplication object [Security],DeleteScope method, DeleteScope, DeleteScope method [Security], DeleteScope method [Security],AzApplication object, DeleteScope method [Security],IAzApplication interface, IAzApplication interface [Security],DeleteScope method, IAzApplication.DeleteScope, IAzApplication::DeleteScope, azroles/IAzApplication::DeleteScope, security.iazapplication_deletescope
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
 - IAzApplication::DeleteScope
 - azroles/IAzApplication::DeleteScope
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
 - IAzApplication.DeleteScope
 - AzApplication.DeleteScope
---

# IAzApplication::DeleteScope

## -description

The **DeleteScope** method removes the [IAzScope](nn-azroles-iazscope.md) object with the specified name from the [IAzApplication](nn-azroles-iazapplication.md) object.

## -parameters

### -param bstrScopeName [in]

Name of the [IAzScope](nn-azroles-iazscope.md) object to delete.

### -param varReserved [in, optional]

Reserved for future use.

## -returns

If the method succeeds, it will return `S_OK`. Any other **HRESULT** value indicates that the operation failed.

## -remarks

If there are any [IAzScope](nn-azroles-iazscope.md) references to an **IAzScope** object that has been deleted from the cache, the **IAzScope** object can no longer be used. In C++, you must release references to deleted **IAzScope** objects by calling the [IUnknown::Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) method. In C# and Visual Basic, references to deleted objects are automatically released.

## -see-also

[IAzScope](nn-azroles-iazscope.md)

[IAzApplication](nn-azroles-iazapplication.md)
