---
UID: NF:taskschd.IActionCollection.Remove
title: IActionCollection::Remove (taskschd.h)
description: Removes the specified action from the collection.
helpviewer_keywords: ["IActionCollection interface [Task Scheduler]","Remove method","IActionCollection.Remove","IActionCollection::Remove","Remove","Remove method [Task Scheduler]","Remove method [Task Scheduler]","IActionCollection interface","actions [Task Scheduler]","removing","taskschd.iactioncollection_remove","taskschd/IActionCollection::Remove"]
old-location: taskschd\iactioncollection_remove.htm
tech.root: taskschd
ms.assetid: 91332ec0-8225-421a-baae-1a106be157a9
ms.date: 12/05/2018
ms.keywords: IActionCollection interface [Task Scheduler],Remove method, IActionCollection.Remove, IActionCollection::Remove, Remove, Remove method [Task Scheduler], Remove method [Task Scheduler],IActionCollection interface, actions [Task Scheduler],removing, taskschd.iactioncollection_remove, taskschd/IActionCollection::Remove
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
 - IActionCollection::Remove
 - taskschd/IActionCollection::Remove
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
 - IActionCollection.Remove
---

# IActionCollection::Remove


## -description

Removes the specified action from the collection.

## -parameters

### -param index [in]

The index of the action to be removed. Use a LONG value for the index number.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

<b>IActionCollection::Remove</b> returns E_INVALIDARG and E_TYPE_MISMATCH instead of E_INVALID_VARIANT when an invalid argument is specified.

When removing items, note that the index for the first item in the collection is 1 and the index for the last item is the value of the <a href="/windows/desktop/api/taskschd/nf-taskschd-iactioncollection-get_count">Count</a> property of IActionCollection.

## -see-also

<a href="/windows/desktop/api/taskschd/nn-taskschd-iactioncollection">IActionCollection</a>



<a href="/windows/desktop/TaskSchd/task-scheduler-start-page">Task Scheduler</a>