---
UID: NF:azroles.IAzApplicationGroup.get_AppNonMembers
title: IAzApplicationGroup::get_AppNonMembers (azroles.h)
author: windows-sdk-content
description: Retrieves the application groups that are refused membership in this application group.
old-location: security\iazapplicationgroup_appnonmembers.htm
tech.root: SecAuthZ
ms.assetid: a85a9004-f3f5-44ce-a0d7-fa450af74917
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: AppNonMembers property [Security], AppNonMembers property [Security],AzApplicationGroup object, AppNonMembers property [Security],IAzApplicationGroup interface, AzApplicationGroup object [Security],AppNonMembers property, IAzApplicationGroup interface [Security],AppNonMembers property, IAzApplicationGroup.AppNonMembers, IAzApplicationGroup.get_AppNonMembers, IAzApplicationGroup::AppNonMembers, IAzApplicationGroup::get_AppNonMembers, azroles/IAzApplicationGroup::AppNonMembers, azroles/IAzApplicationGroup::get_AppNonMembers, get_AppNonMembers, security.iazapplicationgroup_appnonmembers
ms.topic: method
f1_keywords: 
 - "azroles/IAzApplicationGroup.AppNonMembers"
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Azroles.dll
api_name:
 - IAzApplicationGroup.AppNonMembers
 - IAzApplicationGroup.get_AppNonMembers
 - AzApplicationGroup.AppNonMembers
product: Windows
targetos: Windows
req.typenames: 
req.redist: Windows Server 2003 Administration Tools Pack on Windows XP
ms.custom: 19H1
---

# IAzApplicationGroup::get_AppNonMembers


## -description


The <b>AppNonMembers</b> property retrieves the application groups that are refused membership in this application group.

This property is read-only.


## -parameters


## -remarks



Denying membership to an account in an application group does not prevent that account from being assigned to a role through a different application group, nor from being granted permission to a resource through assignment to any other role.

In JScript, the returned <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/ns-oaidl-tagsafearray">SAFEARRAY</a> must be converted to the JScript <a href="https://docs.microsoft.com/scripting/javascript/reference/array-object-javascript">Array</a> object. 



