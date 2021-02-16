---
UID: NF:azroles.IAzApplication.get_Roles
title: IAzApplication::get_Roles (azroles.h)
description: The Roles property of IAzApplication retrieves an IAzRoles object that is used to enumerate IAzRole objects from the policy data.
helpviewer_keywords: ["AzApplication object [Security]","Roles property","IAzApplication interface [Security]","Roles property","IAzApplication.Roles","IAzApplication.get_Roles","IAzApplication::Roles","IAzApplication::get_Roles","Roles property [Security]","Roles property [Security]","AzApplication object","Roles property [Security]","IAzApplication interface","azroles/IAzApplication::Roles","azroles/IAzApplication::get_Roles","get_Roles","security.iazapplication_roles"]
old-location: security\iazapplication_roles.htm
tech.root: security
ms.assetid: 02acf473-b072-4814-92e1-47a32baae4fc
ms.date: 12/05/2018
ms.keywords: AzApplication object [Security],Roles property, IAzApplication interface [Security],Roles property, IAzApplication.Roles, IAzApplication.get_Roles, IAzApplication::Roles, IAzApplication::get_Roles, Roles property [Security], Roles property [Security],AzApplication object, Roles property [Security],IAzApplication interface, azroles/IAzApplication::Roles, azroles/IAzApplication::get_Roles, get_Roles, security.iazapplication_roles
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
 - IAzApplication::get_Roles
 - azroles/IAzApplication::get_Roles
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
 - IAzApplication.Roles
 - IAzApplication.get_Roles
 - AzApplication.Roles
---

# IAzApplication::get_Roles


## -description

The <b>Roles</b> property retrieves an <a href="/windows/desktop/api/azroles/nn-azroles-iazroles">IAzRoles</a> object that is used to enumerate <a href="/windows/desktop/api/azroles/nn-azroles-iazrole">IAzRole</a> objects from the policy data.

This property is read-only.

## -parameters

## -remarks

This property can be used only to enumerate <a href="/windows/desktop/api/azroles/nn-azroles-iazrole">IAzRole</a> objects that are direct child objects of the <a href="/windows/desktop/api/azroles/nn-azroles-iazapplication">IAzApplication</a> object.