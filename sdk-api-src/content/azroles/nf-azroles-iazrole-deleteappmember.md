---
UID: NF:azroles.IAzRole.DeleteAppMember
title: IAzRole::DeleteAppMember (azroles.h)
description: Removes the specified IAzApplicationGroup object from the list of application groups that belong to the role.
helpviewer_keywords: ["AzRole object [Security]","DeleteAppMember method","DeleteAppMember","DeleteAppMember method [Security]","DeleteAppMember method [Security]","AzRole object","DeleteAppMember method [Security]","IAzRole interface","IAzRole interface [Security]","DeleteAppMember method","IAzRole.DeleteAppMember","IAzRole::DeleteAppMember","azroles/IAzRole::DeleteAppMember","security.iazrole_deleteappmember"]
old-location: security\iazrole_deleteappmember.htm
tech.root: security
ms.assetid: b2856d75-cf16-4eec-a0e1-2e9e9fff601e
ms.date: 12/05/2018
ms.keywords: AzRole object [Security],DeleteAppMember method, DeleteAppMember, DeleteAppMember method [Security], DeleteAppMember method [Security],AzRole object, DeleteAppMember method [Security],IAzRole interface, IAzRole interface [Security],DeleteAppMember method, IAzRole.DeleteAppMember, IAzRole::DeleteAppMember, azroles/IAzRole::DeleteAppMember, security.iazrole_deleteappmember
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
 - IAzRole::DeleteAppMember
 - azroles/IAzRole::DeleteAppMember
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
 - IAzRole.DeleteAppMember
 - AzRole.DeleteAppMember
---

# IAzRole::DeleteAppMember


## -description

The <b>DeleteAppMember</b> method removes the specified <a href="/windows/desktop/api/azroles/nn-azroles-iazapplicationgroup">IAzApplicationGroup</a> object from the list of application groups that belong to the role.

## -parameters

### -param bstrProp [in]

String that contains the <a href="/windows/desktop/api/azroles/nf-azroles-iazapplicationgroup-get_name">Name</a> property of the <a href="/windows/desktop/api/azroles/nn-azroles-iazapplicationgroup">IAzApplicationGroup</a> object to remove from the list of  application groups that belong to the role.

### -param varReserved [in, optional]

Reserved for future use.

## -remarks

To view the list of application groups that belong to the role, use the <a href="/windows/desktop/api/azroles/nf-azroles-iazrole-get_appmembers">AppMembers</a> property.