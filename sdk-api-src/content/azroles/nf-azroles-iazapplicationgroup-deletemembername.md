---
UID: NF:azroles.IAzApplicationGroup.DeleteMemberName
title: IAzApplicationGroup::DeleteMemberName (azroles.h)
description: Removes the specified account name from the list of accounts that belong to the application group.
helpviewer_keywords: ["AzApplicationGroup object [Security]","DeleteMemberName method","DeleteMemberName","DeleteMemberName method [Security]","DeleteMemberName method [Security]","AzApplicationGroup object","DeleteMemberName method [Security]","IAzApplicationGroup interface","IAzApplicationGroup interface [Security]","DeleteMemberName method","IAzApplicationGroup.DeleteMemberName","IAzApplicationGroup::DeleteMemberName","azroles/IAzApplicationGroup::DeleteMemberName","security.iazapplicationgroup_deletemembername"]
old-location: security\iazapplicationgroup_deletemembername.htm
tech.root: security
ms.assetid: 3b3a8aee-b1ef-464a-9b67-80b703d41d69
ms.date: 03/20/2023
ms.keywords: AzApplicationGroup object [Security],DeleteMemberName method, DeleteMemberName, DeleteMemberName method [Security], DeleteMemberName method [Security],AzApplicationGroup object, DeleteMemberName method [Security],IAzApplicationGroup interface, IAzApplicationGroup interface [Security],DeleteMemberName method, IAzApplicationGroup.DeleteMemberName, IAzApplicationGroup::DeleteMemberName, azroles/IAzApplicationGroup::DeleteMemberName, security.iazapplicationgroup_deletemembername
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
 - IAzApplicationGroup::DeleteMemberName
 - azroles/IAzApplicationGroup::DeleteMemberName
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
 - IAzApplicationGroup.DeleteMemberName
 - AzApplicationGroup.DeleteMemberName
---

# IAzApplicationGroup::DeleteMemberName

## -description

The **DeleteMemberName** method removes  the specified account name from the list of accounts that belong to the application group.

## -parameters

### -param bstrProp [in]

String that contains the account name to remove from the list of accounts that belong to the application group. The account name must be in user principal name (UPN) format (for example, `someone@example.com`). The [LookupAccountName](/windows/win32/api/winbase/nf-winbase-lookupaccountnamea) function is called to retrieve the domain.

### -param varReserved [in, optional]

Reserved for future use.

## -returns

If the method succeeds, it will return `S_OK`. Any other **HRESULT** value indicates that the operation failed.

## -remarks

To view the list of account names of  accounts that belong to this application group, use the [MembersName](nf-azroles-iazapplicationgroup-get_membersname.md) property.

## -see-also

[MembersName](nf-azroles-iazapplicationgroup-get_membersname.md)

[LookupAccountName](/windows/win32/api/winbase/nf-winbase-lookupaccountnamea)
