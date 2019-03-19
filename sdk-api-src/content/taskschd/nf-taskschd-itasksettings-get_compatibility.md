---
UID: NF:taskschd.ITaskSettings.get_Compatibility
title: ITaskSettings::get_Compatibility (taskschd.h)
author: windows-sdk-content
description: Gets or sets an integer value that indicates which version of Task Scheduler a task is compatible with.
old-location: taskschd\itasksettings_compatibility.htm
tech.root: taskschd
ms.assetid: 04f77d3c-44fa-4091-b99e-af062f067ef9
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: Compatibility property [Task Scheduler], Compatibility property [Task Scheduler],ITaskSettings interface, ITaskSettings interface [Task Scheduler],Compatibility property, ITaskSettings.Compatibility, ITaskSettings.get_Compatibility, ITaskSettings::Compatibility, ITaskSettings::get_Compatibility, ITaskSettings::put_Compatibility, TASK_COMPATIBILITY_AT, TASK_COMPATIBILITY_V1, TASK_COMPATIBILITY_V2, get_Compatibility, taskschd.itasksettings_compatibility, taskschd/ITaskSettings::Compatibility, taskschd/ITaskSettings::get_Compatibility, taskschd/ITaskSettings::put_Compatibility
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
 - ITaskSettings.Compatibility
 - ITaskSettings.get_Compatibility
 - ITaskSettings.put_Compatibility
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITaskSettings::get_Compatibility


## -description


Gets or sets an integer value that indicates which version of Task Scheduler a task is compatible with.

This property is read/write.


## -parameters


## -remarks



 Task compatibility, which is set through the <b>Compatibility</b> property, should only be set to TASK_COMPATIBILITY_V1 if a task needs to be accessed or modified from a  Windows XP, Windows Server 2003, or Windows 2000 computer. Otherwise, it is recommended that Task Scheduler 2.0 compatibility be used because the task will have more features.

Tasks compatible with the AT command can only have one time trigger.

Tasks compatible with Task Scheduler 1.0 can only have a time trigger, a logon trigger, or a boot trigger, and the task can only have an executable action.

For more information about task compatibility, see <a href="https://msdn.microsoft.com/43fbbbd2-6e97-4ba5-9474-23c5e2b33612">What's New in Task Scheduler</a> and <a href="https://msdn.microsoft.com/24c43834-5731-4b14-9409-7d7cf20b1a71">Tasks</a>.




## -see-also




<a href="https://msdn.microsoft.com/203264d1-f67c-45ba-931b-206d7f57a2a6">ITaskSettings</a>



<a href="https://msdn.microsoft.com/a842ab84-26e1-49bd-bf57-1a1073a17183">TASK_COMPATIBILITY</a>



<a href="https://msdn.microsoft.com/15970a51-c139-48b8-b82b-605728d0f386">Task Scheduler</a>
 

 

