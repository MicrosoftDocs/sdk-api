---
UID: NF:mstask.ITaskScheduler.IsOfType
title: ITaskScheduler::IsOfType (mstask.h)
description: The IsOfType method checks the object's type to verify that it supports a particular interface.
helpviewer_keywords: ["ITaskScheduler interface [Task Scheduler]","IsOfType method","ITaskScheduler.IsOfType","ITaskScheduler::IsOfType","IsOfType","IsOfType method [Task Scheduler]","IsOfType method [Task Scheduler]","ITaskScheduler interface","_msb_itaskscheduler_isoftype","mstask/ITaskScheduler::IsOfType","taskschd.itaskscheduler_isoftype"]
old-location: taskschd\itaskscheduler_isoftype.htm
tech.root: taskschd
ms.assetid: 6d0a474d-398f-4d85-8e58-5dc2b6283086
ms.date: 12/05/2018
ms.keywords: ITaskScheduler interface [Task Scheduler],IsOfType method, ITaskScheduler.IsOfType, ITaskScheduler::IsOfType, IsOfType, IsOfType method [Task Scheduler], IsOfType method [Task Scheduler],ITaskScheduler interface, _msb_itaskscheduler_isoftype, mstask/ITaskScheduler::IsOfType, taskschd.itaskscheduler_isoftype
req.header: mstask.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Mstask.lib
req.dll: Mstask.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: Internet Explorer 4.0 or later on Windows NT 4.0 and Windows 95
ms.custom: 19H1
f1_keywords:
 - ITaskScheduler::IsOfType
 - mstask/ITaskScheduler::IsOfType
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Mstask.dll
api_name:
 - ITaskScheduler.IsOfType
---

# ITaskScheduler::IsOfType


## -description

<p class="CCE_Message">[[This API may be altered or unavailable in subsequent versions of the operating system or product. Please use the <a href="/windows/desktop/TaskSchd/task-scheduler-2-0-interfaces">Task Scheduler 2.0 Interfaces</a> instead.] ]

The 
<b>IsOfType</b> method checks the object's type to verify that it supports a particular interface.

## -parameters

### -param pwszName [in]

A null-terminated string that contains the name of the object to check.

### -param riid [in]

The reference identifier of the interface to be matched.

## -returns

The 
<b>IsOfType</b> method returns S_OK if the object named by <i>pwszName</i> supports the interface specified in <i>riid</i>. Otherwise,  S_FALSE is returned.

## -see-also

<a href="/windows/desktop/api/mstask/nn-mstask-itaskscheduler">ITaskScheduler</a>