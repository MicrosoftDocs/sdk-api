---
UID: NF:azroles.IAzTasks.get_Count
title: IAzTasks::get_Count (azroles.h)
description: Retrieves the number of IAzTask objects in the collection.
helpviewer_keywords: ["AzTasks object [Security]","Count property","Count property [Security]","Count property [Security]","AzTasks object","Count property [Security]","IAzTasks interface","IAzTasks interface [Security]","Count property","IAzTasks.Count","IAzTasks.get_Count","IAzTasks::Count","IAzTasks::get_Count","azroles/IAzTasks::Count","azroles/IAzTasks::get_Count","get_Count","security.iaztasks_count"]
old-location: security\iaztasks_count.htm
tech.root: security
ms.assetid: 505768ce-27a3-4f36-aeea-081cf8e45d14
ms.date: 12/05/2018
ms.keywords: AzTasks object [Security],Count property, Count property [Security], Count property [Security],AzTasks object, Count property [Security],IAzTasks interface, IAzTasks interface [Security],Count property, IAzTasks.Count, IAzTasks.get_Count, IAzTasks::Count, IAzTasks::get_Count, azroles/IAzTasks::Count, azroles/IAzTasks::get_Count, get_Count, security.iaztasks_count
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
 - IAzTasks::get_Count
 - azroles/IAzTasks::get_Count
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
 - IAzTasks.Count
 - IAzTasks.get_Count
 - AzTasks.Count
---

# IAzTasks::get_Count


## -description

The <b>Count</b> property retrieves the number of <a href="/windows/desktop/api/azroles/nn-azroles-iaztask">IAzTask</a> objects in the collection.

This property is read-only.

## -parameters

## -remarks

The <b>Count</b> property can be used to specify the last <a href="/windows/desktop/api/azroles/nn-azroles-iaztask">IAzTask</a> object in a collection when retrieving a specific <b>IAzTask</b> object using the  <a href="/windows/desktop/api/azroles/nf-azroles-iaztasks-get_item">IAzTasks.Item</a> property.