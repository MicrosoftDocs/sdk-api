---
UID: NF:azroles.IAzAuthorizationStore.DeletePolicyReader
title: IAzAuthorizationStore::DeletePolicyReader (azroles.h)
description: Removes the specified security identifier (SID) in text form from the list of principals that act as policy readers.
helpviewer_keywords: ["AzAuthorizationStore object [Security]","DeletePolicyReader method","DeletePolicyReader","DeletePolicyReader method [Security]","DeletePolicyReader method [Security]","AzAuthorizationStore object","DeletePolicyReader method [Security]","IAzAuthorizationStore interface","IAzAuthorizationStore interface [Security]","DeletePolicyReader method","IAzAuthorizationStore.DeletePolicyReader","IAzAuthorizationStore::DeletePolicyReader","azroles/IAzAuthorizationStore::DeletePolicyReader","security.azauthorizationstore_deletepolicyreader"]
old-location: security\azauthorizationstore_deletepolicyreader.htm
tech.root: security
ms.assetid: 948732bb-4d29-402b-bb12-02d2b73bc443
ms.date: 03/20/2023
ms.keywords: AzAuthorizationStore object [Security],DeletePolicyReader method, DeletePolicyReader, DeletePolicyReader method [Security], DeletePolicyReader method [Security],AzAuthorizationStore object, DeletePolicyReader method [Security],IAzAuthorizationStore interface, IAzAuthorizationStore interface [Security],DeletePolicyReader method, IAzAuthorizationStore.DeletePolicyReader, IAzAuthorizationStore::DeletePolicyReader, azroles/IAzAuthorizationStore::DeletePolicyReader, security.azauthorizationstore_deletepolicyreader
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
 - IAzAuthorizationStore::DeletePolicyReader
 - azroles/IAzAuthorizationStore::DeletePolicyReader
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
 - AzAuthorizationStore.DeletePolicyReader
 - IAzAuthorizationStore.DeletePolicyReader
---

# IAzAuthorizationStore::DeletePolicyReader

## -description

The **DeletePolicyReader** method removes the specified [security identifier](/windows/win32/SecGloss/s-gly) (SID) in text form from the list of principals that act as policy readers.

## -parameters

### -param bstrReader [in]

Text form of the SID to remove from the list of policy readers.

### -param varReserved [in, optional]

Reserved for future use.

## -returns

If the method succeeds, it will return `S_OK`. Any other **HRESULT** value indicates that the operation failed.

## -remarks

Policy readers for an object can read attributes for the object and for child objects of the object. Readers can also  use the policy; for example, readers can call the [AccessCheck](nf-azroles-iazclientcontext-accesscheck.md) method. Readers cannot modify the object or its child objects.

To view the list of policy readers, use the [PolicyReaders](nf-azroles-iazauthorizationstore-get_policyreaders.md) property.

## -see-also

[AccessCheck](nf-azroles-iazclientcontext-accesscheck.md)

[PolicyReaders](nf-azroles-iazauthorizationstore-get_policyreaders.md)
