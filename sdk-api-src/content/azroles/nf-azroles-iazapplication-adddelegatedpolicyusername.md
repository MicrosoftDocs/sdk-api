---
UID: NF:azroles.IAzApplication.AddDelegatedPolicyUserName
title: IAzApplication::AddDelegatedPolicyUserName (azroles.h)
description: Adds the specified account name to the list of principals that act as delegated policy users. (IAzApplication.AddDelegatedPolicyUserName)
helpviewer_keywords: ["AddDelegatedPolicyUserName","AddDelegatedPolicyUserName method [Security]","AddDelegatedPolicyUserName method [Security]","AzApplication object","AddDelegatedPolicyUserName method [Security]","IAzApplication interface","AzApplication object [Security]","AddDelegatedPolicyUserName method","IAzApplication interface [Security]","AddDelegatedPolicyUserName method","IAzApplication.AddDelegatedPolicyUserName","IAzApplication::AddDelegatedPolicyUserName","azroles/IAzApplication::AddDelegatedPolicyUserName","security.iazapplication_adddelegatedpolicyusername"]
old-location: security\iazapplication_adddelegatedpolicyusername.htm
tech.root: security
ms.assetid: f30392f6-7100-43dd-ab20-419cd02d9ea5
ms.date: 12/05/2018
ms.keywords: AddDelegatedPolicyUserName, AddDelegatedPolicyUserName method [Security], AddDelegatedPolicyUserName method [Security],AzApplication object, AddDelegatedPolicyUserName method [Security],IAzApplication interface, AzApplication object [Security],AddDelegatedPolicyUserName method, IAzApplication interface [Security],AddDelegatedPolicyUserName method, IAzApplication.AddDelegatedPolicyUserName, IAzApplication::AddDelegatedPolicyUserName, azroles/IAzApplication::AddDelegatedPolicyUserName, security.iazapplication_adddelegatedpolicyusername
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
 - IAzApplication::AddDelegatedPolicyUserName
 - azroles/IAzApplication::AddDelegatedPolicyUserName
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
 - IAzApplication.AddDelegatedPolicyUserName
 - AzApplication.AddDelegatedPolicyUserName
---

# IAzApplication::AddDelegatedPolicyUserName


## -description

The <b>AddDelegatedPolicyUserName</b> method adds the specified account name to the list of principals that act as delegated policy users.

## -parameters

### -param bstrDelegatedPolicyUser [in]

Account name to add to the list of delegated policy users. The account name must be in user principal name (UPN) format (for example, "someone@example.com"). The <a href="/windows/desktop/api/winbase/nf-winbase-lookupaccountnamea">LookupAccountName</a> function is called to retrieve the domain.

### -param varReserved [in, optional]

Reserved for future use.

## -returns

 If the method succeeds, the method returns S_OK.

An attempt to call this method on an XML store will return E_INVALIDARG.

Any other <b>HRESULT</b> value indicates that the operation failed.

## -remarks

Delegated policy users are principals that are allowed to read the subset of the policy data that the policy administrator of an <a href="/windows/desktop/api/azroles/nn-azroles-iazapplication">IAzApplication</a> object uses to administer the delegated object.

<div class="alert"><b>Note</b>  Delegated policy users are not supported for XML stores.</div>
<div> </div>
To view the list of delegated policy users in account name format, use the <a href="/windows/desktop/api/azroles/nf-azroles-iazapplication-get_delegatedpolicyusersname">DelegatedPolicyUsersName</a> property.

You must call the <a href="/windows/desktop/api/azroles/nf-azroles-iazapplication-submit">Submit</a> method to persist any changes made by this method.
