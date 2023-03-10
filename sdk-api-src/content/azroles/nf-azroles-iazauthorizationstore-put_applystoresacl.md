---
UID: NF:azroles.IAzAuthorizationStore.put_ApplyStoreSacl
title: IAzAuthorizationStore::put_ApplyStoreSacl (azroles.h)
description: Sets or retrieves a value that indicates whether policy audits should be generated when the authorization store is modified. (IAzAuthorizationStore.put_ApplyStoreSacl)
helpviewer_keywords: ["ApplyStoreSacl property [Security]","ApplyStoreSacl property [Security]","AzAuthorizationStore object","ApplyStoreSacl property [Security]","IAzAuthorizationStore interface","AzAuthorizationStore object [Security]","ApplyStoreSacl property","IAzAuthorizationStore interface [Security]","ApplyStoreSacl property","IAzAuthorizationStore.ApplyStoreSacl","IAzAuthorizationStore.put_ApplyStoreSacl","IAzAuthorizationStore::ApplyStoreSacl","IAzAuthorizationStore::get_ApplyStoreSacl","IAzAuthorizationStore::put_ApplyStoreSacl","azroles/IAzAuthorizationStore::ApplyStoreSacl","azroles/IAzAuthorizationStore::get_ApplyStoreSacl","azroles/IAzAuthorizationStore::put_ApplyStoreSacl","put_ApplyStoreSacl","security.azauthorizationstore_applystoresacl"]
old-location: security\azauthorizationstore_applystoresacl.htm
tech.root: security
ms.assetid: fdace7a9-4b6b-4698-812d-c53fc3b8f0d8
ms.date: 12/05/2018
ms.keywords: ApplyStoreSacl property [Security], ApplyStoreSacl property [Security],AzAuthorizationStore object, ApplyStoreSacl property [Security],IAzAuthorizationStore interface, AzAuthorizationStore object [Security],ApplyStoreSacl property, IAzAuthorizationStore interface [Security],ApplyStoreSacl property, IAzAuthorizationStore.ApplyStoreSacl, IAzAuthorizationStore.put_ApplyStoreSacl, IAzAuthorizationStore::ApplyStoreSacl, IAzAuthorizationStore::get_ApplyStoreSacl, IAzAuthorizationStore::put_ApplyStoreSacl, azroles/IAzAuthorizationStore::ApplyStoreSacl, azroles/IAzAuthorizationStore::get_ApplyStoreSacl, azroles/IAzAuthorizationStore::put_ApplyStoreSacl, put_ApplyStoreSacl, security.azauthorizationstore_applystoresacl
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
 - IAzAuthorizationStore::put_ApplyStoreSacl
 - azroles/IAzAuthorizationStore::put_ApplyStoreSacl
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
 - IAzAuthorizationStore.ApplyStoreSacl
 - IAzAuthorizationStore.get_ApplyStoreSacl
 - IAzAuthorizationStore.put_ApplyStoreSacl
 - AzAuthorizationStore.ApplyStoreSacl
---

# IAzAuthorizationStore::put_ApplyStoreSacl


## -description

The <b>ApplyStoreSacl</b> property sets or retrieves a value that indicates whether policy audits should be generated when the authorization store is modified.

This property is read/write.

## -parameters

## -remarks

Policy audits are generated when the underlying policy store is modified. Both success and failure audits are requested.

