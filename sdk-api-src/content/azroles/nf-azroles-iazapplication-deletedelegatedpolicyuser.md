---
UID: NF:azroles.IAzApplication.DeleteDelegatedPolicyUser
title: IAzApplication::DeleteDelegatedPolicyUser (azroles.h)
description: The IAzApplication::DeleteDelegatedPolicyUser method removes the specified security identifier in text form from the list of principals that act as delegated policy users.
helpviewer_keywords: ["AzApplication object [Security]","DeleteDelegatedPolicyUser method","DeleteDelegatedPolicyUser","DeleteDelegatedPolicyUser method [Security]","DeleteDelegatedPolicyUser method [Security]","AzApplication object","DeleteDelegatedPolicyUser method [Security]","IAzApplication interface","IAzApplication interface [Security]","DeleteDelegatedPolicyUser method","IAzApplication.DeleteDelegatedPolicyUser","IAzApplication::DeleteDelegatedPolicyUser","azroles/IAzApplication::DeleteDelegatedPolicyUser","security.iazapplication_deletedelegatedpolicyuser"]
old-location: security\iazapplication_deletedelegatedpolicyuser.htm
tech.root: security
ms.assetid: 92e7f4fa-ff86-4ef5-8b87-086dd73966d1
ms.date: 03/20/2023
ms.keywords: AzApplication object [Security],DeleteDelegatedPolicyUser method, DeleteDelegatedPolicyUser, DeleteDelegatedPolicyUser method [Security], DeleteDelegatedPolicyUser method [Security],AzApplication object, DeleteDelegatedPolicyUser method [Security],IAzApplication interface, IAzApplication interface [Security],DeleteDelegatedPolicyUser method, IAzApplication.DeleteDelegatedPolicyUser, IAzApplication::DeleteDelegatedPolicyUser, azroles/IAzApplication::DeleteDelegatedPolicyUser, security.iazapplication_deletedelegatedpolicyuser
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
 - IAzApplication::DeleteDelegatedPolicyUser
 - azroles/IAzApplication::DeleteDelegatedPolicyUser
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
 - IAzApplication.DeleteDelegatedPolicyUser
 - AzApplication.DeleteDelegatedPolicyUser
---

# IAzApplication::DeleteDelegatedPolicyUser

## -description

The **DeleteDelegatedPolicyUser** method removes the specified [security identifier](/windows/win32/SecGloss/s-gly) (SID) in text form from the list of principals that act as delegated policy users.

## -parameters

### -param bstrDelegatedPolicyUser [in]

Text form of the SID to remove from the list of delegated policy users.

### -param varReserved [in, optional]

Reserved for future use.

## -returns

If the method succeeds, it will return `S_OK`. Any other **HRESULT** value indicates that the operation failed.

## -remarks

Delegated policy users are principals that are allowed to read the subset of the policy data that the policy administrator of an [IAzApplication](nn-azroles-iazapplication.md) object uses to administer the delegated object.

> [!NOTE]
> Delegated policy users are not supported for XML stores.

To view the list of delegated policy users, use the [DelegatedPolicyUsers](nf-azroles-iazapplication-get_delegatedpolicyusers.md) property.

## -see-also

[IAzApplication](nn-azroles-iazapplication.md)

[DelegatedPolicyUsers](nf-azroles-iazapplication-get_delegatedpolicyusers.md)
