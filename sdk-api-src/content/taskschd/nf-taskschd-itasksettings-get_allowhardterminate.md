---
UID: NF:taskschd.ITaskSettings.get_AllowHardTerminate
title: ITaskSettings::get_AllowHardTerminate
author: windows-sdk-content
description: Gets or sets a Boolean value that indicates that the task may be terminated by the Task Scheduler service using TerminateProcess.
old-location: taskschd\itasksettings_allowhardterminate.htm
tech.root: TaskSchd
ms.assetid: fd8105cf-5ef1-4ae4-8bb7-05469758b6b4
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: AllowHardTerminate property [Task Scheduler], AllowHardTerminate property [Task Scheduler],ITaskSettings interface, AllowHardTerminate property [Task Scheduler],TaskSettings class, ITaskSettings interface [Task Scheduler],AllowHardTerminate property, ITaskSettings.AllowHardTerminate, ITaskSettings.get_AllowHardTerminate, ITaskSettings::AllowHardTerminate, ITaskSettings::get_AllowHardTerminate, ITaskSettings::put_AllowHardTerminate, TaskSettings class [Task Scheduler],AllowHardTerminate property, get_AllowHardTerminate, taskschd.itasksettings_allowhardterminate, taskschd/ITaskSettings::AllowHardTerminate, taskschd/ITaskSettings::get_AllowHardTerminate, taskschd/ITaskSettings::put_AllowHardTerminate
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.lib: Taskschd.lib
req.dll: Taskschd.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - taskschd.dll
api_name:
 - ITaskSettings.AllowHardTerminate
 - ITaskSettings.get_AllowHardTerminate
 - ITaskSettings.put_AllowHardTerminate
 - TaskSettings.AllowHardTerminate
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- taskschd.h
: 
- ITaskSettings.get_AllowHardTerminate
: 
---

# ITaskSettings::get_AllowHardTerminate


## -description


Gets or sets a Boolean value that indicates that the task may be terminated by the Task Scheduler service using  <a href="https://msdn.microsoft.com/0e1a8195-4fd3-43d4-ae9e-1a1e05c2119a">TerminateProcess</a>. The service will try to close the running task by sending the <a href="_win32_WM_CLOSE_cpp">WM_CLOSE</a> notification, and if the  task does not respond, the task will be terminated only if this property is set to true.

This property is read/write.


## -parameters


## -remarks



When reading or writing XML for a task, this setting is specified in the <a href="https://msdn.microsoft.com/093a3cc6-d3e1-48e3-bc9e-0b15df2a54de">AllowHardTerminate</a> element of the Task Scheduler schema.




## -see-also




<a href="https://msdn.microsoft.com/203264d1-f67c-45ba-931b-206d7f57a2a6">ITaskSettings</a>



<a href="https://msdn.microsoft.com/15970a51-c139-48b8-b82b-605728d0f386">Task Scheduler</a>



TaskSettings
 

 

