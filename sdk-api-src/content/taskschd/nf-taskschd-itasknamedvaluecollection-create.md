---
UID: NF:taskschd.ITaskNamedValueCollection.Create
title: ITaskNamedValueCollection::Create
author: windows-sdk-content
description: Creates a name-value pair in the collection.
old-location: taskschd\itasknamedvaluecollection_create.htm
old-project: taskschd
ms.assetid: aec5ca20-b983-48e1-a5d0-761f18557fe4
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: Create, Create method [Task Scheduler], Create method [Task Scheduler],ITaskNamedValueCollection interface, ITaskNamedValueCollection interface [Task Scheduler],Create method, ITaskNamedValueCollection.Create, ITaskNamedValueCollection::Create, taskschd.itasknamedvaluecollection_create, taskschd/ITaskNamedValueCollection::Create
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
 - ITaskNamedValueCollection.Create
product: Windows
targetos: Windows
req.lib: Taskschd.lib
req.dll: Taskschd.dll
req.irql: 
req.product: Windows XP with SP1 and later
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

Pass in a reference to a <b>NULL</b> <a href="https://msdn.microsoft.com/b9d186a3-017d-409e-9d67-e74dc69a486a">ITaskNamedValuePair</a> interface pointer. Referencing a non-<b>NULL</b> pointer can cause a memory leak because the pointer will be overwritten.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/440dc70b-02de-4974-ad2a-462491d12775">ITaskNamedValueCollection</a>
 

 

