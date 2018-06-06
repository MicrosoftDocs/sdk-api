---
UID: NF:taskschd.IEmailAction.get_Server
title: IEmailAction::get_Server
author: windows-sdk-content
description: Gets or sets the name of the SMTP server that you use to send email from.
old-location: taskschd\iemailaction_server.htm
old-project: TaskSchd
ms.assetid: c781f189-f27b-4f37-af53-144e1ae8cb75
ms.author: windowssdkdev
ms.date: 05/09/2018
ms.keywords: IEmailAction interface [Task Scheduler],Server property, IEmailAction.Server, IEmailAction.get_Server, IEmailAction::Server, IEmailAction::get_Server, IEmailAction::put_Server, Server property [Task Scheduler], Server property [Task Scheduler],IEmailAction interface, get_Server, taskschd.iemailaction_server, taskschd/IEmailAction::Server, taskschd/IEmailAction::get_Server, taskschd/IEmailAction::put_Server
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
 - IEmailAction.Server
 - IEmailAction.get_Server
 - IEmailAction.put_Server
product: Windows
targetos: Windows
req.lib: Taskschd.lib
req.dll: Taskschd.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# IEmailAction::get_Server


## -description


<p class="CCE_Message">[This interface is no longer supported. Please use IExecAction with the  powershell <a href="796227F5-C9FF-402D-8A04-CDE9E0C180EE">Send-MailMessage</a> cmdlet as a workaround.]

Gets or sets the name of the SMTP server that you use to send email from.

This property is read/write.


## -parameters


## -remarks



Make sure the SMTP server that sends the email is setup correctly. E-mail is sent using NTLM authentication for Windows SMTP servers, which means that the security credentials used for running the task must also have privileges on the SMTP server to send email message. If the SMTP server is a non-Windows based server, then the email will be sent if the server allows anonymous access.  For information about setting up the SMTP server, see <a href="http://go.microsoft.com/fwlink/p/?linkid=69001">SMTP Server Setup</a>, and for information about managing SMTP server settings, see <a href="http://go.microsoft.com/fwlink/p/?linkid=69002">SMTP Administration</a>.





## -see-also




<a href="https://msdn.microsoft.com/2f08fd42-233a-40ee-96d0-f0ac8b25b847">IEmailAction</a>
 

 

