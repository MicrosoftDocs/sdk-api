---
UID: NF:azroles.IAzApplicationGroup.AddNonMemberName
title: IAzApplicationGroup::AddNonMemberName (azroles.h)
description: Adds the specified account name to the list of accounts that are refused membership in the application group.
helpviewer_keywords: ["AddNonMemberName","AddNonMemberName method [Security]","AddNonMemberName method [Security]","AzApplicationGroup object","AddNonMemberName method [Security]","IAzApplicationGroup interface","AzApplicationGroup object [Security]","AddNonMemberName method","IAzApplicationGroup interface [Security]","AddNonMemberName method","IAzApplicationGroup.AddNonMemberName","IAzApplicationGroup::AddNonMemberName","azroles/IAzApplicationGroup::AddNonMemberName","security.iazapplicationgroup_addnonmembername"]
old-location: security\iazapplicationgroup_addnonmembername.htm
tech.root: security
ms.assetid: 56bde3d9-f4f7-449d-a080-5215dda940a0
ms.date: 12/05/2018
ms.keywords: AddNonMemberName, AddNonMemberName method [Security], AddNonMemberName method [Security],AzApplicationGroup object, AddNonMemberName method [Security],IAzApplicationGroup interface, AzApplicationGroup object [Security],AddNonMemberName method, IAzApplicationGroup interface [Security],AddNonMemberName method, IAzApplicationGroup.AddNonMemberName, IAzApplicationGroup::AddNonMemberName, azroles/IAzApplicationGroup::AddNonMemberName, security.iazapplicationgroup_addnonmembername
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
 - IAzApplicationGroup::AddNonMemberName
 - azroles/IAzApplicationGroup::AddNonMemberName
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
 - IAzApplicationGroup.AddNonMemberName
 - AzApplicationGroup.AddNonMemberName
---

# IAzApplicationGroup::AddNonMemberName


## -description

The <b>AddNonMemberName</b> method adds the specified account name to the list of  accounts that are refused membership in the application group.

## -parameters

### -param bstrProp [in]

String that contains the SID to add to the list of accounts that are refused membership in the application group. The account name must be in user principal name (UPN) format (for example, "someone@example.com"). The <a href="/windows/desktop/api/winbase/nf-winbase-lookupaccountnamea">LookupAccountName</a> function is called to retrieve the domain.

### -param varReserved [in, optional]

Reserved for future use.

## -remarks

The application group will never have an  account added using this method as a member, even if that account is specified directly or indirectly by the <a href="/windows/desktop/api/azroles/nf-azroles-iazapplicationgroup-get_members">Members</a> property.

Denying membership to an account in an application group does not prevent that account from being assigned to a role through a different application group, nor from being granted permission to a resource through assignment to any other role.

To view the list of account names of  accounts that are refused membership in this application group, use the <a href="/windows/desktop/api/azroles/nf-azroles-iazapplicationgroup-get_nonmembersname">NonMembersName</a> property.

You must call the <a href="/windows/desktop/api/azroles/nf-azroles-iazapplicationgroup-submit">Submit</a> method to persist any changes made by this method.