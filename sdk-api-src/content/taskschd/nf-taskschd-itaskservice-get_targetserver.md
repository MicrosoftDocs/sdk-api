---
UID: NF:taskschd.ITaskService.get_TargetServer
title: ITaskService::get_TargetServer
author: windows-sdk-content
description: Gets the name of the computer that is running the Task Scheduler service that the user is connected to.
old-location: taskschd\itaskservice_targetserver.htm
old-project: TaskSchd
ms.assetid: 2b8c55d7-72e2-4b75-8850-3f042ba83c60
ms.author: windowssdkdev
ms.date: 05/09/2018
ms.keywords: ITaskService interface [Task Scheduler],TargetServer property, ITaskService.TargetServer, ITaskService.get_TargetServer, ITaskService::TargetServer, ITaskService::get_TargetServer, TargetServer property [Task Scheduler], TargetServer property [Task Scheduler],ITaskService interface, get_TargetServer, taskschd.itaskservice_targetserver, taskschd/ITaskService::TargetServer, taskschd/ITaskService::get_TargetServer
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
 - ITaskService.TargetServer
 - ITaskService.get_TargetServer
product: Windows
targetos: Windows
req.lib: Taskschd.lib
req.dll: Taskschd.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# ITaskService::get_TargetServer


## -description


Gets the name of the computer that is running the Task Scheduler service that the user is connected to.

This property is read-only.


## -parameters


## -remarks



This property returns an empty string when the user passes an IP address, Localhost, or  '.' into the <i>pServer</i> parameter, and it returns the name of the computer that is running the Task Scheduler service when the user does not pass any parameter value.




## -see-also




<a href="https://msdn.microsoft.com/2459aaae-4c3a-458a-ad2c-bfff3a0322d3">ITaskService</a>
 

 

