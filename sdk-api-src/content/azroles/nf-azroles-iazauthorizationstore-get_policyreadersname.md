---
UID: NF:azroles.IAzAuthorizationStore.get_PolicyReadersName
title: IAzAuthorizationStore::get_PolicyReadersName (azroles.h)
description: Retrieves the account names of principals that act as policy readers. (IAzAuthorizationStore.get_PolicyReadersName)
helpviewer_keywords: ["AzAuthorizationStore object [Security]","PolicyReadersName property","IAzAuthorizationStore interface [Security]","PolicyReadersName property","IAzAuthorizationStore.PolicyReadersName","IAzAuthorizationStore.get_PolicyReadersName","IAzAuthorizationStore::PolicyReadersName","IAzAuthorizationStore::get_PolicyReadersName","PolicyReadersName property [Security]","PolicyReadersName property [Security]","AzAuthorizationStore object","PolicyReadersName property [Security]","IAzAuthorizationStore interface","azroles/IAzAuthorizationStore::PolicyReadersName","azroles/IAzAuthorizationStore::get_PolicyReadersName","get_PolicyReadersName","security.azauthorizationstore_policyreadersname"]
old-location: security\azauthorizationstore_policyreadersname.htm
tech.root: security
ms.assetid: d550448e-a1ea-45f3-9151-affd4b8c0b14
ms.date: 12/05/2018
ms.keywords: AzAuthorizationStore object [Security],PolicyReadersName property, IAzAuthorizationStore interface [Security],PolicyReadersName property, IAzAuthorizationStore.PolicyReadersName, IAzAuthorizationStore.get_PolicyReadersName, IAzAuthorizationStore::PolicyReadersName, IAzAuthorizationStore::get_PolicyReadersName, PolicyReadersName property [Security], PolicyReadersName property [Security],AzAuthorizationStore object, PolicyReadersName property [Security],IAzAuthorizationStore interface, azroles/IAzAuthorizationStore::PolicyReadersName, azroles/IAzAuthorizationStore::get_PolicyReadersName, get_PolicyReadersName, security.azauthorizationstore_policyreadersname
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
 - IAzAuthorizationStore::get_PolicyReadersName
 - azroles/IAzAuthorizationStore::get_PolicyReadersName
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
 - IAzAuthorizationStore.PolicyReadersName
 - IAzAuthorizationStore.get_PolicyReadersName
 - AzAuthorizationStore.PolicyReadersName
---

# IAzAuthorizationStore::get_PolicyReadersName


## -description

The <b>PolicyReadersName</b> property retrieves the account names of principals that act as policy readers.

This property is read-only.

## -parameters

## -remarks

Policy readers for an object can read attributes for the object and for child objects of the object. Readers can also  use the policy; for example, readers can call the <a href="/windows/desktop/api/azroles/nf-azroles-iazclientcontext-accesscheck">AccessCheck</a> method. Readers cannot modify the object or its child objects.

In  JScript, the returned <a href="/windows/desktop/api/oaidl/ns-oaidl-safearray">SAFEARRAY</a> must be converted to the JScript <a href="/scripting/javascript/reference/array-object-javascript">Array</a> object.
