---
UID: NF:taskschd.IEmailAction.get_Server
title: IEmailAction::get_Server (taskschd.h)
description: Gets or sets the name of the SMTP server that you use to send email from. (Get)
helpviewer_keywords: ["IEmailAction interface [Task Scheduler]","Server property","IEmailAction.Server","IEmailAction.get_Server","IEmailAction::Server","IEmailAction::get_Server","IEmailAction::put_Server","Server property [Task Scheduler]","Server property [Task Scheduler]","IEmailAction interface","get_Server","taskschd.iemailaction_server","taskschd/IEmailAction::Server","taskschd/IEmailAction::get_Server","taskschd/IEmailAction::put_Server"]
old-location: taskschd\iemailaction_server.htm
tech.root: taskschd
ms.assetid: c781f189-f27b-4f37-af53-144e1ae8cb75
ms.date: 08/15/2022
ms.keywords: IEmailAction interface [Task Scheduler],Server property, IEmailAction.Server, IEmailAction.get_Server, IEmailAction::Server, IEmailAction::get_Server, IEmailAction::put_Server, Server property [Task Scheduler], Server property [Task Scheduler],IEmailAction interface, get_Server, taskschd.iemailaction_server, taskschd/IEmailAction::Server, taskschd/IEmailAction::get_Server, taskschd/IEmailAction::put_Server
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
 - IEmailAction::get_Server
 - taskschd/IEmailAction::get_Server
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
 - IEmailAction.Server
 - IEmailAction.get_Server
 - IEmailAction.put_Server
---

# IEmailAction::get_Server


## -description

<p class="CCE_Message">[This interface is no longer supported. Please use IExecAction with the  powershell <a href="/powershell/module/microsoft.powershell.utility/send-mailmessage">Send-MailMessage</a> cmdlet as a workaround.]

Gets or sets the name of the SMTP server that you use to send email from.

This property is read/write.

## -parameters

## -remarks

Make sure the SMTP server that sends the email is setup correctly. E-mail is sent using NTLM authentication for Windows SMTP servers, which means that the security credentials used for running the task must also have privileges on the SMTP server to send email message. If the SMTP server is a non-Windows based server, then the email will be sent if the server allows anonymous access. For information about managing SMTP server settings, see <a href="/previous-versions/windows/it-pro/windows-server-2003/cc758258(v=ws.10)">SMTP administration</a>.

## -see-also

<a href="/windows/desktop/api/taskschd/nn-taskschd-iemailaction">IEmailAction</a>
