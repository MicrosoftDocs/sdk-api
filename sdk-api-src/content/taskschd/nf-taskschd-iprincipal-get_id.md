---
UID: NF:taskschd.IPrincipal.get_Id
title: IPrincipal::get_Id (taskschd.h)
description: Gets or sets the identifier of the principal. (Get)
helpviewer_keywords: ["IPrincipal interface [Task Scheduler]","Id property","IPrincipal.Id","IPrincipal.get_Id","IPrincipal::Id","IPrincipal::get_Id","IPrincipal::put_Id","Id property [Task Scheduler]","Id property [Task Scheduler]","IPrincipal interface","get_Id","taskschd.iprincipal_id","taskschd/IPrincipal::Id","taskschd/IPrincipal::get_Id","taskschd/IPrincipal::put_Id"]
old-location: taskschd\iprincipal_id.htm
tech.root: taskschd
ms.assetid: 70c31ea8-508a-4971-b62a-b94e87a8857d
ms.date: 12/05/2018
ms.keywords: IPrincipal interface [Task Scheduler],Id property, IPrincipal.Id, IPrincipal.get_Id, IPrincipal::Id, IPrincipal::get_Id, IPrincipal::put_Id, Id property [Task Scheduler], Id property [Task Scheduler],IPrincipal interface, get_Id, taskschd.iprincipal_id, taskschd/IPrincipal::Id, taskschd/IPrincipal::get_Id, taskschd/IPrincipal::put_Id
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
 - IPrincipal::get_Id
 - taskschd/IPrincipal::get_Id
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
 - IPrincipal.Id
 - IPrincipal.get_Id
 - IPrincipal.put_Id
---

# IPrincipal::get_Id


## -description

Gets or sets the identifier of the principal.

This property is read/write.

## -parameters

## -remarks

This identifier is also used when specifying the  <a href="/windows/desktop/api/taskschd/nf-taskschd-iactioncollection-get_context">IActionCollection::Context</a> property.

When reading or writing XML for a task, the identifier of the principal is specified in the Id attribute of the <a href="/windows/desktop/TaskSchd/taskschedulerschema-principal-principaltype-element">Principal</a> element of the Task Scheduler schema.

## -see-also

<a href="/windows/desktop/api/taskschd/nf-taskschd-iactioncollection-get_context">IActionCollection.Context</a>



<a href="/windows/desktop/api/taskschd/nn-taskschd-iprincipal">IPrincipal</a>



<a href="/windows/desktop/TaskSchd/task-scheduler-start-page">Task Scheduler</a>
