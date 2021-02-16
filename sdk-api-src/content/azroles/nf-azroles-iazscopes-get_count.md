---
UID: NF:azroles.IAzScopes.get_Count
title: IAzScopes::get_Count (azroles.h)
description: Retrieves the number of IAzScope objects in the collection.
helpviewer_keywords: ["AzScopes object [Security]","Count property","Count property [Security]","Count property [Security]","AzScopes object","Count property [Security]","IAzScopes interface","IAzScopes interface [Security]","Count property","IAzScopes.Count","IAzScopes.get_Count","IAzScopes::Count","IAzScopes::get_Count","azroles/IAzScopes::Count","azroles/IAzScopes::get_Count","get_Count","security.iazscopes_count"]
old-location: security\iazscopes_count.htm
tech.root: security
ms.assetid: aff809a6-c768-4cfe-a41f-ee227f77a3b1
ms.date: 12/05/2018
ms.keywords: AzScopes object [Security],Count property, Count property [Security], Count property [Security],AzScopes object, Count property [Security],IAzScopes interface, IAzScopes interface [Security],Count property, IAzScopes.Count, IAzScopes.get_Count, IAzScopes::Count, IAzScopes::get_Count, azroles/IAzScopes::Count, azroles/IAzScopes::get_Count, get_Count, security.iazscopes_count
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
 - IAzScopes::get_Count
 - azroles/IAzScopes::get_Count
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
 - IAzScopes.Count
 - IAzScopes.get_Count
 - AzScopes.Count
---

# IAzScopes::get_Count


## -description

The <b>Count</b> property retrieves the number of <a href="/windows/desktop/api/azroles/nn-azroles-iazscope">IAzScope</a> objects in the collection.

This property is read-only.

## -parameters

## -remarks

The <b>Count</b> property can be used to specify the last <a href="/windows/desktop/api/azroles/nn-azroles-iazscope">IAzScope</a> object in a collection when retrieving a specific <b>IAzScope</b> object using the  <a href="/windows/desktop/api/azroles/nf-azroles-iazscopes-get_item">IAzScopes.Item</a> property.