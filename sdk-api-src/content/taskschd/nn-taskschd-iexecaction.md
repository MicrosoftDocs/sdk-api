---
UID: NN:taskschd.IExecAction
title: IExecAction
author: windows-sdk-content
description: Represents an action that executes a command-line operation.
old-location: taskschd\iexecaction.htm
tech.root: TaskSchd
ms.assetid: 46a4cd60-df23-4109-8a86-b7755a6922dd
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: IExecAction, IExecAction interface [Task Scheduler], IExecAction interface [Task Scheduler],described, execute action [Task Scheduler],interface, taskschd.iexecaction, taskschd/IExecAction
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
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
 - IExecAction
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IExecAction interface


## -description


Represents an action that executes a command-line operation.


## -remarks



This action performs a command-line operation. For example, the action could run a script or launch an executable.

When reading or writing XML, an execution action is specified in the <a href="https://msdn.microsoft.com/84bdd1ec-4279-4282-b44a-4b5ad30503eb">Exec</a> element of the Task Scheduler schema.

If environment variables are used in the <a href="https://msdn.microsoft.com/307e59e9-5460-40aa-bac7-fa8cb4755d35">Path</a>, <a href="https://msdn.microsoft.com/623b3ffb-ff0f-46bf-ae3d-146e38c8bbc8">Arguments</a>, or <a href="https://msdn.microsoft.com/7cebc827-2587-46e4-a963-ad0fccfbcec7">WorkingDirectory</a> properties, then the values of the environment variables are cached and used when the Taskeng.exe (the task engine) is launched. Changes to the environment variables that occur after the task engine is launched will not be used by the task engine.


#### Examples

For more information and example code for this interface, see <a href="https://msdn.microsoft.com/e45b18b0-5a7f-4283-b42f-15e9ffcfaff7">Time Trigger Example (C++)</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/50d60cf0-642a-43fe-9163-51740e75fa8d">IAction</a>



<a href="https://msdn.microsoft.com/15970a51-c139-48b8-b82b-605728d0f386">Task Scheduler</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa383606(v=VS.85).aspx">Task Scheduler Interfaces</a>
 

 

