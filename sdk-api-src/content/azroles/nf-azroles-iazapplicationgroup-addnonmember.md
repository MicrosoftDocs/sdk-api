---
UID: NF:azroles.IAzApplicationGroup.AddNonMember
title: IAzApplicationGroup::AddNonMember (azroles.h)
description: Adds the specified security identifier (SID) in text form to the list of accounts that are refused membership in the application group.
helpviewer_keywords: ["AddNonMember","AddNonMember method [Security]","AddNonMember method [Security]","AzApplicationGroup object","AddNonMember method [Security]","IAzApplicationGroup interface","AzApplicationGroup object [Security]","AddNonMember method","IAzApplicationGroup interface [Security]","AddNonMember method","IAzApplicationGroup.AddNonMember","IAzApplicationGroup::AddNonMember","azroles/IAzApplicationGroup::AddNonMember","security.iazapplicationgroup_addnonmember"]
old-location: security\iazapplicationgroup_addnonmember.htm
tech.root: security
ms.assetid: a61f0b97-cd8a-40e5-b2ef-8eb48359fead
ms.date: 03/20/2023
ms.keywords: AddNonMember, AddNonMember method [Security], AddNonMember method [Security],AzApplicationGroup object, AddNonMember method [Security],IAzApplicationGroup interface, AzApplicationGroup object [Security],AddNonMember method, IAzApplicationGroup interface [Security],AddNonMember method, IAzApplicationGroup.AddNonMember, IAzApplicationGroup::AddNonMember, azroles/IAzApplicationGroup::AddNonMember, security.iazapplicationgroup_addnonmember
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
 - IAzApplicationGroup::AddNonMember
 - azroles/IAzApplicationGroup::AddNonMember
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
 - IAzApplicationGroup.AddNonMember
 - AzApplicationGroup.AddNonMember
---

# IAzApplicationGroup::AddNonMember

## -description

The **AddNonMember** method adds the specified [security identifier](/windows/win32/SecGloss/s-gly) (SID) in text form to the list of accounts that are refused membership in the application group.

## -parameters

### -param bstrProp [in]

String that contains the text form of the SID to add to the list of accounts that are refused membership in the application group.

### -param varReserved [in, optional]

Reserved for future use.

## -returns

If the method succeeds, it will return `S_OK`. Any other **HRESULT** value indicates that the operation failed.

## -remarks

The application group will never have an  account added using this method as a member, even if that account is specified directly or indirectly by the [Members](nf-azroles-iazapplicationgroup-get_members.md) property.

Denying membership to an account in an application group does not prevent that account from being assigned to a role through a different application group, nor from being granted permission to a resource through assignment to any other role.

To view the list of SIDs of accounts that are refused membership in this application group in text form, use the [NonMembers](nf-azroles-iazapplicationgroup-get_nonmembers.md) property.

You must call the [Submit](nf-azroles-iazapplicationgroup-submit.md) method to persist any changes made by this method.

## -see-also

[Members](nf-azroles-iazapplicationgroup-get_members.md)

[NonMembers](nf-azroles-iazapplicationgroup-get_nonmembers.md)

[Submit](nf-azroles-iazapplicationgroup-submit.md)
