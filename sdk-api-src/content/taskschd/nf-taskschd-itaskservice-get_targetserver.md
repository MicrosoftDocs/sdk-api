---
UID: NF:taskschd.ITaskService.get_TargetServer
title: ITaskService::get_TargetServer (taskschd.h)
description: Gets the name of the computer that is running the Task Scheduler service that the user is connected to.
helpviewer_keywords: ["ITaskService interface [Task Scheduler]","TargetServer property","ITaskService.TargetServer","ITaskService.get_TargetServer","ITaskService::TargetServer","ITaskService::get_TargetServer","TargetServer property [Task Scheduler]","TargetServer property [Task Scheduler]","ITaskService interface","get_TargetServer","taskschd.itaskservice_targetserver","taskschd/ITaskService::TargetServer","taskschd/ITaskService::get_TargetServer"]
old-location: taskschd\itaskservice_targetserver.htm
tech.root: taskschd
ms.assetid: 2b8c55d7-72e2-4b75-8850-3f042ba83c60
ms.date: 12/05/2018
ms.keywords: ITaskService interface [Task Scheduler],TargetServer property, ITaskService.TargetServer, ITaskService.get_TargetServer, ITaskService::TargetServer, ITaskService::get_TargetServer, TargetServer property [Task Scheduler], TargetServer property [Task Scheduler],ITaskService interface, get_TargetServer, taskschd.itaskservice_targetserver, taskschd/ITaskService::TargetServer, taskschd/ITaskService::get_TargetServer
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
 - ITaskService::get_TargetServer
 - taskschd/ITaskService::get_TargetServer
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
 - ITaskService.TargetServer
 - ITaskService.get_TargetServer
---

# ITaskService::get_TargetServer


## -description

Gets the name of the computer that is running the Task Scheduler service that the user is connected to.

This property is read-only.

## -parameters

## -remarks

This property returns an empty string when the user passes an IP address, Localhost, or  '.' into the <i>pServer</i> parameter, and it returns the name of the computer that is running the Task Scheduler service when the user does not pass any parameter value.

## -see-also

<a href="/windows/desktop/api/taskschd/nn-taskschd-itaskservice">ITaskService</a>