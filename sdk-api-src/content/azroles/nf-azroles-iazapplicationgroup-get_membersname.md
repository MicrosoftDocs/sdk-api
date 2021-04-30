---
UID: NF:azroles.IAzApplicationGroup.get_MembersName
title: IAzApplicationGroup::get_MembersName (azroles.h)
description: Retrieves the account names of accounts that belong to the application group.
helpviewer_keywords: ["AzApplicationGroup object [Security]","MembersName property","IAzApplicationGroup interface [Security]","MembersName property","IAzApplicationGroup.MembersName","IAzApplicationGroup.get_MembersName","IAzApplicationGroup::MembersName","IAzApplicationGroup::get_MembersName","MembersName property [Security]","MembersName property [Security]","AzApplicationGroup object","MembersName property [Security]","IAzApplicationGroup interface","azroles/IAzApplicationGroup::MembersName","azroles/IAzApplicationGroup::get_MembersName","get_MembersName","security.iazapplicationgroup_membersname"]
old-location: security\iazapplicationgroup_membersname.htm
tech.root: security
ms.assetid: bdd6f88f-ea06-4075-b563-d0c7707107f8
ms.date: 12/05/2018
ms.keywords: AzApplicationGroup object [Security],MembersName property, IAzApplicationGroup interface [Security],MembersName property, IAzApplicationGroup.MembersName, IAzApplicationGroup.get_MembersName, IAzApplicationGroup::MembersName, IAzApplicationGroup::get_MembersName, MembersName property [Security], MembersName property [Security],AzApplicationGroup object, MembersName property [Security],IAzApplicationGroup interface, azroles/IAzApplicationGroup::MembersName, azroles/IAzApplicationGroup::get_MembersName, get_MembersName, security.iazapplicationgroup_membersname
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
 - IAzApplicationGroup::get_MembersName
 - azroles/IAzApplicationGroup::get_MembersName
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
 - IAzApplicationGroup.MembersName
 - IAzApplicationGroup.get_MembersName
 - AzApplicationGroup.MembersName
---

# IAzApplicationGroup::get_MembersName


## -description

The <b>MembersName</b> property retrieves the account names of  accounts that belong to the application group.

This property is read-only.

## -parameters

## -remarks

This property is ignored unless the <a href="/windows/desktop/api/azroles/nf-azroles-iazapplicationgroup-get_type">Type</a> property is AZ_GROUPTYPE_BASIC.

In JScript, the returned <a href="/windows/desktop/api/oaidl/ns-oaidl-safearray">SAFEARRAY</a> must be converted to the JScript <a href="/scripting/javascript/reference/array-object-javascript">Array</a> object.