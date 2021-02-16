---
UID: NF:azroles.IAzApplicationGroups.get_Count
title: IAzApplicationGroups::get_Count (azroles.h)
description: Retrieves the number of IAzApplicationGroup objects in the collection.
helpviewer_keywords: ["AzApplicationGroups object [Security]","Count property","Count property [Security]","Count property [Security]","AzApplicationGroups object","Count property [Security]","IAzApplicationGroups interface","IAzApplicationGroups interface [Security]","Count property","IAzApplicationGroups.Count","IAzApplicationGroups.get_Count","IAzApplicationGroups::Count","IAzApplicationGroups::get_Count","azroles/IAzApplicationGroups::Count","azroles/IAzApplicationGroups::get_Count","get_Count","security.iazapplicationgroups_count"]
old-location: security\iazapplicationgroups_count.htm
tech.root: security
ms.assetid: d57e4428-3666-4eb0-8157-8b35acfc517b
ms.date: 12/05/2018
ms.keywords: AzApplicationGroups object [Security],Count property, Count property [Security], Count property [Security],AzApplicationGroups object, Count property [Security],IAzApplicationGroups interface, IAzApplicationGroups interface [Security],Count property, IAzApplicationGroups.Count, IAzApplicationGroups.get_Count, IAzApplicationGroups::Count, IAzApplicationGroups::get_Count, azroles/IAzApplicationGroups::Count, azroles/IAzApplicationGroups::get_Count, get_Count, security.iazapplicationgroups_count
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
 - IAzApplicationGroups::get_Count
 - azroles/IAzApplicationGroups::get_Count
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
 - IAzApplicationGroups.Count
 - IAzApplicationGroups.get_Count
 - AzApplicationGroups.Count
---

# IAzApplicationGroups::get_Count


## -description

The <b>Count</b> property retrieves the number of <a href="/windows/desktop/api/azroles/nn-azroles-iazapplicationgroup">IAzApplicationGroup</a> objects in the collection.

This property is read-only.

## -parameters

## -remarks

The <b>Count</b> property can be used to specify the last <a href="/windows/desktop/api/azroles/nn-azroles-iazapplicationgroup">IAzApplicationGroup</a> object in a collection when retrieving a specific <b>IAzApplicationGroup</b> object using the  <a href="/windows/desktop/api/azroles/nf-azroles-iazapplicationgroups-get_item">IAzApplicationGroups.Item</a> property.