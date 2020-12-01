---
UID: NF:azroles.IAzRole.AddMember
title: IAzRole::AddMember (azroles.h)
description: Adds the specified security identifier (SID) in text form to the list of Windows accounts that belong to the role.
helpviewer_keywords: ["AddMember","AddMember method [Security]","AddMember method [Security]","AzRole object","AddMember method [Security]","IAzRole interface","AzRole object [Security]","AddMember method","IAzRole interface [Security]","AddMember method","IAzRole.AddMember","IAzRole::AddMember","azroles/IAzRole::AddMember","security.iazrole_addmember"]
old-location: security\iazrole_addmember.htm
tech.root: security
ms.assetid: b2be62cb-7256-4031-8af9-24f3043a8430
ms.date: 12/05/2018
ms.keywords: AddMember, AddMember method [Security], AddMember method [Security],AzRole object, AddMember method [Security],IAzRole interface, AzRole object [Security],AddMember method, IAzRole interface [Security],AddMember method, IAzRole.AddMember, IAzRole::AddMember, azroles/IAzRole::AddMember, security.iazrole_addmember
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
 - IAzRole::AddMember
 - azroles/IAzRole::AddMember
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
 - IAzRole.AddMember
 - AzRole.AddMember
---

# IAzRole::AddMember


## -description

The <b>AddMember</b> method adds the specified <a href="/windows/desktop/SecGloss/s-gly">security identifier</a> (SID) in text form to the list of Windows  accounts that belong to the role.

## -parameters

### -param bstrProp [in]

String that contains the text form of the SID to add to the list of Windows  accounts that belong to the role.

### -param varReserved [in, optional]

Reserved for future use.

## -remarks

To view the list of SIDs of Windows accounts that belong to this role in text form, use the <a href="/windows/desktop/api/azroles/nf-azroles-iazrole-get_members">Members</a> property.

You must call the <a href="/windows/desktop/api/azroles/nf-azroles-iazrole-submit">Submit</a> method to persist any changes made by this method.