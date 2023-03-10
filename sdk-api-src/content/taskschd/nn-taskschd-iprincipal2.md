---
UID: NN:taskschd.IPrincipal2
title: IPrincipal2 (taskschd.h)
description: Provides the extended settings applied to security credentials for a principal.
helpviewer_keywords: ["IPrincipal2","IPrincipal2 interface [Task Scheduler]","IPrincipal2 interface [Task Scheduler]","described","taskschd.iprincipal2","taskschd/IPrincipal2"]
old-location: taskschd\iprincipal2.htm
tech.root: taskschd
ms.assetid: 480f8038-0f67-4a69-b6f6-d7ba881d9d57
ms.date: 12/05/2018
ms.keywords: IPrincipal2, IPrincipal2 interface [Task Scheduler], IPrincipal2 interface [Task Scheduler],described, taskschd.iprincipal2, taskschd/IPrincipal2
req.header: taskschd.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Taskschd.idl
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
 - IPrincipal2
 - taskschd/IPrincipal2
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
 - IPrincipal2
---

# IPrincipal2 interface


## -description

Provides the extended settings applied to security credentials  for a principal. These security credentials define the security context for the tasks that are associated with the principal.

## -inheritance

The <b>IPrincipal2</b> interface inherits from the <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>IPrincipal2</b> also has these types of members:

## -remarks

When reading or writing XML for a task, the security credentials for a principal are specified in the <a href="/windows/desktop/TaskSchd/taskschedulerschema-principal-principaltype-element">Principal</a> element of the Task Scheduler schema.


#### Examples

For more information and example code for this interface, see <a href="/windows/desktop/TaskSchd/time-trigger-example--c---">Time Trigger Example (C++)</a> or <a href="/windows/desktop/TaskSchd/registration-trigger-example--c---">Registration Trigger Example (C++)</a>.

<div class="code"></div>

## -see-also

<a href="/windows/desktop/api/taskschd/nn-taskschd-itaskdefinition">ITaskDefinition</a>



<a href="/windows/desktop/api/taskschd/nf-taskschd-itaskdefinition-get_principal">Principal Property of ITaskDefinition</a>



<a href="/windows/desktop/TaskSchd/task-scheduler-interfaces">Task Scheduler Interfaces</a>
