---
UID: NF:azroles.IAzApplicationGroup.AddAppMember
title: IAzApplicationGroup::AddAppMember (azroles.h)
description: Adds the specified IAzApplicationGroup object to the list of application groups that belong to this application group.
helpviewer_keywords: ["AddAppMember","AddAppMember method [Security]","AddAppMember method [Security]","AzApplicationGroup object","AddAppMember method [Security]","IAzApplicationGroup interface","AzApplicationGroup object [Security]","AddAppMember method","IAzApplicationGroup interface [Security]","AddAppMember method","IAzApplicationGroup.AddAppMember","IAzApplicationGroup::AddAppMember","azroles/IAzApplicationGroup::AddAppMember","security.iazapplicationgroup_addappmember"]
old-location: security\iazapplicationgroup_addappmember.htm
tech.root: security
ms.assetid: 35b6c928-0c11-420d-8ba7-f28b0c67f55d
ms.date: 12/05/2018
ms.keywords: AddAppMember, AddAppMember method [Security], AddAppMember method [Security],AzApplicationGroup object, AddAppMember method [Security],IAzApplicationGroup interface, AzApplicationGroup object [Security],AddAppMember method, IAzApplicationGroup interface [Security],AddAppMember method, IAzApplicationGroup.AddAppMember, IAzApplicationGroup::AddAppMember, azroles/IAzApplicationGroup::AddAppMember, security.iazapplicationgroup_addappmember
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
 - IAzApplicationGroup::AddAppMember
 - azroles/IAzApplicationGroup::AddAppMember
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
 - IAzApplicationGroup.AddAppMember
 - AzApplicationGroup.AddAppMember
---

# IAzApplicationGroup::AddAppMember


## -description

The <b>AddAppMember</b> method adds the specified <a href="/windows/desktop/api/azroles/nn-azroles-iazapplicationgroup">IAzApplicationGroup</a> object to the list of application groups that belong to this application group.

## -parameters

### -param bstrProp [in]

String that contains the <a href="/windows/desktop/api/azroles/nf-azroles-iazapplicationgroup-get_name">Name</a> property of the <a href="/windows/desktop/api/azroles/nn-azroles-iazapplicationgroup">IAzApplicationGroup</a> object to add to the list of the application groups that belong to this application group.

### -param varReserved [in, optional]

Reserved for future use.

## -remarks

To view the list of application groups that belong to this application group, use the <a href="/windows/desktop/api/azroles/nf-azroles-iazapplicationgroup-get_appmembers">AppMembers</a> property.

You must call the <a href="/windows/desktop/api/azroles/nf-azroles-iazapplicationgroup-submit">Submit</a> method to persist any changes made by this method.