---
UID: NF:taskschd.IActionCollection.Remove
title: IActionCollection::Remove
author: windows-sdk-content
description: Removes the specified action from the collection.
old-location: taskschd\iactioncollection_remove.htm
old-project: TaskSchd
ms.assetid: 91332ec0-8225-421a-baae-1a106be157a9
ms.author: windowssdkdev
ms.date: 05/09/2018
ms.keywords: IActionCollection interface [Task Scheduler],Remove method, IActionCollection.Remove, IActionCollection::Remove, Remove, Remove method [Task Scheduler], Remove method [Task Scheduler],IActionCollection interface, actions [Task Scheduler],removing, taskschd.iactioncollection_remove, taskschd/IActionCollection::Remove
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
req.typenames: TASK_TRIGGER_TYPE2
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	taskschd.dll
api_name:
-	IActionCollection.Remove
product: Windows
targetos: Windows
req.lib: Taskschd.lib
req.dll: Taskschd.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# IActionCollection::Remove


## -description


Removes the specified action from the collection.


## -parameters




### -param index [in]

The index of the action to be removed. Use a LONG value for the index number.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



<b>IActionCollection::Remove</b> returns E_INVALIDARG and E_TYPE_MISMATCH instead of E_INVALID_VARIANT when an invalid argument is specified.

When removing items, note that the index for the first item in the collection is 1 and the index for the last item is the value of the <a href="https://msdn.microsoft.com/library/windows/hardware/hh406342">Count</a> property of IActionCollection.




## -see-also




<a href="https://msdn.microsoft.com/aa7781b6-2600-4af5-95b8-2ac7928946fa">IActionCollection</a>



<a href="https://msdn.microsoft.com/15970a51-c139-48b8-b82b-605728d0f386">Task Scheduler</a>
 

 

