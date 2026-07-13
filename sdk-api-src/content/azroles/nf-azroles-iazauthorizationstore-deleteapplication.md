---
UID: NF:azroles.IAzAuthorizationStore.DeleteApplication
title: IAzAuthorizationStore::DeleteApplication (azroles.h)
description: Removes the IAzApplication object with the specified name from the AzAuthorizationStore object.
helpviewer_keywords: ["AzAuthorizationStore object [Security]","DeleteApplication method","DeleteApplication","DeleteApplication method [Security]","DeleteApplication method [Security]","AzAuthorizationStore object","DeleteApplication method [Security]","IAzAuthorizationStore interface","IAzAuthorizationStore interface [Security]","DeleteApplication method","IAzAuthorizationStore.DeleteApplication","IAzAuthorizationStore::DeleteApplication","azroles/IAzAuthorizationStore::DeleteApplication","security.azauthorizationstore_deleteapplication"]
old-location: security\azauthorizationstore_deleteapplication.htm
tech.root: security
ms.assetid: 512907fc-8657-4f2a-8b4a-af3027c6bbcd
ms.date: 03/20/2023
ms.keywords: AzAuthorizationStore object [Security],DeleteApplication method, DeleteApplication, DeleteApplication method [Security], DeleteApplication method [Security],AzAuthorizationStore object, DeleteApplication method [Security],IAzAuthorizationStore interface, IAzAuthorizationStore interface [Security],DeleteApplication method, IAzAuthorizationStore.DeleteApplication, IAzAuthorizationStore::DeleteApplication, azroles/IAzAuthorizationStore::DeleteApplication, security.azauthorizationstore_deleteapplication
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
 - IAzAuthorizationStore::DeleteApplication
 - azroles/IAzAuthorizationStore::DeleteApplication
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
 - AzAuthorizationStore.DeleteApplication
 - IAzAuthorizationStore.DeleteApplication
---

# IAzAuthorizationStore::DeleteApplication

## -description

The **DeleteApplication** method removes the [IAzApplication](nn-azroles-iazapplication.md) object with the specified name from the [AzAuthorizationStore](nn-azroles-iazauthorizationstore.md) object.

## -parameters

### -param bstrApplicationName [in]

Name of the [IAzApplication](nn-azroles-iazapplication.md) object to delete.

### -param varReserved [in, optional]

Reserved for future use.

## -returns

If the method succeeds, it will return `S_OK`. Any other **HRESULT** value indicates that the operation failed.

## -remarks

If the deleted [IAzApplication](nn-azroles-iazapplication.md) object has child objects, those objects are deleted, as well. If there are any **IAzApplication** references to an **IAzApplication** object that has been deleted from the cache, the **IAzApplication** object can no longer be used. In C++, you must release references to deleted **IAzApplication** objects by calling the [IUnknown::Release](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) method. In C# and Visual Basic, references to deleted objects are automatically released.

## -see-also

[IAzApplication](nn-azroles-iazapplication.md)
