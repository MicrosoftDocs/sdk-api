---
UID: NF:azroles.IAzAuthorizationStore.DeletePolicyAdministrator
title: IAzAuthorizationStore::DeletePolicyAdministrator (azroles.h)
description: Removes the specified security identifier (SID) in text form from the list of principals that act as policy administrators.
helpviewer_keywords: ["AzAuthorizationStore object [Security]","DeletePolicyAdministrator method","DeletePolicyAdministrator","DeletePolicyAdministrator method [Security]","DeletePolicyAdministrator method [Security]","AzAuthorizationStore object","DeletePolicyAdministrator method [Security]","IAzAuthorizationStore interface","IAzAuthorizationStore interface [Security]","DeletePolicyAdministrator method","IAzAuthorizationStore.DeletePolicyAdministrator","IAzAuthorizationStore::DeletePolicyAdministrator","azroles/IAzAuthorizationStore::DeletePolicyAdministrator","security.azauthorizationstore_deletepolicyadministrator"]
old-location: security\azauthorizationstore_deletepolicyadministrator.htm
tech.root: security
ms.assetid: c27ca754-7808-4c96-8966-0be3960f2926
ms.date: 03/20/2023
ms.keywords: AzAuthorizationStore object [Security],DeletePolicyAdministrator method, DeletePolicyAdministrator, DeletePolicyAdministrator method [Security], DeletePolicyAdministrator method [Security],AzAuthorizationStore object, DeletePolicyAdministrator method [Security],IAzAuthorizationStore interface, IAzAuthorizationStore interface [Security],DeletePolicyAdministrator method, IAzAuthorizationStore.DeletePolicyAdministrator, IAzAuthorizationStore::DeletePolicyAdministrator, azroles/IAzAuthorizationStore::DeletePolicyAdministrator, security.azauthorizationstore_deletepolicyadministrator
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
 - IAzAuthorizationStore::DeletePolicyAdministrator
 - azroles/IAzAuthorizationStore::DeletePolicyAdministrator
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
 - AzAuthorizationStore.DeletePolicyAdministrator
 - IAzAuthorizationStore.DeletePolicyAdministrator
---

# IAzAuthorizationStore::DeletePolicyAdministrator

## -description

The **DeletePolicyAdministrator** method removes the specified [security identifier](/windows/win32/SecGloss/s-gly) (SID) in text form from the list of principals that act as policy administrators.

## -parameters

### -param bstrAdmin [in]

Text form of the SID to remove from the list of policy administrators.

### -param varReserved [in, optional]

Reserved for future use.

## -returns

If the method succeeds, it will return `S_OK`. Any other **HRESULT** value indicates that the operation failed.

## -remarks

Policy administrators for an object can perform the following tasks:

- Read the object
- Write attributes to the object
- Read attributes of child objects of the object
- Write attributes to child objects of the object
- Delete the object
- Delete child objects of the object
- Create child objects of the object

To view the list of policy administrators, use the [PolicyAdministrators](nf-azroles-iazauthorizationstore-get_policyadministrators.md) property.

## -see-also

[PolicyAdministrators](nf-azroles-iazauthorizationstore-get_policyadministrators.md)
