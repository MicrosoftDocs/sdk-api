---
UID: NF:azroles.IAzScope.get_PolicyReadersName
title: IAzScope::get_PolicyReadersName (azroles.h)
description: Retrieves the account names of principals that act as policy readers. (IAzScope.get_PolicyReadersName)
helpviewer_keywords: ["AzScope object [Security]","PolicyReadersName property","IAzScope interface [Security]","PolicyReadersName property","IAzScope.PolicyReadersName","IAzScope.get_PolicyReadersName","IAzScope::PolicyReadersName","IAzScope::get_PolicyReadersName","PolicyReadersName property [Security]","PolicyReadersName property [Security]","AzScope object","PolicyReadersName property [Security]","IAzScope interface","azroles/IAzScope::PolicyReadersName","azroles/IAzScope::get_PolicyReadersName","get_PolicyReadersName","security.iazscope_policyreadersname"]
old-location: security\iazscope_policyreadersname.htm
tech.root: security
ms.assetid: 4f56ee3f-f987-4569-9e19-c13ab3ff100a
ms.date: 12/05/2018
ms.keywords: AzScope object [Security],PolicyReadersName property, IAzScope interface [Security],PolicyReadersName property, IAzScope.PolicyReadersName, IAzScope.get_PolicyReadersName, IAzScope::PolicyReadersName, IAzScope::get_PolicyReadersName, PolicyReadersName property [Security], PolicyReadersName property [Security],AzScope object, PolicyReadersName property [Security],IAzScope interface, azroles/IAzScope::PolicyReadersName, azroles/IAzScope::get_PolicyReadersName, get_PolicyReadersName, security.iazscope_policyreadersname
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
 - IAzScope::get_PolicyReadersName
 - azroles/IAzScope::get_PolicyReadersName
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
 - IAzScope.PolicyReadersName
 - IAzScope.get_PolicyReadersName
 - AzScope.PolicyReadersName
---

# IAzScope::get_PolicyReadersName


## -description

The <b>PolicyReadersName</b> property retrieves the account names of principals that act as policy readers.

This property is read-only.

## -parameters

## -remarks

Policy readers for an object can read attributes for the object and for child objects of the object. Readers can also  use the policy; for example, readers can call the <a href="/windows/desktop/api/azroles/nf-azroles-iazclientcontext-accesscheck">AccessCheck</a> method. Readers cannot modify the object or its child objects.

In JScript, the returned <a href="/windows/desktop/api/oaidl/ns-oaidl-safearray">SAFEARRAY</a> must be converted to the JScript <a href="/scripting/javascript/reference/array-object-javascript">Array</a> object.
