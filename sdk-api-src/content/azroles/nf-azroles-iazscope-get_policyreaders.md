---
UID: NF:azroles.IAzScope.get_PolicyReaders
title: IAzScope::get_PolicyReaders (azroles.h)
description: The PolicyReaders property of IAzScope retrieves the security identifiers (SIDs), in text form, of principals that act as policy readers.
helpviewer_keywords: ["AzScope object [Security]","PolicyReaders property","IAzScope interface [Security]","PolicyReaders property","IAzScope.PolicyReaders","IAzScope.get_PolicyReaders","IAzScope::PolicyReaders","IAzScope::get_PolicyReaders","PolicyReaders property [Security]","PolicyReaders property [Security]","AzScope object","PolicyReaders property [Security]","IAzScope interface","azroles/IAzScope::PolicyReaders","azroles/IAzScope::get_PolicyReaders","get_PolicyReaders","security.iazscope_policyreaders"]
old-location: security\iazscope_policyreaders.htm
tech.root: security
ms.assetid: 7576997c-a585-4f0d-bec5-c616d39633f9
ms.date: 12/05/2018
ms.keywords: AzScope object [Security],PolicyReaders property, IAzScope interface [Security],PolicyReaders property, IAzScope.PolicyReaders, IAzScope.get_PolicyReaders, IAzScope::PolicyReaders, IAzScope::get_PolicyReaders, PolicyReaders property [Security], PolicyReaders property [Security],AzScope object, PolicyReaders property [Security],IAzScope interface, azroles/IAzScope::PolicyReaders, azroles/IAzScope::get_PolicyReaders, get_PolicyReaders, security.iazscope_policyreaders
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
 - IAzScope::get_PolicyReaders
 - azroles/IAzScope::get_PolicyReaders
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
 - IAzScope.PolicyReaders
 - IAzScope.get_PolicyReaders
 - AzScope.PolicyReaders
---

# IAzScope::get_PolicyReaders


## -description

The <b>PolicyReaders</b> property retrieves the <a href="/windows/desktop/SecGloss/s-gly">security identifiers</a> (SIDs), in text form, of principals that act as policy readers.

This property is read-only.

## -parameters

## -remarks

Policy readers for an object can read attributes for the object and for child objects of the object. Readers can also  use the policy; for example, readers can call the <a href="/windows/desktop/api/azroles/nf-azroles-iazclientcontext-accesscheck">AccessCheck</a> method. Readers cannot modify the object or its child objects.

In JScript, the returned <a href="/windows/desktop/api/oaidl/ns-oaidl-safearray">SAFEARRAY</a> must be converted to the JScript <a href="/scripting/javascript/reference/array-object-javascript">Array</a> object.