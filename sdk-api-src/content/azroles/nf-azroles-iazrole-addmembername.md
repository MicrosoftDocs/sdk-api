---
UID: NF:azroles.IAzRole.AddMemberName
title: IAzRole::AddMemberName (azroles.h)
description: Adds the specified account name to the list of accounts that belong to the role.
helpviewer_keywords: ["AddMemberName","AddMemberName method [Security]","AddMemberName method [Security]","AzRole object","AddMemberName method [Security]","IAzRole interface","AzRole object [Security]","AddMemberName method","IAzRole interface [Security]","AddMemberName method","IAzRole.AddMemberName","IAzRole::AddMemberName","azroles/IAzRole::AddMemberName","security.iazrole_addmembername"]
old-location: security\iazrole_addmembername.htm
tech.root: security
ms.assetid: fc2ca62e-40b1-4b09-a129-50d6162c6807
ms.date: 03/20/2023
ms.keywords: AddMemberName, AddMemberName method [Security], AddMemberName method [Security],AzRole object, AddMemberName method [Security],IAzRole interface, AzRole object [Security],AddMemberName method, IAzRole interface [Security],AddMemberName method, IAzRole.AddMemberName, IAzRole::AddMemberName, azroles/IAzRole::AddMemberName, security.iazrole_addmembername
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
 - IAzRole::AddMemberName
 - azroles/IAzRole::AddMemberName
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
 - IAzRole.AddMemberName
 - AzRole.AddMemberName
---

# IAzRole::AddMemberName

## -description

The **AddMemberName** method adds the specified account name to the list of accounts that belong to the role.

## -parameters

### -param bstrProp [in]

String that contains the account name to add to the list of accounts that belong to the role. The account name can be in either user principal name (UPN) format (for example, `someone@example.com`) or in the `ExampleDomain\UserName` format. If the domain is not in the `ExampleDomain\UserName` format, the [LookupAccountName](/windows/win32/api/winbase/nf-winbase-lookupaccountnamea) function is called to retrieve the domain.

### -param varReserved [in, optional]

Reserved for future use.

## -returns

If the method succeeds, it will return `S_OK`. Any other **HRESULT** value indicates that the operation failed.

## -remarks

To view the list of account names of accounts that belong to this role, use the [MembersName](nf-azroles-iazrole-get_membersname.md) property.

You must call the [Submit](nf-azroles-iazrole-submit.md) method to persist any changes made by this method.

## -see-also

[MembersName](nf-azroles-iazrole-get_membersname.md)

[Submit](nf-azroles-iazrole-submit.md)

[LookupAccountName](/windows/win32/api/winbase/nf-winbase-lookupaccountnamea)
