---
UID: NF:azroles.IAzAuthorizationStore.get_PolicyAdministrators
title: IAzAuthorizationStore::get_PolicyAdministrators (azroles.h)
description: Retrieves the security identifiers (SIDs) of principals that act as policy administrators in text form.
helpviewer_keywords: ["AzAuthorizationStore object [Security]","PolicyAdministrators property","IAzAuthorizationStore interface [Security]","PolicyAdministrators property","IAzAuthorizationStore.PolicyAdministrators","IAzAuthorizationStore.get_PolicyAdministrators","IAzAuthorizationStore::PolicyAdministrators","IAzAuthorizationStore::get_PolicyAdministrators","PolicyAdministrators property [Security]","PolicyAdministrators property [Security]","AzAuthorizationStore object","PolicyAdministrators property [Security]","IAzAuthorizationStore interface","azroles/IAzAuthorizationStore::PolicyAdministrators","azroles/IAzAuthorizationStore::get_PolicyAdministrators","get_PolicyAdministrators","security.azauthorizationstore_policyadministrators"]
old-location: security\azauthorizationstore_policyadministrators.htm
tech.root: security
ms.assetid: 388d4970-5de4-4216-8c26-b9b24cc82ca3
ms.date: 12/05/2018
ms.keywords: AzAuthorizationStore object [Security],PolicyAdministrators property, IAzAuthorizationStore interface [Security],PolicyAdministrators property, IAzAuthorizationStore.PolicyAdministrators, IAzAuthorizationStore.get_PolicyAdministrators, IAzAuthorizationStore::PolicyAdministrators, IAzAuthorizationStore::get_PolicyAdministrators, PolicyAdministrators property [Security], PolicyAdministrators property [Security],AzAuthorizationStore object, PolicyAdministrators property [Security],IAzAuthorizationStore interface, azroles/IAzAuthorizationStore::PolicyAdministrators, azroles/IAzAuthorizationStore::get_PolicyAdministrators, get_PolicyAdministrators, security.azauthorizationstore_policyadministrators
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
 - IAzAuthorizationStore::get_PolicyAdministrators
 - azroles/IAzAuthorizationStore::get_PolicyAdministrators
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
 - IAzAuthorizationStore.PolicyAdministrators
 - IAzAuthorizationStore.get_PolicyAdministrators
 - AzAuthorizationStore.PolicyAdministrators
---

# IAzAuthorizationStore::get_PolicyAdministrators


## -description

The <b>PolicyAdministrators</b> property retrieves the <a href="/windows/desktop/SecGloss/s-gly">security identifiers</a> (SIDs) of principals that act as policy administrators in text form.

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
In  JScript, the returned <a href="/windows/desktop/api/oaidl/ns-oaidl-safearray">SAFEARRAY</a> must be converted to the JScript <a href="/scripting/javascript/reference/array-object-javascript">Array</a> object.