---
UID: NF:taskschd.IEmailAction.put_Body
title: IEmailAction::put_Body
author: windows-driver-content
description: Gets or sets the body of the email that contains the email message.
old-location: taskschd\iemailaction_body.htm
old-project: TaskSchd
ms.assetid: c2bc5924-8014-4463-9537-a115266776ee
ms.author: windowsdriverdev
ms.date: 5/9/2018
ms.keywords: Body property [Task Scheduler], Body property [Task Scheduler],IEmailAction interface, IEmailAction interface [Task Scheduler],Body property, IEmailAction.Body, IEmailAction.put_Body, IEmailAction::Body, IEmailAction::get_Body, IEmailAction::put_Body, put_Body, taskschd.iemailaction_body, taskschd/IEmailAction::Body, taskschd/IEmailAction::get_Body, taskschd/IEmailAction::put_Body
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: TASK_TRIGGER_TYPE2
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	taskschd.dll
api_name:
-	IEmailAction.Body
-	IEmailAction.get_Body
-	IEmailAction.put_Body
product: Windows
targetos: Windows
req.lib: Taskschd.lib
req.dll: Taskschd.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# IEmailAction::put_Body


## -description


<p class="CCE_Message">[This interface is no longer supported. Please use IExecAction with the  powershell <a href="796227F5-C9FF-402D-8A04-CDE9E0C180EE">Send-MailMessage</a> cmdlet as a workaround.]

Gets or sets the body of the email that contains the email message.

This property is read/write.


## -parameters


## -remarks



When setting this property value, the value can be text that is retrieved from a resource .dll file. A specialized string is used to reference the text from the resource file.  The format of the string is $(@ [Dll], [ResourceID]) where [Dll] is the path to the .dll file that contains the resource and [ResourceID] is the identifier for the resource text. For example, the setting this property value to $(@ %SystemRoot%\System32\ResourceName.dll, -101) will set the property to the value of the resource text  with an identifier equal to -101 in the  %SystemRoot%\System32\ResourceName.dll file.





## -see-also




<a href="https://msdn.microsoft.com/2f08fd42-233a-40ee-96d0-f0ac8b25b847">IEmailAction</a>
 

 

