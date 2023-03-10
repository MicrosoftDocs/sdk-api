---
UID: NF:azroles.IAzApplication.AddPolicyAdministratorName
title: IAzApplication::AddPolicyAdministratorName (azroles.h)
description: Adds the specified account name to the list of principals that act as policy administrators. (IAzApplication.AddPolicyAdministratorName)
helpviewer_keywords: ["AddPolicyAdministratorName","AddPolicyAdministratorName method [Security]","AddPolicyAdministratorName method [Security]","AzApplication object","AddPolicyAdministratorName method [Security]","IAzApplication interface","AzApplication object [Security]","AddPolicyAdministratorName method","IAzApplication interface [Security]","AddPolicyAdministratorName method","IAzApplication.AddPolicyAdministratorName","IAzApplication::AddPolicyAdministratorName","azroles/IAzApplication::AddPolicyAdministratorName","security.iazapplication_addpolicyadministratorname"]
old-location: security\iazapplication_addpolicyadministratorname.htm
tech.root: security
ms.assetid: cc5f74c6-e1b6-4924-b5c1-2d3600ce37ef
ms.date: 12/05/2018
ms.keywords: AddPolicyAdministratorName, AddPolicyAdministratorName method [Security], AddPolicyAdministratorName method [Security],AzApplication object, AddPolicyAdministratorName method [Security],IAzApplication interface, AzApplication object [Security],AddPolicyAdministratorName method, IAzApplication interface [Security],AddPolicyAdministratorName method, IAzApplication.AddPolicyAdministratorName, IAzApplication::AddPolicyAdministratorName, azroles/IAzApplication::AddPolicyAdministratorName, security.iazapplication_addpolicyadministratorname
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
 - IAzApplication::AddPolicyAdministratorName
 - azroles/IAzApplication::AddPolicyAdministratorName
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
 - IAzApplication.AddPolicyAdministratorName
 - AzApplication.AddPolicyAdministratorName
---

# IAzApplication::AddPolicyAdministratorName


## -description

The <b>AddPolicyAdministratorName</b> method adds the specified account name to the list of principals that act as policy administrators.

## -parameters

### -param bstrAdmin [in]

Account name to add to the list of policy administrators. The account name must be in user principal name (UPN) format (for example, "someone@example.com"). The <a href="/windows/desktop/api/winbase/nf-winbase-lookupaccountnamea">LookupAccountName</a> function is called to retrieve the domain.

### -param varReserved [in, optional]

Reserved for future use.

## -returns

 If the method succeeds, the method returns S_OK.

Any other <b>HRESULT</b> value indicates that the operation failed.

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
To view the list of policy administrators in account name format, use the <a href="/windows/desktop/api/azroles/nf-azroles-iazapplication-get_policyadministratorsname">PolicyAdministratorsName</a> property.

You must call the <a href="/windows/desktop/api/azroles/nf-azroles-iazapplication-submit">Submit</a> method to persist any changes made by this method.
