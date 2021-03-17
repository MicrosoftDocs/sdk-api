---
UID: NF:azroles.IAzRole.DeleteMember
title: IAzRole::DeleteMember (azroles.h)
description: Removes the specified security identifier (SID) in text form from the list of Windows accounts that belong to the role.
helpviewer_keywords: ["AzRole object [Security]","DeleteMember method","DeleteMember","DeleteMember method [Security]","DeleteMember method [Security]","AzRole object","DeleteMember method [Security]","IAzRole interface","IAzRole interface [Security]","DeleteMember method","IAzRole.DeleteMember","IAzRole::DeleteMember","azroles/IAzRole::DeleteMember","security.iazrole_deletemember"]
old-location: security\iazrole_deletemember.htm
tech.root: security
ms.assetid: 676f0469-f57f-4f3f-8295-b9c99eb13de8
ms.date: 12/05/2018
ms.keywords: AzRole object [Security],DeleteMember method, DeleteMember, DeleteMember method [Security], DeleteMember method [Security],AzRole object, DeleteMember method [Security],IAzRole interface, IAzRole interface [Security],DeleteMember method, IAzRole.DeleteMember, IAzRole::DeleteMember, azroles/IAzRole::DeleteMember, security.iazrole_deletemember
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
 - IAzRole::DeleteMember
 - azroles/IAzRole::DeleteMember
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
 - IAzRole.DeleteMember
 - AzRole.DeleteMember
---

# IAzRole::DeleteMember


## -description

The <b>DeleteMember</b> method removes  the specified <a href="/windows/desktop/SecGloss/s-gly">security identifier</a> (SID) in text form from the list of Windows  accounts that belong to the role.

## -parameters

### -param bstrProp [in]

String that contains the text form of the SID to remove from the list of Windows  accounts that belong to the role.

### -param varReserved [in, optional]

Reserved for future use.

## -remarks

To view the list of SIDs of Windows accounts that belong to the role in text form, use the <a href="/windows/desktop/api/azroles/nf-azroles-iazrole-get_members">Members</a> property.