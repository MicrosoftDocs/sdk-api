---
UID: NF:azroles.IAzScope.AddPolicyAdministratorName
title: IAzScope::AddPolicyAdministratorName (azroles.h)
description: The AddPolicyAdministratorName method of IAzScope adds the specified account name to the list of principals that act as policy administrators.
helpviewer_keywords: ["AddPolicyAdministratorName","AddPolicyAdministratorName method [Security]","AddPolicyAdministratorName method [Security]","AzScope object","AddPolicyAdministratorName method [Security]","IAzScope interface","AzScope object [Security]","AddPolicyAdministratorName method","IAzScope interface [Security]","AddPolicyAdministratorName method","IAzScope.AddPolicyAdministratorName","IAzScope::AddPolicyAdministratorName","azroles/IAzScope::AddPolicyAdministratorName","security.iazscope_addpolicyadministratorname"]
old-location: security\iazscope_addpolicyadministratorname.htm
tech.root: security
ms.assetid: a160e4cb-e779-413e-9d8a-5fb9684a48f2
ms.date: 03/20/2023
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

The **AddPolicyAdministratorName** method adds the specified account name to the list of principals that act as policy administrators.

## -parameters

### -param bstrAdmin [in]

The account name to add to the list of policy administrators. The account name can be in either user principal name (UPN) format (for example, `someone@example.com`) or in the `ExampleDomain\UserName` format. If the domain is not  in the `ExampleDomain\UserName` format, the [LookupAccountName](/windows/win32/api/winbase/nf-winbase-lookupaccountnamea) function is called to retrieve the domain.

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

You must call the [Submit](nf-azroles-iazscope-submit.md) method to persist any changes made by this method.

## -see-also

[LookupAccountName](/windows/win32/api/winbase/nf-winbase-lookupaccountnamea)

[PolicyAdministratorsName](nf-azroles-iazscope-get_policyadministratorsname.md)

[Submit](nf-azroles-iazscope-submit.md)
