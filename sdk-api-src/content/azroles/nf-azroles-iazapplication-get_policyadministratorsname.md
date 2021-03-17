---
UID: NF:azroles.IAzApplication.get_PolicyAdministratorsName
title: IAzApplication::get_PolicyAdministratorsName (azroles.h)
description: The IAzApplication::PolicyAdministratorsName property retrieves the account names of principals that act as policy administrators.
helpviewer_keywords: ["AzApplication object [Security]","PolicyAdministratorsName property","IAzApplication interface [Security]","PolicyAdministratorsName property","IAzApplication.PolicyAdministratorsName","IAzApplication.get_PolicyAdministratorsName","IAzApplication::PolicyAdministratorsName","IAzApplication::get_PolicyAdministratorsName","PolicyAdministratorsName property [Security]","PolicyAdministratorsName property [Security]","AzApplication object","PolicyAdministratorsName property [Security]","IAzApplication interface","azroles/IAzApplication::PolicyAdministratorsName","azroles/IAzApplication::get_PolicyAdministratorsName","get_PolicyAdministratorsName","security.iazapplication_policyadministratorsname"]
old-location: security\iazapplication_policyadministratorsname.htm
tech.root: security
ms.assetid: fdabb04b-deb4-494a-bdde-264a301388b3
ms.date: 12/05/2018
ms.keywords: AzApplication object [Security],PolicyAdministratorsName property, IAzApplication interface [Security],PolicyAdministratorsName property, IAzApplication.PolicyAdministratorsName, IAzApplication.get_PolicyAdministratorsName, IAzApplication::PolicyAdministratorsName, IAzApplication::get_PolicyAdministratorsName, PolicyAdministratorsName property [Security], PolicyAdministratorsName property [Security],AzApplication object, PolicyAdministratorsName property [Security],IAzApplication interface, azroles/IAzApplication::PolicyAdministratorsName, azroles/IAzApplication::get_PolicyAdministratorsName, get_PolicyAdministratorsName, security.iazapplication_policyadministratorsname
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
 - IAzApplication::get_PolicyAdministratorsName
 - azroles/IAzApplication::get_PolicyAdministratorsName
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
 - IAzApplication.PolicyAdministratorsName
 - IAzApplication.get_PolicyAdministratorsName
 - AzApplication.PolicyAdministratorsName
---

# IAzApplication::get_PolicyAdministratorsName


## -description

The <b>PolicyAdministratorsName</b> property retrieves the account names of principals that act as policy administrators.

This property is read-only.

## -parameters

## -remarks

Policy administrators for an object can perform the following tasks:

<ul>
<li>Read the object</li>
<li>Write attributes to the object</li>
<li>Read attributes of child objects of the object</li>
<li>Write attributes to child objects of the object</li>
<li>Delete the object</li>
<li>Delete child objects of the object</li>
<li>Create child objects of the object</li>
</ul>
In JScript, the returned <a href="/windows/desktop/api/oaidl/ns-oaidl-safearray">SAFEARRAY</a> must be converted to the JScript <a href="/scripting/javascript/reference/array-object-javascript">Array</a> object.