---
UID: NF:azroles.IAzApplicationGroup.DeleteNonMember
title: IAzApplicationGroup::DeleteNonMember (azroles.h)
description: Removes the specified security identifier (SID) in text form from the list of accounts that are refused membership in the application group.
helpviewer_keywords: ["AzApplicationGroup object [Security]","DeleteNonMember method","DeleteNonMember","DeleteNonMember method [Security]","DeleteNonMember method [Security]","AzApplicationGroup object","DeleteNonMember method [Security]","IAzApplicationGroup interface","IAzApplicationGroup interface [Security]","DeleteNonMember method","IAzApplicationGroup.DeleteNonMember","IAzApplicationGroup::DeleteNonMember","azroles/IAzApplicationGroup::DeleteNonMember","security.iazapplicationgroup_deletenonmember"]
old-location: security\iazapplicationgroup_deletenonmember.htm
tech.root: security
ms.assetid: 05d58f62-fa34-4829-a535-65ea0f5144ab
ms.date: 12/05/2018
ms.keywords: AzApplicationGroup object [Security],DeleteNonMember method, DeleteNonMember, DeleteNonMember method [Security], DeleteNonMember method [Security],AzApplicationGroup object, DeleteNonMember method [Security],IAzApplicationGroup interface, IAzApplicationGroup interface [Security],DeleteNonMember method, IAzApplicationGroup.DeleteNonMember, IAzApplicationGroup::DeleteNonMember, azroles/IAzApplicationGroup::DeleteNonMember, security.iazapplicationgroup_deletenonmember
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
 - IAzApplicationGroup::DeleteNonMember
 - azroles/IAzApplicationGroup::DeleteNonMember
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
 - IAzApplicationGroup.DeleteNonMember
 - AzApplicationGroup.DeleteNonMember
---

# IAzApplicationGroup::DeleteNonMember


## -description

The <b>DeleteNonMember</b> method removes the specified <a href="/windows/desktop/SecGloss/s-gly">security identifier</a> (SID) in text form from the list of  accounts that are refused membership in the application group.

## -parameters

### -param bstrProp [in]

String that contains the text form of the SID to remove from the list of  accounts that are refused membership in the application group.

### -param varReserved [in, optional]

Reserved for future use.

## -remarks

To view the list of SIDs of accounts that are refused membership in this application group in text form, use the <a href="/windows/desktop/api/azroles/nf-azroles-iazapplicationgroup-get_nonmembers">NonMembers</a> property.