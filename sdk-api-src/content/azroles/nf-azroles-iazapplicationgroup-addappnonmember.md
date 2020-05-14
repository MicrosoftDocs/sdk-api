---
UID: NF:azroles.IAzApplicationGroup.AddAppNonMember
title: IAzApplicationGroup::AddAppNonMember (azroles.h)
description: Adds the specified IAzApplicationGroup object to the list of application groups that are refused membership in this application group.helpviewer_keywords: ["AddAppNonMember","AddAppNonMember method [Security]","AddAppNonMember method [Security]","AzApplicationGroup object","AddAppNonMember method [Security]","IAzApplicationGroup interface","AzApplicationGroup object [Security]","AddAppNonMember method","IAzApplicationGroup interface [Security]","AddAppNonMember method","IAzApplicationGroup.AddAppNonMember","IAzApplicationGroup::AddAppNonMember","azroles/IAzApplicationGroup::AddAppNonMember","security.iazapplicationgroup_addappnonmember"]
old-location: security\iazapplicationgroup_addappnonmember.htm
tech.root: SecAuthZ
ms.assetid: 31b8538f-afe1-4fd3-bf6f-6f3f0641fc2a
ms.date: 12/05/2018
ms.keywords: AddAppNonMember, AddAppNonMember method [Security], AddAppNonMember method [Security],AzApplicationGroup object, AddAppNonMember method [Security],IAzApplicationGroup interface, AzApplicationGroup object [Security],AddAppNonMember method, IAzApplicationGroup interface [Security],AddAppNonMember method, IAzApplicationGroup.AddAppNonMember, IAzApplicationGroup::AddAppNonMember, azroles/IAzApplicationGroup::AddAppNonMember, security.iazapplicationgroup_addappnonmember
f1_keywords:
- azroles/IAzApplicationGroup.AddAppNonMember
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
- IAzApplicationGroup.AddAppNonMember
- AzApplicationGroup.AddAppNonMember
targetos: Windows
req.typenames: 
req.redist: Windows Server 2003 Administration Tools Pack on Windows XP
ms.custom: 19H1
---

# IAzApplicationGroup::AddAppNonMember


## -description


The <b>AddAppNonMember</b> method adds the specified <a href="https://docs.microsoft.com/windows/desktop/api/azroles/nn-azroles-iazapplicationgroup">IAzApplicationGroup</a> object to the list of application groups that are refused membership in this application group.


## -parameters




### -param bstrProp [in]

String that contains the <a href="https://docs.microsoft.com/windows/desktop/api/azroles/nf-azroles-iazapplicationgroup-get_name">Name</a> property of the <a href="https://docs.microsoft.com/windows/desktop/api/azroles/nn-azroles-iazapplicationgroup">IAzApplicationGroup</a> object to add to the list of the application groups that are refused membership in this application group.


### -param varReserved [in, optional]

Reserved for future use.


## -remarks



To view the list of application groups that are refused membership in this application group, use the <a href="https://docs.microsoft.com/windows/desktop/api/azroles/nf-azroles-iazapplicationgroup-get_appnonmembers">AppNonMembers</a> property.

Denying membership to an account in an application group does not prevent that account from being assigned to a role through a different application group, nor from being granted permission to a resource through assignment to any other role.

You must call the <a href="https://docs.microsoft.com/windows/desktop/api/azroles/nf-azroles-iazapplicationgroup-submit">Submit</a> method to persist any changes made by this method.



