---
UID: NF:taskschd.IRunningTaskCollection.get_Item
title: IRunningTaskCollection::get_Item (taskschd.h)
description: Gets the specified task from the collection.
helpviewer_keywords: ["IRunningTaskCollection interface [Task Scheduler]","Item property","IRunningTaskCollection.Item","IRunningTaskCollection.get_Item","IRunningTaskCollection::Item","IRunningTaskCollection::get_Item","Item property [Task Scheduler]","Item property [Task Scheduler]","IRunningTaskCollection interface","get_Item","taskschd.irunningtaskcollection_item","taskschd/IRunningTaskCollection::Item","taskschd/IRunningTaskCollection::get_Item"]
old-location: taskschd\irunningtaskcollection_item.htm
tech.root: taskschd
ms.assetid: e82e7e1b-a3bd-4456-85a9-e0005f954618
ms.date: 12/05/2018
ms.keywords: IRunningTaskCollection interface [Task Scheduler],Item property, IRunningTaskCollection.Item, IRunningTaskCollection.get_Item, IRunningTaskCollection::Item, IRunningTaskCollection::get_Item, Item property [Task Scheduler], Item property [Task Scheduler],IRunningTaskCollection interface, get_Item, taskschd.irunningtaskcollection_item, taskschd/IRunningTaskCollection::Item, taskschd/IRunningTaskCollection::get_Item
req.header: taskschd.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Taskschd.lib
req.dll: Taskschd.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IRunningTaskCollection::get_Item
 - taskschd/IRunningTaskCollection::get_Item
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - taskschd.dll
api_name:
 - IRunningTaskCollection.Item
 - IRunningTaskCollection.get_Item
---

# IRunningTaskCollection::get_Item


## -description

Gets the specified task from the collection.

This property is read-only.

## -parameters

## -remarks

IRunningTaskCollection::get_Item returns E_INVALIDARG and E_TYPE_MISMATCH instead of E_INVALID_VARIANT when an invalid argument is specified.

Collections are 1-based. That is, the index for the first item in the collection is 1.

## -see-also

<a href="/windows/desktop/api/taskschd/nn-taskschd-irunningtask">IRunningTask</a>



<a href="/windows/desktop/api/taskschd/nn-taskschd-irunningtaskcollection">IRunningTaskCollection</a>