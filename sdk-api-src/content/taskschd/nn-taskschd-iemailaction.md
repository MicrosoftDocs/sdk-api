---
UID: NN:taskschd.IEmailAction
title: IEmailAction
author: windows-driver-content
description: Represents an action that sends an email message.
old-location: taskschd\iemailaction.htm
old-project: TaskSchd
ms.assetid: 2f08fd42-233a-40ee-96d0-f0ac8b25b847
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: IEmailAction, IEmailAction interface [Task Scheduler], IEmailAction interface [Task Scheduler],described, taskschd.iemailaction, taskschd/IEmailAction
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: TASK_TRIGGER_TYPE2
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	taskschd.dll
api_name:
-	IEmailAction
product: Windows
targetos: Windows
req.lib: Taskschd.lib
req.dll: Taskschd.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# IEmailAction interface


## -description


<p class="CCE_Message">[This interface is no longer supported. Please use IExecAction with the  powershell <a href="796227F5-C9FF-402D-8A04-CDE9E0C180EE">Send-MailMessage</a> cmdlet as a workaround.]

Represents an action that sends an email message.


## -remarks



The email action must have a valid value for the <a href="https://msdn.microsoft.com/c781f189-f27b-4f37-af53-144e1ae8cb75">Server</a>, <a href="https://msdn.microsoft.com/a0e85063-73eb-425a-a306-63ac65ab7ec8">From</a>, and <a href="https://msdn.microsoft.com/5144875a-6854-4907-89cd-6438f6adcc49">To</a> or <a href="https://msdn.microsoft.com/23493ac7-0906-4ea3-9445-3dd56c30bb13">Cc</a> properties for the task to register and run correctly.

When reading or writing your own XML for a task, an email action is specified using the <a href="https://msdn.microsoft.com/83416b02-8327-47b3-9dfc-1bf5b9365728">SendEmail</a> element of the Task Scheduler schema.

<b>Windows 8 and Windows Server 2012:  </b>This interface has been removed. Please use IExecAction with the  powershell <a href="796227F5-C9FF-402D-8A04-CDE9E0C180EE">Send-MailMessage</a> cmdlet as a workaround.


#### Examples

For more information and example code for this interface, see <a href="https://msdn.microsoft.com/cacc1b72-7c58-4117-b204-ddb3a312bb08">Event Trigger Example (C++)</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/library/windows/hardware/ff538787">IAction</a>



<a href="https://msdn.microsoft.com/aa7781b6-2600-4af5-95b8-2ac7928946fa">IActionCollection</a>



<a href="https://msdn.microsoft.com/15970a51-c139-48b8-b82b-605728d0f386">Task Scheduler</a>
 

 

