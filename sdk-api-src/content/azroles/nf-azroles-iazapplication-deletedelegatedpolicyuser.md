---
UID: NF:azroles.IAzApplication.DeleteDelegatedPolicyUser
title: IAzApplication::DeleteDelegatedPolicyUser (azroles.h)
description: The IAzApplication::DeleteDelegatedPolicyUser method removes the specified security identifier in text form from the list of principals that act as delegated policy users.
helpviewer_keywords: ["AzApplication object [Security]","DeleteDelegatedPolicyUser method","DeleteDelegatedPolicyUser","DeleteDelegatedPolicyUser method [Security]","DeleteDelegatedPolicyUser method [Security]","AzApplication object","DeleteDelegatedPolicyUser method [Security]","IAzApplication interface","IAzApplication interface [Security]","DeleteDelegatedPolicyUser method","IAzApplication.DeleteDelegatedPolicyUser","IAzApplication::DeleteDelegatedPolicyUser","azroles/IAzApplication::DeleteDelegatedPolicyUser","security.iazapplication_deletedelegatedpolicyuser"]
old-location: security\iazapplication_deletedelegatedpolicyuser.htm
tech.root: security
ms.assetid: 92e7f4fa-ff86-4ef5-8b87-086dd73966d1
ms.date: 12/05/2018
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

The <b>DeleteDelegatedPolicyUser</b> method removes the specified <a href="/windows/desktop/SecGloss/s-gly">security identifier</a>  (SID) in text form from the list of principals that act as delegated policy users.

## -parameters

### -param bstrDelegatedPolicyUser [in]

Text form of the SID to remove from the list of delegated policy users.

### -param varReserved [in, optional]

Reserved for future use.

## -remarks

Delegated policy users are principals that are allowed to read the subset of the policy data that the policy administrator of an <a href="/windows/desktop/api/azroles/nn-azroles-iazapplication">IAzApplication</a> object uses to administer the delegated object.

<div class="alert"><b>Note</b>  Delegated policy users are not supported for XML stores.</div>
<div> </div>
To view the list of delegated policy users, use the <a href="/windows/desktop/api/azroles/nf-azroles-iazapplication-get_delegatedpolicyusers">DelegatedPolicyUsers</a> property.