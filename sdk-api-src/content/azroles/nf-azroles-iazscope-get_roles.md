---
UID: NF:azroles.IAzScope.get_Roles
title: IAzScope::get_Roles (azroles.h)
description: Retrieves an IAzRoles object that is used to enumerate IAzRole objects from the policy data.
helpviewer_keywords: ["AzScope object [Security]","Roles property","IAzScope interface [Security]","Roles property","IAzScope.Roles","IAzScope.get_Roles","IAzScope::Roles","IAzScope::get_Roles","Roles property [Security]","Roles property [Security]","AzScope object","Roles property [Security]","IAzScope interface","azroles/IAzScope::Roles","azroles/IAzScope::get_Roles","get_Roles","security.iazscope_roles"]
old-location: security\iazscope_roles.htm
tech.root: security
ms.assetid: 4dcf0e1b-d824-4675-b2d1-f59a58adb00a
ms.date: 12/05/2018
ms.keywords: AzScope object [Security],Roles property, IAzScope interface [Security],Roles property, IAzScope.Roles, IAzScope.get_Roles, IAzScope::Roles, IAzScope::get_Roles, Roles property [Security], Roles property [Security],AzScope object, Roles property [Security],IAzScope interface, azroles/IAzScope::Roles, azroles/IAzScope::get_Roles, get_Roles, security.iazscope_roles
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
 - IAzScope::get_Roles
 - azroles/IAzScope::get_Roles
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
 - IAzScope.Roles
 - IAzScope.get_Roles
 - AzScope.Roles
---

# IAzScope::get_Roles


## -description

The <b>Roles</b> property retrieves an <a href="/windows/desktop/api/azroles/nn-azroles-iazroles">IAzRoles</a> object that is used to enumerate <a href="/windows/desktop/api/azroles/nn-azroles-iazrole">IAzRole</a> objects from the policy data.

This property is read-only.

## -parameters

## -remarks

This property can be used only to enumerate <a href="/windows/desktop/api/azroles/nn-azroles-iazrole">IAzRole</a> objects that are direct child objects of the <a href="/windows/desktop/api/azroles/nn-azroles-iazscope">IAzScope</a> object.