---
UID: NF:azroles.IAzScope.AddPolicyAdministratorName
title: IAzScope::AddPolicyAdministratorName (azroles.h)
description: The AddPolicyAdministratorName method of IAzScope adds the specified account name to the list of principals that act as policy administrators.
helpviewer_keywords: ["AddPolicyAdministratorName","AddPolicyAdministratorName method [Security]","AddPolicyAdministratorName method [Security]","AzScope object","AddPolicyAdministratorName method [Security]","IAzScope interface","AzScope object [Security]","AddPolicyAdministratorName method","IAzScope interface [Security]","AddPolicyAdministratorName method","IAzScope.AddPolicyAdministratorName","IAzScope::AddPolicyAdministratorName","azroles/IAzScope::AddPolicyAdministratorName","security.iazscope_addpolicyadministratorname"]
old-location: security\iazscope_addpolicyadministratorname.htm
tech.root: security
ms.assetid: a160e4cb-e779-413e-9d8a-5fb9684a48f2
ms.date: 12/05/2018
ms.keywords: AddPolicyAdministratorName, AddPolicyAdministratorName method [Security], AddPolicyAdministratorName method [Security],AzScope object, AddPolicyAdministratorName method [Security],IAzScope interface, AzScope object [Security],AddPolicyAdministratorName method, IAzScope interface [Security],AddPolicyAdministratorName method, IAzScope.AddPolicyAdministratorName, IAzScope::AddPolicyAdministratorName, azroles/IAzScope::AddPolicyAdministratorName, security.iazscope_addpolicyadministratorname
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
 - IAzScope::AddPolicyAdministratorName
 - azroles/IAzScope::AddPolicyAdministratorName
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
 - IAzScope.AddPolicyAdministratorName
 - AzScope.AddPolicyAdministratorName
---

# IAzScope::AddPolicyAdministratorName


## -description

The <b>AddPolicyAdministratorName</b> method adds the specified account name to the list of principals that act as policy administrators.

## -parameters

### -param bstrAdmin [in]

The account name to add to the list of policy administrators.  The account name can be in either user principal name (UPN) format (for example, "someone@example.com") or in the "ExampleDomain\UserName" format. If the domain is not  in the "ExampleDomain\UserName" format, the <a href="/windows/desktop/api/winbase/nf-winbase-lookupaccountnamea">LookupAccountName</a> function is called to retrieve the domain.

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

You must call the <a href="/windows/desktop/api/azroles/nf-azroles-iazscope-submit">Submit</a> method to persist any changes made by this method.