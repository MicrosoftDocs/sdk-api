---
UID: NF:azroles.IAzRole.get_Members
title: IAzRole::get_Members (azroles.h)
description: Retrieves the security identifiers (SIDs), in text form, of Windows accounts that belong to the role.
helpviewer_keywords: ["AzRole object [Security]","Members property","IAzRole interface [Security]","Members property","IAzRole.Members","IAzRole.get_Members","IAzRole::Members","IAzRole::get_Members","Members property [Security]","Members property [Security]","AzRole object","Members property [Security]","IAzRole interface","azroles/IAzRole::Members","azroles/IAzRole::get_Members","get_Members","security.iazrole_members"]
old-location: security\iazrole_members.htm
tech.root: security
ms.assetid: 03391842-fc8a-4dc2-878e-4fe1c41cc4dd
ms.date: 12/05/2018
ms.keywords: AzRole object [Security],Members property, IAzRole interface [Security],Members property, IAzRole.Members, IAzRole.get_Members, IAzRole::Members, IAzRole::get_Members, Members property [Security], Members property [Security],AzRole object, Members property [Security],IAzRole interface, azroles/IAzRole::Members, azroles/IAzRole::get_Members, get_Members, security.iazrole_members
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
 - IAzRole::get_Members
 - azroles/IAzRole::get_Members
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
 - IAzRole.Members
 - IAzRole.get_Members
 - AzRole.Members
---

# IAzRole::get_Members


## -description

The <b>Members</b> property retrieves the <a href="/windows/desktop/SecGloss/s-gly">security identifiers</a> (SIDs), in text form, of Windows  accounts that belong to the role.

This property is read-only.

## -parameters

## -remarks

In  JScript, the returned <a href="/windows/desktop/api/oaidl/ns-oaidl-safearray">SAFEARRAY</a> must be converted to the JScript <a href="/scripting/javascript/reference/array-object-javascript">Array</a> object.