---
UID: NF:azroles.IAzScope.DeletePolicyAdministratorName
title: IAzScope::DeletePolicyAdministratorName (azroles.h)
description: The DeletePolicyAdministratorName method of IAzScope removes the specified account name from the list of principals that act as policy administrators.
helpviewer_keywords: ["AzScope object [Security]","DeletePolicyAdministratorName method","DeletePolicyAdministratorName","DeletePolicyAdministratorName method [Security]","DeletePolicyAdministratorName method [Security]","AzScope object","DeletePolicyAdministratorName method [Security]","IAzScope interface","IAzScope interface [Security]","DeletePolicyAdministratorName method","IAzScope.DeletePolicyAdministratorName","IAzScope::DeletePolicyAdministratorName","azroles/IAzScope::DeletePolicyAdministratorName","security.iazscope_deletepolicyadministratorname"]
old-location: security\iazscope_deletepolicyadministratorname.htm
tech.root: security
ms.assetid: 6314e1d5-e5ea-42c4-9457-dad5d6f57897
ms.date: 12/05/2018
ms.keywords: AzScope object [Security],DeletePolicyAdministratorName method, DeletePolicyAdministratorName, DeletePolicyAdministratorName method [Security], DeletePolicyAdministratorName method [Security],AzScope object, DeletePolicyAdministratorName method [Security],IAzScope interface, IAzScope interface [Security],DeletePolicyAdministratorName method, IAzScope.DeletePolicyAdministratorName, IAzScope::DeletePolicyAdministratorName, azroles/IAzScope::DeletePolicyAdministratorName, security.iazscope_deletepolicyadministratorname
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
 - IAzScope::DeletePolicyAdministratorName
 - azroles/IAzScope::DeletePolicyAdministratorName
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
 - IAzScope.DeletePolicyAdministratorName
 - AzScope.DeletePolicyAdministratorName
---

# IAzScope::DeletePolicyAdministratorName


## -description

The <b>DeletePolicyAdministratorName</b> method removes the specified account name from the list of principals that act as policy administrators.

## -parameters

### -param bstrAdmin [in]

Account name to remove from the list of policy administrators. The account name can be in either user principal name (UPN) format (for example, "someone@example.com") or in the "ExampleDomain\UserName" format. If the domain is not  in the "ExampleDomain\UserName" format, the <a href="/windows/desktop/api/winbase/nf-winbase-lookupaccountnamea">LookupAccountName</a> function is called to retrieve the domain.

### -param varReserved [in, optional]

Reserved for future use.

## -remarks

Policy administrators for an object can perform the following tasks:

<ul>
<li>Read the object</li>
<li>Write attributes to the object</li>
<li>Read attributes of child objects of the object</li>
<li>Write attributes to child objects of the object</li>
<li>Delete the object</li>
<li>Delete child objects of the object</li>
<li>Create child objects of the object</li>
</ul>
To view the list of policy administrators in account name format, use the <a href="/windows/desktop/api/azroles/nf-azroles-iazscope-get_policyadministratorsname">PolicyAdministratorsName</a> property.