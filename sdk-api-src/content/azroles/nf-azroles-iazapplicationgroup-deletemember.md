---
UID: NF:azroles.IAzApplicationGroup.DeleteMember
title: IAzApplicationGroup::DeleteMember (azroles.h)
description: Removes the specified security identifier (SID) in text form from the list of accounts that belong to the application group.
helpviewer_keywords: ["AzApplicationGroup object [Security]","DeleteMember method","DeleteMember","DeleteMember method [Security]","DeleteMember method [Security]","AzApplicationGroup object","DeleteMember method [Security]","IAzApplicationGroup interface","IAzApplicationGroup interface [Security]","DeleteMember method","IAzApplicationGroup.DeleteMember","IAzApplicationGroup::DeleteMember","azroles/IAzApplicationGroup::DeleteMember","security.iazapplicationgroup_deletemember"]
old-location: security\iazapplicationgroup_deletemember.htm
tech.root: security
ms.assetid: 9db3b162-b37d-4a86-a3c0-cb594370238b
ms.date: 03/20/2023
ms.keywords: AzApplicationGroup object [Security],DeleteMember method, DeleteMember, DeleteMember method [Security], DeleteMember method [Security],AzApplicationGroup object, DeleteMember method [Security],IAzApplicationGroup interface, IAzApplicationGroup interface [Security],DeleteMember method, IAzApplicationGroup.DeleteMember, IAzApplicationGroup::DeleteMember, azroles/IAzApplicationGroup::DeleteMember, security.iazapplicationgroup_deletemember
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
 - IAzApplicationGroup::DeleteMember
 - azroles/IAzApplicationGroup::DeleteMember
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
 - IAzApplicationGroup.DeleteMember
 - AzApplicationGroup.DeleteMember
---

# IAzApplicationGroup::DeleteMember

## -description

The **DeleteMember** method removes  the specified [security identifier](/windows/win32/SecGloss/s-gly) (SID) in text form from the list of accounts that belong to the application group.

## -parameters

### -param bstrProp [in]

String that contains the text form of the SID to remove from the list of accounts that belong to the application group.

### -param varReserved [in, optional]

Reserved for future use.

## -returns

If the method succeeds, it will return `S_OK`. Any other **HRESULT** value indicates that the operation failed.

## -remarks

To view the list of SIDs of accounts that belong to this application group in text form, use the [Members](nf-azroles-iazapplicationgroup-get_members.md) property.

## -see-also

[Members](nf-azroles-iazapplicationgroup-get_members.md)
