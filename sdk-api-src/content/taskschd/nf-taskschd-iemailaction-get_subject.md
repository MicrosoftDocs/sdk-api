---
UID: NF:taskschd.IEmailAction.get_Subject
title: IEmailAction::get_Subject
author: windows-sdk-content
description: Gets or sets the subject of the email message.
old-location: taskschd\iemailaction_subject.htm
old-project: taskschd
ms.assetid: 7e5e6e84-7d2f-4aa3-946f-fe7fac6e49db
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: IEmailAction interface [Task Scheduler],Subject property, IEmailAction.Subject, IEmailAction.get_Subject, IEmailAction::Subject, IEmailAction::get_Subject, IEmailAction::put_Subject, Subject property [Task Scheduler], Subject property [Task Scheduler],IEmailAction interface, get_Subject, taskschd.iemailaction_subject, taskschd/IEmailAction::Subject, taskschd/IEmailAction::get_Subject, taskschd/IEmailAction::put_Subject
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: taskschd.h
req.include-header: 
req.redist: 
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
 - IEmailAction.Subject
 - IEmailAction.get_Subject
 - IEmailAction.put_Subject
product: Windows
targetos: Windows
req.lib: Taskschd.lib
req.dll: Taskschd.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# IEmailAction::get_Subject


## -description


<p class="CCE_Message">[This interface is no longer supported. Please use IExecAction with the  powershell <a href="https://msdn.microsoft.com/library/Hh849925(v=WPS.620).aspx">Send-MailMessage</a> cmdlet as a workaround.]

Gets or sets the subject of the email message.

This property is read/write.


## -parameters


## -remarks



When setting this property value, the value can be text that is retrieved from a resource .dll file. A specialized string is used to reference the text from the resource file.  The format of the string is $(@ [Dll], [ResourceID]) where [Dll] is the path to the .dll file that contains the resource and [ResourceID] is the identifier for the resource text. For example, the setting this property value to $(@ %SystemRoot%\System32\ResourceName.dll, -101) will set the property to the value of the resource text  with an identifier equal to -101 in the  %SystemRoot%\System32\ResourceName.dll file.





## -see-also




<a href="https://msdn.microsoft.com/2f08fd42-233a-40ee-96d0-f0ac8b25b847">IEmailAction</a>
 

 

