---
UID: NF:taskschd.IPrincipal.put_GroupId
title: IPrincipal::put_GroupId (taskschd.h)
description: Gets or sets the identifier of the user group that is required to run the tasks that are associated with the principal. (Put)
helpviewer_keywords: ["GroupId property [Task Scheduler]","GroupId property [Task Scheduler]","IPrincipal interface","IPrincipal interface [Task Scheduler]","GroupId property","IPrincipal.GroupId","IPrincipal.put_GroupId","IPrincipal::GroupId","IPrincipal::get_GroupId","IPrincipal::put_GroupId","put_GroupId","taskschd.iprincipal_groupid","taskschd/IPrincipal::GroupId","taskschd/IPrincipal::get_GroupId","taskschd/IPrincipal::put_GroupId"]
old-location: taskschd\iprincipal_groupid.htm
tech.root: taskschd
ms.assetid: df4bffa3-ee38-49cd-bec7-28edda48a953
ms.date: 12/05/2018
ms.keywords: GroupId property [Task Scheduler], GroupId property [Task Scheduler],IPrincipal interface, IPrincipal interface [Task Scheduler],GroupId property, IPrincipal.GroupId, IPrincipal.put_GroupId, IPrincipal::GroupId, IPrincipal::get_GroupId, IPrincipal::put_GroupId, put_GroupId, taskschd.iprincipal_groupid, taskschd/IPrincipal::GroupId, taskschd/IPrincipal::get_GroupId, taskschd/IPrincipal::put_GroupId
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
 - IPrincipal::put_GroupId
 - taskschd/IPrincipal::put_GroupId
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
 - IPrincipal.GroupId
 - IPrincipal.get_GroupId
 - IPrincipal.put_GroupId
---

# IPrincipal::put_GroupId


## -description

Gets or sets the identifier of the user group that is required to run the tasks that are associated with the principal.

This property is read/write.

## -parameters

## -remarks

Do not set this property if a user identifier is specified in the <a href="/windows/desktop/api/taskschd/nf-taskschd-iprincipal-get_userid">UserId</a> property.

When reading or writing XML for a task, the group identifier for a principal is specified in the <a href="/windows/desktop/TaskSchd/taskschedulerschema-groupid-principaltype-element">GroupId</a> element of the Task Scheduler schema.

## -see-also

<a href="/windows/desktop/api/taskschd/nn-taskschd-iprincipal">IPrincipal</a>



<a href="/windows/desktop/TaskSchd/task-scheduler-start-page">Task Scheduler</a>



<a href="/windows/desktop/api/taskschd/nf-taskschd-iprincipal-get_userid">UserId</a>
