---
UID: NF:azroles.IAzApplication.get_PolicyAdministrators
title: IAzApplication::get_PolicyAdministrators (azroles.h)
description: Retrieves the security identifiers (SIDs), in text form, of principals that act as policy administrators.
helpviewer_keywords: ["AzApplication object [Security]","PolicyAdministrators property","IAzApplication interface [Security]","PolicyAdministrators property","IAzApplication.PolicyAdministrators","IAzApplication.get_PolicyAdministrators","IAzApplication::PolicyAdministrators","IAzApplication::get_PolicyAdministrators","PolicyAdministrators property [Security]","PolicyAdministrators property [Security]","AzApplication object","PolicyAdministrators property [Security]","IAzApplication interface","azroles/IAzApplication::PolicyAdministrators","azroles/IAzApplication::get_PolicyAdministrators","get_PolicyAdministrators","security.iazapplication_policyadministrators"]
old-location: security\iazapplication_policyadministrators.htm
tech.root: security
ms.assetid: a0b66213-3dc7-4886-9c93-0d27d43a7d92
ms.date: 12/05/2018
ms.keywords: AzApplication object [Security],PolicyAdministrators property, IAzApplication interface [Security],PolicyAdministrators property, IAzApplication.PolicyAdministrators, IAzApplication.get_PolicyAdministrators, IAzApplication::PolicyAdministrators, IAzApplication::get_PolicyAdministrators, PolicyAdministrators property [Security], PolicyAdministrators property [Security],AzApplication object, PolicyAdministrators property [Security],IAzApplication interface, azroles/IAzApplication::PolicyAdministrators, azroles/IAzApplication::get_PolicyAdministrators, get_PolicyAdministrators, security.iazapplication_policyadministrators
f1_keywords:
- azroles/IAzApplication.PolicyAdministrators
dev_langs:
- c++
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
- IAzApplication.PolicyAdministrators
- IAzApplication.get_PolicyAdministrators
- AzApplication.PolicyAdministrators
targetos: Windows
req.typenames: 
req.redist: Windows Server 2003 Administration Tools Pack on Windows XP
ms.custom: 19H1
---

# IAzApplication::get_PolicyAdministrators


## -description


The <b>PolicyAdministrators</b> property retrieves the <a href="https://docs.microsoft.com/windows/desktop/SecGloss/s-gly">security identifiers</a> (SIDs), in text form, of principals that act as policy administrators.

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
In JScript, the returned <a href="https://docs.microsoft.com/windows/desktop/api/oaidl/ns-oaidl-safearray">SAFEARRAY</a> must be converted to the JScript <a href="https://docs.microsoft.com/scripting/javascript/reference/array-object-javascript">Array</a> object. 



