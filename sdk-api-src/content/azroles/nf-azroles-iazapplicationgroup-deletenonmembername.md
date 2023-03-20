---
UID: NF:azroles.IAzApplicationGroup.DeleteNonMemberName
title: IAzApplicationGroup::DeleteNonMemberName (azroles.h)
description: Removes the specified account name from the list of accounts that are refused membership in the application group.
helpviewer_keywords: ["AzApplicationGroup object [Security]","DeleteNonMemberName method","DeleteNonMemberName","DeleteNonMemberName method [Security]","DeleteNonMemberName method [Security]","AzApplicationGroup object","DeleteNonMemberName method [Security]","IAzApplicationGroup interface","IAzApplicationGroup interface [Security]","DeleteNonMemberName method","IAzApplicationGroup.DeleteNonMemberName","IAzApplicationGroup::DeleteNonMemberName","azroles/IAzApplicationGroup::DeleteNonMemberName","security.iazapplicationgroup_deletenonmembername"]
old-location: security\iazapplicationgroup_deletenonmembername.htm
tech.root: security
ms.assetid: 8011e55a-1e62-45a6-a91c-07a488384d84
ms.date: 03/20/2023
ms.keywords: AzApplicationGroup object [Security],DeleteNonMemberName method, DeleteNonMemberName, DeleteNonMemberName method [Security], DeleteNonMemberName method [Security],AzApplicationGroup object, DeleteNonMemberName method [Security],IAzApplicationGroup interface, IAzApplicationGroup interface [Security],DeleteNonMemberName method, IAzApplicationGroup.DeleteNonMemberName, IAzApplicationGroup::DeleteNonMemberName, azroles/IAzApplicationGroup::DeleteNonMemberName, security.iazapplicationgroup_deletenonmembername
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
 - IAzApplicationGroup::DeleteNonMemberName
 - azroles/IAzApplicationGroup::DeleteNonMemberName
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
 - IAzApplicationGroup.DeleteNonMemberName
 - AzApplicationGroup.DeleteNonMemberName
---

# IAzApplicationGroup::DeleteNonMemberName

## -description

The **DeleteNonMemberName** method removes the specified account name from the list of accounts that are refused membership in the application group.

## -parameters

### -param bstrProp [in]

String that contains the account name to remove from the list of accounts that are refused membership in the application group. The account name must be in user principal name (UPN) format (for example, `someone@example.com`). The [LookupAccountName](/windows/win32/api/winbase/nf-winbase-lookupaccountnamea) function is called to retrieve the domain.

### -param varReserved [in, optional]

Reserved for future use.

## -returns

If the method succeeds, it will return `S_OK`. Any other **HRESULT** value indicates that the operation failed.

## -remarks

To view the list of account names of accounts that are refused membership in this application group, use the [NonMembersName](nf-azroles-iazapplicationgroup-get_nonmembersname.md) property.

## -see-also

[LookupAccountName](/windows/win32/api/winbase/nf-winbase-lookupaccountnamea)

[NonMembersName](nf-azroles-iazapplicationgroup-get_nonmembersname.md)
