---
UID: NN:taskschd.IEmailAction
title: IEmailAction (taskschd.h)
description: Represents an action that sends an email message.
helpviewer_keywords: ["IEmailAction","IEmailAction interface [Task Scheduler]","IEmailAction interface [Task Scheduler]","described","taskschd.iemailaction","taskschd/IEmailAction"]
old-location: taskschd\iemailaction.htm
tech.root: taskschd
ms.assetid: 2f08fd42-233a-40ee-96d0-f0ac8b25b847
ms.date: 12/05/2018
ms.keywords: IEmailAction, IEmailAction interface [Task Scheduler], IEmailAction interface [Task Scheduler],described, taskschd.iemailaction, taskschd/IEmailAction
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
 - IEmailAction
 - taskschd/IEmailAction
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
 - IEmailAction
---

# IEmailAction interface


## -description

<p class="CCE_Message">[This interface is no longer supported. Please use IExecAction with the  powershell <a href="/powershell/module/microsoft.powershell.utility/send-mailmessage">Send-MailMessage</a> cmdlet as a workaround.]

Represents an action that sends an email message.

## -remarks

The email action must have a valid value for the <a href="/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_server">Server</a>, <a href="/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_from">From</a>, and <a href="/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_to">To</a> or <a href="/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_cc">Cc</a> properties for the task to register and run correctly.

When reading or writing your own XML for a task, an email action is specified using the <a href="/windows/desktop/TaskSchd/taskschedulerschema-sendemail-actiongroup-element">SendEmail</a> element of the Task Scheduler schema.

<b>Windows 8 and Windows Server 2012:  </b>This interface has been removed. Please use IExecAction with the  powershell <a href="/powershell/module/microsoft.powershell.utility/send-mailmessage">Send-MailMessage</a> cmdlet as a workaround.


#### Examples

For more information and example code for this interface, see <a href="/previous-versions/aa446886(v=vs.85)">Event Trigger Example (C++)</a>.

<div class="code"></div>

## -see-also

<a href="/windows/desktop/api/taskschd/nn-taskschd-iaction">IAction</a>



<a href="/windows/desktop/api/taskschd/nn-taskschd-iactioncollection">IActionCollection</a>



<a href="/windows/desktop/TaskSchd/task-scheduler-start-page">Task Scheduler</a>