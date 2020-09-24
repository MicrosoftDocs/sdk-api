---
UID: NN:taskschd.ITaskNamedValuePair
title: ITaskNamedValuePair (taskschd.h)
description: Creates a name-value pair in which the name is associated with the value.
helpviewer_keywords: ["ITaskNamedValuePair","ITaskNamedValuePair interface [Task Scheduler]","ITaskNamedValuePair interface [Task Scheduler]","described","taskschd.itasknamedvaluepair","taskschd/ITaskNamedValuePair"]
old-location: taskschd\itasknamedvaluepair.htm
tech.root: taskschd
ms.assetid: b9d186a3-017d-409e-9d67-e74dc69a486a
ms.date: 12/05/2018
ms.keywords: ITaskNamedValuePair, ITaskNamedValuePair interface [Task Scheduler], ITaskNamedValuePair interface [Task Scheduler],described, taskschd.itasknamedvaluepair, taskschd/ITaskNamedValuePair
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
 - ITaskNamedValuePair
 - taskschd/ITaskNamedValuePair
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
 - ITaskNamedValuePair
---

# ITaskNamedValuePair interface


## -description

Creates a name-value pair in which the name is associated with the value.

## -remarks

When reading or writing your own XML for a task, a name-value pair is specified using the <a href="/windows/desktop/TaskSchd/taskschedulerschema-valuequeries-eventtriggertype-element">ValueQueries</a> element of the Task Scheduler schema.

## -see-also

<a href="/windows/desktop/api/taskschd/nn-taskschd-itasknamedvaluecollection">ITaskNamedValueCollection</a>