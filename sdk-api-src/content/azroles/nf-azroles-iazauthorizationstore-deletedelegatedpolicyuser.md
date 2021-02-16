---
UID: NF:azroles.IAzAuthorizationStore.DeleteDelegatedPolicyUser
title: IAzAuthorizationStore::DeleteDelegatedPolicyUser (azroles.h)
description: Removes the specified security identifier (SID) in text form from the list of principals that act as delegated policy users.
helpviewer_keywords: ["AzAuthorizationStore object [Security]","DeleteDelegatedPolicyUser method","DeleteDelegatedPolicyUser","DeleteDelegatedPolicyUser method [Security]","DeleteDelegatedPolicyUser method [Security]","AzAuthorizationStore object","DeleteDelegatedPolicyUser method [Security]","IAzAuthorizationStore interface","IAzAuthorizationStore interface [Security]","DeleteDelegatedPolicyUser method","IAzAuthorizationStore.DeleteDelegatedPolicyUser","IAzAuthorizationStore::DeleteDelegatedPolicyUser","azroles/IAzAuthorizationStore::DeleteDelegatedPolicyUser","security.azauthorizationstore_deletedelegatedpolicyuser"]
old-location: security\azauthorizationstore_deletedelegatedpolicyuser.htm
tech.root: security
ms.assetid: cb00abca-7116-4a71-aed0-87ed9caff0fb
ms.date: 12/05/2018
ms.keywords: AzAuthorizationStore object [Security],DeleteDelegatedPolicyUser method, DeleteDelegatedPolicyUser, DeleteDelegatedPolicyUser method [Security], DeleteDelegatedPolicyUser method [Security],AzAuthorizationStore object, DeleteDelegatedPolicyUser method [Security],IAzAuthorizationStore interface, IAzAuthorizationStore interface [Security],DeleteDelegatedPolicyUser method, IAzAuthorizationStore.DeleteDelegatedPolicyUser, IAzAuthorizationStore::DeleteDelegatedPolicyUser, azroles/IAzAuthorizationStore::DeleteDelegatedPolicyUser, security.azauthorizationstore_deletedelegatedpolicyuser
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
 - IAzAuthorizationStore::DeleteDelegatedPolicyUser
 - azroles/IAzAuthorizationStore::DeleteDelegatedPolicyUser
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
 - AzAuthorizationStore.DeleteDelegatedPolicyUser
 - IAzAuthorizationStore.DeleteDelegatedPolicyUser
---

# IAzAuthorizationStore::DeleteDelegatedPolicyUser


## -description

The <b>DeleteDelegatedPolicyUser</b> method removes the specified <a href="/windows/desktop/SecGloss/s-gly">security identifier</a> (SID) in text form from the list of principals that act as delegated policy users.

## -parameters

### -param bstrDelegatedPolicyUser [in]

Text form of the SID to remove from the list of delegated policy users.

### -param varReserved [in, optional]

Reserved for future use.

## -remarks

Delegated policy users are principals that are allowed to read the subset of the policy data that the policy administrator of an <a href="/windows/desktop/api/azroles/nn-azroles-iazapplication">IAzApplication</a>  or <a href="/windows/desktop/api/azroles/nn-azroles-iazscope">IAzScope</a> object uses to administer the delegated object. 

<div class="alert"><b>Note</b>  Delegated policy users are not supported for XML stores.</div>
<div> </div>
To view the list of delegated policy users, use the <a href="/windows/desktop/api/azroles/nf-azroles-iazauthorizationstore-get_delegatedpolicyusers">DelegatedPolicyUsers</a> property.