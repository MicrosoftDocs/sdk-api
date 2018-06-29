---
UID: NN:taskschd.IAction
title: IAction
author: windows-sdk-content
description: Provides the common properties inherited by all action objects.
old-location: taskschd\iaction.htm
old-project: TaskSchd
ms.assetid: 50d60cf0-642a-43fe-9163-51740e75fa8d
ms.author: windowssdkdev
ms.date: 05/09/2018
ms.keywords: IAction, IAction interface [Task Scheduler], IAction interface [Task Scheduler],described, taskschd.iaction, taskschd/IAction
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
 - IAction
product: Windows
targetos: Windows
req.lib: Taskschd.lib
req.dll: Taskschd.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# IAction interface


## -description


Provides the common properties inherited by all action objects. An action object is created by the <a href="https://msdn.microsoft.com/815a000b-ba02-470d-80e6-06ba3c8ea014">IActionCollection::Create</a> method.


## -remarks



For more information about how actions and tasks work together, see <a href="https://msdn.microsoft.com/4cbe739d-4c4e-4469-8289-4be41b93950c">Task Actions</a>. The following table contains the interfaces that represent the actions  that can be performed:<table>
<tr>
<th>API</th>
<th>Description</th>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/fb5cc2c3-ba86-401a-b51f-b28d1f5be58f">IComHandlerAction</a>
</td>
<td>Represents an action that fires a handler.</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/46a4cd60-df23-4109-8a86-b7755a6922dd">IExecAction</a>
</td>
<td>Represents an action that executes a command-line operation.</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/2f08fd42-233a-40ee-96d0-f0ac8b25b847">IEmailAction</a>
</td>
<td>Represents an action that sends an email message.</td>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/329232de-6068-4757-b567-3ce4d2c5ba4a">IShowMessageAction</a>
</td>
<td>Represents an action that shows a message box.</td>
</tr>
</table>
 



When reading or writing XML, the actions of a task are specified in the <a href="https://msdn.microsoft.com/0a48fbd6-8a6f-4bad-9b28-0631dce15748">Actions</a> element of the Task Scheduler schema.


#### Examples

For more information and a code example  for this interface, see <a href="https://msdn.microsoft.com/e45b18b0-5a7f-4283-b42f-15e9ffcfaff7">Time Trigger Example (C++)</a>, <a href="https://msdn.microsoft.com/cacc1b72-7c58-4117-b204-ddb3a312bb08">Event Trigger Example (C++)</a>, <a href="https://msdn.microsoft.com/f1038142-b83e-4159-9a7b-db2ae4ed3bd2">Daily Trigger Example (C++)</a>, <a href="https://msdn.microsoft.com/5e2e8fa6-66c7-4356-8fd6-22f7974791b9">Registration Trigger Example (C++)</a>, <a href="https://msdn.microsoft.com/7c70b743-aff2-4ef5-b65b-ef0b5fdacade">Weekly Trigger Example (C++)</a>, <a href="https://msdn.microsoft.com/15647234-8d1f-4d75-b215-92927b300c1f">Logon Trigger Example (C++)</a>, or <a href="https://msdn.microsoft.com/d4dbbfe5-bde9-4a1c-8e11-24cd1e14646c">Boot Trigger Example (C++)</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/aa7781b6-2600-4af5-95b8-2ac7928946fa">IActionCollection</a>



<a href="https://msdn.microsoft.com/815a000b-ba02-470d-80e6-06ba3c8ea014">IActionCollection::Create</a>



<a href="https://msdn.microsoft.com/15970a51-c139-48b8-b82b-605728d0f386">Task Scheduler</a>



<a href="https://msdn.microsoft.com/library/Aa383606(v=VS.85).aspx">Task Scheduler Interfaces</a>
 

 

