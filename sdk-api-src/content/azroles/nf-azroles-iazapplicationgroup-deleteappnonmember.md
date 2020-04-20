---
UID: NF:azroles.IAzApplicationGroup.DeleteAppNonMember
title: IAzApplicationGroup::DeleteAppNonMember (azroles.h)
description: Removes the specified IAzApplicationGroup object from the list of application groups that are refused membership in this application group.helpviewer_keywords: ["AzApplicationGroup object [Security]","DeleteAppNonMember method","DeleteAppNonMember","DeleteAppNonMember method [Security]","DeleteAppNonMember method [Security]","AzApplicationGroup object","DeleteAppNonMember method [Security]","IAzApplicationGroup interface","IAzApplicationGroup interface [Security]","DeleteAppNonMember method","IAzApplicationGroup.DeleteAppNonMember","IAzApplicationGroup::DeleteAppNonMember","azroles/IAzApplicationGroup::DeleteAppNonMember","security.iazapplicationgroup_deleteappnonmember"]
old-location: security\iazapplicationgroup_deleteappnonmember.htm
tech.root: SecAuthZ
ms.assetid: d78f3cd9-4ccb-47b7-98bd-5e69ebbb178c
ms.date: 12/05/2018
ms.keywords: AzApplicationGroup object [Security],DeleteAppNonMember method, DeleteAppNonMember, DeleteAppNonMember method [Security], DeleteAppNonMember method [Security],AzApplicationGroup object, DeleteAppNonMember method [Security],IAzApplicationGroup interface, IAzApplicationGroup interface [Security],DeleteAppNonMember method, IAzApplicationGroup.DeleteAppNonMember, IAzApplicationGroup::DeleteAppNonMember, azroles/IAzApplicationGroup::DeleteAppNonMember, security.iazapplicationgroup_deleteappnonmember
f1_keywords:
- azroles/IAzApplicationGroup.DeleteAppNonMember
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
- IAzApplicationGroup.DeleteAppNonMember
- AzApplicationGroup.DeleteAppNonMember
targetos: Windows
req.typenames: 
req.redist: Windows Server 2003 Administration Tools Pack on Windows XP
ms.custom: 19H1
---

# IAzApplicationGroup::DeleteAppNonMember


## -description


The <b>DeleteAppNonMember</b> method removes the specified <a href="https://docs.microsoft.com/windows/desktop/api/azroles/nn-azroles-iazapplicationgroup">IAzApplicationGroup</a> object from the list of application groups that are refused membership in this application group.


## -parameters




### -param bstrProp [in]

String that contains the <a href="https://docs.microsoft.com/windows/desktop/api/azroles/nf-azroles-iazapplicationgroup-get_name">Name</a> property of the <a href="https://docs.microsoft.com/windows/desktop/api/azroles/nn-azroles-iazapplicationgroup">IAzApplicationGroup</a> object to remove from the list of the application groups that are refused membership in this application group.


### -param varReserved [in, optional]

Reserved for future use.


## -remarks



To view the list of application groups that are refused membership in this application group, use the <a href="https://docs.microsoft.com/windows/desktop/api/azroles/nf-azroles-iazapplicationgroup-get_appnonmembers">AppNonMembers</a> property.



