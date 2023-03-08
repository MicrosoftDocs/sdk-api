---
UID: NF:taskschd.IEmailAction.put_Subject
title: IEmailAction::put_Subject (taskschd.h)
description: Gets or sets the subject of the email message. (Put)
helpviewer_keywords: ["IEmailAction interface [Task Scheduler]","Subject property","IEmailAction.Subject","IEmailAction.put_Subject","IEmailAction::Subject","IEmailAction::get_Subject","IEmailAction::put_Subject","Subject property [Task Scheduler]","Subject property [Task Scheduler]","IEmailAction interface","put_Subject","taskschd.iemailaction_subject","taskschd/IEmailAction::Subject","taskschd/IEmailAction::get_Subject","taskschd/IEmailAction::put_Subject"]
old-location: taskschd\iemailaction_subject.htm
tech.root: taskschd
ms.assetid: 7e5e6e84-7d2f-4aa3-946f-fe7fac6e49db
ms.date: 12/05/2018
ms.keywords: IEmailAction interface [Task Scheduler],Subject property, IEmailAction.Subject, IEmailAction.put_Subject, IEmailAction::Subject, IEmailAction::get_Subject, IEmailAction::put_Subject, Subject property [Task Scheduler], Subject property [Task Scheduler],IEmailAction interface, put_Subject, taskschd.iemailaction_subject, taskschd/IEmailAction::Subject, taskschd/IEmailAction::get_Subject, taskschd/IEmailAction::put_Subject
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
 - IEmailAction::put_Subject
 - taskschd/IEmailAction::put_Subject
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
 - IEmailAction.Subject
 - IEmailAction.get_Subject
 - IEmailAction.put_Subject
---

# IEmailAction::put_Subject


## -description

<p class="CCE_Message">[This interface is no longer supported. Please use IExecAction with the  powershell <a href="/powershell/module/microsoft.powershell.utility/send-mailmessage">Send-MailMessage</a> cmdlet as a workaround.]

Gets or sets the subject of the email message.

This property is read/write.

## -parameters

## -remarks

When setting this property value, the value can be text that is retrieved from a resource .dll file. A specialized string is used to reference the text from the resource file.  The format of the string is $(@ [Dll], [ResourceID]) where [Dll] is the path to the .dll file that contains the resource and [ResourceID] is the identifier for the resource text. For example, the setting this property value to $(@ %SystemRoot%\System32\ResourceName.dll, -101) will set the property to the value of the resource text  with an identifier equal to -101 in the  %SystemRoot%\System32\ResourceName.dll file.

## -see-also

<a href="/windows/desktop/api/taskschd/nn-taskschd-iemailaction">IEmailAction</a>
