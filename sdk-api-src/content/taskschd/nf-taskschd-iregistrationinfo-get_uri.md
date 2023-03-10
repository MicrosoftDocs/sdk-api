---
UID: NF:taskschd.IRegistrationInfo.get_URI
title: IRegistrationInfo::get_URI (taskschd.h)
description: Gets or sets the URI of the task. (Get)
helpviewer_keywords: ["IRegistrationInfo interface [Task Scheduler]","URI property","IRegistrationInfo.URI","IRegistrationInfo.get_URI","IRegistrationInfo::URI","IRegistrationInfo::get_URI","IRegistrationInfo::put_URI","URI property [Task Scheduler]","URI property [Task Scheduler]","IRegistrationInfo interface","get_URI","taskschd.iregistrationinfo_uri","taskschd/IRegistrationInfo::URI","taskschd/IRegistrationInfo::get_URI","taskschd/IRegistrationInfo::put_URI"]
old-location: taskschd\iregistrationinfo_uri.htm
tech.root: taskschd
ms.assetid: 347898de-7960-42b8-84ff-4734137d0683
ms.date: 12/05/2018
ms.keywords: IRegistrationInfo interface [Task Scheduler],URI property, IRegistrationInfo.URI, IRegistrationInfo.get_URI, IRegistrationInfo::URI, IRegistrationInfo::get_URI, IRegistrationInfo::put_URI, URI property [Task Scheduler], URI property [Task Scheduler],IRegistrationInfo interface, get_URI, taskschd.iregistrationinfo_uri, taskschd/IRegistrationInfo::URI, taskschd/IRegistrationInfo::get_URI, taskschd/IRegistrationInfo::put_URI
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
 - IRegistrationInfo::get_URI
 - taskschd/IRegistrationInfo::get_URI
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
 - IRegistrationInfo.URI
 - IRegistrationInfo.get_URI
 - IRegistrationInfo.put_URI
---

# IRegistrationInfo::get_URI


## -description

Gets or sets the URI of the task.

This property is read/write.

## -parameters

## -remarks

When reading or writing XML for a task, the task URI is specified using the <a href="/windows/desktop/TaskSchd/taskschedulerschema-uri-registrationinfotype-element">URI</a> element of the Task Scheduler schema.

## -see-also

<a href="/windows/desktop/api/taskschd/nn-taskschd-iregistrationinfo">IRegistrationInfo</a>



<a href="/windows/desktop/TaskSchd/task-scheduler-start-page">Task Scheduler</a>
