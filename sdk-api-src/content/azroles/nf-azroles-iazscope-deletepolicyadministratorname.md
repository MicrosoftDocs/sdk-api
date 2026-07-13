---
UID: NF:azroles.IAzScope.DeletePolicyAdministratorName
title: IAzScope::DeletePolicyAdministratorName (azroles.h)
description: The DeletePolicyAdministratorName method of IAzScope removes the specified account name from the list of principals that act as policy administrators.
helpviewer_keywords: ["AzScope object [Security]","DeletePolicyAdministratorName method","DeletePolicyAdministratorName","DeletePolicyAdministratorName method [Security]","DeletePolicyAdministratorName method [Security]","AzScope object","DeletePolicyAdministratorName method [Security]","IAzScope interface","IAzScope interface [Security]","DeletePolicyAdministratorName method","IAzScope.DeletePolicyAdministratorName","IAzScope::DeletePolicyAdministratorName","azroles/IAzScope::DeletePolicyAdministratorName","security.iazscope_deletepolicyadministratorname"]
old-location: security\iazscope_deletepolicyadministratorname.htm
tech.root: security
ms.assetid: 6314e1d5-e5ea-42c4-9457-dad5d6f57897
ms.date: 03/20/2023
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

The **DeletePolicyAdministratorName** method removes the specified account name from the list of principals that act as policy administrators.

## -parameters

### -param bstrAdmin [in]

Account name to remove from the list of policy administrators. The account name can be in either user principal name (UPN) format (for example, `someone@example.com`) or in the `ExampleDomain\UserName` format. If the domain is not in the `ExampleDomain\UserName` format, the [LookupAccountName](/windows/win32/api/winbase/nf-winbase-lookupaccountnamea) function is called to retrieve the domain.

### -param varReserved [in, optional]

Reserved for future use.

## -returns

If the method succeeds, it will return `S_OK`. Any other **HRESULT** value indicates that the operation failed.

## -remarks

Policy administrators for an object can perform the following tasks:

- Read the object
- Write attributes to the object
- Read attributes of child objects of the object
- Write attributes to child objects of the object
- Delete the object
- Delete child objects of the object
- Create child objects of the object

To view the list of policy administrators in account name format, use the [PolicyAdministratorsName](nf-azroles-iazscope-get_policyadministratorsname.md) property.

## -see-also

[LookupAccountName](/windows/win32/api/winbase/nf-winbase-lookupaccountnamea)

[PolicyAdministratorsName](nf-azroles-iazscope-get_policyadministratorsname.md)
