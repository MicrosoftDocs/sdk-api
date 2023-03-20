---
UID: NF:azroles.IAzRole.DeleteMemberName
title: IAzRole::DeleteMemberName (azroles.h)
description: Removes the specified account name from the list of accounts that belong to the role.
helpviewer_keywords: ["AzRole object [Security]","DeleteMemberName method","DeleteMemberName","DeleteMemberName method [Security]","DeleteMemberName method [Security]","AzRole object","DeleteMemberName method [Security]","IAzRole interface","IAzRole interface [Security]","DeleteMemberName method","IAzRole.DeleteMemberName","IAzRole::DeleteMemberName","azroles/IAzRole::DeleteMemberName","security.iazrole_deletemembername"]
old-location: security\iazrole_deletemembername.htm
tech.root: security
ms.assetid: 3ca3e242-deab-46e7-b3f5-d6a75e5a2c08
ms.date: 03/20/2023
ms.keywords: AzRole object [Security],DeleteMemberName method, DeleteMemberName, DeleteMemberName method [Security], DeleteMemberName method [Security],AzRole object, DeleteMemberName method [Security],IAzRole interface, IAzRole interface [Security],DeleteMemberName method, IAzRole.DeleteMemberName, IAzRole::DeleteMemberName, azroles/IAzRole::DeleteMemberName, security.iazrole_deletemembername
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
 - IAzRole::DeleteMemberName
 - azroles/IAzRole::DeleteMemberName
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
 - IAzRole.DeleteMemberName
 - AzRole.DeleteMemberName
---

# IAzRole::DeleteMemberName

## -description

The **DeleteMemberName** method removes  the specified account name from the list of accounts that belong to the role.

## -parameters

### -param bstrProp [in]

String that contains the account name to remove from the list of accounts that belong to the role. The account name can be in either user principal name (UPN) format (for example, `someone@example.com`) or in the `ExampleDomain\UserName` format. If the domain is not in the `ExampleDomain\UserName` format, the [LookupAccountName](/windows/win32/api/winbase/nf-winbase-lookupaccountnamea) function is called to retrieve the domain.

### -param varReserved [in, optional]

Reserved for future use.

## -returns

If the method succeeds, it will return `S_OK`. Any other **HRESULT** value indicates that the operation failed.

## -remarks

To view the list of account names of accounts that belong to the role, use the [MembersName](nf-azroles-iazrole-get_membersname.md) property.

## -see-also

[LookupAccountName](/windows/win32/api/winbase/nf-winbase-lookupaccountnamea)

[MembersName](nf-azroles-iazrole-get_membersname.md)
