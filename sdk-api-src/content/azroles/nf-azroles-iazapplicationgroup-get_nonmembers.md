---
UID: NF:azroles.IAzApplicationGroup.get_NonMembers
title: IAzApplicationGroup::get_NonMembers (azroles.h)
description: Retrieves the security identifiers (SIDs), in text form, of accounts that are refused membership in the application group.
helpviewer_keywords: ["AzApplicationGroup object [Security]","NonMembers property","IAzApplicationGroup interface [Security]","NonMembers property","IAzApplicationGroup.NonMembers","IAzApplicationGroup.get_NonMembers","IAzApplicationGroup::NonMembers","IAzApplicationGroup::get_NonMembers","NonMembers property [Security]","NonMembers property [Security]","AzApplicationGroup object","NonMembers property [Security]","IAzApplicationGroup interface","azroles/IAzApplicationGroup::NonMembers","azroles/IAzApplicationGroup::get_NonMembers","get_NonMembers","security.iazapplicationgroup_nonmembers"]
old-location: security\iazapplicationgroup_nonmembers.htm
tech.root: security
ms.assetid: 43bdd205-4750-4ff6-8063-8de2c5962b09
ms.date: 12/05/2018
ms.keywords: AzApplicationGroup object [Security],NonMembers property, IAzApplicationGroup interface [Security],NonMembers property, IAzApplicationGroup.NonMembers, IAzApplicationGroup.get_NonMembers, IAzApplicationGroup::NonMembers, IAzApplicationGroup::get_NonMembers, NonMembers property [Security], NonMembers property [Security],AzApplicationGroup object, NonMembers property [Security],IAzApplicationGroup interface, azroles/IAzApplicationGroup::NonMembers, azroles/IAzApplicationGroup::get_NonMembers, get_NonMembers, security.iazapplicationgroup_nonmembers
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
 - IAzApplicationGroup::get_NonMembers
 - azroles/IAzApplicationGroup::get_NonMembers
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
 - IAzApplicationGroup.NonMembers
 - IAzApplicationGroup.get_NonMembers
 - AzApplicationGroup.NonMembers
---

# IAzApplicationGroup::get_NonMembers


## -description

The <b>NonMembers</b> property retrieves the <a href="/windows/desktop/SecGloss/s-gly">security identifiers</a> (SIDs), in text form, of  accounts that are refused membership in  the application group.

This property is read-only.

## -parameters

## -remarks

The application group will never have an  account specified by this property as a member, even if that account is specified directly or indirectly by the <a href="/windows/desktop/api/azroles/nf-azroles-iazapplicationgroup-get_members">Members</a> property.

This property is ignored unless the <a href="/windows/desktop/api/azroles/nf-azroles-iazapplicationgroup-get_type">Type</a> property is AZ_GROUPTYPE_BASIC.

In JScript, the returned <a href="/windows/desktop/api/oaidl/ns-oaidl-safearray">SAFEARRAY</a> must be converted to the JScript <a href="/scripting/javascript/reference/array-object-javascript">Array</a> object.

Denying membership to an account in an application group does not prevent that account from being assigned to a role through a different application group, nor from being granted permission to a resource through assignment to any other role.