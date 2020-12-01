---
UID: NF:azroles.IAzApplicationGroup.DeleteAppMember
title: IAzApplicationGroup::DeleteAppMember (azroles.h)
description: Removes the specified IAzApplicationGroup object from the list of application groups that belong to this application group.
helpviewer_keywords: ["AzApplicationGroup object [Security]","DeleteAppMember method","DeleteAppMember","DeleteAppMember method [Security]","DeleteAppMember method [Security]","AzApplicationGroup object","DeleteAppMember method [Security]","IAzApplicationGroup interface","IAzApplicationGroup interface [Security]","DeleteAppMember method","IAzApplicationGroup.DeleteAppMember","IAzApplicationGroup::DeleteAppMember","azroles/IAzApplicationGroup::DeleteAppMember","security.iazapplicationgroup_deleteappmember"]
old-location: security\iazapplicationgroup_deleteappmember.htm
tech.root: security
ms.assetid: 856d9b18-927a-462a-b238-78b704bcc58b
ms.date: 12/05/2018
ms.keywords: AzApplicationGroup object [Security],DeleteAppMember method, DeleteAppMember, DeleteAppMember method [Security], DeleteAppMember method [Security],AzApplicationGroup object, DeleteAppMember method [Security],IAzApplicationGroup interface, IAzApplicationGroup interface [Security],DeleteAppMember method, IAzApplicationGroup.DeleteAppMember, IAzApplicationGroup::DeleteAppMember, azroles/IAzApplicationGroup::DeleteAppMember, security.iazapplicationgroup_deleteappmember
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
 - IAzApplicationGroup::DeleteAppMember
 - azroles/IAzApplicationGroup::DeleteAppMember
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
 - IAzApplicationGroup.DeleteAppMember
 - AzApplicationGroup.DeleteAppMember
---

# IAzApplicationGroup::DeleteAppMember


## -description

The <b>DeleteAppMember</b> method removes the specified <a href="/windows/desktop/api/azroles/nn-azroles-iazapplicationgroup">IAzApplicationGroup</a> object from the list of application groups that belong to this application group.

## -parameters

### -param bstrProp [in]

String that contains the <a href="/windows/desktop/api/azroles/nf-azroles-iazapplicationgroup-get_name">Name</a> property of the <a href="/windows/desktop/api/azroles/nn-azroles-iazapplicationgroup">IAzApplicationGroup</a> object to remove from the list of  application groups that belong to this application group.

### -param varReserved [in, optional]

Reserved for future use.

## -remarks

To view the list of application groups that belong to this application group, use the <a href="/windows/desktop/api/azroles/nf-azroles-iazapplicationgroup-get_appmembers">AppMembers</a> property.