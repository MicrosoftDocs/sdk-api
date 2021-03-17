---
UID: NF:azroles.IAzRole.get_MembersName
title: IAzRole::get_MembersName (azroles.h)
description: Retrieves the account names of accounts that belong to the role.
helpviewer_keywords: ["AzRole object [Security]","MembersName property","IAzRole interface [Security]","MembersName property","IAzRole.MembersName","IAzRole.get_MembersName","IAzRole::MembersName","IAzRole::get_MembersName","MembersName property [Security]","MembersName property [Security]","AzRole object","MembersName property [Security]","IAzRole interface","azroles/IAzRole::MembersName","azroles/IAzRole::get_MembersName","get_MembersName","security.iazrole_membersname"]
old-location: security\iazrole_membersname.htm
tech.root: security
ms.assetid: defaefa8-2d76-49c6-bd1c-8b386f9dc5f1
ms.date: 12/05/2018
ms.keywords: AzRole object [Security],MembersName property, IAzRole interface [Security],MembersName property, IAzRole.MembersName, IAzRole.get_MembersName, IAzRole::MembersName, IAzRole::get_MembersName, MembersName property [Security], MembersName property [Security],AzRole object, MembersName property [Security],IAzRole interface, azroles/IAzRole::MembersName, azroles/IAzRole::get_MembersName, get_MembersName, security.iazrole_membersname
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
 - IAzRole::get_MembersName
 - azroles/IAzRole::get_MembersName
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
 - IAzRole.MembersName
 - IAzRole.get_MembersName
 - AzRole.MembersName
---

# IAzRole::get_MembersName


## -description

The <b>MembersName</b> property retrieves the account names of  accounts that belong to the role.

This property is read-only.

## -parameters

## -remarks

In JScript, the returned <a href="/windows/desktop/api/oaidl/ns-oaidl-safearray">SAFEARRAY</a> must be converted to the JScript <a href="/scripting/javascript/reference/array-object-javascript">Array</a> object.