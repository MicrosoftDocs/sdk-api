---
UID: NF:azroles.IAzApplications.get_Count
title: IAzApplications::get_Count (azroles.h)
description: Retrieves the number of IAzApplication objects in the collection.
helpviewer_keywords: ["AzApplications object [Security]","Count property","Count property [Security]","Count property [Security]","AzApplications object","Count property [Security]","IAzApplications interface","IAzApplications interface [Security]","Count property","IAzApplications.Count","IAzApplications.get_Count","IAzApplications::Count","IAzApplications::get_Count","azroles/IAzApplications::Count","azroles/IAzApplications::get_Count","get_Count","security.iazapplications_count"]
old-location: security\iazapplications_count.htm
tech.root: security
ms.assetid: 2f12fd9f-4632-4eef-8ac4-80e73a731539
ms.date: 12/05/2018
ms.keywords: AzApplications object [Security],Count property, Count property [Security], Count property [Security],AzApplications object, Count property [Security],IAzApplications interface, IAzApplications interface [Security],Count property, IAzApplications.Count, IAzApplications.get_Count, IAzApplications::Count, IAzApplications::get_Count, azroles/IAzApplications::Count, azroles/IAzApplications::get_Count, get_Count, security.iazapplications_count
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
 - IAzApplications::get_Count
 - azroles/IAzApplications::get_Count
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
 - IAzApplications.Count
 - IAzApplications.get_Count
 - AzApplications.Count
---

# IAzApplications::get_Count


## -description

The <b>Count</b> property retrieves the number of <a href="/windows/desktop/api/azroles/nn-azroles-iazapplication">IAzApplication</a> objects in the collection.

This property is read-only.

## -parameters

## -remarks

The <b>Count</b> property can be used to specify the last <a href="/windows/desktop/api/azroles/nn-azroles-iazapplication">IAzApplication</a> object in a collection when retrieving a specific <b>IAzApplication</b> object using the  <a href="/windows/desktop/api/azroles/nf-azroles-iazapplications-get_item">IAzApplications.Item</a> property.