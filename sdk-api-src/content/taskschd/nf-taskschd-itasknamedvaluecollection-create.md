---
UID: NF:taskschd.ITaskNamedValueCollection.Create
title: ITaskNamedValueCollection::Create (taskschd.h)
description: Creates a name-value pair in the collection.
helpviewer_keywords: ["Create","Create method [Task Scheduler]","Create method [Task Scheduler]","ITaskNamedValueCollection interface","ITaskNamedValueCollection interface [Task Scheduler]","Create method","ITaskNamedValueCollection.Create","ITaskNamedValueCollection::Create","taskschd.itasknamedvaluecollection_create","taskschd/ITaskNamedValueCollection::Create"]
old-location: taskschd\itasknamedvaluecollection_create.htm
tech.root: taskschd
ms.assetid: aec5ca20-b983-48e1-a5d0-761f18557fe4
ms.date: 12/05/2018
ms.keywords: Create, Create method [Task Scheduler], Create method [Task Scheduler],ITaskNamedValueCollection interface, ITaskNamedValueCollection interface [Task Scheduler],Create method, ITaskNamedValueCollection.Create, ITaskNamedValueCollection::Create, taskschd.itasknamedvaluecollection_create, taskschd/ITaskNamedValueCollection::Create
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
 - ITaskNamedValueCollection::Create
 - taskschd/ITaskNamedValueCollection::Create
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
 - ITaskNamedValueCollection.Create
---

# ITaskNamedValueCollection::Create


## -description

Creates a name-value pair in the collection.

## -parameters

### -param name [in]

The name associated with a value in a name-value pair.

### -param value [in]

The value associated with a name in a name-value pair.

### -param ppPair [out, retval]

The name-value pair created in the collection.

Pass in a reference to a <b>NULL</b> <a href="/windows/desktop/api/taskschd/nn-taskschd-itasknamedvaluepair">ITaskNamedValuePair</a> interface pointer. Referencing a non-<b>NULL</b> pointer can cause a memory leak because the pointer will be overwritten.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/taskschd/nn-taskschd-itasknamedvaluecollection">ITaskNamedValueCollection</a>