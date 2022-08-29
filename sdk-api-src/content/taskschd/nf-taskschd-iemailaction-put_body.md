---
UID: NF:taskschd.IEmailAction.put_Body
title: IEmailAction::put_Body (taskschd.h)
description: Gets or sets the body of the email that contains the email message. (Put)
helpviewer_keywords: ["Body property [Task Scheduler]","Body property [Task Scheduler]","IEmailAction interface","IEmailAction interface [Task Scheduler]","Body property","IEmailAction.Body","IEmailAction.put_Body","IEmailAction::Body","IEmailAction::get_Body","IEmailAction::put_Body","put_Body","taskschd.iemailaction_body","taskschd/IEmailAction::Body","taskschd/IEmailAction::get_Body","taskschd/IEmailAction::put_Body"]
old-location: taskschd\iemailaction_body.htm
tech.root: taskschd
ms.assetid: c2bc5924-8014-4463-9537-a115266776ee
ms.date: 08/15/2022
ms.keywords: Body property [Task Scheduler], Body property [Task Scheduler],IEmailAction interface, IEmailAction interface [Task Scheduler],Body property, IEmailAction.Body, IEmailAction.put_Body, IEmailAction::Body, IEmailAction::get_Body, IEmailAction::put_Body, put_Body, taskschd.iemailaction_body, taskschd/IEmailAction::Body, taskschd/IEmailAction::get_Body, taskschd/IEmailAction::put_Body
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
 - IEmailAction::put_Body
 - taskschd/IEmailAction::put_Body
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
 - IEmailAction.Body
 - IEmailAction.get_Body
 - IEmailAction.put_Body
---

# IEmailAction::put_Body


## -description

<p class="CCE_Message">[This interface is no longer supported. Please use IExecAction with the  powershell <a href="/powershell/module/microsoft.powershell.utility/send-mailmessage">Send-MailMessage</a> cmdlet as a workaround.]

Gets or sets the body of the email that contains the email message.

This property is read/write.

## -parameters

## -remarks

When setting this property value, the value can be text that is retrieved from a resource .dll file. A specialized string is used to reference the text from the resource file.  The format of the string is $(@ [Dll], [ResourceID]) where [Dll] is the path to the .dll file that contains the resource and [ResourceID] is the identifier for the resource text. For example, the setting this property value to $(@ %SystemRoot%\System32\ResourceName.dll, -101) will set the property to the value of the resource text  with an identifier equal to -101 in the  %SystemRoot%\System32\ResourceName.dll file.

## -see-also

<a href="/windows/desktop/api/taskschd/nn-taskschd-iemailaction">IEmailAction</a>

