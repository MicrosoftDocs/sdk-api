---
UID: NF:taskschd.ITriggerCollection.Remove
title: ITriggerCollection::Remove (taskschd.h)
description: Removes the specified trigger from the collection of triggers used by the task.
helpviewer_keywords: ["ITriggerCollection interface [Task Scheduler]","Remove method","ITriggerCollection.Remove","ITriggerCollection::Remove","Remove","Remove method [Task Scheduler]","Remove method [Task Scheduler]","ITriggerCollection interface","taskschd.itriggercollection_remove","taskschd/ITriggerCollection::Remove","triggers [Task Scheduler]","removing"]
old-location: taskschd\itriggercollection_remove.htm
tech.root: taskschd
ms.assetid: af3e04e6-20ec-412b-a0d2-41d31137dfca
ms.date: 12/05/2018
ms.keywords: ITriggerCollection interface [Task Scheduler],Remove method, ITriggerCollection.Remove, ITriggerCollection::Remove, Remove, Remove method [Task Scheduler], Remove method [Task Scheduler],ITriggerCollection interface, taskschd.itriggercollection_remove, taskschd/ITriggerCollection::Remove, triggers [Task Scheduler],removing
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
 - ITriggerCollection::Remove
 - taskschd/ITriggerCollection::Remove
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
 - ITriggerCollection.Remove
---

# ITriggerCollection::Remove


## -description

Removes the specified trigger from the collection of triggers used by the task.

## -parameters

### -param index [in]

The index of the trigger to be removed. Use a LONG value for the index number.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

When removing items, note that the index for the first item in the collection is 1 and the index for the last item is the value of the <a href="/windows/desktop/api/taskschd/nf-taskschd-itriggercollection-get_count">Count</a> property.

This method will return <b>E_INVALIDARG</b> when the value passed to the <i>index</i> parameter is not valid.

## -see-also

<a href="/windows/desktop/api/taskschd/nn-taskschd-itriggercollection">ITriggerCollection</a>



<a href="/windows/desktop/TaskSchd/task-scheduler-start-page">Task Scheduler</a>