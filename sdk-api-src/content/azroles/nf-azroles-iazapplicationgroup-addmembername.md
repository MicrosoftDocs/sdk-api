---
UID: NF:azroles.IAzApplicationGroup.AddMemberName
title: IAzApplicationGroup::AddMemberName (azroles.h)
description: Adds the specified account name to the list of accounts that belong to the application group.helpviewer_keywords: ["AddMemberName","AddMemberName method [Security]","AddMemberName method [Security]","AzApplicationGroup object","AddMemberName method [Security]","IAzApplicationGroup interface","AzApplicationGroup object [Security]","AddMemberName method","IAzApplicationGroup interface [Security]","AddMemberName method","IAzApplicationGroup.AddMemberName","IAzApplicationGroup::AddMemberName","azroles/IAzApplicationGroup::AddMemberName","security.iazapplicationgroup_addmembername"]
old-location: security\iazapplicationgroup_addmembername.htm
tech.root: SecAuthZ
ms.assetid: 148be96b-be8d-4ad7-a5ad-f22599114cfa
ms.date: 12/05/2018
ms.keywords: AddMemberName, AddMemberName method [Security], AddMemberName method [Security],AzApplicationGroup object, AddMemberName method [Security],IAzApplicationGroup interface, AzApplicationGroup object [Security],AddMemberName method, IAzApplicationGroup interface [Security],AddMemberName method, IAzApplicationGroup.AddMemberName, IAzApplicationGroup::AddMemberName, azroles/IAzApplicationGroup::AddMemberName, security.iazapplicationgroup_addmembername
f1_keywords:
- azroles/IAzApplicationGroup.AddMemberName
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
- IAzApplicationGroup.AddMemberName
- AzApplicationGroup.AddMemberName
targetos: Windows
req.typenames: 
req.redist: Windows Server 2003 Administration Tools Pack on Windows XP
ms.custom: 19H1
---

# IAzApplicationGroup::AddMemberName


## -description


The <b>AddMemberName</b> method adds the specified account name to the list of  accounts that belong to the application group.


## -parameters




### -param bstrProp [in]

String that contains the account name to add to the list of accounts that belong to the application group. The account name must be in user principal name (UPN) format. The <a href="https://docs.microsoft.com/windows/desktop/api/winbase/nf-winbase-lookupaccountnamea">LookupAccountName</a> function is called to retrieve the domain.


### -param varReserved [in, optional]

Reserved for future use.


## -remarks



To view the list of account names of  accounts that belong to this application group, use the <a href="https://docs.microsoft.com/windows/desktop/api/azroles/nf-azroles-iazapplicationgroup-get_membersname">MembersName</a> property.

You must call the <a href="https://docs.microsoft.com/windows/desktop/api/azroles/nf-azroles-iazapplicationgroup-submit">Submit</a> method to persist any changes made by this method.



