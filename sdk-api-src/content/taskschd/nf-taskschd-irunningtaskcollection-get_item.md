---
UID: NF:taskschd.IRunningTaskCollection.get_Item
title: IRunningTaskCollection::get_Item
author: windows-sdk-content
description: Gets the specified task from the collection.
old-location: taskschd\irunningtaskcollection_item.htm
old-project: TaskSchd
ms.assetid: e82e7e1b-a3bd-4456-85a9-e0005f954618
ms.author: windowssdkdev
ms.date: 05/09/2018
ms.keywords: IRunningTaskCollection interface [Task Scheduler],Item property, IRunningTaskCollection.Item, IRunningTaskCollection.get_Item, IRunningTaskCollection::Item, IRunningTaskCollection::get_Item, Item property [Task Scheduler], Item property [Task Scheduler],IRunningTaskCollection interface, get_Item, taskschd.irunningtaskcollection_item, taskschd/IRunningTaskCollection::Item, taskschd/IRunningTaskCollection::get_Item
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
tech.root: 
req.typenames: TASK_TRIGGER_TYPE2
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
product: Windows
targetos: Windows
req.lib: Taskschd.lib
req.dll: Taskschd.dll
req.irql: 
req.product: Windows XP with SP1 and later
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




<a href="https://msdn.microsoft.com/71a06a8f-8628-415d-b002-977c0d27f9a4">IRunningTask</a>



<a href="https://msdn.microsoft.com/f95efba5-563d-49c0-81d3-143aa158ad8f">IRunningTaskCollection</a>
 

 

