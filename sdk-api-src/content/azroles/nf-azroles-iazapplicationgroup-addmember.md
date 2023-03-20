---
UID: NF:azroles.IAzApplicationGroup.AddMember
title: IAzApplicationGroup::AddMember (azroles.h)
description: Adds the specified security identifier (SID) in text form to the list of accounts that belong to the application group.
helpviewer_keywords: ["AddMember","AddMember method [Security]","AddMember method [Security]","AzApplicationGroup object","AddMember method [Security]","IAzApplicationGroup interface","AzApplicationGroup object [Security]","AddMember method","IAzApplicationGroup interface [Security]","AddMember method","IAzApplicationGroup.AddMember","IAzApplicationGroup::AddMember","azroles/IAzApplicationGroup::AddMember","security.iazapplicationgroup_addmember"]
old-location: security\iazapplicationgroup_addmember.htm
tech.root: security
ms.assetid: 934ca397-2067-451a-bccd-103ab4db3b1f
ms.date: 03/20/2023
ms.keywords: AddMember, AddMember method [Security], AddMember method [Security],AzApplicationGroup object, AddMember method [Security],IAzApplicationGroup interface, AzApplicationGroup object [Security],AddMember method, IAzApplicationGroup interface [Security],AddMember method, IAzApplicationGroup.AddMember, IAzApplicationGroup::AddMember, azroles/IAzApplicationGroup::AddMember, security.iazapplicationgroup_addmember
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
 - IAzApplicationGroup::AddMember
 - azroles/IAzApplicationGroup::AddMember
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
 - IAzApplicationGroup.AddMember
 - AzApplicationGroup.AddMember
---

# IAzApplicationGroup::AddMember

## -description

The **AddMember** method adds the specified [security identifier](/windows/win32/SecGloss/s-gly) (SID) in text form to the list of accounts that belong to the application group.

## -parameters

### -param bstrProp [in]

String that contains the text form of the SID to add to the list of accounts that belong to the application group.

### -param varReserved [in, optional]

Reserved for future use.

## -returns

If the method succeeds, it will return `S_OK`. Any other **HRESULT** value indicates that the operation failed.

## -remarks

To view the list of SIDs of accounts that belong to this application group in text form, use the [Members](nf-azroles-iazapplicationgroup-get_members.md) property.

You must call the [Submit](nf-azroles-iazapplicationgroup-submit.md) method to persist any changes made by this method.

## -see-also

[Members](nf-azroles-iazapplicationgroup-get_members.md)

[Submit](nf-azroles-iazapplicationgroup-submit.md)
