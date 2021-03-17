---
UID: NF:azroles.IAzRoles.get_Count
title: IAzRoles::get_Count (azroles.h)
description: Retrieves the number of IAzRole objects in the collection.
helpviewer_keywords: ["AzRoles object [Security]","Count property","Count property [Security]","Count property [Security]","AzRoles object","Count property [Security]","IAzRoles interface","IAzRoles interface [Security]","Count property","IAzRoles.Count","IAzRoles.get_Count","IAzRoles::Count","IAzRoles::get_Count","azroles/IAzRoles::Count","azroles/IAzRoles::get_Count","get_Count","security.iazroles_count"]
old-location: security\iazroles_count.htm
tech.root: security
ms.assetid: 4bf2c00e-dc33-4718-a6d1-f8c3ccccbae8
ms.date: 12/05/2018
ms.keywords: AzRoles object [Security],Count property, Count property [Security], Count property [Security],AzRoles object, Count property [Security],IAzRoles interface, IAzRoles interface [Security],Count property, IAzRoles.Count, IAzRoles.get_Count, IAzRoles::Count, IAzRoles::get_Count, azroles/IAzRoles::Count, azroles/IAzRoles::get_Count, get_Count, security.iazroles_count
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
 - IAzRoles::get_Count
 - azroles/IAzRoles::get_Count
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
 - IAzRoles.Count
 - IAzRoles.get_Count
 - AzRoles.Count
---

# IAzRoles::get_Count


## -description

The <b>Count</b> property retrieves the number of <a href="/windows/desktop/api/azroles/nn-azroles-iazrole">IAzRole</a> objects in the collection.

This property is read-only.

## -parameters

## -remarks

The <b>Count</b> property can be used to specify the last <a href="/windows/desktop/api/azroles/nn-azroles-iazrole">IAzRole</a> object in a collection when retrieving a specific <b>IAzRole</b> object using the  <a href="/windows/desktop/api/azroles/nf-azroles-iazroles-get_item">IAzRoles.Item</a> property.