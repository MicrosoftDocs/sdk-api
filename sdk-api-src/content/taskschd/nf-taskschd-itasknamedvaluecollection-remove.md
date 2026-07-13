---
UID: NF:taskschd.ITaskNamedValueCollection.Remove
title: ITaskNamedValueCollection::Remove (taskschd.h)
description: Removes a selected name-value pair from the collection.
helpviewer_keywords: ["ITaskNamedValueCollection interface [Task Scheduler]","Remove method","ITaskNamedValueCollection.Remove","ITaskNamedValueCollection::Remove","Remove","Remove method [Task Scheduler]","Remove method [Task Scheduler]","ITaskNamedValueCollection interface","taskschd.itasknamedvaluecollection_remove","taskschd/ITaskNamedValueCollection::Remove"]
old-location: taskschd\itasknamedvaluecollection_remove.htm
tech.root: taskschd
ms.assetid: 7c73fb37-5551-497f-86d9-b7158109ca38
ms.date: 12/05/2018
ms.keywords: ITaskNamedValueCollection interface [Task Scheduler],Remove method, ITaskNamedValueCollection.Remove, ITaskNamedValueCollection::Remove, Remove, Remove method [Task Scheduler], Remove method [Task Scheduler],ITaskNamedValueCollection interface, taskschd.itasknamedvaluecollection_remove, taskschd/ITaskNamedValueCollection::Remove
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
 - ITaskNamedValueCollection::Remove
 - taskschd/ITaskNamedValueCollection::Remove
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
 - ITaskNamedValueCollection.Remove
---

# ITaskNamedValueCollection::Remove


## -description

Removes a selected name-value pair from the collection.

## -parameters

### -param index [in]

The index of the name-value pair to be removed.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/taskschd/nn-taskschd-itasknamedvaluecollection">ITaskNamedValueCollection</a>