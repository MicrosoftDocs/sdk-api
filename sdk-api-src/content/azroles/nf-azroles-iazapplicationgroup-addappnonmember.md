---
UID: NF:azroles.IAzApplicationGroup.AddAppNonMember
title: IAzApplicationGroup::AddAppNonMember (azroles.h)
description: Adds the specified IAzApplicationGroup object to the list of application groups that are refused membership in this application group.
helpviewer_keywords: ["AddAppNonMember","AddAppNonMember method [Security]","AddAppNonMember method [Security]","AzApplicationGroup object","AddAppNonMember method [Security]","IAzApplicationGroup interface","AzApplicationGroup object [Security]","AddAppNonMember method","IAzApplicationGroup interface [Security]","AddAppNonMember method","IAzApplicationGroup.AddAppNonMember","IAzApplicationGroup::AddAppNonMember","azroles/IAzApplicationGroup::AddAppNonMember","security.iazapplicationgroup_addappnonmember"]
old-location: security\iazapplicationgroup_addappnonmember.htm
tech.root: security
ms.assetid: 31b8538f-afe1-4fd3-bf6f-6f3f0641fc2a
ms.date: 03/20/2023
ms.keywords: AddAppNonMember, AddAppNonMember method [Security], AddAppNonMember method [Security],AzApplicationGroup object, AddAppNonMember method [Security],IAzApplicationGroup interface, AzApplicationGroup object [Security],AddAppNonMember method, IAzApplicationGroup interface [Security],AddAppNonMember method, IAzApplicationGroup.AddAppNonMember, IAzApplicationGroup::AddAppNonMember, azroles/IAzApplicationGroup::AddAppNonMember, security.iazapplicationgroup_addappnonmember
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
 - IAzApplicationGroup::AddAppNonMember
 - azroles/IAzApplicationGroup::AddAppNonMember
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
 - IAzApplicationGroup.AddAppNonMember
 - AzApplicationGroup.AddAppNonMember
---

# IAzApplicationGroup::AddAppNonMember

## -description

The **AddAppNonMember** method adds the specified [IAzApplicationGroup](nn-azroles-iazapplicationgroup.md) object to the list of application groups that are refused membership in this application group.

## -parameters

### -param bstrProp [in]

String that contains the [Name](nf-azroles-iazapplicationgroup-get_name.md) property of the [IAzApplicationGroup](nn-azroles-iazapplicationgroup.md) object to add to the list of the application groups that are refused membership in this application group.

### -param varReserved [in, optional]

Reserved for future use.

## -returns

If the method succeeds, it will return `S_OK`. Any other **HRESULT** value indicates that the operation failed.

## -remarks

To view the list of application groups that are refused membership in this application group, use the [AppNonMembers](nf-azroles-iazapplicationgroup-get_appnonmembers.md) property.

Denying membership to an account in an application group does not prevent that account from being assigned to a role through a different application group, nor from being granted permission to a resource through assignment to any other role.

You must call the [Submit](nf-azroles-iazapplicationgroup-submit.md) method to persist any changes made by this method.

## -see-also

[IAzApplicationGroup](nn-azroles-iazapplicationgroup.md)
