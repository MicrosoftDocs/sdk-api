---
UID: NF:azroles.IAzApplicationGroup.get_NonMembersName
title: IAzApplicationGroup::get_NonMembersName (azroles.h)
description: Retrieves the account names of accounts that are refused membership in the application group.
helpviewer_keywords: ["AzApplicationGroup object [Security]","NonMembersName property","IAzApplicationGroup interface [Security]","NonMembersName property","IAzApplicationGroup.NonMembersName","IAzApplicationGroup.get_NonMembersName","IAzApplicationGroup::NonMembersName","IAzApplicationGroup::get_NonMembersName","NonMembersName property [Security]","NonMembersName property [Security]","AzApplicationGroup object","NonMembersName property [Security]","IAzApplicationGroup interface","azroles/IAzApplicationGroup::NonMembersName","azroles/IAzApplicationGroup::get_NonMembersName","get_NonMembersName","security.iazapplicationgroup_nonmembersname"]
old-location: security\iazapplicationgroup_nonmembersname.htm
tech.root: security
ms.assetid: d78556ae-0d22-4df0-b850-dd7077fa3f85
ms.date: 12/05/2018
ms.keywords: AzApplicationGroup object [Security],NonMembersName property, IAzApplicationGroup interface [Security],NonMembersName property, IAzApplicationGroup.NonMembersName, IAzApplicationGroup.get_NonMembersName, IAzApplicationGroup::NonMembersName, IAzApplicationGroup::get_NonMembersName, NonMembersName property [Security], NonMembersName property [Security],AzApplicationGroup object, NonMembersName property [Security],IAzApplicationGroup interface, azroles/IAzApplicationGroup::NonMembersName, azroles/IAzApplicationGroup::get_NonMembersName, get_NonMembersName, security.iazapplicationgroup_nonmembersname
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
 - IAzApplicationGroup::get_NonMembersName
 - azroles/IAzApplicationGroup::get_NonMembersName
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
 - IAzApplicationGroup.NonMembersName
 - IAzApplicationGroup.get_NonMembersName
 - AzApplicationGroup.NonMembersName
---

# IAzApplicationGroup::get_NonMembersName


## -description

The <b>NonMembersName</b> property retrieves the account names of  accounts that are refused membership in  the application group.

This property is read-only.

## -parameters

## -remarks

The application group will never have an  account specified by this property as a member, even if that account is specified directly or indirectly by the <a href="/windows/desktop/api/azroles/nf-azroles-iazapplicationgroup-get_members">Members</a> property.

Denying membership to an account in an application group does not prevent that account from being assigned to a role through a different application group, nor from being granted permission to a resource through assignment to any other role.

This property is ignored unless the <a href="/windows/desktop/api/azroles/nf-azroles-iazapplicationgroup-get_type">Type</a> property is AZ_GROUPTYPE_BASIC.

In JScript, the returned <a href="/windows/desktop/api/oaidl/ns-oaidl-safearray">SAFEARRAY</a> must be converted to the JScript <a href="/scripting/javascript/reference/array-object-javascript">Array</a> object.