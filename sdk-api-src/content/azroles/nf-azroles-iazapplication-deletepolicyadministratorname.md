---
UID: NF:azroles.IAzApplication.DeletePolicyAdministratorName
title: IAzApplication::DeletePolicyAdministratorName (azroles.h)
description: Removes the specified account name from the list of principals that act as policy administrators. (IAzApplication.DeletePolicyAdministratorName)
helpviewer_keywords: ["AzApplication object [Security]","DeletePolicyAdministratorName method","DeletePolicyAdministratorName","DeletePolicyAdministratorName method [Security]","DeletePolicyAdministratorName method [Security]","AzApplication object","DeletePolicyAdministratorName method [Security]","IAzApplication interface","IAzApplication interface [Security]","DeletePolicyAdministratorName method","IAzApplication.DeletePolicyAdministratorName","IAzApplication::DeletePolicyAdministratorName","azroles/IAzApplication::DeletePolicyAdministratorName","security.iazapplication_deletepolicyadministratorname"]
old-location: security\iazapplication_deletepolicyadministratorname.htm
tech.root: security
ms.assetid: 6da92103-6de0-4310-b52c-c1441e775da8
ms.date: 12/05/2018
ms.keywords: AzApplication object [Security],DeletePolicyAdministratorName method, DeletePolicyAdministratorName, DeletePolicyAdministratorName method [Security], DeletePolicyAdministratorName method [Security],AzApplication object, DeletePolicyAdministratorName method [Security],IAzApplication interface, IAzApplication interface [Security],DeletePolicyAdministratorName method, IAzApplication.DeletePolicyAdministratorName, IAzApplication::DeletePolicyAdministratorName, azroles/IAzApplication::DeletePolicyAdministratorName, security.iazapplication_deletepolicyadministratorname
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
 - IAzApplication::DeletePolicyAdministratorName
 - azroles/IAzApplication::DeletePolicyAdministratorName
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
 - IAzApplication.DeletePolicyAdministratorName
 - AzApplication.DeletePolicyAdministratorName
---

# IAzApplication::DeletePolicyAdministratorName


## -description

The <b>DeletePolicyAdministratorName</b> method removes the specified account name from the list of principals that act as policy administrators.

## -parameters

### -param bstrAdmin [in]

Account name to remove from the list of policy administrators. The account name can be in either user principal name (UPN) format (for example, "someone@example.com") or in the format of "ExampleDomain\UserName". If the domain is not  in the "ExampleDomain\UserName" format, the <a href="/windows/desktop/api/winbase/nf-winbase-lookupaccountnamea">LookupAccountName</a> function is called to retrieve the domain.

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
