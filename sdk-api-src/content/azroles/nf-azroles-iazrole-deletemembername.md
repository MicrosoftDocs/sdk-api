---
UID: NF:azroles.IAzRole.DeleteMemberName
title: IAzRole::DeleteMemberName (azroles.h)
description: Removes the specified account name from the list of accounts that belong to the role.helpviewer_keywords: ["AzRole object [Security]","DeleteMemberName method","DeleteMemberName","DeleteMemberName method [Security]","DeleteMemberName method [Security]","AzRole object","DeleteMemberName method [Security]","IAzRole interface","IAzRole interface [Security]","DeleteMemberName method","IAzRole.DeleteMemberName","IAzRole::DeleteMemberName","azroles/IAzRole::DeleteMemberName","security.iazrole_deletemembername"]
old-location: security\iazrole_deletemembername.htm
tech.root: SecAuthZ
ms.assetid: 3ca3e242-deab-46e7-b3f5-d6a75e5a2c08
ms.date: 12/05/2018
ms.keywords: AzRole object [Security],DeleteMemberName method, DeleteMemberName, DeleteMemberName method [Security], DeleteMemberName method [Security],AzRole object, DeleteMemberName method [Security],IAzRole interface, IAzRole interface [Security],DeleteMemberName method, IAzRole.DeleteMemberName, IAzRole::DeleteMemberName, azroles/IAzRole::DeleteMemberName, security.iazrole_deletemembername
f1_keywords:
- azroles/IAzRole.DeleteMemberName
dev_langs:
- c++
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
targetos: Windows
req.typenames: 
req.redist: Windows Server 2003 Administration Tools Pack on Windows XP
ms.custom: 19H1
---

# IAzRole::DeleteMemberName


## -description


The <b>DeleteMemberName</b> method removes  the specified account name from the list of  accounts that belong to the role.


## -parameters




### -param bstrProp [in]

String that contains the account name to remove from the list of  accounts that belong to the role. The account name can be in either user principal name (UPN) format (for example, "someone@example.com") or in the "ExampleDomain\UserName" format. If the domain is not  in the "ExampleDomain\UserName" format, the <a href="https://docs.microsoft.com/windows/desktop/api/winbase/nf-winbase-lookupaccountnamea">LookupAccountName</a> function is called to retrieve the domain.


### -param varReserved [in, optional]

Reserved for future use.


## -remarks



To view the list of account names of accounts that belong to the role, use the <a href="https://docs.microsoft.com/windows/desktop/api/azroles/nf-azroles-iazrole-get_membersname">MembersName</a> property.



