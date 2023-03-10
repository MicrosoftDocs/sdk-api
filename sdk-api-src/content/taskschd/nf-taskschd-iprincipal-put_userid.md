---
UID: NF:taskschd.IPrincipal.put_UserId
title: IPrincipal::put_UserId (taskschd.h)
description: Gets or sets the user identifier that is required to run the tasks that are associated with the principal. (Put)
helpviewer_keywords: ["IPrincipal interface [Task Scheduler]","UserId property","IPrincipal.UserId","IPrincipal.put_UserId","IPrincipal::UserId","IPrincipal::get_UserId","IPrincipal::put_UserId","UserId property [Task Scheduler]","UserId property [Task Scheduler]","IPrincipal interface","put_UserId","taskschd.iprincipal_userid","taskschd/IPrincipal::UserId","taskschd/IPrincipal::get_UserId","taskschd/IPrincipal::put_UserId"]
old-location: taskschd\iprincipal_userid.htm
tech.root: taskschd
ms.assetid: b85a1f05-acb0-4b3c-bea0-393ad7c6a43d
ms.date: 12/05/2018
ms.keywords: IPrincipal interface [Task Scheduler],UserId property, IPrincipal.UserId, IPrincipal.put_UserId, IPrincipal::UserId, IPrincipal::get_UserId, IPrincipal::put_UserId, UserId property [Task Scheduler], UserId property [Task Scheduler],IPrincipal interface, put_UserId, taskschd.iprincipal_userid, taskschd/IPrincipal::UserId, taskschd/IPrincipal::get_UserId, taskschd/IPrincipal::put_UserId
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
 - IPrincipal::put_UserId
 - taskschd/IPrincipal::put_UserId
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
 - IPrincipal.UserId
 - IPrincipal.get_UserId
 - IPrincipal.put_UserId
---

# IPrincipal::put_UserId


## -description

Gets or sets the user identifier that is required to run the tasks  that are associated with the principal.

This property is read/write.

## -parameters

## -remarks

Do not set this property if a group identifier is specified in the <a href="/windows/desktop/api/taskschd/nf-taskschd-iprincipal-get_groupid">GroupId</a> property.

When reading or writing XML for a task, the user identifier for a principal is specified in the <a href="/windows/desktop/TaskSchd/taskschedulerschema-userid-principaltype-element">UserId</a> element of the Task Scheduler schema.

## -see-also

<a href="/windows/desktop/api/taskschd/nf-taskschd-iprincipal-get_groupid">GroupId Property of IPrincipal</a>



<a href="/windows/desktop/api/taskschd/nn-taskschd-iprincipal">IPrincipal</a>



<a href="/windows/desktop/TaskSchd/task-scheduler-start-page">Task Scheduler</a>
