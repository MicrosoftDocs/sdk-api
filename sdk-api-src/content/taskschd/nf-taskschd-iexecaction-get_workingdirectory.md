---
UID: NF:taskschd.IExecAction.get_WorkingDirectory
title: IExecAction::get_WorkingDirectory (taskschd.h)
author: windows-sdk-content
description: Gets or sets the directory that contains either the executable file or the files that are used by the executable file.
old-location: taskschd\iexecaction_workingdirectory.htm
tech.root: taskschd
ms.assetid: 7cebc827-2587-46e4-a963-ad0fccfbcec7
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IExecAction interface [Task Scheduler],WorkingDirectory property, IExecAction.WorkingDirectory, IExecAction.get_WorkingDirectory, IExecAction::WorkingDirectory, IExecAction::get_WorkingDirectory, IExecAction::put_WorkingDirectory, WorkingDirectory property [Task Scheduler], WorkingDirectory property [Task Scheduler],IExecAction interface, get_WorkingDirectory, taskschd.iexecaction_workingdirectory, taskschd/IExecAction::WorkingDirectory, taskschd/IExecAction::get_WorkingDirectory, taskschd/IExecAction::put_WorkingDirectory
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
 - IExecAction.WorkingDirectory
 - IExecAction.get_WorkingDirectory
 - IExecAction.put_WorkingDirectory
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IExecAction::get_WorkingDirectory


## -description


Gets or sets the directory that contains either the executable file or the files that are used by the executable file.

This property is read/write.


## -parameters


## -remarks



When reading or writing XML, the working directory of the application is specified in the <a href="https://msdn.microsoft.com/09e53748-6d21-42df-bbdd-f0fd9693aab0">WorkingDirectory</a> element of the Task Scheduler schema.

The path is checked to make sure it is valid when the task is registered, not when this property is set.




## -see-also




<a href="https://msdn.microsoft.com/46a4cd60-df23-4109-8a86-b7755a6922dd">IExecAction</a>



<a href="https://msdn.microsoft.com/15970a51-c139-48b8-b82b-605728d0f386">Task Scheduler</a>
 

 

