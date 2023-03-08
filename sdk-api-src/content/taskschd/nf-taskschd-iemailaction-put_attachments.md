---
UID: NF:taskschd.IEmailAction.put_Attachments
title: IEmailAction::put_Attachments (taskschd.h)
description: Gets or sets the pointer to an array of attachments that is sent with the email message. (Put)
helpviewer_keywords: ["Attachments property [Task Scheduler]","Attachments property [Task Scheduler]","IEmailAction interface","IEmailAction interface [Task Scheduler]","Attachments property","IEmailAction.Attachments","IEmailAction.put_Attachments","IEmailAction::Attachments","IEmailAction::get_Attachments","IEmailAction::put_Attachments","put_Attachments","taskschd.iemailaction_attachments","taskschd/IEmailAction::Attachments","taskschd/IEmailAction::get_Attachments","taskschd/IEmailAction::put_Attachments"]
old-location: taskschd\iemailaction_attachments.htm
tech.root: taskschd
ms.assetid: 06a3cf8f-d7fd-4ed6-9fd6-ea45face034a
ms.date: 12/05/2018
ms.keywords: Attachments property [Task Scheduler], Attachments property [Task Scheduler],IEmailAction interface, IEmailAction interface [Task Scheduler],Attachments property, IEmailAction.Attachments, IEmailAction.put_Attachments, IEmailAction::Attachments, IEmailAction::get_Attachments, IEmailAction::put_Attachments, put_Attachments, taskschd.iemailaction_attachments, taskschd/IEmailAction::Attachments, taskschd/IEmailAction::get_Attachments, taskschd/IEmailAction::put_Attachments
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
 - IEmailAction::put_Attachments
 - taskschd/IEmailAction::put_Attachments
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
 - IEmailAction.Attachments
 - IEmailAction.get_Attachments
 - IEmailAction.put_Attachments
---

# IEmailAction::put_Attachments


## -description

<p class="CCE_Message">[This interface is no longer supported. Please use IExecAction with the  powershell <a href="/powershell/module/microsoft.powershell.utility/send-mailmessage">Send-MailMessage</a> cmdlet as a workaround.]

Gets or sets the pointer to an array of attachments that is sent with the email message.

This property is read/write.

## -parameters

## -remarks

A maximum of eight attachments can be in the array of attachments.

## -see-also

<a href="/windows/desktop/api/taskschd/nn-taskschd-iemailaction">IEmailAction</a>
