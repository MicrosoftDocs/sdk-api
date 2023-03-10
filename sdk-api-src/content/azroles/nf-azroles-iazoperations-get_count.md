---
UID: NF:azroles.IAzOperations.get_Count
title: IAzOperations::get_Count (azroles.h)
description: Retrieves the number of IAzOperation objects in the collection.
helpviewer_keywords: ["AzOperations object [Security]","Count property","Count property [Security]","Count property [Security]","AzOperations object","Count property [Security]","IAzOperations interface","IAzOperations interface [Security]","Count property","IAzOperations.Count","IAzOperations.get_Count","IAzOperations::Count","IAzOperations::get_Count","azroles/IAzOperations::Count","azroles/IAzOperations::get_Count","get_Count","security.iazoperations_count"]
old-location: security\iazoperations_count.htm
tech.root: security
ms.assetid: 665fdf1f-4606-4cfc-b33b-6bae4ce3b6c9
ms.date: 12/05/2018
ms.keywords: AzOperations object [Security],Count property, Count property [Security], Count property [Security],AzOperations object, Count property [Security],IAzOperations interface, IAzOperations interface [Security],Count property, IAzOperations.Count, IAzOperations.get_Count, IAzOperations::Count, IAzOperations::get_Count, azroles/IAzOperations::Count, azroles/IAzOperations::get_Count, get_Count, security.iazoperations_count
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
 - IAzOperations::get_Count
 - azroles/IAzOperations::get_Count
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
 - IAzOperations.Count
 - IAzOperations.get_Count
 - AzOperations.Count
---

# IAzOperations::get_Count


## -description

The <b>Count</b> property retrieves the number of <a href="/windows/desktop/api/azroles/nn-azroles-iazoperation">IAzOperation</a> objects in the collection.

This property is read-only.

## -parameters

## -remarks

The <b>Count</b> property can be used to specify the last <a href="/windows/desktop/api/azroles/nn-azroles-iazoperation">IAzOperation</a> object in a collection when retrieving a specific <b>IAzOperation</b> object using the  <a href="/windows/desktop/api/azroles/nf-azroles-iazoperations-get_item">IAzOperations.Item</a> property.