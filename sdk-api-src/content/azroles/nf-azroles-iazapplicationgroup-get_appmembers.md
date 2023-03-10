---
UID: NF:azroles.IAzApplicationGroup.get_AppMembers
title: IAzApplicationGroup::get_AppMembers (azroles.h)
description: Retrieves the application groups that belong to this application group.
helpviewer_keywords: ["AppMembers property [Security]","AppMembers property [Security]","AzApplicationGroup object","AppMembers property [Security]","IAzApplicationGroup interface","AzApplicationGroup object [Security]","AppMembers property","IAzApplicationGroup interface [Security]","AppMembers property","IAzApplicationGroup.AppMembers","IAzApplicationGroup.get_AppMembers","IAzApplicationGroup::AppMembers","IAzApplicationGroup::get_AppMembers","azroles/IAzApplicationGroup::AppMembers","azroles/IAzApplicationGroup::get_AppMembers","get_AppMembers","security.iazapplicationgroup_appmembers"]
old-location: security\iazapplicationgroup_appmembers.htm
tech.root: security
ms.assetid: 74239ac2-b6ea-4839-b4c5-7a77d454aa0b
ms.date: 12/05/2018
ms.keywords: AppMembers property [Security], AppMembers property [Security],AzApplicationGroup object, AppMembers property [Security],IAzApplicationGroup interface, AzApplicationGroup object [Security],AppMembers property, IAzApplicationGroup interface [Security],AppMembers property, IAzApplicationGroup.AppMembers, IAzApplicationGroup.get_AppMembers, IAzApplicationGroup::AppMembers, IAzApplicationGroup::get_AppMembers, azroles/IAzApplicationGroup::AppMembers, azroles/IAzApplicationGroup::get_AppMembers, get_AppMembers, security.iazapplicationgroup_appmembers
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
 - IAzApplicationGroup::get_AppMembers
 - azroles/IAzApplicationGroup::get_AppMembers
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
 - IAzApplicationGroup.AppMembers
 - IAzApplicationGroup.get_AppMembers
 - AzApplicationGroup.AppMembers
---

# IAzApplicationGroup::get_AppMembers


## -description

The <b>AppMembers</b> property retrieves the application groups that belong to this application group.

This property is read-only.

## -parameters

## -remarks

This property allows the nesting of <a href="/windows/desktop/api/azroles/nn-azroles-iazapplicationgroup">IAzApplicationGroup</a> objects within another <b>IAzApplicationGroup</b> object.

In JScript, the returned <a href="/windows/desktop/api/oaidl/ns-oaidl-safearray">SAFEARRAY</a> must be converted to the JScript <a href="/scripting/javascript/reference/array-object-javascript">Array</a> object.