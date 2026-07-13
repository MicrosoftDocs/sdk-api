---
UID: NF:azroles.IAzAuthorizationStore.CloseApplication
title: IAzAuthorizationStore::CloseApplication (azroles.h)
description: Unloads a specified IAzApplication object from the cache.
helpviewer_keywords: ["AZ_AZSTORE_FORCE_APPLICATION_CLOSE","AzAuthorizationStore object [Security]","CloseApplication method","CloseApplication","CloseApplication method [Security]","CloseApplication method [Security]","AzAuthorizationStore object","CloseApplication method [Security]","IAzAuthorizationStore interface","IAzAuthorizationStore interface [Security]","CloseApplication method","IAzAuthorizationStore.CloseApplication","IAzAuthorizationStore::CloseApplication","azroles/IAzAuthorizationStore::CloseApplication","security.azauthorizationstore_closeapplication"]
old-location: security\azauthorizationstore_closeapplication.htm
tech.root: security
ms.assetid: 7ba5fc77-676a-4fbe-8de8-2af5bf5f82f6
ms.date: 03/20/2023
ms.keywords: AZ_AZSTORE_FORCE_APPLICATION_CLOSE, AzAuthorizationStore object [Security],CloseApplication method, CloseApplication, CloseApplication method [Security], CloseApplication method [Security],AzAuthorizationStore object, CloseApplication method [Security],IAzAuthorizationStore interface, IAzAuthorizationStore interface [Security],CloseApplication method, IAzAuthorizationStore.CloseApplication, IAzAuthorizationStore::CloseApplication, azroles/IAzAuthorizationStore::CloseApplication, security.azauthorizationstore_closeapplication
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
 - IAzAuthorizationStore::CloseApplication
 - azroles/IAzAuthorizationStore::CloseApplication
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
 - AzAuthorizationStore.CloseApplication
 - IAzAuthorizationStore.CloseApplication
---

# IAzAuthorizationStore::CloseApplication

## -description

The **CloseApplication** method unloads a specified [IAzApplication](nn-azroles-iazapplication.md) object from the cache.

This method is not supported for XML authorization policy stores.

## -parameters

### -param bstrApplicationName [in]

The name of the [IAzApplication](nn-azroles-iazapplication.md) object to close.

### -param lFlag [in]

Flags that control the behavior of the operation. The following table shows the possible values.

| Value | Meaning |
|--------|--------|
| **0** | Child objects of the specified [IAzApplication](nn-azroles-iazapplication.md) object will be unloaded from the cache only when the user closes the last handle to the **IAzApplication** object. |
| **AZ_AZSTORE_FORCE_APPLICATION_CLOSE** | All child objects of the specified [IAzApplication](nn-azroles-iazapplication.md) object will be forcefully closed. Attempts to reference an open handle to a child object of the specified **IAzApplication** object will result in an **HRESULT_FROM_WIN32(ERROR_INVALID_HANDLE)** error. This flag should be used only if the user has implemented code to gracefully handle the  error. |

## -returns

If the method succeeds, it will return `S_OK`. Any other **HRESULT** value indicates that the operation failed.

## -see-also

[IAzApplication](nn-azroles-iazapplication.md)
