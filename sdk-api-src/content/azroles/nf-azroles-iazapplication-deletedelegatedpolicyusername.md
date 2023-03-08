---
UID: NF:azroles.IAzApplication.DeleteDelegatedPolicyUserName
title: IAzApplication::DeleteDelegatedPolicyUserName (azroles.h)
description: Removes the specified account name from the list of principals that act as delegated policy users. (IAzApplication.DeleteDelegatedPolicyUserName)
helpviewer_keywords: ["AzApplication object [Security]","DeleteDelegatedPolicyUserName method","DeleteDelegatedPolicyUserName","DeleteDelegatedPolicyUserName method [Security]","DeleteDelegatedPolicyUserName method [Security]","AzApplication object","DeleteDelegatedPolicyUserName method [Security]","IAzApplication interface","IAzApplication interface [Security]","DeleteDelegatedPolicyUserName method","IAzApplication.DeleteDelegatedPolicyUserName","IAzApplication::DeleteDelegatedPolicyUserName","azroles/IAzApplication::DeleteDelegatedPolicyUserName","security.iazapplication_deletedelegatedpolicyusername"]
old-location: security\iazapplication_deletedelegatedpolicyusername.htm
tech.root: security
ms.assetid: b6abe8d6-9212-4c92-ba35-d6eaa8df1115
ms.date: 12/05/2018
ms.keywords: AzApplication object [Security],DeleteDelegatedPolicyUserName method, DeleteDelegatedPolicyUserName, DeleteDelegatedPolicyUserName method [Security], DeleteDelegatedPolicyUserName method [Security],AzApplication object, DeleteDelegatedPolicyUserName method [Security],IAzApplication interface, IAzApplication interface [Security],DeleteDelegatedPolicyUserName method, IAzApplication.DeleteDelegatedPolicyUserName, IAzApplication::DeleteDelegatedPolicyUserName, azroles/IAzApplication::DeleteDelegatedPolicyUserName, security.iazapplication_deletedelegatedpolicyusername
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
 - IAzApplication::DeleteDelegatedPolicyUserName
 - azroles/IAzApplication::DeleteDelegatedPolicyUserName
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
 - IAzApplication.DeleteDelegatedPolicyUserName
 - AzApplication.DeleteDelegatedPolicyUserName
---

# IAzApplication::DeleteDelegatedPolicyUserName


## -description

The <b>DeleteDelegatedPolicyUserName</b> method removes the specified account name from the list of principals that act as delegated policy users.

## -parameters

### -param bstrDelegatedPolicyUser [in]

The account name to remove from the list of delegated policy users. The account name must be in user principal name (UPN) format (for example, "someone@example.com"). The <a href="/windows/desktop/api/winbase/nf-winbase-lookupaccountnamea">LookupAccountName</a> function is called to retrieve the domain.

### -param varReserved [in, optional]

Reserved for future use.

## -returns

 If the method succeeds, the method returns S_OK.

Any other <b>HRESULT</b> value indicates that the operation failed. An attempt to call this method on an XML store will return E_INVALIDARG.

## -remarks

Delegated policy users are principals that are allowed to read the subset of the policy data that the policy administrator of an <a href="/windows/desktop/api/azroles/nn-azroles-iazapplication">IAzApplication</a> object uses to administer the delegated object.

<div class="alert"><b>Note</b>  Delegated policy users are not supported for XML stores.</div>
<div> </div>
To view the list of delegated policy users in account name format, use the <a href="/windows/desktop/api/azroles/nf-azroles-iazapplication-get_delegatedpolicyusersname">DelegatedPolicyUsersName</a> property.
