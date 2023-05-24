---
UID: NF:azroles.IAzRole.AddMember
title: IAzRole::AddMember (azroles.h)
description: Adds the specified security identifier (SID) in text form to the list of Windows accounts that belong to the role.
helpviewer_keywords: ["AddMember","AddMember method [Security]","AddMember method [Security]","AzRole object","AddMember method [Security]","IAzRole interface","AzRole object [Security]","AddMember method","IAzRole interface [Security]","AddMember method","IAzRole.AddMember","IAzRole::AddMember","azroles/IAzRole::AddMember","security.iazrole_addmember"]
old-location: security\iazrole_addmember.htm
tech.root: security
ms.assetid: b2be62cb-7256-4031-8af9-24f3043a8430
ms.date: 03/20/2023
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

The **AddMember** method adds the specified [security identifier](/windows/win32/SecGloss/s-gly) (SID) in text form to the list of Windows accounts that belong to the role.

## -parameters

### -param bstrProp [in]

String that contains the text form of the SID to add to the list of Windows accounts that belong to the role.

### -param varReserved [in, optional]

Reserved for future use.

## -returns

If the method succeeds, it will return `S_OK`. Any other **HRESULT** value indicates that the operation failed.

## -remarks

To view the list of SIDs of Windows accounts that belong to this role in text form, use the [Members](nf-azroles-iazrole-get_members.md) property.

You must call the [Submit](nf-azroles-iazrole-submit.md) method to persist any changes made by this method.

## -see-also

[Members](nf-azroles-iazrole-get_members.md)

[Submit](nf-azroles-iazrole-submit.md)
