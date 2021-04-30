---
UID: NF:azroles.IAzApplicationGroup.get_Members
title: IAzApplicationGroup::get_Members (azroles.h)
description: Retrieves the security identifiers (SIDs), in text form, of accounts that belong to the application group.
helpviewer_keywords: ["AzApplicationGroup object [Security]","Members property","IAzApplicationGroup interface [Security]","Members property","IAzApplicationGroup.Members","IAzApplicationGroup.get_Members","IAzApplicationGroup::Members","IAzApplicationGroup::get_Members","Members property [Security]","Members property [Security]","AzApplicationGroup object","Members property [Security]","IAzApplicationGroup interface","azroles/IAzApplicationGroup::Members","azroles/IAzApplicationGroup::get_Members","get_Members","security.iazapplicationgroup_members"]
old-location: security\iazapplicationgroup_members.htm
tech.root: security
ms.assetid: 1370fe81-a729-477e-a500-1823abb713e1
ms.date: 12/05/2018
ms.keywords: AzApplicationGroup object [Security],Members property, IAzApplicationGroup interface [Security],Members property, IAzApplicationGroup.Members, IAzApplicationGroup.get_Members, IAzApplicationGroup::Members, IAzApplicationGroup::get_Members, Members property [Security], Members property [Security],AzApplicationGroup object, Members property [Security],IAzApplicationGroup interface, azroles/IAzApplicationGroup::Members, azroles/IAzApplicationGroup::get_Members, get_Members, security.iazapplicationgroup_members
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
 - IAzApplicationGroup::get_Members
 - azroles/IAzApplicationGroup::get_Members
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
 - IAzApplicationGroup.Members
 - IAzApplicationGroup.get_Members
 - AzApplicationGroup.Members
---

# IAzApplicationGroup::get_Members


## -description

The <b>Members</b> property retrieves the <a href="/windows/desktop/SecGloss/s-gly">security identifiers</a> (SIDs), in text form, of accounts that belong to the application group.

This property is read-only.

## -parameters

## -remarks

This property is ignored unless the <a href="/windows/desktop/api/azroles/nf-azroles-iazapplicationgroup-get_type">Type</a> property is AZ_GROUPTYPE_BASIC.

In JScript, the returned <a href="/windows/desktop/api/oaidl/ns-oaidl-safearray">SAFEARRAY</a> must be converted to the JScript <a href="/scripting/javascript/reference/array-object-javascript">Array</a> object.