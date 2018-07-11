---
UID: NF:taskschd.ITriggerCollection.Remove
title: ITriggerCollection::Remove
author: windows-sdk-content
description: Removes the specified trigger from the collection of triggers used by the task.
old-location: taskschd\itriggercollection_remove.htm
old-project: taskschd
ms.assetid: af3e04e6-20ec-412b-a0d2-41d31137dfca
ms.author: windowssdkdev
ms.date: 05/10/2018
ms.keywords: ITriggerCollection interface [Task Scheduler],Remove method, ITriggerCollection.Remove, ITriggerCollection::Remove, Remove, Remove method [Task Scheduler], Remove method [Task Scheduler],ITriggerCollection interface, taskschd.itriggercollection_remove, taskschd/ITriggerCollection::Remove, triggers [Task Scheduler],removing
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
 - ITriggerCollection.Remove
product: Windows
targetos: Windows
req.lib: Taskschd.lib
req.dll: Taskschd.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# ITriggerCollection::Remove


## -description


Removes the specified trigger from the collection of triggers used by the task.


## -parameters




### -param index [in]

The index of the trigger to be removed. Use a LONG value for the index number.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



When removing items, note that the index for the first item in the collection is 1 and the index for the last item is the value of the <a href="https://msdn.microsoft.com/library/windows/hardware/hh406342">Count</a> property.

This method will return <b>E_INVALIDARG</b> when the value passed to the <i>index</i> parameter is not valid.




## -see-also




<a href="https://msdn.microsoft.com/5985ff67-3aa2-4ade-9d53-da4d640f5f6e">ITriggerCollection</a>



<a href="https://msdn.microsoft.com/15970a51-c139-48b8-b82b-605728d0f386">Task Scheduler</a>
 

 

