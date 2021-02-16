---
UID: NF:azroles.IAzApplication.get_DelegatedPolicyUsersName
title: IAzApplication::get_DelegatedPolicyUsersName (azroles.h)
description: The DelegatedPolicyUsersName property of IAzApplication retrieves the account names of principals that act as delegated policy users.
helpviewer_keywords: ["AzApplication object [Security]","DelegatedPolicyUsersName property","DelegatedPolicyUsersName property [Security]","DelegatedPolicyUsersName property [Security]","AzApplication object","DelegatedPolicyUsersName property [Security]","IAzApplication interface","IAzApplication interface [Security]","DelegatedPolicyUsersName property","IAzApplication.DelegatedPolicyUsersName","IAzApplication.get_DelegatedPolicyUsersName","IAzApplication::DelegatedPolicyUsersName","IAzApplication::get_DelegatedPolicyUsersName","azroles/IAzApplication::DelegatedPolicyUsersName","azroles/IAzApplication::get_DelegatedPolicyUsersName","get_DelegatedPolicyUsersName","security.iazapplication_delegatedpolicyusersname"]
old-location: security\iazapplication_delegatedpolicyusersname.htm
tech.root: security
ms.assetid: ee18b86f-7ae2-4984-ac7a-3909eda647e3
ms.date: 12/05/2018
ms.keywords: AzApplication object [Security],DelegatedPolicyUsersName property, DelegatedPolicyUsersName property [Security], DelegatedPolicyUsersName property [Security],AzApplication object, DelegatedPolicyUsersName property [Security],IAzApplication interface, IAzApplication interface [Security],DelegatedPolicyUsersName property, IAzApplication.DelegatedPolicyUsersName, IAzApplication.get_DelegatedPolicyUsersName, IAzApplication::DelegatedPolicyUsersName, IAzApplication::get_DelegatedPolicyUsersName, azroles/IAzApplication::DelegatedPolicyUsersName, azroles/IAzApplication::get_DelegatedPolicyUsersName, get_DelegatedPolicyUsersName, security.iazapplication_delegatedpolicyusersname
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
 - IAzApplication::get_DelegatedPolicyUsersName
 - azroles/IAzApplication::get_DelegatedPolicyUsersName
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
 - IAzApplication.DelegatedPolicyUsersName
 - IAzApplication.get_DelegatedPolicyUsersName
 - AzApplication.DelegatedPolicyUsersName
---

# IAzApplication::get_DelegatedPolicyUsersName


## -description

The <b>DelegatedPolicyUsersName</b> property retrieves the account names of principals that act as delegated policy users.

This property is read-only.

## -parameters

## -remarks

Delegated policy users are principals that are allowed to read the subset of the policy data that the policy administrator of an <a href="/windows/desktop/api/azroles/nn-azroles-iazapplication">IAzApplication</a> object uses to administer the delegated object.

<div class="alert"><b>Note</b>  Delegated policy users are not supported for XML stores.</div>
<div> </div>
In JScript, the returned <a href="/windows/desktop/api/oaidl/ns-oaidl-safearray">SAFEARRAY</a> must be converted to the JScript <a href="/scripting/javascript/reference/array-object-javascript">Array</a> object.